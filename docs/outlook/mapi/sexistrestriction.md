---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418939"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Exist-Einschränkung, die verwendet wird, um zu testen, ob eine bestimmte Eigenschaft als Spalte in der Tabelle vorhanden ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Elemente

 **ulReserved1**
  
> Reserviert; muss null sein. 
    
 **ulPropTag**
  
> Eigenschaftstag, das die Spalte identifiziert, die in jeder Zeile auf ihre Existenz getestet werden soll.
    
 **ulReserved2**
  
> Reserviert; muss null sein.
    
## <a name="remarks"></a>Hinweise

Die Exist-Einschränkung wird verwendet, um aussagekräftige Ergebnisse für andere Arten von Einschränkungen zu gewährleisten, die Eigenschaften betreffen, z. B. Eigenschaften- und Inhaltseinschränkungen. Wenn eine Einschränkung, die eine Eigenschaft umfasst, an [IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md) übergeben wird und die Eigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert. Durch Das Erstellen einer **AND-Einschränkung,** die die Eigenschaftseinschränkung mit einer vorhandenen Einschränkung beitritt, kann ein Aufrufer genaue Ergebnisse garantiert werden. 
  
Exist-Einschränkungen können nicht mit Unterobjekteigenschaften verwendet werden, die Typeigenschaften PT_OBJECT. 
  
Weitere Informationen zur **SExistRestriction-Struktur** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

