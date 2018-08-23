---
title: Zugreifen auf die Mitglieder einer Verteilerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595363"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Zugreifen auf die Mitglieder einer Verteilerliste

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **Zum Abrufen der Mitglieder einer Verteilerliste**
  
1. Erstellen Sie ein Größe Eigenschaft Tag-Array mit den Eigenschaften der Elemente aus, wie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([ abgerufen werden sollen. PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , um die Verteilerliste zu öffnen. 
    
3. Rufen Sie die Verteilerliste **IABContainer::GetContentsTable** -Methode zum Zugriff auf die Inhaltstabelle. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) zum Abrufen aller Zeilen der Tabelle, die Mitglieder der Verteilerliste darstellt. 
    

