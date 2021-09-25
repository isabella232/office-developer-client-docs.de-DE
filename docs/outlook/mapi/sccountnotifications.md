---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de46b401053fa31b93d1dbd2f34a1741a8da1a1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578711"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe eines Arrays von Ereignisbenachrichtigungen in Byte und überprüft den dem Array zugeordneten Speicher.
  
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
  
> [in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, die durch den  _rgntf-Parameter_ angegeben werden. 
    
 _rgntf_
  
> [in] Zeiger auf das Array von **NOTIFICATION-Strukturen,** dessen Größe bestimmt werden soll. 
    
 _Pcb_
  
> [out] Optionaler Zeiger auf die Größe des Arrays in Byte, auf das der  _rgntf-Parameter_ verweist. Wenn NULL, überprüft **ScCountNotifications** das Array von Benachrichtigungen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Anzahl wurde erfolgreich ermittelt.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde eine ungültige Benachrichtigung gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn NULL im _Parameter "parameters"_ übergeben wird, überprüft die **ScCountNotifications-Funktion** nur das Array von Benachrichtigungen, aber es wird keine Zählung durchgeführt. Wenn ein Wert ungleich NULL in _einem Stift_ übergeben wird, bestimmt **ScCountNotifications** die Größe des Arrays und speichert die _Ursache._ Der  _Parameter "parameters"_ muss groß genug sein, um das gesamte Array enthalten zu können. 
  

