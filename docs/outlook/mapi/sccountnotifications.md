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
ms.openlocfilehash: 923864c625cb032c3b351bb999ff7cc782eae588
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567167"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe in Bytes, der ein Array von ereignisbenachrichtigungen, und das Array zugeordneten Arbeitsspeicher überprüft.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cntf_
  
> [in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben. 
    
 _rgntf_
  
> [in] Zeiger auf das Array von **Benachrichtigung** Strukturen, deren Größe ist bestimmt werden soll. 
    
 _PCB_
  
> [out] Optional Zeiger auf die Größe des Arrays auf das durch den Parameter _Rgntf_ in Bytes. Wenn NULL, überprüft **ScCountNotifications** das Array von Benachrichtigungen. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Count wurde erfolgreich bestimmt.
    
MAPI_E_INVALID_PARAMETER
  
> Eine ungültige Benachrichtigung aufgetreten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn NULL in der _pcb_ -Parameter übergeben wird, überprüft die Funktion **ScCountNotifications** nur das Array von Benachrichtigungen, aber keine Zählung abgeschlossen ist. Wenn ein Wert ungleich Null in _pcb_übergeben wird, bestimmt die Größe des Arrays und speichert die Ursache **ScCountNotifications** _pcb_. Der Parameter _pcb_ muss groß genug für das gesamte Array sein. 
  

