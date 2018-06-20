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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a913f2f3a72a365ec7d5078eccf31c4212ca83a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792845"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Betrifft**: Outlook 
  
Erstellt eine Tabellenansicht, einen Zeiger auf eine Implementierung [IMAPITable](imapitableiunknown.md) zurückgibt. 
  
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
  
> [in] Ein Zeiger auf eine Sortierung Reihenfolge-Struktur, die Sortierreihenfolge für die Tabellenansicht beschreibt. Wenn NULL in der _LpSSortOrderSet_ -Parameter übergeben wird, wird die Ansicht nicht sortiert. 
    
 _lpfCallerRelease_
  
> [in] Ein Zeiger auf eine Rückruffunktion, die basierend auf der [CALLERRELEASE](callerrelease.md) Prototyp, den MAPI-aufrufen, wenn sie die Ansicht loslässt. Wenn NULL in der _LpfCallerRelease_ -Parameter übergeben wird, wird auf die Version der Ansicht keine Funktion aufgerufen. 
    
 _ulCallerData_
  
> [in] Die Daten, die mit der neuen Ansicht gespeichert und an die Rückruffunktion übergeben werden müssen, auf die _LpfCallerRelease_.
    
 _lppMAPITable_
  
> [out] Ein Zeiger auf einen Zeiger auf die neu erstellte Ansicht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Ansicht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrGetView** -Methode erstellt eine schreibgeschützte Ansicht der Daten in der Tabelle, in der auf das durch den Parameter _LpSSortOrderSet_ Reihenfolge sortiert. Der Cursor befindet sich am Anfang der ersten Zeile in der Ansicht. Eine Implementierung von **IMAPITable** für den Zugriff auf die Ansicht wird zurückgegeben. 
  
Dienstanbieter Aufrufen **HrGetView** , wenn sie eine Clientzugriff auf eine Tabelle gewähren müssen. **HrGetView** die Ansicht erstellt und gibt den **IMAPITable** Zeiger zurück. Dienstanbieter übergeben wiederum den Mauszeiger an den Client. Wenn der Client mithilfe der Tabelle abgeschlossen ist und dessen [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode aufruft, ruft **HrGetView** die Callback-Funktion, die auf den durch den Parameter _LpfCallerRelease_ verwiesen. 
  
Wenn es sich bei ein Dienstanbieter muss eine Ansicht an einen Client zurück, die eine benutzerdefinierte Spalte festgelegt wurde, oder eine Einschränkung der Anbieter Aufrufen der Ansicht [IMAPITable::SetColumns](imapitable-setcolumns.md) [Methode IMAPITable:: Restrict](imapitable-restrict.md) Methoden und bevor die Clientzugriff. 
  
## <a name="see-also"></a>Siehe auch



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

