---
title: Verwenden eines Dialogfelds für die erweiterte Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437301"
---
# <a name="using-an-advanced-search-dialog-box"></a>Verwenden eines Dialogfelds für die erweiterte Suche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, mit der Clients nach anderen Eigenschaften als PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) suchen können. Adressbuchcontainer, die erweiterte Suchen unterstützen, verfügen über eine Containerobjekteigenschaft namens **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Dieses Containerobjekt bietet Zugriff auf eine Anzeigetabelle, die das Suchdialogfeld beschreibt – ein Dialogfeld, das zum Eingeben und Bearbeiten der erweiterten Suchkriterien verwendet wird.
  
 **So führen Sie eine erweiterte Suche in einem Adressbuchcontainer aus**
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md)  des Containers auf, und geben PR_SEARCH für das Eigenschaftstag und IID_IMAPIContainer für die Schnittstellen-ID an. 
    
2. Rufen Sie die **IMAPIProp::OpenProperty-Methode** des Suchobjekts auf, und geben Sie **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) für das Eigenschaftstag und IID_IMAPITable für den Schnittstellenbezeichner an. 
    
3. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Suchobjekts auf, um Werte für die Eigenschaften zu erstellen, die in der erweiterten Suche verwendet werden sollen. 
    
4. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des Suchobjekts auf, um die erweiterten Suchkriterien zu speichern. 
    
Diese Abfolge von Aufrufen führt dazu, dass eine Einschränkung verfügbar ist, wenn ein Client die **GetSearchCriteria-Methode des Suchobjekts** aufruft. 
  

