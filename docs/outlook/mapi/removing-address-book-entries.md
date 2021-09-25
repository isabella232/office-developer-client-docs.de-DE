---
title: Entfernen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea2671ecdafc5a3cc0445a510613a5eab3dac813
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609670"
---
# <a name="removing-address-book-entries"></a>Entfernen von Adressbucheinträgen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABContainer::D eleteEntries-Methode](iabcontainer-deleteentries.md) ihres Containers wird aufgerufen, um einen oder mehrere Empfänger zu entfernen. **DeleteEntries** hat zwei Parameter: ein Array von Eintragsbezeichnern, die die zu löschenden Empfänger darstellen, und einen reservierten Flagwert. Das Löschen eines Empfängers wirkt sich auf das Inhaltsverzeichnis Ihres Containers aus. Zusätzlich zum Löschen des Empfängers muss Ihr Container die Inhaltstabellenzeile löschen, die den Empfänger darstellt. Wenn die Zeile aus der Tabelle entfernt wurde, muss Ihr Container eine Tabellenbenachrichtigung für jeden registrierten Client ausgeben. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>So implementieren Sie IABContainer::D eleteEntries
  
1. Löschen Sie jeden Empfänger, der durch den Eintragsbezeichner dargestellt wird, aus Ihrem Container.
    
2. Wenn das Inhaltsverzeichnis Ihres Containers geöffnet ist:
    
   - Senden Sie eine  _fnevTableModified-Benachrichtigung,_ wobei das **ulTableEvent-Mitglied** für jede gelöschte Inhaltstabellenzeile auf TABLE_ROW_DELETED für registrierte Clients festgelegt ist. Wenn Ihr Anbieter das Benachrichtigungsprogramm verwendet, rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) auf, um diese Benachrichtigungen zu senden. 
    
   - Wenn Ihr Anbieter Objektbenachrichtigungen unterstützt, senden Sie auch eine _fnevObjectDeleted-Benachrichtigung._ 
    

