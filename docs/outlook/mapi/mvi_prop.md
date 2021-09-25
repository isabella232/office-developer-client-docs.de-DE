---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22521bce4bec39c3d7c21cb7c69d1e1e20cdb0d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556035"
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

 _Tag_
  
> Das zu ändernde Eigenschaftentag.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das MVI_FLAG kombiniert die Einstellung von MV_FLAG, die Identifizierung einer Eigenschaft als mehrwertige eigenschaft und MV_INSTANCE und fordert an, dass eine mehrwertige Eigenschaft in einer Tabelle in mehreren Zeilen angezeigt wird. Der Eigenschaftstyp der betroffenen Eigenschaft wird geändert, der Bezeichner bleibt jedoch unverändert. 
  
Wenn das MVI_PROP Makro beispielsweise auf eine Eigenschaft vom Typ PT_FLOAT angewendet wird, wird der Typ in PT_MV_FLOAT geändert. Wenn sie in einer Tabelle enthalten ist, werden mehrere Zeilen verwendet, um die Eigenschaft darzustellen, die für jeden Wert eine Zeile enthält. Die Eigenschaften für die anderen Spalten werden wiederholt. 
  
Weitere Informationen zu diesen Flags finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

