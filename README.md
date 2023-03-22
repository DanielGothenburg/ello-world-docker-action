An Action is NOT a workflow. A workflow can use an Action (as part of workflow).
An action is a custom application for the GitHub Actions platform that performs a complex but frequently repeated task. Hence it can be called by a workflow.
If you have a custom action to use in your workflow you can store the action in same repo. Potwntially in a dedicated folder structure, or otherwise directly in root (as in this example)

The action is defined by an action file. The action can use other related files. as in the example below.

In this exampl a workflow has been created in workflows folder. The worklfow file (named: thisrun) will call below action. However before doing that ti seems a checkout is needed. checkout is done by calling another action, this action is a standard action and can therefore directly be called by using path actions/checkout@v3

There is a problem with the workflow file, despite it contains command "dispatch" it does not seem as you can run the workflow. Since under "Actions" it does not show this workflow and hence you can not start it. Maybe some problem with syntax in workflow file. To be checked.

#-------------------------------------------------------------------------------------------------
Below follows the contents of the action file. Intention is to add more comments below about the commands used in the action file. To better describe it.

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
