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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407389"
---
# <a name="implementing-advanced-searching"></a>Implementieren der erweiterten Suche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, mit der Clients nach anderen Eigenschaften als PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) suchen können. Um erweiterte Suchen zu unterstützen, muss Ihr Anbieter einen speziellen Container implementieren, auf den über die **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md))-Eigenschaft Ihrer anderen Container zugegriffen werden kann. **PR_SEARCH** enthält ein Containerobjekt, das Zugriff auf eine Anzeigetabelle bietet, in der das Dialogfeld zum Eingeben und Bearbeiten der erweiterten Suchkriterien beschrieben wird. 
  
 **So unterstützen Sie die erweiterte Suche**
  
1. Definieren Sie eine Eigenschaft für jedes Suchkriterium.
    
2. Im Codeabschnitt in der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) Ihres Containers, die die PR_SEARCH **behandelt:** 
    
1. Überprüfen Sie, ob der Client die **IMAPIContainer-Schnittstelle** anfordert. Wenn eine unangemessene Schnittstelle angefordert wird, führen Sie einen Fehler aus, und geben Sie MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Erstellen Sie ein neues Suchobjekt, das die **IMAPIContainer-Schnittstelle** unterstützt. 
    
3. An diesem Punkt wird die **IMAPIProp::OpenProperty-Methode** des Suchcontainers aufgerufen, um die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft abzurufen. Ihr Anbieter muss eine Anzeigetabelle liefern, in der Regel über einen Aufruf von [BuildDisplayTable,](builddisplaytable.md)in der das dialogfeld erweiterte Suche des Containers beschrieben wird.
    
4. MAPI zeigt das Suchdialogfeld an, sodass der Benutzer die entsprechenden Kriterien eingeben kann. Wenn der Benutzer fertig ist, ruft MAPI die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Containers auf, um die Suchkriterien zu speichern. 
    
5. Es wird ein Aufruf zum Anfordern des Inhaltsverzeichnisses des Suchcontainers vorgenommen. Füllen Sie die Inhaltstabelle mit allen Einträgen im Container auf, die den Kriterien entsprechen.
    

