
# aws-cloudformation-stack-status

Clean display of single most recent event status for each resource in
a CloudFormation stack.

Useful for monitoring the progress of a stack's creation, update, and
delete.

## Synopsis

Monitor all stack resource progress live (Interrupt with ^C):

    aws-cloudformation-stack-status --watch --region $region --stack-name $stack

The `--stack-name` is optional, and multiple stacks can be monitored
together:

    watch aws-cloudformation-stack-status --watch $webstack $dbstack $dnsstack

One time display of latest status for each stack resource:

    aws-cloudformation-stack-status --region $region --stack-name $stack
