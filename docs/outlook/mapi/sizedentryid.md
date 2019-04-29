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
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405709"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [Eintrags](entryid.md) -Struktur, die ein **ab** -Element einer angegebenen Größe enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parameter

__CB_
  
> Die Anzahl der Bytes im **ab** -Element der neuen Struktur. 
    
__Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedENTRYID** -Makro können Sie eine Eintrags-ID definieren, nachdem die Anforderungen an die Arraylänge bekannt sind. Verwenden Sie dieses Makro, um eine Eintrags-ID mit expliziten Begrenzungen zu erstellen. 
  
Um die neue Struktur zu verwenden, die aus dem **SizedENTRYID** -Makro als Zeiger auf eine **Eintrags** -Struktur resultiert, führen Sie die folgenden Schritte aus: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Siehe auch

- [ENTRYID](entryid.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

