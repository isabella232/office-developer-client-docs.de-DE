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
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356896"
---
# <a name="message-store-tables"></a>Nachrichtenspeichertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtenspeichertabelle enthält Informationen zu Nachrichtenspeicher Anbietern im aktuellen Profil. Es gibt eine Nachrichtenspeichertabelle für jede MAPI-Sitzung, die von MAPI implementiert und von Clients verwendet wird. Clients können diese Tabelle verwenden, um beispielsweise alle Instanzen eines bestimmten Anbieters zu finden oder einen bestimmten Nachrichtenspeicher zu finden. 
  
Die Nachrichtenspeichertabelle ist dynamisch. Wenn der Benutzer einer Clientanwendung das Profil bearbeitet und den Standardnachrichtenspeicher ändert, werden beispielsweise die Werte der **PR_DEFAULT_STORE** -Eigenschaften für die betroffenen Nachrichtenspeicher sofort aktualisiert. 
  
Clients greifen auf die Nachrichtenspeichertabelle zu, indem Sie die [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode aufrufen. 
  
Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in der Nachrichtenspeichertabelle dar:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([Pidtagdefaultstore (](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([Pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

