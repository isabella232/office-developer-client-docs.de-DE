---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b89aef1aff41f7fd1f84d687c72d37ce306cc31e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610398"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sendet eine Benachrichtigung für eine Tabellenzeile.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die der  _lpSPropValue-Parameter_ verweist. 
    
 _lpSPropValue_
  
> [in] Ein Zeiger auf eine **SPropValue-Struktur,** die die Werte der Spalten in der Zielzeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrNotify-Methode** sendet eine TABLE_ROW_MODIFIED Benachrichtigung für die Zeile, die mit der Zeile übereinstimmt, die durch die Eigenschaften beschrieben wird, auf die der  _lpSPropValue-Parameter_ verweist. **HrNotify** sendet die Benachrichtigung unabhängig davon, ob Änderungen an der Zeile vorgenommen wurden. Alle Clients und Dienstanbieter, die Ansichten der Tabelle haben und [IMAPITable::Advise](imapitable-advise.md) aufgerufen haben, um sich für Benachrichtigungen in ihren Ansichten zu registrieren, erhalten diese Benachrichtigung. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

