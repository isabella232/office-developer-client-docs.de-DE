---
title: Verwenden eines Dialogfelds für die erweiterte Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5498b6309c0c650f96503fbd30c62279c9dfd2ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578403"
---
# <a name="using-an-advanced-search-dialog-box"></a>Verwenden eines Dialogfelds für die erweiterte Suche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, mit der Clients andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) durchsuchen können. Adressbuchcontainer, die erweiterte Suchvorgänge unterstützen, verfügen über eine Containerobjekteigenschaft **namens PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Dieses Containerobjekt ermöglicht den Zugriff auf eine Anzeigetabelle, die das Suchdialogfeld beschreibt – ein Dialogfeld zum Eingeben und Bearbeiten der erweiterten Suchkriterien.
  
 **So führen Sie eine erweiterte Suche für einen Adressbuchcontainer durch**
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers auf, und geben Sie **PR_SEARCH** für das Eigenschaftentag und IID_IMAPIContainer für den Schnittstellenbezeichner an. 
    
2. Rufen Sie die **IMAPIProp::OpenProperty-Methode** des Suchobjekts auf, und geben Sie **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) für das Eigenschaftentag und IID_IMAPITable für den Schnittstellenbezeichner an. 
    
3. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Suchobjekts auf, um Werte für die Eigenschaften festzulegen, die in der erweiterten Suche verwendet werden sollen. 
    
4. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des Suchobjekts auf, um die erweiterten Suchkriterien zu speichern. 
    
Diese Abfolge von Aufrufen führt dazu, dass eine Einschränkung verfügbar ist, wenn ein Client die **GetSearchCriteria-Methode** des Suchobjekts aufruft. 
  

