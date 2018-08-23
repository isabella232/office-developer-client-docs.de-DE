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
ms.openlocfilehash: ef0dc212a6a6f761cd8dd0cae5312c548c02ae50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583820"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft eine Tabellenzeile.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> [in] Ein Zeiger auf eine Eigenschaft-Wert-Struktur, die beschreibt die Indexspalte der Zeile abgerufen werden sollen. Der **UlPropTag** Member der Eigenschaft Wert Struktur sollte das gleiche Eigenschafts-Tag als _UlPropTagIndexColumn_ -Parameter aus dem Aufruf der Funktion [CreateTable](createtable.md) enthalten, die greift auf die [ITableData](itabledataiunknown.md) Implementierung. 
    
 _lppSRow_
  
> [out] Ein Zeiger auf einen Zeiger auf die abgerufenen Zeile. 
    
 _lpuliRow_
  
> [in, out] Auf Eingabe, ein gültiger Zeiger oder NULL der angibt, dass keine Informationen zurückgegeben werden soll. Bei der Ausgabe zeigt, die ein gültiger Zeiger auf die Zeile Zeilennummer, eine fortlaufende Zahl, die die Zeilenposition in der Tabelle identifiziert.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeile wurde erfolgreich abgerufen.
    
MAPI_E_INVALID_PARAMETER 
  
> Die [SPropValue](spropvalue.md) -Struktur, _LpSPropValue_ verweist, enthält nicht die Index-Spalte-Eigenschaft. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrQueryRow** -Methode ruft alle Eigenschaften für die Zeile, die eine Indexspalte vorhanden ist, die den Wert der Indexspalte in der Eigenschaft Struktur auf den _LpSPropValue_enthalten entspricht. **HrQueryRow** gibt auch die Nummer der Zeile zurück, wenn der Anrufer, anfordert, auf dem die Zeilenposition in der Tabelle identifiziert. 
  
Da **HrQueryRow** nicht die **SPropValue** -Struktur, die auf den _LpSPropValue_ändert, müssen Anrufer die Struktur frei, wenn **HrQueryRow** zurückgegeben. Anrufer müssen auch die Struktur **SRow** frei, die die abgerufene Zeile enthält. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

