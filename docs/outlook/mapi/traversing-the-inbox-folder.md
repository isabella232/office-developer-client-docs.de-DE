---
title: Durchlaufen des Posteingangsordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594488"
---
# <a name="traversing-the-inbox-folder"></a>Durchlaufen des Posteingangsordners

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **Durchlaufen aller Nachrichten im Posteingang**
  
1. Rufen Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , um die Eintrags-ID des Posteingangs abzurufen. 
    
2. Rufen Sie **IMAPIFolder::OpenEntry** , um den Posteingang zu öffnen. 
    
3. Rufen Sie den Posteingang [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode zum Abrufen der Inhaltstabelle. 
    
4. Rufen Sie den Inhalt der Tabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode zum Beschränken der Spalte auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) festgelegt und alle anderen Spalten, die Sie benötigen. 
    
5. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen einer Gruppe von Zeilen. 
    
6. Bis alle Zeilen in der Inhaltstabelle mehr vorhanden sind:
    
1. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen der Nachricht, durch die Eintrags-ID aus jeder Zeile dargestellt. 
    
2. Weisen Sie des _LppUnk_ -Parameters auf einen lokalen **IMessage** -Schnittstellenzeiger. 
    
3. Arbeiten Sie mit den Eigenschaften der Nachricht.
    
4. Heben Sie den Zeiger auf den durch den Parameter _LppUnk_ verwiesen. 
    
5. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen der nächsten Gruppe von Zeilen. 
    
7. Version der Inhaltstabelle.
    

