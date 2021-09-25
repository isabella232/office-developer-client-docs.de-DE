---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d111c6a0e51f3487014a411b6b7ebf4e3d588744
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578417"
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
  
> [in] Gibt die zu überprüfende Methode anhand der Aufzählung an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler hat verhindert, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

Parameter, die zwischen MAPI und Dienstanbietern übergeben werden, werden als korrekt angenommen und werden nur mit dem [CheckParms-Makro](checkparms.md) einer Debugüberprüfung unterzogen. Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, clients sollten jedoch davon ausgehen, dass MAPI- und Anbieterparameter korrekt sind. Verwenden Sie das **makro HR_FAILED,** um Rückgabewerte zu testen. 
  
Das **UlValidateParms-Makro** wird unterschiedlich aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist. Dieses Makro wird verwendet, um Parameter für die wenigen **IUnknown-** und MAPI-Methoden zu überprüfen, die ULONG anstelle von HRESULT-Werten zurückgeben. Das [Makro "ValidateParms"](validateparms.md) funktioniert für alle anderen. 
  

