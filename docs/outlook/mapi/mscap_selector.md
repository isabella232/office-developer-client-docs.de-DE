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
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417203"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
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
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_FOLDER* 
  
> Funktionen zur Unterstützung von Ordnern in einem Speicher.
    
 *MSCAP_SEL_RESERVED3* 
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Funktionen zur Unterstützung von Einschränkungen in einem Speicher.
    

