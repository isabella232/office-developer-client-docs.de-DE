---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Ruft die Anzahl der nächste angegebene Blöcke mit Frei/Gebucht-Daten in eine Enumeration.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790957"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Ruft die Anzahl der nächste angegebene Blöcke mit Frei/Gebucht-Daten in eine Enumeration.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameter

_celt_
  
> [in] Die Anzahl der Frei/Gebucht-Daten Bausteine in *Pblk* abgerufen. 
    
_PBLK_
  
> [in] Ein Zeiger auf ein Array von Frei/Gebucht-Blöcke. Das Array ist eine Größe von *Celt* zugewiesen. Die angeforderte Blöcke Frei/Gebucht-Informationen werden in diesem Array zurückgegeben. 
    
_pcfetch_
  
> [out] Die Anzahl der Frei/Gebucht-Blöcke, die tatsächlich in *Pblk* zurückgegeben. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Die angeforderte Anzahl Blöcke wurde zurückgegeben.  <br/> |
|S_FALSE  <br/> |Die angeforderte Anzahl Blöcke wurde nicht zurückgegeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

