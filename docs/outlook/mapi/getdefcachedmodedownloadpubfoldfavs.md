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
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299888"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob der Exchange-Cache-Modus für den Ordner **Favoriten für Öffentliche Ordner** aktiviert ist und ob dieser durch die Richtlinie erzwungen wird. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32. dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

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



[GetDefCachedMode](getdefcachedmode.md)

