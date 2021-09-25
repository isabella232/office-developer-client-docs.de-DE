---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 37651071bdc3ae99b4f374dcb7864a8f31dc1246
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614066"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt Spalten an den Anfang einer vorhandenen Tabelle hinzu oder verschiebt sie. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>Parameter

 _lptbl_
  
> [in] Zeiger auf die betroffene MAPI-Tabelle. 
    
 _lpproptagColumnsNew_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftentags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _lpfnFilterColumns_
  
> [in] Zeiger auf eine Rückruffunktion, die vom Aufrufer bereitgestellt wird. Wenn der  _Parameter lpfnFilterColumns_ auf NULL festgelegt ist, wird kein Rückruf ausgeführt. 
    
 _ptaga_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die das Array von Eigenschaftentags enthält, die bereits in der Tabelle vorhanden sind, bevor Eigenschaften hinzugefügt oder an den Anfang verschoben werden. **HrAddColumnsEx** übergibt diesen Zeiger als Parameter an die Rückruffunktion, auf die von  _lpfnFilterColumns_ verwiesen wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.
    
## <a name="remarks"></a>Bemerkungen

Die Eigenschaften, die mit dem _LpproptagColumnsNew-Parameter_ an **HrAddColumnsEx** übergeben werden, werden zu den ersten Eigenschaften, die bei nachfolgenden Aufrufen der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) verfügbar gemacht werden. Alle eigenschaften zuvor in der Tabelle, die nicht im  _lpproptagColumnsNew-Parameter_ angegeben wurden, werden nach allen hinzugefügten und verschobenen Eigenschaften verfügbar gemacht. 
  
Wenn Tabelleneigenschaften beim Aufrufen von **QueryRows** nicht definiert sind, werden sie mit eigenschaftentyp PT_NULL und Eigenschaftenbezeichner PROP_ID_NULL zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mit der **HrAddColumnsEx-Funktion** kann der Aufrufer eine Rückruffunktion einrichten, um die Spalten zu filtern, die bereits in der Tabelle enthalten waren, z. B. um Zeichenfolgen vom Eigenschaftentyp PT_UNICODE in PT_STRING8 zu konvertieren. **HrAddColumnsEx** übergibt einen Zeiger auf die zuvor vorhandene Spaltengruppe als Parameter an die Rückruffunktion. Die Rückruffunktion kann Daten im Eigenschaftentagarray ändern, aber keine neuen Tags hinzufügen. 
  
 **HrAddColumnsEx** ruft zuerst die Rückruffunktion auf, wenn eine eingerichtet ist, fügt dann die angegebenen Spalten hinzu oder verschiebt sie und ruft schließlich [IMAPITable::SetColumns](imapitable-setcolumns.md)auf. 
  
Die _Eingabeparameter lpAllocateBuffer_ und _lpFreeBuffer_ verweisen jeweils auf die Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer.](mapifreebuffer.md) Die genauen Werte der Zeiger, die an **HrAddColumnsEx** übergeben werden, hängen davon ab, ob der Aufrufer eine Clientanwendung oder ein Dienstanbieter ist. Ein Client übergibt Zeiger an die MAPI-Funktionen mit den angegebenen Namen. Ein Dienstanbieter übergibt die Zeiger, die er beim Initialisierungsaufruf empfangen oder durch Aufrufen der [IMAPISupport::GetMemAllocRoutines-Methode](imapisupport-getmemallocroutines.md) abgerufen hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

