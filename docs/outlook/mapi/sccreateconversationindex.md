---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9c37bd8613f8dc344fad841309b26fb763639935
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609544"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, wo in einem Nachrichtenthread eine Nachricht gehört. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der Bytes im Index der übergeordneten Unterhaltung.
    
 _lpbParent_
  
> [in] Zeiger auf Bytes im Index der übergeordneten Unterhaltung. Dies kann NULL sein, wenn  _cbParent_ null ist. 
    
 _lpcbIndex_
  
> [out] Zeiger auf die Anzahl der Bytes im neuen Unterhaltungsindex, der vom Aufruf zurückgegeben wird. 
    
 _lppbIndex_
  
> [out] Zeiger auf einen Zeiger auf den neuen Unterhaltungsindex, der vom Aufruf zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

