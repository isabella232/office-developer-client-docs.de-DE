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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792443"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Betrifft**: Outlook 
  
Beendet die asynchrone Vorgänge derzeit in Arbeit für die Tabelle.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Eine oder mehrere asynchrone Vorgänge wurden angehalten.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Ein asynchroner Vorgang ist in Arbeit und kann nicht beendet werden oder wurde bereits abgeschlossen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::Abort** -Methode beendet jede asynchrone Operation, die derzeit ausgeführt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um herauszufinden, ob eine asynchrone Operation ausgeführt wird, rufen Sie die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode. 
  
**Abbrechen** die Verarbeitung von einem Aufruf der [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode wird angehalten, werden der Status der Tabelle zum Zeitpunkt wurde, die der Anruf **Abbrechen** verarbeitet wird. 
  
Wenn die Verarbeitung von einem Aufruf der [SortTable](imapitable-sorttable.md) -Methode **abgebrochen** wird angehalten, Sortierreihenfolge für die Tabelle nicht betroffenen und bleibt wie vor dem Aufruf der **SortTable** . 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[Methode IMAPITable:: Restrict](imapitable-restrict.md)
  
[SortTable](imapitable-sorttable.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

