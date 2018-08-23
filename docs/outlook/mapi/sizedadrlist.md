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
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574741"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **SizedADRLIST** können Sie eine Empfängerliste definieren, die explizite Grenzen hat, wenn Array Länge Anforderungen bekannt sind. Der folgende Code zeigt, wie das Ergebnis des **SizedADRLIST** Makros in einer **ADRLIST** Struktur Zeiger umgewandelt wird: 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

