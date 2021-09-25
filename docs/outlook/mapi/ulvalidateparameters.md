---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a1736001faee62e498784c8a28d24b40f43b781
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623999"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter und MAPI übergeben haben. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT UlValidateParameters(
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
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>Bemerkungen

Das **UlValidateParameters-Makro** wurde durch das [UlValidateParms-Makro](ulvalidateparms.md) abgelöst. **UlValidateParameters** funktioniert auf RISC-Plattformen nicht ordnungsgemäß und kann jetzt nicht mehr kompiliert werden. Es wird weiterhin auf Intel-Plattformen kompiliert und funktioniert ordnungsgemäß, **aber UlValidateParms** wird auf allen Plattformen empfohlen. 
  

