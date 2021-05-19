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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415656"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, wohin in einem Nachrichtenthread eine Nachricht gehört. 
  
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
  
> [in] Anzahl der Bytes im übergeordneten Unterhaltungsindex.
    
 _lpbParent_
  
> [in] Zeiger auf Bytes im übergeordneten Unterhaltungsindex. Dies kann NULL sein,  _wenn cbParent_ null ist. 
    
 _lpcbIndex_
  
> [out] Zeiger auf die Anzahl der Bytes im neuen Unterhaltungsindex, der vom Aufruf zurückgegeben wird. 
    
 _lppbIndex_
  
> [out] Zeiger auf einen Zeiger auf den neuen Unterhaltungsindex, der vom Anruf zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

