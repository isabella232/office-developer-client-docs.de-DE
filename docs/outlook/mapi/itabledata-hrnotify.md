---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792857"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Durch den Parameter _LpSPropValue_ auf zeigt die Anzahl der Eigenschaftswerte in der Struktur [SPropValue](spropvalue.md) . 
    
 _lpSPropValue_
  
> [in] Ein Zeiger auf eine **SPropValue** -Struktur, die die Werte der Spalten in der Zielzeile beschreibt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrNotify** -Methode sendet eine Benachrichtigung TABLE_ROW_MODIFIED für die Zeile, die mit die Zeile, die durch die Eigenschaften auf das durch den Parameter _LpSPropValue_ beschriebenen übereinstimmt. **HrNotify** sendet die Benachrichtigung, unabhängig davon, ob die Zeile geändert wurden. Alle Clients und -Dienstanbieter, die Ansichten für die Tabelle und [IMAPITable::Advise](imapitable-advise.md) zum Registrieren für Benachrichtigungen für ihre Ansichten aufgerufen haben erhalten diese Benachrichtigung. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

