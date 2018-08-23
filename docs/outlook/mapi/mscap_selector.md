---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588125"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, das die Funktionen für einen Speicher zurückgegeben.
  
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
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_FOLDER* 
  
> Funktionen zur Unterstützung von Ordnern in einem Speicher.
    
 *MSCAP_SEL_RESERVED3* 
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Funktionen zur Unterstützung von Einschränkungen in einem Speicher.
    

