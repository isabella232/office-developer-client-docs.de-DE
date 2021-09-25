---
title: Zugreifen auf die Mitglieder einer Verteilerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3a11b53aebf1e25ef93ac778da3e69401f1416f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605223"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Zugreifen auf die Mitglieder einer Verteilerliste

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So rufen Sie die Mitglieder einer Verteilerliste ab**
  
1. Erstellen Sie ein Eigenschaftentagarray der Größe mit den Eigenschaften der Elemente, die Sie abrufen möchten, z. **B. PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) auf, um die Verteilerliste zu öffnen. 
    
3. Rufen Sie die **IABContainer::GetContentsTable-Methode** der Verteilerliste auf, um auf das Inhaltsverzeichnis zuzugreifen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen der Tabelle abzurufen, die die Mitglieder der Verteilerliste darstellen. 
    

