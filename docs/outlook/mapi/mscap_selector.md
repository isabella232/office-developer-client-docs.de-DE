---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab0041d579f4c8aac6d531fe94a4b18ba7825379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575386"
---
# <a name="mscap_selector"></a>MSCAP_SELECTOR

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Funktionen an, die für einen Speicher zurückgegeben werden sollen.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>Elemente

 *MSCAP_SEL_RESERVED1* 
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_FOLDER* 
  
> Funktionen zum Unterstützen von Ordnern in einem Speicher.
    
 *MSCAP_SEL_RESERVED3* 
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Funktionen zur Unterstützung von Einschränkungen für einen Store.
    

