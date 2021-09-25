---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b03d7a18b1013dffde8f9f3d729d655915b01c02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579733"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine neue Tabellenzeile ein, wobei möglicherweise eine vorhandene Zeile ersetzt wird.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameter

 _lpSRow_
  
> [in] Ein Zeiger auf eine [SRow-Struktur,](srow.md) die die hinzuzufügende Zeile beschreibt oder eine vorhandene Zeile ersetzt. Eine der Eigenschaftswertstrukturen, auf die vom **lpProps-Element** der **SRow-Struktur** verwiesen wird, sollte die Indexspalte enthalten, derselbe Wert, der im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion](createtable.md) angegeben wurde. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Die übergebene Zeile verfügt nicht über eine Indexspalte.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrModifyRow-Methode** fügt die Zeile ein, die durch die **SRow-Struktur** beschrieben wird, auf die der  _lpSRow-Parameter_ verweist. Wenn eine Zeile mit demselben Wert für ihre Indexspalte wie die Zeile, auf die  _lpSRow_ verweist, bereits in der Tabelle vorhanden ist, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden ist, die mit der in der **SRow-Struktur** enthaltenen Zeile übereinstimmt, fügt **HrModifyRow** die Zeile am Ende der Tabelle hinzu. 
  
Alle Ansichten der Tabelle werden geändert, um die Zeile einzuschließen, auf die mit  _lpSRow_ verwiesen wird. Wenn jedoch eine Ansicht eine Einschränkung enthält, die die Zeile ausschließt, ist sie für den Benutzer möglicherweise nicht sichtbar. 
  
Die Spalten in der Zeile, auf die  _lpSRow_ verweist, müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein. Der Aufrufer kann auch Spalteneigenschaften enthalten, die sich derzeit nicht in der Tabelle befinden. Für vorhandene Ansichten stellt **HrModifyRow** diese neuen Spalten zur Verfügung, schließt sie jedoch nicht in den aktuellen Spaltensatz ein. Für zukünftige Ansichten schließt **HrModifyRow** die neuen Spalten in den Spaltensatz ein. 
  
Nachdem **HrModifyRow** die Zeile hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die eine Ansicht der Tabelle haben und die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

