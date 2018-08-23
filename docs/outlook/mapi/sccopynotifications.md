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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593354"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Kopiert eine Gruppe von ereignisbenachrichtigungen in einen einzelnen Block Arbeitsspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben. 
    
 _rgntf_
  
> [in] Zeiger auf ein Array von **Benachrichtigung** Strukturen definieren die ereignisbenachrichtigungen kopiert werden soll. 
    
 _pvDst_
  
> [out] Zeiger auf die zurückgegebenen Benachrichtigungen. 
    
 _PCB_
  
> [out] Optionaler Zeiger auf eine Variable, die die Größe in Bytes des Arrays mit der _Rgntf_ -Parameter, in dem gezeigt wird gespeichert. Wenn nicht NULL-Wert der _pcb_ -Parameter wird festgelegt, um die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Ereignisbenachrichtigungen wurden erfolgreich kopiert.
    
E_INVALIDARG
  
> Eine ungültige Benachrichtigung aufgetreten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn NULL in der _pcb_ -Parameter übergeben wird, wird keine kopieren ausgeführt. Wenn Sie ein nicht-Nullwert _pcb_übergeben wird, kopiert die **ScCopyNotifications** -Funktion die Größe des Arrays und das Array selbst in einen einzelnen Block Arbeitsspeicher. Wenn _pcb_ ungleich NULL ist, wird es auf die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert festgelegt. Der Parameter _PvDst_ muss groß genug für das gesamte Array sein. 
  

