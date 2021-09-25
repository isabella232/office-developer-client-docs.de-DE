---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bc55f579e7d161d9899d29e5c8239db347980c53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630684"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Asynchrone Vorgänge wurden beendet.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Ein asynchroner Vorgang wird ausgeführt und kann nicht beendet werden, oder er wurde bereits abgeschlossen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::Abort-Methode** beendet alle asynchronen Vorgänge, die derzeit ausgeführt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) auf, um herauszufinden, ob ein asynchroner Vorgang ausgeführt wird. 
  
Wenn **Abort** die Verarbeitung eines Aufrufs der [IMAPITable::Restrict-Methode](imapitable-restrict.md) anbricht, entspricht der Status der Tabelle dem Zeitpunkt, zu dem der **Abort-Aufruf** verarbeitet wurde. 
  
Wenn **Abort** die Verarbeitung eines Aufrufs der [IMAPITable::SortTable-Methode](imapitable-sorttable.md) anbricht, bleibt die Sortierreihenfolge der Tabelle unverändert wie vor dem **SortTable-Aufruf.** 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

