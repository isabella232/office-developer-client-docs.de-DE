---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 27, 2021
ms.openlocfilehash: 98111b27b09082c6730b42b0f9d10bdd56d5614c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604908"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019
  
Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgegeben wird, wenn die angegebene Anzahl von Millisekunden abgelaufen ist oder mapi initialisiert wurde. INFINITE kann für eine unendliche Wartezeit verwendet werden.

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>Parameter
_Timeout_
> [in] Die Anzahl von Millisekunden, die auf die Initialisierung der MAPI gewartet werden soll, können Sie INFINITE (0xFFFFFFFF) übergeben, um für immer zu warten.

## <a name="return-value"></a>Rückgabewert

S_OK
> MAPI wurde erfolgreich initialisiert.

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> Wenn ein nicht unendliches Timeout angegeben wird, bedeutet dies, dass die MAPI während dieses Zeitraums nicht initialisiert wurde.

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
