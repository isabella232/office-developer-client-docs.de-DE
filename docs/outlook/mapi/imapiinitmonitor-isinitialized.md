---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062025"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**Gilt für**: Outlook 2013 | Outlook 2016 | 2019
  
Fragt MAPI ab, um zu ermitteln, ob es derzeit im aufrufenden Prozess initialisiert wurde.

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a>Parameter
Keine

## <a name="return-value"></a>Rückgabewert
Ein BOOL, der den aktuellen Zustand der MAPI-Initialisierung angibt, ein Wert von TRUE bedeutet, dass MAPI initialisiert wurde und zur Verwendung verfügbar ist, während der Wert FALSE bedeutet, dass MAPI aktuell nicht initialisiert ist und nicht verwendet werden kann.

## <a name="remarks"></a>Bemerkungen
Dies kann verwendet werden, um zu ermitteln, ob MAPI einsatzbereit ist, z. B. wenn Ihre Anwendung nur dann etwas tun wollte, wenn MAPI bereits initialisiert wurde, könnte dies eine nützliche Überprüfung einer Hintergrundaufgabe sein, um die Kosten für das Drehen von MAPI für optionale Arbeit zu verhindern.

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
