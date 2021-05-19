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
  
Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter und MAPI übergeben haben. 
  
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
  
> [in] Gibt die zu überprüfende Methode per Enumeration an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument auf dem Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler verhinderte, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>Hinweise

Parameter, die zwischen MAPI und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms-Makro](checkparms.md) einer Debugüberprüfung unterzogen. Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, Clients sollten jedoch davon ausgehen, dass MAPI- und Anbieterparameter korrekt sind. Verwenden Sie das **HR_FAILED,** um Rückgabewerte zu testen. 
  
Das **UlValidateParms-Makro** wird unterschiedlich aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist. Dieses Makro wird verwendet, um Parameter für die wenigen **IUnknown-** und #A0 zu überprüfen, die ULONG anstelle von HRESULT-Werten zurückgeben. Das [ValidateParms-Makro](validateparms.md) funktioniert für alle anderen. 
  

