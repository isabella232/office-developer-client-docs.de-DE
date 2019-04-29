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
# <a name="mviprop"></a>MVI_PROP

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die MVI_FLAG für eine angegebene Eigenschaft fest. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameter

 _Tag_
  
> Das zu ändernde Property-Tag.
    
## <a name="remarks"></a>Bemerkungen

Das MVI_FLAG kombiniert die Einstellung von MV_FLAG, identifiziert eine Eigenschaft als mehrwertige und MV_INSTANCE und fordert, dass eine mehrwertige Eigenschaft in einer Tabelle in mehreren Zeilen angezeigt wird. Der Eigenschaftentyp der betroffenen Eigenschaft wird geändert, aber der Bezeichner bleibt unverändert. 
  
Wenn beispielsweise das MVI_PROP-Makro auf eine Eigenschaft vom Typ PT_FLOAT angewendet wird, wird der Typ in PT_MV_FLOAT geändert. Wenn Sie in einer Tabelle enthalten sind, werden mehrere Zeilen verwendet, um die Eigenschaft darzustellen, die eine Zeile für jeden Wert enthält. Die Eigenschaften für die anderen Spalten werden wiederholt. 
  
Weitere Informationen zu diesen Flags finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md) und [Working with mehrwertig Columns](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

