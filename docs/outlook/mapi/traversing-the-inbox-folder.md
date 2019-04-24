---
title: DurchLaufen des postEingangsOrdners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356581"
---
# <a name="traversing-the-inbox-folder"></a>DurchLaufen des postEingangsOrdners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So wechseln Sie alle Nachrichten im Posteingang**
  
1. Rufen Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner des Posteingangs abzurufen. 
    
2. Rufen Sie **IMAPIFolder:: OpenEntry** auf, um den Posteingang zu öffnen. 
    
3. Rufen Sie die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Posteingangs auf, um die Tabelle Inhalt abzurufen. 
    
4. Rufen Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Inhaltstabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und alle anderen Spalten einzuschränken, die Sie benötigen. 
    
5. Rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) auf, um eine Gruppe von Zeilen abzurufen. 
    
6. Bis keine Zeilen mehr in der Tabelle Contents vorhanden sind:
    
1. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf, um die durch den Eintragsbezeichner dargestellte Nachricht aus jeder Zeile zu öffnen. 
    
2. Weisen Sie den Parameter _lppUnk_ einem lokalen **IMessage** -Schnittstellenzeiger zu. 
    
3. Arbeiten mit den Eigenschaften der Nachricht.
    
4. Lassen Sie den Zeiger, auf den durch den _lppUnk_ -Parameter zeigt. 
    
5. Rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) auf, um die nächste Gruppe von Zeilen abzurufen. 
    
7. Geben Sie die Tabelle Contents frei.
    

