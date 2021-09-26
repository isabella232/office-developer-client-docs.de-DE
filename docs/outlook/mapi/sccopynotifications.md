---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 58eef4b8b11b8ef1cfd5df359869f1950a5d8695
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629592"
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
  
> [in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, die durch den  _rgntf-Parameter_ angegeben werden. 
    
 _rgntf_
  
> [in] Zeiger auf ein Array von **NOTIFICATION-Strukturen,** die die zu kopierenden Ereignisbenachrichtigungen definieren. 
    
 _pvDst_
  
> [out] Zeiger auf die zurückgegebenen Benachrichtigungen. 
    
 _Pcb_
  
> [out] Optionaler Zeiger auf eine Variable, in der die Größe des Arrays, auf das der  _rgntf-Parameter_ verweist, in Byte gespeichert wird. Wenn nicht NULL, wird der  _Parameter "parameters"_ auf die Anzahl von Bytes festgelegt, die im  _pvDst-Parameter_ gespeichert sind. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ereignisbenachrichtigungen wurden erfolgreich kopiert.
    
E_INVALIDARG
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Bemerkungen

Wenn NULL im  _parameter "parameters"_ übergeben wird, wird kein Kopieren ausgeführt; wenn ein Wert ungleich Null in  _einem Arbeitsblatt_ übergeben wird, kopiert die **ScCopyNotifications-Funktion** die Größe des Arrays und das Array selbst in einen einzelnen Speicherblock. Wenn der Wert für  _bytes_ nicht NULL ist, wird die Anzahl der bytes festgelegt, die im  _PvDst-Parameter_ gespeichert sind. Der  _PvDst-Parameter_ muss groß genug sein, um das gesamte Array enthalten zu können. 
  

