---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418372"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine Zeile basierend auf ihrer Position in der Tabelle ab. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Parameter

 _ulRowNumber_
  
> [in] Die Nummer der Zeile, für die Eigenschaften zurückgeben werden. Der Wert im  _ulRowNumber-Parameter_ kann ein beliebiger Wert von 0 sein, der die erste Zeile in der Tabelle bis n - 1 angibt, was die letzte Zeile in der Tabelle angibt. 
    
 _lppSRow_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [SRow-Struktur,](srow.md) die die Zielzeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich abgerufen, oder eine Zeile für die durch den  _ulRowNumber-Parameter_ angegebene Zeilennummer ist nicht vorhanden. 
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrEnumRow-Methode** ruft eine Zeile basierend auf einer sequenziellen Zahl ab. Diese Zahl stellt die Einfügereihenfolge dar (0 gibt die erste Zeile an, und die Anzahl der Zeilen minus 1 gibt die letzte Zeile an). MAPI behält diese chronologische Reihenfolge der Zeileneinfügung für die Lebensdauer des Tabellendatenobjekts bei. 
  
Wenn die in  _ulRowNumber_ angegebene Zahl nicht einer Zeile in der Tabelle entspricht, gibt **HrEnumRow** S_OK zurück und legt den  _lppSRow-Parameter_ auf NULL fest. 
  
MAPI weist speicher für die zurückgegebene **SRow-Struktur** mithilfe der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zu, wenn das Tabellendatenobjekt erstellt wird. Der Aufrufer muss diesen Speicher durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) los. 
  
Zum Abrufen von Zeilen aus einer Tabelle in der Reihenfolge, in der sie eingefügt wurden, rufen Benutzer des Tabellendatenobjekts die **HrEnumRow-Methode** auf. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

