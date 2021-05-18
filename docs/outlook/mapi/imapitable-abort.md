---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406150"
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
  
> Mindestens ein asynchroner Vorgang wurde beendet.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Ein asynchroner Vorgang wird ausgeführt und kann nicht beendet oder bereits abgeschlossen werden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::Abort-Methode** beendet alle asynchronen Vorgänge, die derzeit ausgeführt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um herauszufinden, ob ein asynchroner Vorgang ausgeführt wird, rufen Sie die [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) auf. 
  
Wenn **Abort** die Verarbeitung eines Aufrufs der [IMAPITable::Restrict-Methode](imapitable-restrict.md) beendet, ist der Zustand der Tabelle so wie zum Zeitpunkt der Verarbeitung des **Abbruchaufrufs.** 
  
Wenn **Abort** die Verarbeitung eines Aufrufs der [IMAPITable::SortTable-Methode](imapitable-sorttable.md) beendet, ist die Sortierreihenfolge der Tabelle nicht betroffen und bleibt unverändert wie vor dem **SortTable-Aufruf.** 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

