---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435922"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Gruppe von Ereignisbenachrichtigungen in einen einzelnen Speicherblock. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cntf_
  
> [in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, das durch den  _rgntf-Parameter angegeben_ wird. 
    
 _rgntf_
  
> [in] Zeiger auf ein Array von **NOTIFICATION-Strukturen,** die die zu kopierenden Ereignisbenachrichtigungen definieren. 
    
 _pvDst_
  
> [out] Zeiger auf die zurückgegebenen Benachrichtigungen. 
    
 _leiterplatte_
  
> [out] Optionaler Zeiger auf eine Variable, in der die Größe des Arrays in Bytes gespeichert wird, auf das der  _rgntf-Parameter_ verweist. Wenn nicht NULL, wird  _der Parameter "pcb"_ auf die Anzahl der Bytes festgelegt, die im  _pvDst-Parameter gespeichert_ sind. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ereignisbenachrichtigungen wurden erfolgreich kopiert.
    
E_INVALIDARG
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Hinweise

Wenn NULL im  _#A0 übergeben_ wird, wird kein Kopieren ausgeführt. Wenn ein Nicht-Null-Wert  _in_ einer Leiterplatte übergeben wird, kopiert die **ScCopyNotifications-Funktion** die Größe des Arrays und des Arrays selbst in einen einzelnen Speicherblock. Wenn  _die Leiterplatte_ nicht NULL ist, wird sie auf die Anzahl der Bytes festgelegt, die im  _pvDst-Parameter gespeichert_ sind. Der  _pvDst-Parameter_ muss groß genug sein, um das gesamte Array enthalten zu können. 
  

