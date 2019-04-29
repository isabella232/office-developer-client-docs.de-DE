---
title: ITableDataHrInsertRow
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
  
> in Eine sequenzielle Zeilennummer, die eine bestimmte Zeile darstellt. Die neue Zeile wird nach der Zeile, die die Zahl angibt. Der _uliRow_ -Parameter kann Zeilenzahlen von 0 bis n enthalten, wobei n die Gesamtanzahl der Zeilen in der Tabelle ist. Beim Übergeben von n in _uliRow_ wird die Zeile am Ende der Tabelle angefügt. 
    
 _lpSRow_
  
> in Ein Zeiger auf eine [SRow](srow.md) -Struktur, die die einzufügende Zeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine Zeile, die den gleichen Wert für die Indexspalte hat wie die einzufügende Zeile, ist bereits in der Tabelle vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrInsertRow** -Methode fügt eine Zeile an einer bestimmten Position in eine Tabelle ein. Die neue Zeile wird nach der Zeile eingefügt, die sich in der durch den _uliRow_ -Parameter angegebenen Position befindet. 
  
Wenn _uliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile am Ende der Tabelle angefügt. 
  
Die Eigenschaft, die als Indexspalte für die Tabelle fungiert, muss im **lpProps** -Element der [SRow](srow.md) -Struktur enthalten sein, auf die durch den _lpSRow_ -Parameter verwiesen wird. Diese Index Eigenschaft, normalerweise **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md)), wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.
  
Die Eigenschaftenspalten in der **SRow** -Struktur müssen nicht in der gleichen Reihenfolge wie die Eigenschaftenspalten in der Tabelle sein. 
  
Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. Es wird keine Benachrichtigung gesendet, wenn die eingefügte Zeile aufgrund einer Einschränkung nicht in der Ansicht enthalten ist. 
  
## <a name="see-also"></a>Siehe auch



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

