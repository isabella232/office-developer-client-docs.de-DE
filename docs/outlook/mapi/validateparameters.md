---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e2df45a2955182639cf0e551d914d95476762e41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629452"
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
  
> [in] Gibt die zu überprüfende Methode anhand der Aufzählung an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Parameter sind gültig. 
    
MAPI_E_CALL_FAILED 
  
> Mindestens einer der Parameter ist ungültig.
    
## <a name="remarks"></a>Bemerkungen

Das **Makro "ValidateParameters"** wurde durch das [Makro "ValidateParms"](validateparms.md) abgelöst. **ValidateParameters** funktioniert auf RISC-Plattformen nicht ordnungsgemäß und kann jetzt nicht mehr kompiliert werden. Es wird weiterhin kompiliert und funktioniert auf Intel-Plattformen ordnungsgemäß, **validateParms** wird jedoch auf allen Plattformen empfohlen. 
  

