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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795486"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Betrifft**: Outlook 
  
Einen Zeiger in ein bestimmtes Ereignis Benachrichtigung Array passt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben. 
    
 _rgntf_
  
> [in] Zeiger auf das Array von **Benachrichtigung** Strukturen definieren von ereignisbenachrichtigungen in denen ein Zeiger ist angepasst werden. 
    
 _pvBaseOld_
  
> [in] Zeiger auf die ursprüngliche Basisadresse des Arrays durch den Parameter _Rgntf_ angegeben. 
    
 _pvBaseNew_
  
> [in] Der Speicherort, auf das die neue Basisadresse des durch den Parameter _Rgntf_ angegebenen Arrays von **ScRelocNotifications** schreibt. 
    
 _PCB_
  
> [out] Zeiger auf die Größe des durch den Parameter _PvBaseNew_ angegebenen Arrays in Bytes. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Ein Zeiger wurde erfolgreich korrigiert.
    
MAPI_E_INVALID_PARAMETER
  
> Eine ungültige Benachrichtigung aufgetreten.
    
## <a name="remarks"></a>Hinweise

Der Parameter _pcb_ an die Funktion **ScRelocNotifications** ist optional. 
  
## <a name="see-also"></a>Siehe auch



[ScRelocProps](screlocprops.md)

