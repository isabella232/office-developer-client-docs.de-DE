---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434767"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine Tabellenzeile ab.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> in Ein Zeiger auf eine Eigenschaftswert Struktur, die die Indexspalte für die abgerufene Zeile beschreibt. Das **ulPropTag** -Element der Eigenschaftswert Struktur sollte das gleiche Property-Tag wie der _ulPropTagIndexColumn_ -Parameter aus dem Aufruf der [createable](createtable.md) -Funktion enthalten, die auf die [ITableData](itabledataiunknown.md) -Implementierung zugreift. 
    
 _lppSRow_
  
> Out Ein Zeiger auf einen Zeiger auf die abgerufene Zeile. 
    
 _lpuliRow_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger oder NULL, der angibt, dass keine Informationen zurückgegeben werden müssen. Bei der Ausgabe ein gültiger Zeiger, der auf die Zeilennummer der Zeile verweist, eine fortlaufende Nummer, die die Position der Zeile in der Tabelle identifiziert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich abgerufen.
    
MAPI_E_INVALID_PARAMETER 
  
> Die [SPropValue](spropvalue.md) -Struktur, auf die _lpSPropValue_ verweist, enthält nicht die Index Column-Eigenschaft. 
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrQueryRow** -Methode ruft alle Eigenschaften für die Zeile mit einer Indexspalte ab, die mit dem Wert der Indexspalte übereinstimmt, die in der Eigenschaften Struktur enthalten ist, auf die von _lpSPropValue_verwiesen wird. **HrQueryRow** gibt auch die Zeilennummer zurück, wenn der Anrufer Sie anfordert, der die Position der Zeile in der Tabelle identifiziert. 
  
Da **HrQueryRow** die **SPropValue** -Struktur, auf die durch _lpSPropValue_verwiesen wird, nicht ändert, müssen Aufrufer die Struktur freigeben, wenn **HrQueryRow** zurückgegeben wird. Aufrufer müssen auch die **SRow** -Struktur freigeben, die die abgerufene Zeile enthält. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

