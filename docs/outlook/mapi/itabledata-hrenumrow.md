---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea3c421c19174d49e2d46f7799631ccab31eb7e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620436"
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
  
> [in] Die Nummer der Zeile, für die Eigenschaften zurückgegeben werden sollen. Der Wert im  _ulRowNumber-Parameter_ kann ein beliebiger Wert von 0 sein, der die erste Zeile in der Tabelle bis n - 1 angibt, was die letzte Zeile in der Tabelle angibt. 
    
 _lppSRow_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [SRow-Struktur,](srow.md) die die Zielzeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich abgerufen, oder es ist keine Zeile für die durch den  _ulRowNumber-Parameter_ angegebene Zeilennummer vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData::HrEnumRow-Methode** ruft eine Zeile basierend auf einer sequenziellen Zahl ab. Diese Zahl stellt die Einfügereihenfolge dar (0 gibt die erste Zeile an, und die Anzahl der Zeilen minus 1 gibt die letzte Zeile an). MAPI behält diese chronologische Reihenfolge der Zeileneinfügung für die Lebensdauer des Tabellendatenobjekts bei. 
  
Wenn die in  _ulRowNumber_ angegebene Zahl keiner Zeile in der Tabelle entspricht, gibt **HrEnumRow** S_OK zurück und legt den  _lppSRow-Parameter_ auf NULL fest. 
  
MAPI weist Speicher für die zurückgegebene **SRow-Struktur** zu, indem die [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) verwendet wird, wenn das Tabellendatenobjekt erstellt wird. Der Aufrufer muss diesen Speicher freigeben, indem er die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufruft. 
  
Um Zeilen aus einer Tabelle in der Reihenfolge abzurufen, in der sie eingefügt wurden, rufen Benutzer des Tabellendatenobjekts die **HrEnumRow-Methode** auf. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

