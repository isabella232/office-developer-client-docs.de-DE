---
title: Tabellen für Empfängerordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573180"
---
# <a name="receive-folder-tables"></a>Tabellen für Empfängerordner

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine empfangen Ordner-Tabelle enthält Informationen für alle Ordner, die als Ordner für einen Nachrichtenspeicher empfangen. Eine Empfangsordner ist ein Ordner, in dem eingehende Nachrichten von einer bestimmten Nachrichtenklasse platziert werden. Store-implementierte Nachricht empfangen Ordner Tabellen, und Clientanwendungen von Anrufen an die [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode verwenden. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte legen Sie im Ordner Tabellen zu empfangen:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

