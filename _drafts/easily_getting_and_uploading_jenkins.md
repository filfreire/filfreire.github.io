# Easily cloning and uploading jenkins jobs

## TL;DR:
- Create a script to get the names of the jobs you might want (inside a view)
- Create a script to download config for a job name an save it on a file
- Create a script to upload every job config inside a folder to another jenkins instance

## Step 1: Get the names of the jobs you might want to clone

TBD

## Step 2: Download config for a job name and save it on a file

tbd

```shell
#!/bin/bash

# Usage: script.sh <JENKINS_USER> <JENKINS_USER_TOKEN> <JOB_NAME> <JENKINS_URL>

ARGS_NUM=4
if [[ ( "$#" -lt "$ARGS_NUM" ) ]]; then
  echo "Usage: script.sh <JENKINS_USER> <JENKINS_USER_TOKEN> <JOB_NAME> <JENKINS_URL>"
  exit 1
fi

function downloadConfig {
    JENKINS=$4
    echo "curl --user $1:$2 --silent $JENKINS/$3/config.xml -o $3.xml"
    curl --user $1:$2 --silent $JENKINS/$3/config.xml -o $3.xml
}

downloadConfig $1 $2 $3 $4
```

## Step 3: Upload every job config inside a folder to another jenkins instance

tbd

`post_job.sh`:

```shell
#!/bin/bash

# Post a job config to a jenkins

ARGS_NUM=5
if [[ ( 0 -lt  ) ]]; then
  echo "Usage: script.sh <USER> <TOKEN> <JENKINS> <JOB_CONFIG_FILE> <PATH>"
  exit 1
fi

user=$1
token=$2
jenkins=$3
job_config_file=$4
path=$5

function jobName {
  echo $1 | cut -d'.' -f1 | awk '{ print tolower($0) }'
}

name=$( jobName $job_config_file )

cat $path/$job_config_file | curl -X POST -u $user:$token "$jenkins/createItem?name=$name" --header "Content-Type: application/xml" -d @-
```

tbd

`migrate_mutiple_jobs.sh`:

```shell
#!/bin/bash

#  Migrate multiple jobs 

ARGS_NUM=4
if [[ ( "$#" -lt "$ARGS_NUM" ) ]]; then
  echo "Usage: script.sh <JENKINS_USER> <JENKINS_USER_TOKEN> <JENKINS_HOST> <PATH_OF_CONFIG_FILES>"
  exit 1
fi

user=$1
token=$2
jenkins=$3
path=$4 

ls $path | xargs -n1 -I {} ./post_job.sh $user $token $jenkins {} $path
```
