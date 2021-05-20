---
title: ITableDatahrInsertrow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435439"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine Tabellenzeile ein. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameter

 _uliRow_
  
> [in] Eine fortlaufende Zeilennummer, die eine bestimmte Zeile darstellt. Die neue Zeile wird nach der Zeile platziert, die die Zahl angibt. Der  _parameter uliRow_ kann Zeilennummern von 0 bis n enthalten, wobei n die Gesamtzahl der Zeilen in der Tabelle ist. Durch übergeben n in  _uliRow_ wird die Zeile an das Ende der Tabelle angehängt. 
    
 _lpSRow_
  
> [in] Ein Zeiger auf eine [SRow-Struktur,](srow.md) die die eingefügte Zeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine Zeile, die denselben Wert für ihre Indexspalte wie die eingefügte Zeile hat, ist bereits in der Tabelle vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrInsertRow-Methode** fügt eine Zeile in eine Tabelle an einer bestimmten Position ein. Die neue Zeile wird nach der Zeile eingefügt, die sich an der durch den Parameter  _uliRow_ angegebenen Position befindet. 
  
Wenn  _uliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile an das Ende der Tabelle angehängt. 
  
Die Eigenschaft, die als Indexspalte für die Tabelle fungiert, muss im **lpProps-Member** der [SRow-Struktur](srow.md) enthalten sein, auf die der  _Parameter lpSRow_ zeigt. Diese Indexeigenschaft, in der Regel **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.
  
Die Eigenschaftenspalten in der **SRow-Struktur** müssen nicht in der gleichen Reihenfolge wie die Eigenschaftenspalten in der Tabelle sein. 
  
Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. Es wird keine Benachrichtigung gesendet, wenn die eingefügte Zeile aufgrund einer Einschränkung nicht in die Ansicht einbezogen wird. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

