---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793310"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**Betrifft**: Outlook 
  
Legt die MVI_FLAG für eine angegebene Eigenschaft fest. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameter

 _Tag_
  
> Die Eigenschaftentag geändert werden soll.
    
## <a name="remarks"></a>Hinweise

Die MVI_FLAG kombiniert die Einstellung der MV_FLAG, Identifizieren einer Eigenschaft als mehrwertige, und MV_INSTANCE vorhanden, anfordern, dass eine mehrwertige Eigenschaft in einer Tabelle in mehrere Zeilen angezeigt werden. Der Eigenschaftentyp der betroffenen-Eigenschaft wird so geändert, aber der Bezeichner bleibt unverändert. 
  
Wenn das Makro MVI_PROP auf eine Eigenschaft vom Typ PT_FLOAT angewendet wird, wird dieses Typs PT_MV_FLOAT geändert. Wenn in einer Tabelle enthalten, werden mehrere Zeilen verwendet, um die Eigenschaft darstellen, die eine Zeile für jeden Wert hat. Die Eigenschaften für die anderen Spalten werden wiederholt. 
  
Weitere Informationen zu diesen Flags finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md) und [Arbeiten mit Spalten mit mehreren Werten](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

