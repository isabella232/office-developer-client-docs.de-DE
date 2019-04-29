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
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412387"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Zugreifen auf die Mitglieder einer Verteilerliste

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So rufen Sie die Mitglieder einer Verteilerliste ab**
  
1. Erstellen Sie ein Array mit den Eigenschaften der Elemente, die Sie abrufen möchten, wie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) auf, um die Verteilerliste zu öffnen. 
    
3. Rufen Sie die **IABContainer::** getcontentable-Methode der Verteilerliste auf, um auf Ihre Inhaltstabelle zuzugreifen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Tabellenzeilen abzurufen, die die Mitglieder der Verteilerliste darstellen. 
    

