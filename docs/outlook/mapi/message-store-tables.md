---
title: Nachrichten Store Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405352"
---
# <a name="message-store-tables"></a>Nachrichten Store Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Tabelle für den Nachrichtenspeicher enthält Informationen zu Nachrichtenspeicheranbietern im aktuellen Profil. Es gibt eine Nachrichtenspeichertabelle für jede MAPI-Sitzung, die von MAPI implementiert und von Clients verwendet wird. Clients können diese Tabelle z. B. verwenden, um alle Instanzen eines bestimmten Anbieters zu finden oder um einen bestimmten Nachrichtenspeicher zu finden. 
  
Die Tabelle für den Nachrichtenspeicher ist dynamisch. Wenn der Benutzer einer Clientanwendung das Profil bearbeitet, werden beispielsweise die Werte der **PR_DEFAULT_STORE-Eigenschaften** für die betroffenen Nachrichtenspeicher sofort aktualisiert. 
  
Clients greifen auf die Nachrichtenspeichertabelle zu, indem sie die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) aufrufen. 
  
Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in der Nachrichtenspeichertabelle zusammen:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

