---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Ruft die nächste angegebene Anzahl von Frei/Gebucht-Datenblöcken in einer Enumeration ab.
ms.openlocfilehash: b1ebf09aaca466fdd6ee9fc3017d6b395d4326ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605428"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Ruft die nächste angegebene Anzahl von Frei/Gebucht-Datenblöcken in einer Enumeration ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameter

_Celt_
  
> [in] Die Anzahl der Frei/Gebucht-Datenblöcke in  *Pblk,*  die abgerufen werden sollen. 
    
_Pblk_
  
> [in] Ein Zeiger auf ein Array von Frei/Gebucht-Blöcken. Dem Array wird eine Größe von  *Celt*  zugewiesen. Die angeforderten Frei/Gebucht-Blöcke werden in diesem Array zurückgegeben. 
    
_pcfetch_
  
> [out] Die Anzahl der Frei/Gebucht-Blöcke, die tatsächlich in Pblk zurückgegeben *werden.* 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Die angeforderte Anzahl von Blöcken wurde zurückgegeben.  <br/> |
|S_FALSE  <br/> |Die angeforderte Anzahl von Blöcken wurde nicht zurückgegeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

