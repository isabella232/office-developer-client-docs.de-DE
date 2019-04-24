---
title: Zuordnen von TNEF-Attributen zu MAPI-Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 25647a6488fec9a39f8b41441fe9afc4c4aa0a7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357652"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>Zuordnen von TNEF-Attributen zu MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Tabelle sind alle in der TNEF-Implementierung definierten Attribute und ihre Zuordnungen zu MAPI-Eigenschaften aufgeführt. In einigen Fällen werden mehrere MAPI-Eigenschaften als einzelnes Attribut codiert. Einige Attribute haben erweiterte Beschreibungen weiter unten in diesem Abschnitt.
  
|**TNEF-Attribut**|**MAPI-Eigenschaft oder-Eigenschaften**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID** ([Pidtagownerappointmentid (](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN** ([Pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))  <br/> |
|**attAttachment** <br/> |Informationen zu dieser Zuordnung finden Sie unter [TNEF-Attribute](tnef-attributes.md).  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING** ([Pidtagattachrendering (](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** ([Pidtagattachmethod (](pidtagattachmethod-canonical-property.md)), **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME** ([Pidtagattachfilename (](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME** ([Pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))  <br/> |
|**attBody** <br/> |**PR_BODY** ([Pidtagbody (](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY** ([Pidtagconversationkey (](pidtagconversationkey-canonical-property.md)) Diese Eigenschaft ist in Microsoft Exchange Server veraltet: die Verwendung bleibt in Outlook nur für die Suche nach **IPM. MessageManager** -Nachrichten.  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE** ([Pidtagenddate (](pidtagenddate-canonical-property.md)) Details finden Sie unter [attDate-Attribute](attdate-attributes.md) .  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME** Details finden Sie unter [attDate-Attribute](attdate-attributes.md) .  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md)) Details finden Sie unter [attDate-Attribute](attdate-attributes.md) .  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) Details finden Sie unter [attDate-Attribute](attdate-attributes.md) .  <br/> |
|**attDateStart** <br/> |**PR_START_DATE** ([Pidtagstartdate (](pidtagstartdate-canonical-property.md)) Details finden Sie unter [attDate-Attribute](attdate-attributes.md) .  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) und **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |Informationen zu diesem Attribut finden Sie unter [attMAPIProps](attmapiprops.md).  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**attMessageID** <br/> |**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) Siehe [TNEF-Korrelation in X. 400-Gateways und-](tnef-correlation-in-x-400-gateways-and-transports.md)Übertragungen.  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * PR_ORIG_MESSAGE_CLASS * * ([pidtagoriginalmessageclass (](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |Siehe [attOwner](attowner.md).  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY** (**PidTagParentKey**) Diese Eigenschaft ist veraltet. Weitere Informationen finden Sie unter [in dieser Edition veraltetEr API-Elemente](api-elements-deprecated-in-this-edition.md) .  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED** ([Pidtagresponserequested (](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** ([Pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**attSubject** <br/> |**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

