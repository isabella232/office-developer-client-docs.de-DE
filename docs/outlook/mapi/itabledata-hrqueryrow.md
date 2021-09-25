---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a513fbe235a61b331f05c7c99d11f9adc3c987ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556224"
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
  
> [in] Ein Zeiger auf eine Eigenschaftswertstruktur, die die Indexspalte für die abzurufende Zeile beschreibt. Der **ulPropTag-Member** der Eigenschaftswertstruktur sollte dasselbe Eigenschaftstag wie der  _ulPropTagIndexColumn-Parameter_ aus dem Aufruf der [CreateTable-Funktion](createtable.md) enthalten, die auf die [ITableData-Implementierung](itabledataiunknown.md) zugreift. 
    
 _lppSRow_
  
> [out] Ein Zeiger auf einen Zeiger auf die abgerufene Zeile. 
    
 _lpuliRow_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger oder NULL, der angibt, dass keine Informationen zurückgegeben werden müssen. Bei der Ausgabe ein gültiger Zeiger, der auf die Zeilennummer der Zeile zeigt, eine sequenzielle Zahl, die die Position der Zeile in der Tabelle identifiziert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich abgerufen.
    
MAPI_E_INVALID_PARAMETER 
  
> Die [SPropValue-Struktur,](spropvalue.md) auf die  _lpSPropValue_ zeigt, enthält nicht die Indexspalteneigenschaft. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrQueryRow-Methode** ruft alle Eigenschaften für die Zeile mit einer Indexspalte ab, die dem Wert der Indexspalte entspricht, die in der Eigenschaftsstruktur enthalten ist, auf die  _lpSPropValue_ verweist. **HrQueryRow** gibt auch die Zeilennummer zurück, wenn der Aufrufer sie anfordert, die die Position der Zeile in der Tabelle identifiziert. 
  
Da **HrQueryRow** die **SPropValue-Struktur,** auf die von  _lpSPropValue_ verwiesen wird, nicht ändert, müssen Aufrufer die Struktur freigeben, wenn **HrQueryRow** zurückgegeben wird. Aufrufer müssen auch die **SRow-Struktur** freigeben, die die abgerufene Zeile enthält. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

