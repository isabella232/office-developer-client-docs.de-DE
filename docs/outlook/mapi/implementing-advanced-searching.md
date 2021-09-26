---
title: Implementieren der erweiterten Suche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20282c78f6ff9003221429046fa9126cc4abaeec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610468"
---
# <a name="implementing-advanced-searching"></a>Implementieren der erweiterten Suche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Adressbuchcontainer unterstützen eine erweiterte Suchfunktion, mit der Clients andere Eigenschaften als **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) durchsuchen können. Um erweiterte Suchvorgänge zu unterstützen, muss Ihr Anbieter einen speziellen Container implementieren, auf den über die **eigenschaft PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) Ihrer anderen Container zugegriffen werden kann. **PR_SEARCH** enthält ein Containerobjekt, das Zugriff auf eine Anzeigetabelle bietet, in der das Dialogfeld zum Eingeben und Bearbeiten der erweiterten Suchkriterien beschrieben wird. 
  
 **So unterstützen Sie die erweiterte Suche**
  
1. Definieren Sie eine Eigenschaft für jedes Suchkriterium.
    
2. Im Codeabschnitt der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) Ihres Containers, die die **PR_SEARCH-Eigenschaft** behandelt: 
    
1. Überprüfen Sie, ob der Client die **IMAPIContainer-Schnittstelle anfordert.** Wenn eine unangemessene Schnittstelle angefordert wird, schlagen Sie fehl, und geben Sie MAPI_E_INTERFACE_NOT_SUPPORTED zurück. 
    
2. Erstellen Sie ein neues Suchobjekt, das die **IMAPIContainer-Schnittstelle** unterstützt. 
    
3. An diesem Punkt wird die **IMAPIProp::OpenProperty-Methode** des Suchcontainers aufgerufen, um die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft abzurufen. Ihr Anbieter muss eine Anzeigetabelle bereitstellen, in der Regel über einen Aufruf von [BuildDisplayTable,](builddisplaytable.md)in der das Dialogfeld für die erweiterte Suche des Containers beschrieben wird.
    
4. MAPI zeigt das Suchdialogfeld an, in dem der Benutzer die entsprechenden Kriterien eingeben kann. Wenn der Benutzer fertig ist, ruft MAPI die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Containers auf, um die Suchkriterien zu speichern. 
    
5. Es wird ein Aufruf ausgeführt, um das Inhaltsverzeichnis Ihres Suchcontainers anzufordern. Füllen Sie das Inhaltsverzeichnis mit allen Einträgen im Container auf, die den Kriterien entsprechen.
    

