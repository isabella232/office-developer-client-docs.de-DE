---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Ruft die nächste angegebene Anzahl von Blöcken von Frei/Gebucht-Daten in einer Enumeration ab.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422138"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Ruft die nächste angegebene Anzahl von Blöcken von Frei/Gebucht-Daten in einer Enumeration ab.
  
## <a name="quick-info"></a>QuickInfo

Weitere [Informationen finden Sie unter IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameter

_sellert_
  
> [in] Die Anzahl der abzurufende Frei/Gebucht-Datenblöcke in *pblk.* 
    
_pblk_
  
> [in] Ein Zeiger auf ein Array von Frei/Gebucht-Blöcken. Dem Array wird eine Größe von *Kelten zugewiesen.* Die angeforderten Frei/Gebucht-Blöcke werden in diesem Array zurückgegeben. 
    
_pcfetch_
  
> [out] Die Anzahl der frei/gebucht-Blöcke, die tatsächlich in *pblk zurückgegeben werden.* 
    
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

