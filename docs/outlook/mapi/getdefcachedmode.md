---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791813"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Betrifft**: Outlook 
  
Gibt an, ob der Exchange-Cache-Modus für private Exchange-Speicher aktiviert ist, und gibt an, ob dies durch Richtlinien erzwungen wird.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |Msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameter

 _pfPolicy_
  
> [out] **true,** Wenn der Rückgabewert ist dies nicht durch Richtlinien, **false** erzwungen wird. 
    
## <a name="return-values"></a>Rückgabewerte

 **"true"**
  
- Das Zwischenspeichern ist aktiviert.
    
 **false**
  
- Zwischenspeichern ist deaktiviert.
    
## <a name="see-also"></a>Siehe auch



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

