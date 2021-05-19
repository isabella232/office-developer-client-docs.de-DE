---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062011"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**Gilt für**: Outlook 2013 | Outlook 2016 | 2019
  
Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde. INFINITE kann für unendliche Wartezeiten verwendet werden.

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>Parameter
_timeout_
> [in] Die Anzahl der Millisekunden, die auf die Initialisierung von MAPI gewartet werden müssen, können Sie INFINITE (0xFFFFFFFF) übergeben, um für immer zu warten.

## <a name="return-value"></a>Rückgabewert

S_OK
> MAPI wurde erfolgreich initialisiert.

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> Bei einem nicht unendlichen Timeout bedeutet dies, dass MAPI während dieses Zeitraums nicht initialisiert wurde.

## <a name="remarks"></a>Hinweise
  
## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
