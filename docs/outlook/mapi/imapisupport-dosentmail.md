---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82490dbe597ebd3f7198aa7e0c904a10202ecd77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568210"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verarbeitet eine gesendete Nachricht.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpMessage_
  
> [in] Ein Zeiger auf die ge�ffneten Nachricht f�r die eine Nachricht im Ordner speichern gesendete Elemente vorgesehen generiert werden soll.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.
  
 **DoSentMail** f�hrt die folgenden Aufgaben: 
  
- Überprüft die Nachricht für die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft, um festzustellen, ob die Nachricht nach dem Senden gelöscht werden soll.
    
- Bestimmt den Speicherort des Ordners "Gesendete Elemente".
    
- Initiiert die Nachricht Hook Verarbeitung f�r alle Hook auf den Ordner Gesendete Objekte festgelegt.
    
- Verschiebt die Nachricht im Ordner Gesendete Elemente, Ordner Gel�schte Objekte, oder in einen anderen Ordner.
    
- Gibt die Nachricht frei.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[Kanonische PidTagDeleteAfterSubmit-Eigenschaft](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

