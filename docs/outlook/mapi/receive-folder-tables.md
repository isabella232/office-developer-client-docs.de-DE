---
title: Empfangen von Ordnertabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417350"
---
# <a name="receive-folder-tables"></a>Empfangen von Ordnertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Tabelle mit Empfangsordnern enthält Informationen zu allen Ordnern, die als Empfangsordner für einen Nachrichtenspeicher festgelegt sind. Ein Empfangsordner ist ein Ordner, in dem eingehende Nachrichten einer bestimmten Nachrichtenklasse platziert werden. Nachrichtenspeicheranbieter implementieren Empfangsordnertabellen, und Clientanwendungen verwenden sie, indem sie die [IMsgStore::GetReceiveFolderTable-Methode](imsgstore-getreceivefoldertable.md) aufrufen. 
  
Die folgenden Eigenschaften stellen die erforderliche Spaltenmappe in den Tabellen des Empfangsordners zusammen:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

