---
title: Durchlaufen des Posteingangsordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82dfaf9a09a9dca5a29764aad0ee07363d133435
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624013"
---
# <a name="traversing-the-inbox-folder"></a>Durchlaufen des Posteingangsordners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So durchlaufen Sie alle Nachrichten im Posteingang**
  
1. Rufen [Sie IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner des Posteingangs abzurufen. 
    
2. Rufen Sie **IMAPIFolder::OpenEntry** auf, um den Posteingang zu öffnen. 
    
3. Rufen Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Posteingangs auf, um das Inhaltsverzeichnis abzurufen. 
    
4. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) des Inhaltsverzeichnisses auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und alle anderen erforderlichen Spalten zu beschränken. 
    
5. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) auf, um eine Gruppe von Zeilen abzurufen. 
    
6. Bis keine Zeilen mehr im Inhaltsverzeichnis vorhanden sind:
    
1. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) auf, um die durch den Eintragsbezeichner in jeder Zeile dargestellte Nachricht zu öffnen. 
    
2. Weisen Sie den  _lppUnk-Parameter_ einem lokalen **IMessage-Schnittstellenzeiger** zu. 
    
3. Arbeiten mit den Eigenschaften der Nachricht.
    
4. Lassen Sie den Zeiger los, auf den der  _Parameter "lppUnk"_ zeigt. 
    
5. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) auf, um die nächste Gruppe von Zeilen abzurufen. 
    
7. Geben Sie das Inhaltsverzeichnis frei.
    

