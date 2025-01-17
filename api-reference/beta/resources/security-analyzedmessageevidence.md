---
title: "analyzedMessageEvidence resource type"
description: "An email, or analyzed message, that is reported in the alert as evidence."
ms.date: 09/09/2021
author: "BenAlfasi"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: resourcePageType
---

# analyzedMessageEvidence resource type

Namespace: microsoft.graph.security

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

An email, or analyzed message, that is reported in the alert as evidence.

Inherits from [alertEvidence](../resources/security-alertevidence.md).

## Properties
|Property|Type|Description|
|:---|:---|:---|
|antiSpamDirection|String|Direction of the email relative to your network. The possible values are: `Inbound`, `Outbound` or `Intraorg`.|
|attachmentsCount|Int64|Number of attachments in the email.|
|deliveryAction|String|Delivery action of the email. The possible values are: `Delivered`, `DeliveredAsSpam`, `Junked`, `Blocked`, or `Replaced`.|
|deliveryLocation|String|Location where the email was delivered. The possible values are: `Inbox`, `External`, `JunkFolder`, `Quarantine`, `Failed`, `Dropped`, `DeletedFolder` or `Forwarded`.|
|internetMessageId|String|Public-facing identifier for the email that is set by the sending email system.|
|language|String|Detected language of the email content.|
|networkMessageId|String|Unique identifier for the email, generated by Microsoft 365.|
|p1Sender|[microsoft.graph.security.emailSender](../resources/security-emailsender.md)|The P1 sender.|
|p2Sender|[microsoft.graph.security.emailSender](../resources/security-emailsender.md)|The P2 sender.|
|receivedDateTime|DateTimeOffset|Date and time when the email was received.|
|recipientEmailAddress|String|Email address of the recipient, or email address of the recipient after distribution list expansion.|
|senderIp|String|IP address of the last detected mail server that relayed the message.|
|subject|String|Subject of the email.|
|threatDetectionMethods|String collection|Collection of methods used to detect malware, phishing, or other threats found in the email.|
|threats|String collection|Collection of detection names for malware or other threats found.|
|urlCount|Int64|Number of embedded URLs in the email.|
|urls|String collection|Collection of the URLs contained in this email.|
|urn|String|Uniform resource name (URN) of the automated investigation where the cluster was identified.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.security.analyzedMessageEvidence"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.analyzedMessageEvidence",
  "createdDateTime": "String (timestamp)",
  "verdict": "String",
  "remediationStatus": "String",
  "remediationStatusDetails": "String",
  "roles": [
    "String"
  ],
  "tags": [
    "String"
  ],
  "networkMessageId": "String",
  "internetMessageId": "String",
  "subject": "String",
  "language": "String",
  "senderIp": "String",
  "recipientEmailAddress": "String",
  "antiSpamDirection": "String",
  "deliveryAction": "String",
  "deliveryLocation": "String",
  "urn": "String",
  "threats": [
    "String"
  ],
  "threatDetectionMethods": [
    "String"
  ],
  "urls": [
    "String"
  ],
  "urlCount": "Integer",
  "attachmentsCount": "Integer",
  "receivedDateTime": "String (timestamp)",
  "p1Sender": {
    "@odata.type": "microsoft.graph.security.emailSender"
  },
  "p2Sender": {
    "@odata.type": "microsoft.graph.security.emailSender"
  }
}
```