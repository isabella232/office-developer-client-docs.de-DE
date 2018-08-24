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
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580733"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>Bemerkungen

Die Funktion **HrAddColumns** ist entspricht der Verwendung von **HrAddColumnsEx** mit _LpfnFilterColumns_ auf NULL festgelegt wurde. 
  
## <a name="see-also"></a>Siehe auch



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

