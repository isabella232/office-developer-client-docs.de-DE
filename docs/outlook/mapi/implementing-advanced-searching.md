---
title: Implementieren der erweiterten Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332816"
---
# <a name="implementing-advanced-searching"></a>Implementieren der erweiterten Suche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, die es Clients ermöglicht, andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zu suchen. Zur Unterstützung erweiterter Suchvorgänge muss der Anbieter einen speziellen Container implementieren, auf den über die **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md))-Eigenschaft der anderen Container zugegriffen werden kann. **PR_SEARCH** enthält ein Container-Objekt, das Zugriff auf eine Anzeigetabelle bietet, in der das Dialogfeld beschrieben wird, das zum eingeben und Bearbeiten der erweiterten Suchkriterien verwendet wird. 
  
 **So unterstützen Sie die erweiterte Suche**
  
1. Definieren Sie eine Eigenschaft für jedes Suchkriterium.
    
2. Im Codeabschnitt in der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode ihres Containers, die die **PR_SEARCH** -Eigenschaft behandelt: 
    
1. Überprüfen Sie, ob der Client die **IMAPIContainer** -Schnittstelle anfordert. Wenn eine ungeeignete Schnittstelle angefordert wird, schlagen Sie fehl und geben MAPI_E_INTERFACE_NOT_SUPPORTED zurück. 
    
2. Erstellen Sie ein neues Search-Objekt, das die **IMAPIContainer** -Schnittstelle unterstützt. 
    
3. An dieser Stelle wird ein Aufruf an die **IMAPIProp:: OpenProperty** -Methode des Such Containers durchgeführt, um die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft abzurufen. Der Anbieter muss eine Anzeigetabelle angeben, normalerweise durch einen Aufruf von [BuildDisplayTable](builddisplaytable.md), der das Dialogfeld Erweiterte Suche des Containers beschreibt.
    
4. MAPI zeigt das Dialogfeld Suchen an, in dem der Benutzer die entsprechenden Kriterien eingeben kann. Wenn der Benutzer fertig ist, ruft MAPI die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Containers auf, um die Suchkriterien zu speichern. 
    
5. Es wird ein Anruf getätigt, um die Inhaltstabelle Ihres Such Containers anzufordern. Füllen Sie die Tabelle Contents mit allen Einträgen im Container, die den Kriterien entsprechen.
    

