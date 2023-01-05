# Hello world docker action
The name of the action is found inside the action.yml file

Inside action.yml you find action name, which has been set to be: HelloWorldAll

This action prints "Hello World" or "Hello" + the name of a person to greet to the log.

## Inputs

## `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

## `time`

The time we greeted you.

## Example usage

uses: ello-world-docker-action/HelloWorldAll
with:
  who-to-greet: 'Mona the Octocat'
