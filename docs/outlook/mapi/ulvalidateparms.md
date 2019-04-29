---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419611"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die von Clientanwendungen an Dienstanbieter und MAPI übergeben wurden. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parameter

 _eMethod_
  
> in Gibt die zu überprüfende Methode an. 
    
 _First_
  
> in Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Fehler beim Abschließen des Vorgangs.
    
## <a name="remarks"></a>Bemerkungen

Parameter, die zwischen MAPI-und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms](checkparms.md) -Makro überprüft. Anbieter sollten alle Parameter überprüfen, die von Clientanwendungen übergeben wurden, aber Clients sollten davon ausgehen, dass MAPI-und Anbieter Parameter korrekt sind. Verwenden Sie das **HR_FAILED** -Makro, um Rückgabewerte zu testen. 
  
Das **UlValidateParms** -Makro wird anders aufgerufen, je nachdem, ob es sich bei dem aufrufenden Code um C oder C++ handelt. Dieses Makro wird verwendet, um Parameter für die wenigen **IUnknown** -und MAPI-Methoden zu überprüfen, die ULONG anstelle von HRESULT-Werten zurückgeben. Das [ValidateParms](validateparms.md) -Makro funktioniert für alle anderen. 
  

