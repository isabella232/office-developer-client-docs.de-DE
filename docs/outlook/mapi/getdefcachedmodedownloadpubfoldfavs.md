---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791812"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Betrifft**: Outlook 
  
Gibt an, ob der Exchange-Cache-Modus für den Ordner **Öffentliche Ordner-Favoriten** aktiviert ist, und gibt an, ob dies durch Richtlinien erzwungen wird. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |Msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

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



[GetDefCachedMode](getdefcachedmode.md)

