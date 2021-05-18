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
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412744"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob Exchange für den privaten Exchange aktiviert ist und ob dies durch die Richtlinie erzwungen wird.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameter

 _pfPolicy_
  
> [out] **true,** wenn der Rückgabewert von der Richtlinie erzwungen wird, **false,** wenn dies nicht der Fall ist. 
    
## <a name="return-values"></a>Rückgabewerte

 **true**
  
- Die Zwischenspeicherung ist aktiviert.
    
 **false**
  
- Die Zwischenspeicherung ist deaktiviert.
    
## <a name="see-also"></a>Siehe auch



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

