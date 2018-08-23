---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591394"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

 **true**
  
- Das Zwischenspeichern ist aktiviert.
    
 **false**
  
- Zwischenspeichern ist deaktiviert.
    
## <a name="see-also"></a>Siehe auch



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

