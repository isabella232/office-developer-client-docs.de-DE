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
ms.openlocfilehash: 2c5d7a2114f4a85b9f63cd778e899a83d335ff45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581279"
---
# <a name="removing-address-book-entries"></a>Entfernen von Adressbucheinträgen
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Des Containers [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode aufgerufen, um einen oder mehrere Empfänger zu entfernen. **DeleteEntries** hat zwei Parameter: ein Array von Eintragsbezeichner, die die Empfänger zu löschenden darstellt und ein Flagwert reserviert. Löschen eines Empfängers wirkt sich aus die Inhaltstabelle des Containers. Zusätzlich zu den Empfänger löschen, muss der Container für die Tabellenzeile Inhalt löschen, die den Empfänger darstellt. Wenn die Zeile aus der Tabelle entfernt wurde, muss der Container für eine Benachrichtigung über eine Tabelle auf allen registrierten Clients ausstellen. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Implementieren von IABContainer::DeleteEntries
  
1. Löschen Sie jeden Empfänger, dargestellt durch die Eintrags-ID aus dem Container.
    
2. Wenn Inhaltstabelle des Containers geöffnet ist:
    
   - Senden Sie eine Benachrichtigung _FnevTableModified_ mit dem **UlTableEvent** -Element festlegen, um den registrierten Clients für jede Tabellenzeile gelöschten Inhalt TABLE_ROW_DELETED. Wenn der Anbieter das Dienstprogramm Benachrichtigung verwendet wird, rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) , um diese Benachrichtigungen zu senden. 
    
   - Wenn der Anbieter Objekt Benachrichtigungen unterstützt, auch senden Sie eine _FnevObjectDeleted_ -Benachrichtigung. 
    

