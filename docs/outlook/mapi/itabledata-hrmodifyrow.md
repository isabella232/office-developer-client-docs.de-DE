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
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408999"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine neue Tabellenzeile ein und ersetzt möglicherweise eine vorhandene Zeile.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameter

 _lpSRow_
  
> [in] Ein Zeiger auf eine [SRow-Struktur,](srow.md) in der die zu hinzufügende Zeile oder das Ersetzen einer vorhandenen Zeile beschrieben wird. Eine der Eigenschaftenwertstrukturen, auf die das **lpProps-Element** der **SRow-Struktur** verweist, sollte die Indexspalte enthalten, denselben Wert, der im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion](createtable.md) angegeben wurde. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Die übergebene Zeile verfügt nicht über eine Indexspalte.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrModifyRow-Methode** fügt die durch die **SRow-Struktur** beschriebene Zeile ein, auf die der  _lpSRow-Parameter_ verweist. Wenn eine Zeile mit demselben Wert für die Indexspalte wie die Zeile, auf die  _lpSRow_ verweist, bereits in der Tabelle vorhanden ist, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden ist, die mit der in der **SRow-Struktur** enthaltenen Zeile entspricht, fügt **HrModifyRow** die Zeile am Ende der Tabelle hinzu. 
  
Alle Ansichten der Tabelle werden so geändert, dass sie die Zeile enthält, auf die _von lpSRow verwiesen wird._ Wenn eine Ansicht jedoch über eine Einschränkung verfügt, die die Zeile ausschließt, ist sie möglicherweise nicht für den Benutzer sichtbar. 
  
Die Spalten in der Zeile, auf die  _lpSRow_ verweist, müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein. Der Aufrufer kann auch Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind. Für vorhandene Ansichten **stellt HrModifyRow** diese neuen Spalten zur Verfügung, schließt sie jedoch nicht in den aktuellen Spaltensatz ein. Für zukünftige Ansichten **enthält HrModifyRow** die neuen Spalten im Spaltensatz. 
  
Nachdem **HrModifyRow** die Zeile hinzufügt, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

