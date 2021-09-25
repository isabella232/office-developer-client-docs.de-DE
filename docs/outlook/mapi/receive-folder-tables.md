---
title: Empfangsordnertabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2cf12e7e73ca55100fdb51d2d9cc1ba5d5a8b9bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609614"
---
# <a name="receive-folder-tables"></a>Empfangsordnertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Empfangsordnertabelle enthält Informationen zu allen Ordnern, die als Empfangsordner für einen Nachrichtenspeicher festgelegt sind. Ein Empfangsordner ist ein Ordner, in dem eingehende Nachrichten einer bestimmten Nachrichtenklasse platziert werden. Nachrichtenspeicheranbieter implementieren Empfangsordnertabellen, und Clientanwendungen verwenden sie, indem sie die [IMsgStore::GetReceiveFolderTable-Methode](imsgstore-getreceivefoldertable.md) aufrufen. 
  
Die folgenden Eigenschaften bilden die erforderlichen Spalten, die in Empfangsordnertabellen festgelegt sind:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

