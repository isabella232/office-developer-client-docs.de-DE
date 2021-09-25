---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c7fc3875abc26e642b6ae1e5bf4c96c3c017aad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556861"
---
# <a name="checkparms"></a>CheckParms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um Debugparameter für Dienstanbietermethoden zu überprüfen, die von MAPI aufgerufen werden. 
  
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
  
> [in] Gibt die zu überprüfende Methode anhand der Aufzählung an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zu den [Makros ValidateParms](validateparms.md) und [UlValidateParms](ulvalidateparms.md) führt das **CheckParms-Makro** keine vollständige Parameterüberprüfung durch. Zwischen MAPI und Dienstanbietern übergebene Parameter werden als korrekt angenommen, sodass **CheckParms** nur eine Debugüberprüfung durchführt. 
  

