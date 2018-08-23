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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565914"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    

