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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348895"
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
  
> in Die Nummer der Zeile, für die Eigenschaften zurückgegeben werden sollen. Der Wert im _ulRowNumber_ -Parameter kann ein beliebiger Wert von 0 sein, der die erste Zeile in der Tabelle durch n-1 angibt, die die letzte Zeile in der Tabelle angibt. 
    
 _lppSRow_
  
> Out Ein Zeiger auf einen Zeiger auf eine [SRow](srow.md) -Struktur, die die Zielzeile beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich abgerufen, oder eine Zeile für die vom _ulRowNumber_ -Parameter angegebene Zeilennummer ist nicht vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrEnumRow** -Methode ruft eine Zeile basierend auf einer sequenziellen Zahl ab. Diese Zahl stellt die Reihenfolge der Einfügung dar (0 gibt die erste Zeile an, und die Anzahl der Zeilen minus 1 gibt die letzte Zeile an). MAPI behält diese chronologische Reihenfolge der Zeileneinfügung für die Lebensdauer des Tabellendaten Objekts bei. 
  
Wenn die in _ulRowNumber_ angegebene Zahl nicht mit einer Zeile in der Tabelle übereinstimmt, gibt **HRENUMROW** den Wert S_OK zurück und legt den _lppSRow_ -Parameter auf NULL fest. 
  
MAPI reserviert Speicher für die zurückgegebene **SRow** -Struktur mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, wenn das Tabellendaten Objekt erstellt wird. Der Aufrufer muss diesen Speicher freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft. 
  
Zum Abrufen von Zeilen aus einer Tabelle in der Reihenfolge, in der Sie eingefügt wurden, rufen Tabellendaten Objekt Benutzer die **HrEnumRow** -Methode auf. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

