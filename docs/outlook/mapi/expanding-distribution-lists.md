---
title: Erweitern von Verteilerlisten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d0bd0780d8148346e7a18017f0d66d672b16ac9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601058"
---
# <a name="expanding-distribution-lists"></a>Erweitern von Verteilerlisten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So fordern Sie die MAPI auf, eine Verteilerliste zu erweitern**
  
- Legen Sie die **eigenschaft PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) auf MAPIPDL fest.
    
    MAPI erweitert Adressen mit diesem Typ, bevor die Nachricht an den Transportanbieter gesendet wird.
    

