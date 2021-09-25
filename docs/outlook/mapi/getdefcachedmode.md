---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 174320928f94992c010e5c4349ba66e2ec6457cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614164"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob der zwischengespeicherte Exchange modus für den privaten Exchange Speicher aktiviert ist und ob dies durch eine Richtlinie erzwungen wird.
  
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
  
> [out]  true, wenn der Rückgabewert durch die Richtlinie erzwungen wird, false, wenn dies nicht der Fall ist.  
    
## <a name="return-values"></a>Rückgabewerte

 **STIMMT**
  
- Die Zwischenspeicherung ist aktiviert.
    
 **FALSE**
  
- Die Zwischenspeicherung ist deaktiviert.
    
## <a name="see-also"></a>Siehe auch



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

