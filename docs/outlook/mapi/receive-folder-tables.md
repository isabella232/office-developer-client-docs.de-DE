---
title: Ordner Tabellen empfangen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f3bcda3beb29fa91629ea1639522ef24dc6eb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795347"
---
# <a name="receive-folder-tables"></a>Ordner Tabellen empfangen

  
  
**Betrifft**: Outlook 
  
Eine empfangen Ordner-Tabelle enthält Informationen für alle Ordner, die als Ordner für einen Nachrichtenspeicher empfangen. Eine Empfangsordner ist ein Ordner, in dem eingehende Nachrichten von einer bestimmten Nachrichtenklasse platziert werden. Store-implementierte Nachricht empfangen Ordner Tabellen, und Clientanwendungen von Anrufen an die [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode verwenden. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte legen Sie im Ordner Tabellen zu empfangen:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

