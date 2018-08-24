---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5ef210aedc884e5c09eca6335199e2ef284b901c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574832"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine neue Tabellenzeile, die möglicherweise eine vorhandene Zeile ersetzen.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameter

 _lpSRow_
  
> [in] Ein Zeiger auf eine [SRow](srow.md) -Struktur, die Zeile hinzugefügt werden soll, oder um eine vorhandene Zeile ersetzen beschreibt. Eine der Eigenschaft Wert Strukturen auf den die **LpProps** Member der Struktur **' srow '** sollte die Indexspalte den gleichen Wert enthalten, die in der _UlPropTagIndexColumn_ -Parameter im Aufruf der [CreateTable angegeben wurde ](createtable.md)Funktion. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Die Zeile übergeben in einer Indexspalte keinen.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData::HrModifyRow** -Methode fügt die Zeile mit der **SRow** -Struktur, die auf das durch den Parameter _LpSRow_ beschrieben. Wenn eine Zeile, die den gleichen Wert für die Indexspalte der Zeile, _LpSRow_ verweist, in der Tabelle bereits vorhanden ist, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden, die in der Struktur **SRow** enthaltene übereinstimmt ist, fügt **HrModifyRow** die Zeile an das Ende der Tabelle an. 
  
Alle Ansichten für die Tabelle werden geändert, um die Zeile, die auf den _LpSRow_einschließen. Jedoch, wenn eine Ansicht eine Einschränkung eingerichtet, die die Zeile ausschließt hat, es für den Benutzer sichtbar möglicherweise nicht. 
  
Die Spalten in der Zeile, die auf den _LpSRow_ müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle werden. Der Aufrufer kann auch als Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind. Für vorhandene Ansichten **HrModifyRow** diesen neuen Spalten zur Verfügung umfasst aber nicht sie in der aktuellen Spalte Gruppe. Für zukünftige Ansichten enthält **HrModifyRow** die neuen Spalten in der Spalte festlegen. 
  
Nachdem **HrModifyRow** die Zeile hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

