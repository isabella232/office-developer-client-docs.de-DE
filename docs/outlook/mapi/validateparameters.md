---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425203"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter übergeben haben. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT ValidateParameters(
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
  
> Alle Parameter sind gültig. 
    
MAPI_E_CALL_FAILED 
  
> Mindestens einer der Parameter ist ungültig.
    
## <a name="remarks"></a>Hinweise

Das **Makro ValidateParameters** wurde durch das Makro [ValidateParms ersetzt.](validateparms.md) **ValidateParameters** funktioniert auf RISC-Plattformen nicht ordnungsgemäß und kann jetzt nicht mehr für sie kompiliert werden. Es wird weiterhin auf Intel-Plattformen kompiliert und funktioniert ordnungsgemäß, **validateParms** wird jedoch auf allen Plattformen empfohlen. 
  

