#an action practice guided by https://docs.github.com/en/actions/creating-actions/creating-a-docker-container-action#creating-a-dockerfile
#Triggered by push action,and print out a greet word.

#main.yml
redirect to the ./ directory action.yml, and pass the inputs parameter 'Mona the Octocat'.

#action.yml
defines the metadata for the Action. Specify the use of a Docker image to run the Action.

#Dockerfile
build a Docker image. and specifies the entry point to run when the container starts (entrypoint.sh).

#entrypoint.sh
echo to print.

This action prints "Hello World" or "Hello" + the name of a person to greet to the log.

## Inputs

## `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

## `time`

The time we greeted you.

## Example usage

uses: actions/hello-world-docker-action@v2
with:
  who-to-greet: 'Mona the Octocat'

