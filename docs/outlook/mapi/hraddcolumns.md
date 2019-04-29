---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422474"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt oder verschiebt Spalten an den Anfang einer vorhandenen Tabelle.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter.  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>Parameter

 _lptbl_
  
> in Zeiger auf die betroffene MAPI-Tabelle.
    
 _lpproptagColumnsNew_
  
> in Zeiger auf eine **SPropTagArray** -Struktur, die ein Array von Property-Tags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die **MAPIAllocateBuffer** -Funktion. Wird zum Reservieren von Arbeitsspeicher verwendet. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die **mapifreebufferfreigegeben** -Funktion. Wird verwendet, um Arbeitsspeicher freizugeben. 
    
## <a name="return-value"></a>Rückgabewert

 **S_OK**
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.
    
## <a name="remarks"></a>Bemerkungen

Die **HrAddColumns** -Funktion entspricht der Verwendung von **HrAddColumnsEx** mit _lpfnFilterColumns_ auf NULL festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

