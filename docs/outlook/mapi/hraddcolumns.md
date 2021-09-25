---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 670c5000d3bebc6723b37a5bce9821fdb069f78a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561670"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt Spalten an den Anfang einer vorhandenen Tabelle hinzu oder verschiebt sie.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter.  <br/> |
   
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
  
> [in] Zeiger auf die betroffene MAPI-Tabelle.
    
 _lpproptagColumnsNew_
  
> [in] Zeiger auf eine **SPropTagArray-Struktur,** die ein Array von Eigenschaftentags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die **MAPIAllocateBuffer-Funktion.** Wird zum Zuordnen von Arbeitsspeicher verwendet. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die **MAPIFreeBuffer-Funktion.** Wird verwendet, um Arbeitsspeicher freizugeben. 
    
## <a name="return-value"></a>Rückgabewert

 **S_OK**
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **HrAddColumns-Funktion** entspricht der Verwendung von **HrAddColumnsEx** mit  _lpfnFilterColumns,_ die auf NULL festgelegt sind. 
  
## <a name="see-also"></a>Siehe auch



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

