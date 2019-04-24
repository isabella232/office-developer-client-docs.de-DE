---
title: Empfangsordner Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328476"
---
# <a name="receive-folder-tables"></a>Empfangsordner Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Receive Folder-Tabelle enthält Informationen für alle Ordner, die als Empfangsordner für einen Nachrichtenspeicher festgelegt wurden. Ein Empfangsordner ist ein Ordner, in dem eingehende Nachrichten einer bestimmten Nachrichtenklasse abgelegt werden. Nachrichtenspeicher Anbieter implementieren Empfänger Ordner Tabellen und Clientanwendungen verwenden Sie, indem Sie die [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode aufrufen. 
  
Die folgenden Eigenschaften sind der erforderliche Spaltensatz in den Tabellen des Empfangs Ordners:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

