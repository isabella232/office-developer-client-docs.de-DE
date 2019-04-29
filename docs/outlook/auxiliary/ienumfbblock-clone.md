---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Erstellt eine Kopie des Enumerators, wobei dieselbe Zeiteinschränkung verwendet wird, der Cursor jedoch auf den Anfang des Enumerators festgelegt wird.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413402"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Erstellt eine Kopie des Enumerators, wobei dieselbe Zeiteinschränkung verwendet wird, der Cursor jedoch auf den Anfang des Enumerators festgelegt wird.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Parameter

_ppclone_
  
> Out Ein Zeiger auf die Kopie der [IEnumFBBlock](ienumfbblock.md) -Schnittstelle. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OUTOFMEMORY  <br/> |Es ist nicht genügend Arbeitsspeicher für die Kopie vorhanden.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (frei/gebucht-API)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

