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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405912"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die eine **IStorage** -Schnittstellenach der endgültigen Version eines auf Ihr basierenden **IMessage** -Objekts mit der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion freigeben kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> in Enthält Anruf Anwendungsinformationen zur **IMessage** -Schnittstelle. 
    
 _lpMessage_
  
> in Zeiger auf die Nachricht und die Anlagen auf oberster Ebene, die freigegeben wurden.
    
## <a name="return-value"></a>Return value

None.
  

