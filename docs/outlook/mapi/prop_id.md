---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573124"
---
# <a name="propid"></a>PROP_ID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt den Bezeichner eines angegebenen Eigenschaft-Tags.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Eigenschafts-Tag mit dem Bezeichner zurückgegeben werden soll.
    
## <a name="remarks"></a>HinwBemerkungeneise

Jede Eigenschaftentag enthält den Eigenschaftstyp in das niederwertige Wort (Bits 0 bis 15) und der Eigenschaft-ID in das hohe Word (Bits 16 bis 31). Das Makro **eigensch_id** extrahiert Bezeichner der und legt es in Bits 0 bis 15, der die ganze Zahl zurückgegeben werden soll. Die verbleibenden Bits des Rückgabewerts werden für Nullen festgelegt. 
  
Das Makro **eigensch_id** kann verwendet werden, um einen Bezeichner zum Übergeben an [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)abzurufen. **GetNamesFromIDs** abgerufen, der Name der Eigenschaft einen Bezeichner für eine benannte Eigenschaft zugeordnet wird. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

