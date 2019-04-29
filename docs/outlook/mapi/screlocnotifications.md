---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415201"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Passt einen Zeiger in einem angegebenen Ereignis Benachrichtigungs Array an. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cntf_
  
> in Die Anzahl [](notification.md) der Benachrichtigungs Strukturen im durch den _rgntf_ -Parameter angegebenen Array. 
    
 _rgntf_
  
> in Zeiger auf das Array von **Benachrichtigungs** Strukturen, die Ereignisbenachrichtigungen definieren, innerhalb derer ein Zeiger angepasst werden soll. 
    
 _pvBaseOld_
  
> in Zeiger auf die ursprüngliche Basisadresse des vom _rgntf_ -Parameter angegebenen Arrays. 
    
 _pvBaseNew_
  
> in Der Speicherort, an den **ScRelocNotifications** die neue Basisadresse des durch den _rgntf_ -Parameter angegebenen Arrays schreibt. 
    
 _PCB_
  
> Out Zeiger auf die Größe des vom _pvBaseNew_ -Parameter angegebenen Arrays in Byte. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ein Zeiger wurde erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Bemerkungen

Der _PCB_ -Parameter für die **ScRelocNotifications** -Funktion ist optional. 
  
## <a name="see-also"></a>Siehe auch



[ScRelocProps](screlocprops.md)

