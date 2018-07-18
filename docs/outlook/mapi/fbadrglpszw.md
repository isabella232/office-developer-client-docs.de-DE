---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791659"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Betrifft**: Outlook 
  
Überprüft alle Zeichenfolgen in einem Array von Unicode-Zeichenfolgen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Parameter

 _lppszW_
  
> [in] Zeiger auf ein Array mit Null terminierte Unicode-Zeichenfolgen. 
    
 _CString_
  
> [in] Anzahl der Zeichenfolgen im Array auf den durch den Parameter _LppszW_ verwiesen. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Eine oder mehrere der Zeichenfolgen in das angegebene Array ist ungültig. 
    
FALSE 
  
> Die Zeichenfolgen im angegebenen Array sind ungültig.
    

