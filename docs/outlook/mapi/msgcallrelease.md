---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 648a47a814071911aafad9f1b091a47a2647cc66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595658"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die eine **IStorage-Schnittstelle** nach der endgültigen Veröffentlichung eines darauf basierenden **IMessage-Objekts** mit der [OpenIMsgOnIStg-Funktion](openimsgonistg.md) freigeben kann. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> [in] Enthält aufrufende Anwendungsinformationen zur **IMessage-Schnittstelle.** 
    
 _lpMessage_
  
> [in] Zeiger auf die Nachricht auf oberster Ebene und die Anlagen, die freigegeben wurden.
    
## <a name="return-value"></a>Return value

None.
  

