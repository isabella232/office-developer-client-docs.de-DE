---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Erstellt eine Kopie der Enumerator, verwenden die gleichen zeitliche Beschränkung jedoch festlegen des Cursors an den Anfang des den Enumerator.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790951"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Erstellt eine Kopie der Enumerator, verwenden die gleichen zeitliche Beschränkung jedoch festlegen des Cursors an den Anfang des den Enumerator.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Parameter

_ppclone_
  
> [out] Ein Zeiger auf Zeiger auf die Kopie der [IEnumFBBlock](ienumfbblock.md) -Schnittstelle. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OUTOFMEMORY  <br/> |Es ist nicht genügend Speicherplatz für die Kopie.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

