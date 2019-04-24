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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348664"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine neue Tabellenzeile ein, die möglicherweise eine vorhandene Zeile ersetzt.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameter

 _lpSRow_
  
> in Ein Zeiger auf eine [SRow](srow.md) -Struktur, die die hinzuzufügende Zeile beschreibt oder eine vorhandene Zeile ersetzt. Eine der Eigenschaftswert Strukturen, auf die durch das **lpProps** -Element der **SRow** -Struktur verwiesen wird, sollte die Index-Spalte enthalten, den gleichen Wert, der im _ulPropTagIndexColumn_ -Parameter im Aufruf der Create-Basis angegeben wurde. [ ](createtable.md)-Funktion. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Die übergebene Zeile hat keine Indexspalte.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrModifyRow** -Methode fügt die durch die **SRow** -Struktur beschriebene Zeile ein, auf die durch den _lpSRow_ -Parameter verwiesen wird. Wenn eine Zeile, die den gleichen Wert für die Indexspalte hat, wie die Zeile, auf die _lpSRow_ verweist, in der Tabelle bereits vorhanden ist, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden ist, die mit der in der **SRow** -Struktur übereinstimmt, fügt **HrModifyRow** die Zeile am Ende der Tabelle hinzu. 
  
Alle Ansichten der Tabelle werden so geändert, dass Sie die Zeile einbeziehen, auf die von _lpSRow_verwiesen wird. Wenn in einer Ansicht jedoch eine Einschränkung vorhanden ist, die die Zeile ausschließt, ist Sie möglicherweise nicht für den Benutzer sichtbar. 
  
Die Spalten in der Zeile, auf die durch _lpSRow_ verwiesen wird, müssen sich nicht in derselben Reihenfolge wie die Spalten in der Tabelle befinden. Der Aufrufer kann auch als Spalteneigenschaften enthalten, die sich derzeit nicht in der Tabelle befinden. Bei vorhandenen Ansichten stellt **HrModifyRow** diese neuen Spalten zur Verfügung, diese werden jedoch nicht in den aktuellen Spaltensatz aufgenommen. Für zukünftige Ansichten enthält **HrModifyRow** die neuen Spalten in den Spaltensatz. 
  
Nachdem **HrModifyRow** die Zeile hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

