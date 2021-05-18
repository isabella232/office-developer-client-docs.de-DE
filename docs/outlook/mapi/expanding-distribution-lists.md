---
title: Erweitern von Verteilerlisten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5731a35b5d570669d8606be6dd6ca1a23fb87e88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414137"
---
# <a name="expanding-distribution-lists"></a>Erweitern von Verteilerlisten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So fordert Sie MAPI auf, eine Verteilerliste zu erweitern**
  
- Legen Sie **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) -Eigenschaft auf MAPIPDL.
    
    MAPI erweitert Adressen mit diesem Typ, bevor die Nachricht an den Transportanbieter gesendet wird.
    

