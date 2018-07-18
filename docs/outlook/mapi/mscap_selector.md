---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19793268"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Betrifft**: Outlook 
  
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
    

