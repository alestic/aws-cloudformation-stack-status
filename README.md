
# aws-cloudformation-stack-status

Clean display of single most recent event status for each resource in
a CloudFormation stack.

Useful for monitoring the progress of a stack's creation, update, and
delete.

<link rel="stylesheet" type="text/css" href="https://alestic.com/css/asciinema-player.css" />

<asciinema-player cols="115" rows="21" autoplay="1" font-size="small"
 theme="monokai"
 title="aws-cloudformation-stack-status (watching stack-create)"
 author="Eric Hammond" author-url="https://twitter.com/esh"
 src="https://alestic.com/asciinema/201611-aws-cloudformation-stack-status-create.rec"
 poster="npt:2:20"
 ></asciinema-player>

<script src="https://alestic.com/js/asciinema-player.js"></script>

## Synopsis

One time display of latest status for each stack resource:

    aws-cloudformation-stack-status --region $region --stack-name $stack

Monitor all stack resource progress live (Interrupt with ^C):

    aws-cloudformation-stack-status --watch --region $region --stack-name $stack

The `--stack-name` is optional, and multiple stacks can be monitored
together:

    watch aws-cloudformation-stack-status --watch $webstack $dbstack $dnsstack

