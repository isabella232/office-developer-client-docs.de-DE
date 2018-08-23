---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563464"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Löscht eine Tabellenzeile.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> [in] Ein Zeiger auf eine Eigenschaft-Wert-Struktur, die beschreibt die Indexspalte für die Zeile gelöscht werden soll. Der **UlPropTag** Member der Eigenschaft Wert Struktur sollte das gleiche Eigenschafts-Tag als _UlPropTagIndexColumn_ -Parameter aus dem Aufruf der Funktion [CreateTable](createtable.md) enthalten. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeile wurde gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die-Eigenschaft auf das durch den Parameter _LpSPropValue_ wird eine Zeile in der Tabelle nicht identifiziert. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrDeleteRow** -Methode entfernt Tabellenzeile, die die Spalte enthält, die-Eigenschaft auf das durch den Parameter _LpSPropValue_ übereinstimmt. Die Daten für die Zeile werden gelöscht, und die Zeile aus alle geöffneten Ansichten entfernt wird. 
  
Nachdem die Zeile gelöscht wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet. 
  
Löschen einer Zeile wird nicht reduziert die Spalte festlegen, die verfügbar ist, vorhandene Ansichten oder Ansichten, anschließend geöffnet, auch wenn die gelöschte Zeile die letzte Zeile ist, die einen Wert für eine bestimmte Spalte verfügt.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

