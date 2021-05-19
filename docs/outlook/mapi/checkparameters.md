---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433395"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um Debugparameter für von MAPI aufgerufene Dienstanbietermethoden zu überprüfen. 
  
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
  
> [in] Gibt die zu überprüfende Methode per Enumeration an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument auf dem Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Das **Makro CheckParameters** wurde durch das [Makro CheckParms ersetzt.](checkparms.md) **CheckParms** wird auf allen Plattformen empfohlen. 
  

