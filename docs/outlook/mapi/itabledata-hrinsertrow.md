---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1cb53ae3e4f38e202105ef8989257babfe4b456
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613772"
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
  
> [in] Eine fortlaufende Zeilennummer, die eine bestimmte Zeile darstellt. Die neue Zeile wird hinter der Zeile platziert, die die Nummer angibt. Der  _uliRow-Parameter_ kann Zeilennummern von 0 bis n enthalten, wobei n die Gesamtanzahl der Zeilen in der Tabelle ist. Wird n in  _uliRow übergeben,_ wird die Zeile am Ende der Tabelle angefügt. 
    
 _lpSRow_
  
> [in] Ein Zeiger auf eine [SRow-Struktur,](srow.md) die die einzufügende Zeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine Zeile mit demselben Wert für ihre Indexspalte wie die einzufügende Zeile ist bereits in der Tabelle vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData::HrInsertRow-Methode** fügt eine Zeile in eine Tabelle an einer bestimmten Position ein. Die neue Zeile wird nach der Zeile eingefügt, die sich an der durch den  _uliRow-Parameter_ angegebenen Position befindet. 
  
Wenn  _uliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile am Ende der Tabelle angefügt. 
  
Die Eigenschaft, die als Indexspalte für die Tabelle fungiert, muss im **lpProps-Element** der [SRow-Struktur](srow.md) enthalten sein, auf die der  _lpSRow-Parameter_ verweist. Diese Indexeigenschaft, in der Regel **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.
  
Die Eigenschaftsspalten in der **SRow-Struktur** müssen nicht in derselben Reihenfolge wie die Eigenschaftsspalten in der Tabelle sein. 
  
Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die eine Ansicht der Tabelle haben und die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. Es wird keine Benachrichtigung gesendet, wenn die eingefügte Zeile aufgrund einer Einschränkung nicht in der Ansicht enthalten ist. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

