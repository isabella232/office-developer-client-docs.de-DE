---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2161c68517e2f83e2f2388cf209d464116cac454
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567760"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um Debugparameter für Dienstanbietermethoden zu überprüfen, die von MAPI aufgerufen werden. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parameter

 _eMethod_
  
> [in] Gibt die zu überprüfende Methode anhand der Aufzählung an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das **Makro "CheckParameters"** wurde durch das [Makro "CheckParms"](checkparms.md) abgelöst. **CheckParms** wird auf allen Plattformen empfohlen. 
  

