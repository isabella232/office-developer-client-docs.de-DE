---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062018"
---
# <a name="imapiinitmonitorbeginwait"></a>IMAPIInitMonitor::BeginWait
  
**Gilt für**: Outlook 2016 | 2019
  
Starten Sie eine Wartezeit auf die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden bis zum Verstreichen. Dadurch wird eine IMAPIWaitResult-Schnittstelle zurückgegeben, auf die **IMAPIWaitResult::End** aufgerufen werden sollte, um das Warten zu initiieren. Dadurch kann der Aufrufer steuern, welcher Thread während der Wartezeit blockiert wird.

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a>Parameter
_timeout_
>[in] Die Anzahl der Millisekunden, die auf die MAPI-Initialisierung gewartet werden müssen, kann auf INFINITE festgelegt werden, um für immer auf die Initialisierung zu warten.

_ppResult_
>[out] Ein Zeiger zum Empfangen der neu erstellten Warteschnittstelle.

## <a name="return-value"></a>Rückgabewert
S_OK
>Ein Wartevorgang wurde erfolgreich gestartet.

E_OUTOFMEMORY
>Es war nicht genügend Arbeitsspeicher vorhanden, um ein neues Objekt zu erstellen.

## <a name="remarks"></a>Hinweise
Diese API hat dem Aufrufer eine Schnittstelle (threadsicher) bereitgestellt, die verwendet werden kann, um eine Blockierungswarte warten auf die MAPI-Initialisierung zu initiieren. Auf diese Weise kann der Verbraucher am besten auf die Anwendung warten.   Das Verhalten des Aufrufens von IMAPIWaitResult::End ist identisch mit dem Aufrufen von IMAPIInitMonitor::Wait.

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
