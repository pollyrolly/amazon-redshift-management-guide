# Amazon Redshift events<a name="working-with-events"></a>

**Topics**
+ [Cluster events overview](#working-with-events-overview)
+ [Viewing cluster events using the console](#viewing-events-console)
+ [Viewing cluster events using the AWS CLI and Amazon Redshift API](#view-events-api-cli)
+ [Amazon Redshift event notifications](working-with-event-notifications.md)

## Cluster events overview<a name="working-with-events-overview"></a>

Amazon Redshift tracks cluster events and retains information about them for a period of several weeks in your AWS account\. For each event, Amazon Redshift reports information such as the date the event occurred, a description, the event source \(for example, a cluster, a parameter group, or a snapshot\), and the source ID\. 

Amazon Redshift provides notification in advance for some events\. These events have an event category of `pending`\. For example, we send an advance notification if a hardware update is required for one of the nodes in your cluster\. You can subscribe to pending events the same as other Amazon Redshift events\. For more information, see [Subscribing to Amazon Redshift cluster event notifications](working-with-event-notifications.md#working-with-event-notifications-subscribe)\. 

You can use the Amazon Redshift Management Console, the Amazon Redshift API, or the AWS SDKs to obtain event information\. You can obtain a list of all events, or you can apply filters, such as event duration or start and end date, to obtain events information for a specific period\.

You can also obtain events that were generated by a specific source type, such as cluster events or parameter group events\. The *Source* column shows the resource name and resource type that triggers a given action\.

You can create Amazon Redshift event notification subscriptions that specify a set of event filters\. When an event occurs that matches the filter criteria, Amazon Redshift uses Amazon Simple Notification Service to actively inform you that the event has occurred\.

For a list of Amazon Redshift events by source type and category, see [Amazon Redshift event categories and event messages](working-with-event-notifications.md#redshift-event-messages)

## Viewing cluster events using the console<a name="viewing-events-console"></a>

**To view events**

1. Sign in to the AWS Management Console and open the Amazon Redshift console at [https://console\.aws\.amazon\.com/redshift/](https://console.aws.amazon.com/redshift/)\.

1. On the navigation menu, choose **Events**\. 

## Viewing cluster events using the AWS CLI and Amazon Redshift API<a name="view-events-api-cli"></a>

You can use the following Amazon Redshift CLI operation to view events\.
+ [describe\-events](https://docs.aws.amazon.com/cli/latest/reference/redshift/describe-events.html)

 Amazon Redshift provides the following API to view events\.
+ [DescribeEvents](https://docs.aws.amazon.com/redshift/latest/APIReference/API_DescribeEvents.html)