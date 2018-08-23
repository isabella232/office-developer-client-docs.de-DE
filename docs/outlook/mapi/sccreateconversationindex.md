---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594152"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, in dem in einem Thread Nachricht eine Nachricht gehört. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>Parameter

 _cbParent_
  
> [in] Anzahl der Bytes in der übergeordneten Unterhaltung Index.
    
 _lpbParent_
  
> [in] Zeiger auf Bytes im übergeordneten Unterhaltung Index. Dies kann NULL sein, wenn _CbParent_ gleich NULL ist. 
    
 _lpcbIndex_
  
> [out] Zeiger auf die Anzahl der Bytes in den neuen Unterhaltung Index durch den Aufruf zurückgegeben. 
    
 _lppbIndex_
  
> [out] Zeiger auf einen Zeiger auf den neuen Unterhaltung Index durch den Aufruf zurückgegeben.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

