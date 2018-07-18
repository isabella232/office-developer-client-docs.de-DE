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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c149a215a048b96408025e08df55972fa989f46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792838"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Betrifft**: Outlook 
  
Ruft eine Zeile basierend auf seine Position in der Tabelle an. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Parameter

 _ulRowNumber_
  
> [in] Die Anzahl der Zeilen für die Eigenschaften zurückgegeben. Der Wert in der _UlRowNumber_ -Parameter kann ein beliebiger Wert von 0, sein, die die erste Zeile in der Tabelle, bis n - 1, gibt an, welche die gibt die letzte Zeile in der Tabelle an. 
    
 _lppSRow_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [SRow](srow.md) -Struktur, die Zielzeile beschreibt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeile erfolgreich abgerufen wurde, oder eine Zeile für die Nummer der Zeile durch den _UlRowNumber_ -Parameter angegeben ist nicht vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData::HrEnumRow** -Methode ruft eine Zeile basierend auf eine fortlaufende Zahl. Diese Nummer stellt die Reihenfolge des Einfügevorgangs (0 gibt die erste Zeile und die Anzahl der Zeilen minus 1 gibt die letzte Zeile). MAPI behält diese Reihenfolge der Zeile eingefügt für die Lebensdauer des Table-Objekts Daten. 
  
Wenn die Nummer im angegebenen _UlRowNumber_ nicht zu einer Zeile in der Tabelle entspricht, **HrEnumRow** gibt S_OK zurück, und der _LppSRow_ -Parameter auf NULL festgelegt. 
  
MAPI weist Speicher für die zurückgegebene Struktur **' srow '** mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, wenn das Table-Datenobjekt erstellt wird. Der Aufrufer muss diesen Speicher Aufruf der Funktion [MAPIFreeBuffer](mapifreebuffer.md) freigeben. 
  
Um Zeilen aus einer Tabelle in der Reihenfolge abzurufen, dass sie eingefügt wurden, rufen Sie Tabelle Daten Objekt Benutzer die **HrEnumRow** -Methode. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

