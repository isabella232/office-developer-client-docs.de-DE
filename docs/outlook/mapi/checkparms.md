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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e7a4fde57515f0b8a41b9acf4adb01dd177a7a19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791414"
---
# <a name="checkparms"></a>CheckParms

  
  
**Betrifft**: Outlook 
  
Ruft eine interne Funktion zum debugging Parameter für Webdienstmethoden aufgerufen von MAPI-Anbieter zu überprüfen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
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
  
> [in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen. 
    
 _Erster_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Im Gegensatz zu den [ValidateParms](validateparms.md) und [UlValidateParms](ulvalidateparms.md) Makros führt das Makro **CheckParms** keine vollständige Parameter Überprüfung durch. Übergeben Sie Parameter zwischen MAPI- und Service Provider wird angenommen, dass richtig sein, damit **CheckParms** nur eine Debug-Überprüfung durchführt. 
  

