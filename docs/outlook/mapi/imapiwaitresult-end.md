---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 27, 2021
ms.openlocfilehash: 7cc5e122f71399232c07d94a13598b0c9a6fed31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630558"
---
# <a name="imapiwaitresultend"></a>IMAPIWaitResult::End
  
**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019

Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgegeben wird, wenn die angegebene Anzahl von Millisekunden abgelaufen ist oder mapi initialisiert wurde. INFINITE kann für eine unendliche Wartezeit verwendet werden.

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a>Parameter

_Timeout_
> [in] Die Anzahl von Millisekunden, um auf die Initialisierung der MAPI zu warten, können Sie INFINITE (0xFFFFFFFF) übergeben, um für immer zu warten.

## <a name="return-value"></a>Rückgabewert

S_OK
> MAPI wurde erfolgreich initialisiert

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> Wenn ein nicht unendliches Timeout angegeben wird, bedeutet dies, dass die MAPI während dieses Zeitraums nicht initialisiert wurde.

## <a name="remarks"></a>Bemerkungen
Diese API verhält sich genau wie [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).
  
## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
