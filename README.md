
# aws-cloudformation-stack-status

Clean display of single most recent event status for each resource in
a CloudFormation stack.

Useful for monitoring the progress of a CloudFormation stack create,
update, and delete.

[![demo](https://alestic.com/img/blog/2016-11-21-aws-cloudformation-stack-status-play.png)](https://asciinema.org/a/8r36ot853yute0pq902y8jkvm?autoplay=1)

## Examples

Monitor all stack resource progress live (Interrupt with Ctrl-C):

    aws-cloudformation-stack-status --watch --region $region --stack-name $stack

The `--stack-name` is optional, and multiple stacks can be monitored
together:

    watch aws-cloudformation-stack-status --watch $webstack $dbstack $dnsstack

One time display of latest status for each stack resource:

    aws-cloudformation-stack-status --region $region --stack-name $stack

## Requirements

This script does require that you have already installed and
configured the aws-cli.
