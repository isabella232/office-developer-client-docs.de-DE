---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 03ea2aba27b9ea19daa3ea48f6ae0373f48d49ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591206"
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
  
> [in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, die durch den  _rgntf-Parameter_ angegeben werden. 
    
 _rgntf_
  
> [in] Zeiger auf das Array von **NOTIFICATION-Strukturen,** die Ereignisbenachrichtigungen definieren, innerhalb derer ein Zeiger angepasst werden soll. 
    
 _pvBaseOld_
  
> [in] Zeiger auf die ursprüngliche Basisadresse des Arrays, das durch den  _rgntf-Parameter_ angegeben wird. 
    
 _pvBaseNew_
  
> [in] Der Speicherort, an den **ScRelocNotifications** die neue Basisadresse des Arrays schreibt, das durch den  _rgntf-Parameter_ angegeben wird. 
    
 _Pcb_
  
> [out] Zeiger auf die Größe des Arrays in Byte, die durch den  _Parameter "pvBaseNew"_ angegeben wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Ein Zeiger wurde erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der  _parameter parameter_ to the **ScRelocNotifications** function is optional. 
  
## <a name="see-also"></a>Siehe auch



[ScRelocProps](screlocprops.md)

