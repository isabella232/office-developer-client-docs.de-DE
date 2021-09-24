---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b4bbc92c1e7784053773d70c49d204a39e1967f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550014"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine [ADRLIST-Struktur](adrlist.md) mit dem angegebenen Namen, die eine angegebene Anzahl von [ADRENTRY-Strukturen](adrentry.md) enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parameter

_ _centries_
  
> Anzahl der **ADRENTRY-Strukturen,** die in der neuen **ADRLIST-Struktur** enthalten sein sollen. 
    
_ _Name_
  
> Name für die neue **ADRLIST-Struktur.** 
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeADRLIST** können Sie eine Empfängerliste definieren, die explizite Grenzen aufweist, wenn Anforderungen an die Arraylänge bekannt sind. Der folgende Code zeigt, wie das Ergebnis des **Makros SizeADRLIST** in einen **ADRLIST-Strukturzeiger** umgewandelt wird: 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

