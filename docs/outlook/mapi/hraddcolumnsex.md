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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427479"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt Spalten am Anfang einer vorhandenen Tabelle hinzu oder verschiebt sie. 
  
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
    
 _lpproptagColumnsNeu_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
 _lpfnFilterColumns_
  
> [in] Zeiger auf eine Rückruffunktion, die vom Anrufer eingerichtet wurde. Wenn der  _Parameter lpfnFilterColumns_ auf NULL festgelegt ist, wird kein Rückruf vorgenommen. 
    
 _ptaga_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die das Array von Eigenschaftstags enthält, die bereits in der Tabelle vorhanden sind, bevor Eigenschaften hinzugefügt oder an den Anfang verschoben werden. **HrAddColumnsEx** übergibt diesen Zeiger als Parameter an die Rückruffunktion, auf die _von lpfnFilterColumns verwiesen wird._
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.
    
## <a name="remarks"></a>Hinweise

Die Eigenschaften, die mit dem _lpproptagColumnsNew-Parameter_ an **HrAddColumnsEx** übergeben werden, werden die ersten Eigenschaften, die bei nachfolgenden Aufrufen der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) verfügbar gemacht werden. Alle zuvor in der Tabelle angegebenen Eigenschaften, die im  _lpproptagColumnsNew-Parameter_ nicht angegeben wurden, werden nach allen hinzugefügten und verschobenen Eigenschaften verfügbar gemacht. 
  
Wenn Tabelleneigenschaften nicht definiert sind, wenn **QueryRows** aufgerufen wird, werden sie mit eigenschaftentyp-PT_NULL und Eigenschafts-ID-PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mit der **HrAddColumnsEx-Funktion** kann der Aufrufer eine Rückruffunktion hinzufügen, um die Spalten zu filtern, die sich bereits in der Tabelle befindet, z. B. zum Konvertieren von Zeichenfolgen vom Eigenschaftstyp PT_UNICODE in PT_STRING8. **HrAddColumnsEx** übergibt einen Zeiger auf die zuvor vorhandene Spaltensatz als Parameter an die Rückruffunktion. Die Rückruffunktion kann Daten im Eigenschaftentagarray ändern, aber keine neuen Tags hinzufügen. 
  
 **HrAddColumnsEx** ruft zuerst die Rückruffunktion auf, wenn eine eingerichtet ist, fügt dann die angegebenen Spalten hinzu oder verschiebt sie, und ruft schließlich [IMAPITable::SetColumns auf.](imapitable-setcolumns.md) 
  
Die _Eingabeparameter lpAllocateBuffer_ und _lpFreeBuffer_ verweisen auf die [FUNKTIONEN MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer.](mapifreebuffer.md) Die genauen Werte der an **HrAddColumnsEx** übergebenen Zeiger hängen davon ab, ob der Aufrufer eine Clientanwendung oder ein Dienstanbieter ist. Ein Client übergibt Zeiger an die MAPI-Funktionen mit den angegebenen Namen. Ein Dienstanbieter übergibt die Zeiger, die er in seinem Initialisierungsaufruf empfangen oder durch Aufrufen der [IMAPISupport::GetMemAllocRoutines-Methode abgerufen](imapisupport-getmemallocroutines.md) hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

