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
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791896"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Betrifft**: Outlook 
  
Fügt oder Spalten an den Anfang einer vorhandenen Tabelle verschoben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf die MAPI-Tabelle betroffen. 
    
 _lpproptagColumnsNew_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die enthält ein Array von Eigenschaftentags für die Eigenschaften hinzugefügt oder an den Anfang der Tabelle verschoben werden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpfnFilterColumns_
  
> [in] Zeiger auf eine Rückruffunktion, die vom Anrufer bereitgestellt. Wenn der _LpfnFilterColumns_ -Parameter auf NULL festgelegt ist, erfolgt kein Rückruf. 
    
 _ptaga_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die enthält das Array von Eigenschaftentags bereits in der Tabelle, bevor Eigenschaften hinzugefügt oder an den Anfang verschoben werden. **HrAddColumnsEx** übergibt diese Zeiger als Parameter an den Callback-Funktion mit _LpfnFilterColumns_gezeigt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten verschoben oder hinzugefügt wurden.
    
## <a name="remarks"></a>Hinweise

Die Eigenschaften **HrAddColumnsEx** mit dem _LpproptagColumnsNew_ -Parameter übergeben werden die ersten Eigenschaften für nachfolgende Aufrufe [der QueryRows](imapitable-queryrows.md) verfügbar gemacht werden. Alle Eigenschaften zuvor in der Tabelle, die nicht im _LpproptagColumnsNew_ -Parameter angegeben wurden, werden nach alle Eigenschaften hinzugefügten und verschobenen verfügbar gemacht. 
  
Wenn alle Tabelleneigenschaften **QueryRows** aufgerufen wird nicht definiert sind, werden diese mit Eigenschaftentyp PT_NULL und Eigenschaftenbezeichner PROP_ID_NULL zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrAddColumnsEx** -Funktion kann der Aufrufer erhalten Sie vom Netzwerkadministrator eine Callback-Funktion, um die Spalten zu filtern, die bereits in der Tabelle, beispielsweise Zeichenfolgen aus Eigenschaftentyp PT_UNICODE in PT_STRING8 konvertiert wurden. **HrAddColumnsEx** übergibt einen Zeiger auf die zuvor vorhandenen Spalte als Parameter an die Rückruffunktion festgelegt. Die Callback-Funktion kann Daten in dem Array der Tag-Eigenschaft geändert, neue Tags kann nicht hinzugefügt werden. 
  
 **HrAddColumnsEx** ruft zunächst die Callback-Funktion, wenn eine ausgestattet ist, und klicken Sie dann hinzugefügt oder die angegebenen Spalten verschiebt und schließlich [IMAPITable::SetColumns ruft](imapitable-setcolumns.md). 
  
Die Eingabeparametern _LpAllocateBuffer_ und _LpFreeBuffer_ zeigen Sie jeweils auf die Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer](mapifreebuffer.md) . Die genauen Werte Zeiger an **HrAddColumnsEx** übergeben, hängt davon ab, ob der Anrufer eine Clientanwendung oder einem Dienstanbieter ist. Ein Client übergibt Zeiger an die MAPI-Funktionen mit den angegebenen Namen. Ein Dienstanbieter übergibt die Zeiger, die es in seinem Initialisierungsaufruf empfangen oder durch Aufrufen der Methode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) abgerufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

