---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437994"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe eines Arrays von Ereignisbenachrichtigungen in Bytes und überprüft den dem Array zugeordneten Arbeitsspeicher.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cntf_
  
> [in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, das durch den  _rgntf-Parameter angegeben_ wird. 
    
 _rgntf_
  
> [in] Zeiger auf das Array der **NOTIFICATION-Strukturen,** deren Größe bestimmt werden soll. 
    
 _leiterplatte_
  
> [out] Optionaler Zeiger auf die Größe des Arrays in Bytes, auf das der  _rgntf-Parameter_ verweist. Bei NULL überprüft **ScCountNotifications** das Array von Benachrichtigungen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Count wurde erfolgreich ermittelt.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Hinweise

Wenn NULL im  _#A0_ übergeben wird, überprüft **die ScCountNotifications-Funktion** nur das Array der Benachrichtigungen, es wird jedoch keine Zählung durchgeführt. Wenn ein Nicht-Null-Wert  _in_ der Leiterplatte übergeben wird, bestimmt **ScCountNotifications** die Größe des Arrays und speichert die Ursache  _leiterplatte_. Der  _Parameter "pcb"_ muss groß genug sein, um das gesamte Array enthalten zu können. 
  

