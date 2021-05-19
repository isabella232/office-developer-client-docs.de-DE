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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425260"
---
# <a name="removing-address-book-entries"></a>Entfernen von Adressbucheinträgen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABContainer::D eleteEntries-Methode Ihres Containers](iabcontainer-deleteentries.md) wird aufgerufen, um einen oder mehrere Empfänger zu entfernen. **DeleteEntries** verfügt über zwei Parameter: ein Array von Eintragsbezeichnern, die die zu löschenden Empfänger darstellen, und einen reservierten Flagswert. Das Löschen eines Empfängers wirkt sich auf das Inhaltsverzeichnis Des Containers aus. Zusätzlich zum Löschen des Empfängers muss ihr Container die Inhaltsverzeichniszeile löschen, die den Empfänger darstellt. Wenn die Zeile aus der Tabelle entfernt wurde, muss ihr Container eine Tabellenbenachrichtigung an jeden registrierten Client aus senden. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>So implementieren Sie IABContainer::D eleteEntries
  
1. Löschen Sie jeden Empfänger, der durch die Eintrags-ID dargestellt wird, aus Ihrem Container.
    
2. Wenn die Inhaltstabelle Ihres Containers geöffnet ist:
    
   - Senden Sie  _eine fnevTableModified-Benachrichtigung,_ bei der das **ulTableEvent-Element** auf TABLE_ROW_DELETED für jede gelöschte Inhaltstabellenzeile an registrierte Clients gesendet wird. Wenn Ihr Anbieter das Benachrichtigungsprogramm verwendet, rufen [Sie IMAPISupport::Notify auf,](imapisupport-notify.md) um diese Benachrichtigungen zu senden. 
    
   - Wenn Ihr Anbieter Objektbenachrichtigungen unterstützt, senden Sie auch eine _fnevObjectDeleted-Benachrichtigung._ 
    

