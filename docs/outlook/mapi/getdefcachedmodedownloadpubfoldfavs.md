---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 602d9ce178c0d88192d3eaba899b15f6c2445c8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580174"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob zwischengespeicherter Exchange Modus für den Ordner **"Favoriten** für öffentliche Ordner" aktiviert ist und ob dies durch eine Richtlinie erzwungen wird. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameter

 _pfPolicy_
  
> [out]  true, wenn der Rückgabewert durch die Richtlinie erzwungen wird, false, wenn dies nicht der Fall ist.  
    
## <a name="return-values"></a>Rückgabewerte

 **STIMMT**
  
- Die Zwischenspeicherung ist aktiviert.
    
 **FALSE**
  
- Die Zwischenspeicherung ist deaktiviert.
    
## <a name="see-also"></a>Siehe auch



[GetDefCachedMode](getdefcachedmode.md)

