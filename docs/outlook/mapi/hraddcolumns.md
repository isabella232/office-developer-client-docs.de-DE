---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791890"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Betrifft**: Outlook 
  
Fügt oder Spalten an den Anfang einer vorhandenen Tabelle verschoben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter.  <br/> |
   
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
  
> [in] Zeiger auf die MAPI-Tabelle betroffen.
    
 _lpproptagColumnsNew_
  
> [in] Zeiger auf eine **SPropTagArray** -Struktur, die enthält ein Array von Eigenschaftentags für die Eigenschaften hinzugefügt oder an den Anfang der Tabelle verschoben werden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die **MAPIAllocateBuffer** -Funktion. Zuweisen von Arbeitsspeicher verwendet. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die **MAPIFreeBuffer** -Funktion. Verwendet, um Arbeitsspeicher freizugeben. 
    
## <a name="return-value"></a>R�ckgabewert

 **S_OK**
  
> Der Aufruf war erfolgreich, und die angegebenen Spalten verschoben oder hinzugefügt wurden.
    
## <a name="remarks"></a>Hinweise

Die Funktion **HrAddColumns** ist entspricht der Verwendung von **HrAddColumnsEx** mit _LpfnFilterColumns_ auf NULL festgelegt wurde. 
  
## <a name="see-also"></a>Siehe auch



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

