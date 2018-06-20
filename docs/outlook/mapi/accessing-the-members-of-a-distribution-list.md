---
title: Zugreifen auf die Mitglieder von Verteilerlisten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791258"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Zugreifen auf die Mitglieder von Verteilerlisten

  
  
**Betrifft**: Outlook 
  
 **Zum Abrufen der Mitglieder einer Verteilerliste**
  
1. Erstellen Sie ein Größe Eigenschaft Tag-Array mit den Eigenschaften der Elemente aus, wie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([ abgerufen werden sollen. PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , um die Verteilerliste zu öffnen. 
    
3. Rufen Sie die Verteilerliste **IABContainer::GetContentsTable** -Methode zum Zugriff auf die Inhaltstabelle. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) zum Abrufen aller Zeilen der Tabelle, die Mitglieder der Verteilerliste darstellt. 
    

