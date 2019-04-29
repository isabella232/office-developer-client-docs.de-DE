---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422278"
---
# <a name="checkparms"></a>CheckParms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um debuggingparameter für Dienstanbieter Methoden zu überprüfen, die von MAPI aufgerufen werden. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT CheckParms(
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
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Im Gegensatz zu den Makros [ValidateParms](validateparms.md) und [UlValidateParms](ulvalidateparms.md) führt das **CheckParms** -Makro keine vollständige Parameterüberprüfung aus. Parameter, die zwischen MAPI-und Dienstanbietern übergeben werden, werden als richtig angenommen, daher führt **CheckParms** nur eine Debug-Validierung aus. 
  

