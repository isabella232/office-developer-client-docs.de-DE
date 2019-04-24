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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351324"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, wo in einem Nachrichtenthread eine Nachricht gehört. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Die Anzahl der Bytes im übergeordneten Unterhaltungsindex.
    
 _lpbParent_
  
> in Zeiger auf Bytes im übergeordneten Unterhaltungsindex. Dies ist möglicherweise NULL, wenn _cbParent_ NULL ist. 
    
 _lpcbIndex_
  
> Out Zeiger auf die Anzahl von Bytes im neuen unter Haltungs Index, der vom Aufruf zurückgegeben wird. 
    
 _lppbIndex_
  
> Out Zeiger auf einen Zeiger auf den neuen unter Haltungs Index, der vom Aufruf zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

