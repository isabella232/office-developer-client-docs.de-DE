---
title: Nachrichtenspeichertabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793272"
---
# <a name="message-store-tables"></a>Nachrichtenspeichertabellen

  
  
**Betrifft**: Outlook 
  
Die Nachricht Store-Tabelle enthält Informationen zu Anbietern Nachricht im aktuellen Profil. Es wird eine Meldung Store-Tabelle für jedes MAPI-Sitzung von MAPI implementiert und von Clients verwendet wird. Clients können diese Tabelle beispielsweise nach allen Instanzen eines bestimmten Anbieters suchen oder suchen Sie einen bestimmten Nachrichtenspeicher verwenden. 
  
Die Tabelle Store ist dynamisch. Wenn der Benutzer von einer Clientanwendung aus das Profil bearbeitet, werden, Ändern der Standard-Informationsspeicher, beispielsweise die Werte der **PR_DEFAULT_STORE** Eigenschaften für die betroffenen Nachrichtenspeicher unmittelbar aktualisiert. 
  
Clientzugriff durch Aufrufen der Methode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) die Nachricht Store-Tabelle. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte in der Nachricht Store Tabelle festgelegt:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

