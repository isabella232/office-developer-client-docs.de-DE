---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317129"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Lädt das Formular für eine angegebene Nachricht.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Parameter

 _pMessageSite_
  
> in Ein Zeiger auf die Nachrichtenwebsite für das zu ladende Formular.
    
 _pMessage_
  
> in Ein Zeiger auf die Nachricht, für die das Formular geladen werden soll.
    
 _ulMessageStatus_
  
> in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert werden und Informationen zum Status der Nachricht enthalten.
    
 _ulMessageFlags_
  
> in Eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert werden und weitere Informationen zum Status der Nachricht enthalten.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich geladen.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IPersistMessage:: Laden** -Methode auf, um ein Formular für eine vorhandene Nachricht zu laden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

 **Laden** wird nur aufgerufen, wenn sich ein Formular in einem der folgenden Zustände befindet: 
  
- [Initialisierten](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Status "handsofffromnormal](handsofffromnormal-state.md)
    
Wenn ein Formular-Viewer **Laden** aufruft, während sich das Formular in einem anderen Zustand befindet, gibt die Methode E_UNEXPECTED zurück. 
  
Wenn das Formular einen Verweis auf eine aktive Nachrichtenwebsite hat, die nicht an den **Laden**übergeben wird, lassen Sie die ursprüngliche Website frei, da Sie nicht mehr verwendet wird. Speichern Sie die Zeiger auf den Nachrichten Standort und die Nachricht aus den Parametern _pMessageSite_ und _pMessage_ , und rufen Sie die Methoden [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Objekte auf, um Ihre Verweisanzahl zu erhöhen. 
  
Nachdem **AddRef** abgeschlossen ist, speichern Sie die Eigenschaften aus den Parametern _ulMessageStatus_ und _ulMessageFlags_ in dem Formular. Wechseln Sie das Formular in den [Normal](normal-state.md) Zustand, bevor Sie es anzeigen, und Benachrichtigen Sie registrierte Betrachter, indem Sie Ihre [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen. 
  
Wenn keine Fehler auftreten, geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md)
  
[Kanonische Pidtagmessagestatus (-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Nicht initialisierter Status](uninitialized-state.md)
  
[HandsOffAfterSave-Status](handsoffaftersave-state.md)
  
[Status "handsofffromnormal-Status](handsofffromnormal-state.md)
  
[Formular Status](form-states.md)


[IPersistStorage:: Laden](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream:: Laden](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile:: Laden](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

