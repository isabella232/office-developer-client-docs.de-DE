---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793270"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Betrifft**: Outlook 
  
Definiert eine Rückruffunktion, die eine Schnittstelle **IStorage** nach der endgültigen Version eines Objekts mit der Funktion [OpenIMsgOnIStg](openimsgonistg.md) aufbaut **IMessage** freigegeben werden kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> [in] Enthält die aufrufende Anwendungsinformationen zur **IMessage** -Schnittstelle. 
    
 _lpMessage_
  
> [in] Zeiger auf der obersten Ebene Meldung und Anlagen, die veröffentlicht wurden.
    
## <a name="return-value"></a>Rückgabewert

None.
  

