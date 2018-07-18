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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795530"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Betrifft**: Outlook 
  
Definiert eine [ADRLIST](adrlist.md) -Struktur mit dem angegebenen Namen, der eine angegebene Anzahl von [ADRENTRY](adrentry.md) Strukturen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parameter

__centries_
  
> Anzahl der **ADRENTRY** Strukturen, die in der neuen **ADRLIST** -Struktur eingeschlossen werden. 
    
__Namen_
  
> Der Name für die neue **ADRLIST** -Struktur. 
    
## <a name="remarks"></a>Bemerkungen

Das Makro **SizedADRLIST** können Sie eine Empfängerliste definieren, die explizite Grenzen hat, wenn Array Länge Anforderungen bekannt sind. Der folgende Code zeigt, wie das Ergebnis des **SizedADRLIST** Makros in einer **ADRLIST** Struktur Zeiger umgewandelt wird: 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

