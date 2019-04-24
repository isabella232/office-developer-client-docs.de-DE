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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357484"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Gruppe von Ereignisbenachrichtigungen in einen einzelnen Speicherblock. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Die Anzahl [](notification.md) der Benachrichtigungs Strukturen im durch den _rgntf_ -Parameter angegebenen Array. 
    
 _rgntf_
  
> in Zeiger auf ein Array von **Benachrichtigungs** Strukturen, das die zu kopierenden Ereignisbenachrichtigungen definiert. 
    
 _pvDst_
  
> Out Zeiger auf die zurückgegebenen Benachrichtigungen. 
    
 _PCB_
  
> Out Optionaler Zeiger auf eine Variable, in der die Größe des Arrays, auf das durch den _rgntf_ -Parameter verwiesen wird, in Bytes gespeichert wird. Wenn nicht NULL, wird der _PCB_ -Parameter auf die Anzahl von Bytes festgelegt, die im Parameter _pvDst_ gespeichert sind. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ereignisbenachrichtigungen wurden erfolgreich kopiert.
    
E_INVALIDARG
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Bemerkungen

Wenn NULL in den _PCB_ -Parameter übergeben wird, wird kein Kopieren ausgeführt; Wenn ein Wert ungleich NULL in _PCB_übergeben wird, kopiert die **ScCopyNotifications** -Funktion die Größe des Arrays und das Array selbst in einen einzelnen Speicherblock. Wenn _PCB_ nicht NULL ist, wird die Anzahl der Bytes festgelegt, die im Parameter _pvDst_ gespeichert sind. Der Parameter _pvDst_ muss so hoch sein, dass er das gesamte Array enthält. 
  

