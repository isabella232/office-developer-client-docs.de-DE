---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062032"
---
# <a name="imapiwaitresultend"></a>IMAPIWaitResult::End
  
**Gilt für**: Outlook 2013 | Outlook 2016 | 2019

Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde. INFINITE kann für unendliche Wartezeiten verwendet werden.

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a>Parameter

_timeout_
> [in] Die Anzahl der Millisekunden, die auf die Initialisierung von MAPI gewartet werden sollen, können Sie INFINITE (0xFFFFFFFF) übergeben, um für immer zu warten.

## <a name="return-value"></a>Rückgabewert

S_OK
> MAPI wurde erfolgreich initialisiert

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> Bei einem nicht unendlichen Timeout bedeutet dies, dass MAPI während dieses Zeitraums nicht initialisiert wurde.

## <a name="remarks"></a>Bemerkungen
Diese API verhält sich genauso wie [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).
  
## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
