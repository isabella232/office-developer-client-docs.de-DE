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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339277"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine exist-Einschränkung, die verwendet wird, um zu testen, ob eine bestimmte Eigenschaft als Spalte in der Tabelle vorhanden ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Reserviert muss NULL sein. 
    
 **ulPropTag**
  
> Property-Tag, der die zu testende Spalte identifiziert, die in jeder Zeile vorhanden ist.
    
 **ulReserved2**
  
> Reserviert muss NULL sein.
    
## <a name="remarks"></a>Bemerkungen

Die exist-Einschränkung wird verwendet, um aussagekräftige Ergebnisse für andere Arten von Einschränkungen zu gewährleisten, die Eigenschaften wie Eigenschafts-und Inhaltseinschränkungen einschließen. Wenn eine Einschränkung, die eine Eigenschaft umfasst, an [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md) übergeben wird und die Eigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert. Durch das Erstellen einer **and** -Einschränkung, die die Eigenschaftseinschränkung mit einer exist-Einschränkung verknüpft, kann ein Aufrufer exakte Ergebnisse garantieren. 
  
Exist-Einschränkungen können nicht mit Unterobjekt Eigenschaften verwendet werden, die den Typ PT_OBJECT haben. 
  
Weitere Informationen zur **SExistRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

