---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 27, 2021
ms.openlocfilehash: 922ce2f978b5ecfb6c2b34873f7b750b6022035f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564246"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019
  
Fragt die MAPI ab, um festzustellen, ob sie derzeit im aufrufenden Prozess initialisiert ist.

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a>Parameter
Keine

## <a name="return-value"></a>Rückgabewert
Ein BOOL, der den aktuellen Status der MAPI-Initialisierung angibt, bedeutet ein Wert von TRUE, dass die MAPI initialisiert wurde und zur Verwendung verfügbar ist, während der Wert FALSE bedeutet, dass die MAPI aktuell nicht initialisiert ist und nicht verwendet werden kann.

## <a name="remarks"></a>HinwBemerkungeneise
Dies kann verwendet werden, um festzustellen, ob die MAPI einsatzbereit ist, z. B. wenn Ihre Anwendung nur dann etwas tun möchte, wenn die MAPI bereits initialisiert wurde. Dies kann eine nützliche Überprüfung in einer Hintergrundaufgabe sein, um zu verhindern, dass die MAPI für optionale Arbeit rotiert wird.

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
