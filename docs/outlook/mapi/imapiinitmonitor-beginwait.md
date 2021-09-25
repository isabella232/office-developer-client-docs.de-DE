---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 27, 2021
ms.openlocfilehash: beda62b375ce39283030409149c7130ffbcfd517
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564239"
---
# <a name="imapiinitmonitorbeginwait"></a>IMAPIInitMonitor::BeginWait
  
**Gilt für:** Outlook 2016 | Outlook 2019
  
Starten Sie eine Wartezeit für die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden. Dadurch wird eine IMAPIWaitResult-Schnittstelle zurückgegeben, die **IMAPIWaitResult::End** aufgerufen werden sollte, um die Wartezeit zu initiieren. Dadurch kann der Aufrufer steuern, welcher Thread während des Wartens blockiert wird.

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a>Parameter
_Timeout_
>[in] Die Anzahl der Millisekunden, um auf die MAPI-Initialisierung zu warten, kann auf INFINITE festgelegt werden, um für immer auf die Initialisierung zu warten.

_ppResult_
>[out] Ein Zeiger zum Empfangen der neu erstellten Warteschnittstelle.

## <a name="return-value"></a>Rückgabewert
S_OK
>Ein Wartevorgang wurde erfolgreich gestartet.

E_OUTOFMEMORY
>Es war nicht genügend Arbeitsspeicher vorhanden, um ein neues Objekt zu erstellen.

## <a name="remarks"></a>HinwBemerkungeneise
Diese API hat dem Aufrufer eine Schnittstelle bereitgestellt (die threadsicher ist), die verwendet werden kann, um eine Blockierungswarte wartezeit für die MAPI-Initialisierung zu initiieren. Auf diese Weise kann der Verbraucher die beste Wartezeit auf seine Anwendung abwarten. Das Verhalten des Aufrufens von IMAPIWaitResult::End ist identisch mit dem Aufrufen von IMAPIInitMonitor::Wait.

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
