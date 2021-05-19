---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423461"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine [ADRLIST-Struktur](adrlist.md) mit dem angegebenen Namen, der eine angegebene Anzahl von [ADRENTRY-Strukturen](adrentry.md) enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parameter

_ _Centries_
  
> Anzahl der **ADRENTRY-Strukturen,** die in die neue **ADRLIST-Struktur einbezogen werden** sollen. 
    
_ _name_
  
> Name für die neue **ADRLIST-Struktur.** 
    
## <a name="remarks"></a>Hinweise

Mit **dem Makro SizedADRLIST** können Sie eine Empfängerliste definieren, die explizite Grenzen hat, wenn Arraylängenanforderungen bekannt sind. Der folgende Code zeigt, wie das Ergebnis des **SizeADRLIST-Makros** in einen **ADRLIST-Strukturzeiger** umgleitiert wird: 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

