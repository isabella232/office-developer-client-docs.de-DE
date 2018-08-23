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
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573187"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  

