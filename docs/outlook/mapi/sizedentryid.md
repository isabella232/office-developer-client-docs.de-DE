---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563870"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [ENTRYID](entryid.md) -Struktur, die ein Element **Ab** einer angegebenen Größe enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parameter

__cb_
  
> Die Anzahl von Bytes in die neue Struktur Mitglied **Ab** . 
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **SizedENTRYID** können Sie eine Eintrags-ID zu definieren, nach dem Array Länge Anforderungen bekannt sind. Verwenden Sie dieses Makro mit expliziten Grenzen eines Eintrags-ID zu erstellen. 
  
Um die neue Struktur verwenden, die als Zeiger auf eine **ENTRYID** -Struktur aus dem Makro **SizedENTRYID** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Siehe auch

- [ENTRYID](entryid.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

