---
title: Entfernen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328350"
---
# <a name="removing-address-book-entries"></a>Entfernen von Adressbucheinträgen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABContainer::D eleteentries](iabcontainer-deleteentries.md) -Methode des Containers wird aufgerufen, um einen oder mehrere Empfänger zu entfernen. **DeleteEntries** hat zwei Parameter: ein Array von Eintrags Bezeichnern, die die zu löschenden Empfänger und einen reservierten Flags-Wert darstellen. Das Löschen eines Empfängers wirkt sich auf die Inhaltstabelle ihres Containers aus; Zusätzlich zum Löschen des Empfängers muss der Container die Inhaltstabellen Zeile löschen, die den Empfänger darstellt. Wenn die Zeile aus der Tabelle entfernt wurde, muss Ihr Container eine Tabellenbenachrichtigung für jeden registrierten Client ausgeben. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>So implementieren Sie IABContainer::D eleteEntries
  
1. Löschen Sie jeden durch die Eintrags-ID dargestellten Empfänger aus Ihrem Container.
    
2. Wenn die Tabelle Inhalt Ihres Containers geöffnet ist:
    
   - Senden Sie eine _fnevTableModified_ -Benachrichtigung mit dem **ulTableEvent** -Element, das auf TABLE_ROW_DELETED für jede gelöschte Inhaltstabellen Zeile auf registrierte Clients festgelegt ist. Wenn Ihr Anbieter das Benachrichtigungs Dienstprogramm verwendet, rufen Sie [IMAPISupport:: notify](imapisupport-notify.md) auf, um diese Benachrichtigungen zu senden. 
    
   - Wenn Ihr Anbieterobjekt Benachrichtigungen unterstützt, senden Sie auch eine _fnevObjectDeleted_ -Benachrichtigung. 
    

