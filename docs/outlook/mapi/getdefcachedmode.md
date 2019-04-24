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
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299706"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob der Exchange-Cache-Modus für den privaten Exchange-Speicher aktiviert ist und ob dieser durch Richtlinien erzwungen wird.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32. dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameter

 _pfPolicy_
  
> Out **true** , wenn der Rückgabewert durch die Richtlinie erzwungen wird, **false** , wenn dies nicht der Fall ist. 
    
## <a name="return-values"></a>Rückgabewerte

 **true**
  
- Zwischenspeicherung ist aktiviert.
    
 **false**
  
- Zwischenspeicherung ist deaktiviert.
    
## <a name="see-also"></a>Siehe auch



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

