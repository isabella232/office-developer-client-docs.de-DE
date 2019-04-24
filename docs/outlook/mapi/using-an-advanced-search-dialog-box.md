---
title: Verwenden eines Dialog Felds für die erweiterte Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329666"
---
# <a name="using-an-advanced-search-dialog-box"></a>Verwenden eines Dialog Felds für die erweiterte Suche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, die es Clients ermöglicht, andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zu suchen. Adressbuchcontainer, die erweiterte Suchvorgänge unterstützen, verfügen über eine Containerobjekt Eigenschaft namens **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md)). Dieses Container-Objekt ermöglicht den Zugriff auf eine Anzeigetabelle, die das Dialogfeld Suchen beschreibt – ein Dialogfeld zum eingeben und Bearbeiten der erweiterten Suchkriterien.
  
 **So führen Sie eine erweiterte Suche für einen Adressbuchcontainer aus**
  
1. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers auf, und geben Sie **PR_SEARCH** für das Property-Tag und IID_IMAPIContainer für den Schnittstellenbezeichner an. 
    
2. Rufen Sie die **IMAPIProp:: OpenProperty** -Methode des Search-Objekts auf, und geben Sie **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md)) für das Property-Tag und IID_IMAPITable für den Schnittstellenbezeichner an. 
    
3. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Search-Objekts auf, um Werte für die in der erweiterten Suche zu verwendenden Eigenschaften einzurichten. 
    
4. Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des Search-Objekts auf, um die erweiterten Suchkriterien zu speichern. 
    
Diese Sequenz von Aufrufen führt zu einer Einschränkung, die verfügbar ist, wenn ein Client die **GetSearchCriteria** -Methode des Search-Objekts aufruft. 
  

