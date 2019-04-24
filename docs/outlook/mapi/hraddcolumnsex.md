---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348370"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt oder verschiebt Spalten an den Anfang einer vorhandenen Tabelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Zeiger auf die betroffene MAPI-Tabelle. 
    
 _lpproptagColumnsNew_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpfnFilterColumns_
  
> in Zeiger auf eine vom Aufrufer eingerichtete Rückruffunktion. Wenn der _lpfnFilterColumns_ -Parameter auf NULL festgelegt ist, wird kein Rückruf vorgenommen. 
    
 _ptaga_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die das Array von Property-Tags enthält, die bereits in der Tabelle vorhanden sind, bevor Eigenschaften hinzugefügt oder an den Anfang verschoben werden. **HrAddColumnsEx** übergibt diesen Zeiger als Parameter an die Rückruffunktion, auf die durch _lpfnFilterColumns_verwiesen wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.
    
## <a name="remarks"></a>Bemerkungen

Die an **HrAddColumnsEx** übergebenen Eigenschaften werden mithilfe des _lpproptagColumnsNew_ -Parameters zu den ersten Eigenschaften, die bei nachfolgenden Aufrufen der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode verfügbar gemacht werden. Alle zuvor in der Tabelle aufgeführten Eigenschaften, die nicht im _lpproptagColumnsNew_ -Parameter angegeben wurden, werden nach allen hinzugefügten und verschobenen Eigenschaften verfügbar gemacht. 
  
Wenn Tabelleneigenschaften nicht definiert sind, wenn **QueryRows** aufgerufen wird, werden Sie mit Eigenschafts PT_NULL und PROP_ID_NULL der Eigenschaftskennung zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrAddColumnsEx** -Funktion ermöglicht es dem Aufrufer, eine Rückruffunktion bereitzustellen, um die Spalten zu filtern, die bereits in der Tabelle enthalten sind, beispielsweise zum Konvertieren von Zeichenfolgen vom PT_UNICODE in PT_String8. **HrAddColumnsEx** übergibt einen Zeiger auf den zuvor vorhandenen Spaltensatz als Parameter für die Rückruffunktion. Die Callback-Funktion kann Daten im Property-Tag-Array ändern, aber keine neuen Tags hinzufügen. 
  
 **HrAddColumnsEx** ruft zuerst die Callback-Funktion auf, wenn eine eingerichtet ist, fügt die angegebenen Spalten hinzu oder verschiebt Sie und ruft schließlich [IMAPITable::](imapitable-setcolumns.md)SetColumns auf. 
  
Die _lpAllocateBuffer_ -und _lpFreeBuffer_ -Eingabeparameter zeigen auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -und die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion. Die genauen Werte der an **HrAddColumnsEx** übergebenen Zeiger hängen davon ab, ob es sich bei dem Aufrufer um eine Clientanwendung oder einen Dienstanbieter handelt. Ein Client übergibt Zeiger auf die MAPI-Funktionen mit den angegebenen Namen. Ein Dienstanbieter übergibt die Zeiger, die er bei seinem Initialisierungsaufruf erhalten hat, oder wird durch Aufrufen der [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

