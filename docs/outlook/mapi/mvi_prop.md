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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410679"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die MVI_FLAG für eine angegebene Eigenschaft fest. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameter

 _tag_
  
> Das zu ändernde Eigenschaftstag.
    
## <a name="remarks"></a>Hinweise

Das MVI_FLAG kombiniert die Einstellung von MV_FLAG, identifiziert eine Eigenschaft als mehrwertigen Wert und MV_INSTANCE und fordert an, dass eine mehrwertige Eigenschaft in einer Tabelle in mehreren Zeilen angezeigt wird. Der Eigenschaftentyp der betroffenen Eigenschaft wird geändert, der Bezeichner bleibt jedoch unverändert. 
  
Wenn das Makro MVI_PROP auf eine Eigenschaft vom Typ PT_FLOAT angewendet wird, wird der Typ in PT_MV_FLOAT. Wenn sie in einer Tabelle enthalten sind, werden mehrere Zeilen verwendet, um die Eigenschaft mit einer Zeile für jeden Wert zu repräsentieren. Die Eigenschaften für die anderen Spalten werden wiederholt. 
  
Weitere Informationen zu diesen Kennzeichen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md) und [Working with Multivalued Columns](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

