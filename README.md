
# aws-cloudformation-stack-status

Clean display of single most recent event status for each resource in
a CloudFormation stack.

Useful for monitoring the progress of a stack's creation, update, and
delete.

[![demo](https://alestic.com/img/blog/2016-11-aws-cloudformation-stack-status-play.png)](https://asciinema.org/a/arbohsp3hlseoqvvfs7b61be8?autoplay=1)

## Examples

Monitor all stack resource progress live (Interrupt with ^C):

    aws-cloudformation-stack-status --watch --region $region --stack-name $stack

The `--stack-name` is optional, and multiple stacks can be monitored
together:

    watch aws-cloudformation-stack-status --watch $webstack $dbstack $dnsstack

One time display of latest status for each stack resource:

    aws-cloudformation-stack-status --region $region --stack-name $stack

## Requirements

This script does require that you have already installed and
configured the aws-cli.
