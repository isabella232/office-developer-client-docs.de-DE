---
title: Nachrichten Store Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 324696284976d599f4a3fd465a4c3c2433dba059
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551072"
---
# <a name="message-store-tables"></a>Nachrichten Store Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtenspeichertabelle enthält Informationen zu Nachrichtenspeicheranbietern im aktuellen Profil. Es gibt eine Nachrichtenspeichertabelle für jede MAPI-Sitzung, die von der MAPI implementiert und von Clients verwendet wird. Clients können diese Tabelle beispielsweise verwenden, um alle Instanzen eines bestimmten Anbieters oder einen bestimmten Nachrichtenspeicher zu suchen. 
  
Die Nachrichtenspeichertabelle ist dynamisch. Wenn der Benutzer einer Clientanwendung das Profil bearbeitet und den Standardnachrichtenspeicher ändert, werden beispielsweise die Werte der **PR_DEFAULT_STORE** Eigenschaften für die betroffenen Nachrichtenspeicher sofort aktualisiert. 
  
Clients greifen auf die Nachrichtenspeichertabelle zu, indem sie die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) aufrufen. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte, die in der Nachrichtenspeichertabelle festgelegt ist:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

