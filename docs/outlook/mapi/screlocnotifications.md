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
  
Passt einen Zeiger innerhalb eines angegebenen Ereignisbenachrichtigungsarrays an. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, das durch den  _rgntf-Parameter angegeben_ wird. 
    
 _rgntf_
  
> [in] Zeiger auf das Array von **NOTIFICATION-Strukturen,** in dem Ereignisbenachrichtigungen definiert werden, innerhalb derer ein Zeiger angepasst werden soll. 
    
 _pvBaseOld_
  
> [in] Zeiger auf die ursprüngliche Basisadresse des Arrays, die durch den  _rgntf-Parameter angegeben_ wird. 
    
 _pvBaseNeu_
  
> [in] Der Speicherort, an den **ScRelocNotifications** die neue Basisadresse des arrays schreibt, das durch den  _rgntf-Parameter angegeben_ wird. 
    
 _leiterplatte_
  
> [out] Zeiger auf die Größe des durch den  _parameter pvBaseNew_ angegebenen Arrays in Bytes. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ein Zeiger wurde erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>Hinweise

Der  _Parameter "pcb"_ für die **ScRelocNotifications-Funktion** ist optional. 
  
## <a name="see-also"></a>Siehe auch



[ScRelocProps](screlocprops.md)

