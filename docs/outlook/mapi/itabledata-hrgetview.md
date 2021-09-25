---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7567113d1247b55f1ee5a609964728980d928cac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613779"
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
  
> [in] Ein Zeiger auf eine Sortierreihenfolgestruktur, die die Sortierreihenfolge für die Tabellenansicht beschreibt. Wenn NULL im  _lpSSortOrderSet-Parameter_ übergeben wird, wird die Ansicht nicht sortiert. 
    
 _lpfCallerRelease_
  
> [in] Ein Zeiger auf eine Rückruffunktion basierend auf dem [CALLERRELEASE-Prototyp,](callerrelease.md) den MAPI aufruft, wenn sie die Ansicht freigibt. Wenn NULL im  _lpfCallerRelease-Parameter_ übergeben wird, wird bei der Freigabe der Ansicht keine Funktion aufgerufen. 
    
 _ulCallerData_
  
> [in] Die Daten, die mit der neuen Ansicht gespeichert und an die Rückruffunktion übergeben werden müssen, auf die durch  _lpfCallerRelease_ verwiesen wird.
    
 _lppMAPITable_
  
> [out] Ein Zeiger auf einen Zeiger auf die neu erstellte Ansicht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Ansicht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData::HrGetView-Methode** erstellt eine schreibgeschützte Ansicht der Daten in der Tabelle, sortiert in der Reihenfolge, auf die mit dem  _lpSSortOrderSet-Parameter_ verwiesen wird. Der Cursor wird am Anfang der ersten Zeile in der Ansicht platziert. Es wird eine **IMAPITable-Schnittstellenimplementierung** für den Zugriff auf die Ansicht zurückgegeben. 
  
Dienstanbieter rufen **HrGetView** auf, wenn sie einem Client Zugriff auf eine Tabelle gewähren müssen. **HrGetView** erstellt die Ansicht und gibt den **IMAPITable-Zeiger** zurück. Dienstanbieter wiederum übergeben den Zeiger an den Client. Wenn der Client mit der Verwendung der Tabelle fertig ist und die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) aufruft, ruft **HrGetView** die Rückruffunktion auf, auf die der  _Parameter "lpfCallerRelease"_ verweist. 
  
Wenn ein Dienstanbieter zu einem Client eine Ansicht zurückgeben muss, für die ein benutzerdefinierter Spaltensatz oder eine Einschränkung festgelegt ist, kann der Anbieter die [IMAPITable::SetColumns-](imapitable-setcolumns.md) und [IMAPITable::Restrict-Methoden](imapitable-restrict.md) der Ansicht aufrufen, bevor der Clientzugriff zugelassen wird. 
  
## <a name="see-also"></a>Siehe auch



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

