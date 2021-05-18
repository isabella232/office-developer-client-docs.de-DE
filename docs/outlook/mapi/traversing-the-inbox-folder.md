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
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406556"
---
# <a name="traversing-the-inbox-folder"></a>Durchlaufen des Posteingangsordners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So durchzyklen Sie alle Nachrichten im Posteingang**
  
1. Rufen [Sie IMsgStore::GetReceiveFolder auf,](imsgstore-getreceivefolder.md) um die Eintrags-ID des Posteingangs abzurufen. 
    
2. Rufen **Sie IMAPIFolder::OpenEntry auf,** um den Posteingang zu öffnen. 
    
3. Rufen Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Posteingangs auf, um die Inhaltstabelle abzurufen. 
    
4. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Inhaltstabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und alle anderen benötigten Spalten zu beschränken. 
    
5. Rufen [Sie IMAPITable::QueryRows auf,](imapitable-queryrows.md) um eine Gruppe von Zeilen abzurufen. 
    
6. Bis in der Inhaltstabelle keine Zeilen mehr vorhanden sind:
    
1. Rufen [Sie IMsgStore::OpenEntry auf,](imsgstore-openentry.md) um die Durch den Eintragsbezeichner dargestellte Nachricht aus jeder Zeile zu öffnen. 
    
2. Weisen Sie  _den lppUnk-Parameter_ einem lokalen **IMessage-Schnittstellenzeiger** zu. 
    
3. Arbeiten Sie mit den Eigenschaften der Nachricht.
    
4. Lassen Sie den Zeiger los, auf den der  _lppUnk-Parameter_ verweist. 
    
5. Rufen [Sie IMAPITable::QueryRows auf,](imapitable-queryrows.md) um die nächste Gruppe von Zeilen abzurufen. 
    
7. Geben Sie die Inhaltstabelle frei.
    

