---
title: Verwenden eines Dialogfelds für die erweiterte Suche.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588769"
---
# <a name="using-an-advanced-search-dialog-box"></a>Verwenden eines Dialogfelds für die erweiterte Suche.

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Einige Address Book Container unterstützt eine erweiterte Suchfunktionen, mit der Clients auf andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) durchsuchen kann. Address Book Container, die erweiterte Suchvorgänge unterstützen, verfügen über die Container-Objekteigenschaft **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Diese Container-Objekt ermöglicht den Zugriff auf eine zeigt die Tabelle, die das Dialogfeld Suchen beschreibt – ein Dialogfeld zum eingeben und bearbeiten die Kriterien für die erweiterte Suche verwendet.
  
 **Zum Ausführen einer erweiterten Suche auf eine Adressbuchcontainer**
  
1. Rufen Sie den Container [IMAPIProp::OpenProperty](imapiprop-openproperty.md) Methode **PR_SEARCH** für die Eigenschaftentag und IID_IMAPIContainer für den Schnittstellenbezeichner angeben. 
    
2. Rufen Sie das Search-Objekt **IMAPIProp::OpenProperty** Methode **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) für die Eigenschaftentag und IID_IMAPITable für den Schnittstellenbezeichner angeben. 
    
3. Rufen Sie das Search-Objekt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode zum Festlegen der Werte für die Eigenschaften in die erweiterte Suche verwendet werden. 
    
4. Rufen Sie das Search-Objekt [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Kriterien für die erweiterte Suche zu speichern. 
    
Diese Folge der Aufrufe führt eine Einschränkung nicht verfügbar sein, wenn ein Client das Search-Objekt **GetSearchCriteria** -Methode aufruft. 
  

