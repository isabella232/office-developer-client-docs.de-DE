---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571822"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt den Eigenschaftstyp von einem Tag für die angegebene Eigenschaft zurück.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Eigenschafts-Tag, die den Eigenschaftentyp zurückgegeben werden soll.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **PROP_TYPE** kann verwendet werden, um den Typ einer Eigenschaft ermitteln. Beispielsweise Aufruf PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) führt den Wert PT_BINARY zurückgegeben wird.
  
Jede Eigenschaftentag enthält den Eigenschaftstyp in das niederwertige Wort (Bits 0 bis 15) und der Eigenschaft-ID in das hohe Word (Bits 16 bis 31). Das Makro **PROP_TYPE** extrahiert den Eigenschaftentyp und legt es in Bits 0 bis 15, der die ganze Zahl zurückgegeben werden soll. Die verbleibenden Bits des Rückgabewerts werden für Nullen festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

