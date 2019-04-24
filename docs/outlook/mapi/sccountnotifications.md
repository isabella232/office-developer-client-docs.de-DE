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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351371"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe eines Arrays von Ereignisbenachrichtigungen in Byte und überprüft den dem Array zugeordneten Arbeitsspeicher.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cntf_
  
> in Die Anzahl [](notification.md) der Benachrichtigungs Strukturen im durch den _rgntf_ -Parameter angegebenen Array. 
    
 _rgntf_
  
> in Zeiger auf das Array der **Benachrichtigungs** Strukturen, dessen Größe bestimmt werden soll. 
    
 _PCB_
  
> Out Optionaler Zeiger auf die Größe des Arrays, auf das durch den _rgntf_ -Parameter verwiesen wird, in Bytes. Wenn der Wert NULL ist, überprüft **ScCountNotifications** das Array der Benachrichtigungen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Count wurde erfolgreich ermittelt.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Bemerkungen

Wenn NULL im _PCB_ -Parameter übergeben wird, überprüft die **ScCountNotifications** -Funktion nur das Array der Benachrichtigungen, aber es wird keine Zählung durchgeführt; Wenn ein Wert ungleich NULL in _PCB_übergeben wird, bestimmt **ScCountNotifications** die Größe des Arrays und speichert die Ursache _PCB_. Der _PCB_ -Parameter muss so hoch sein, dass er das gesamte Array enthält. 
  

