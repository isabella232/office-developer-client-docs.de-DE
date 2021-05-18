---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278715"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Tabellenansicht und gibt einen Zeiger auf eine [IMAPITable-Implementierung](imapitableiunknown.md) zurück. 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Parameter

 _lpSSortOrderSet_
  
> [in] Ein Zeiger auf eine Sortierreihenfolgenstruktur, die die Sortierreihenfolge für die Tabellenansicht beschreibt. Wenn NULL im  _lpSSortOrderSet-Parameter übergeben_ wird, wird die Ansicht nicht sortiert. 
    
 _lpfCallerRelease_
  
> [in] Ein Zeiger auf eine Rückruffunktion basierend auf dem [CALLERRELEASE-Prototyp,](callerrelease.md) den MAPI aufruft, wenn die Ansicht veröffentlicht wird. Wenn NULL im  _lpfCallerRelease-Parameter übergeben_ wird, wird bei der Freigabe der Ansicht keine Funktion aufgerufen. 
    
 _ulCallerData_
  
> [in] Die Daten, die mit der neuen Ansicht gespeichert und an die Rückruffunktion übergeben werden müssen, auf die von _lpfCallerRelease verwiesen wird._
    
 _lppMAPITable_
  
> [out] Ein Zeiger auf einen Zeiger auf die neu erstellte Ansicht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Ansicht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrGetView-Methode** erstellt eine schreibgeschützte Ansicht der Daten in der Tabelle, sortiert in der Reihenfolge, auf die der  _lpSSortOrderSet-Parameter_ verweist. Der Cursor wird am Anfang der ersten Zeile in der Ansicht platziert. Eine **IMAPITable-Schnittstellenimplementierung** für den Zugriff auf die Ansicht wird zurückgegeben. 
  
Dienstanbieter rufen **HrGetView auf,** wenn sie einem Client Zugriff auf eine Tabelle geben müssen. **HrGetView** erstellt die Ansicht und gibt den **IMAPITable-Zeiger** zurück. Dienstanbieter geben den Zeiger wiederum an den Client weiter. Wenn der Client mit der Tabelle fertig ist und seine [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) aufruft, ruft **HrGetView** die Rückruffunktion auf, auf die der  _lpfCallerRelease-Parameter_ verweist. 
  
Wenn ein Dienstanbieter eine Ansicht mit einem angepassten Spaltensatz oder einer Einschränkung an einen Client zurückgeben muss, kann der Anbieter die [Methoden IMAPITable::SetColumns](imapitable-setcolumns.md) und [IMAPITable::Restrict](imapitable-restrict.md) der Ansicht aufrufen, bevor der Clientzugriff ermöglicht wird. 
  
## <a name="see-also"></a>Siehe auch



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

