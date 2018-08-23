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
ms.openlocfilehash: 6c7942d16cabc61eab55ab145b9c26a1799bbcc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565172"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ein Zeiger auf die Website für die Nachricht für das Formular geladen werden.
    
 _pMessage_
  
> [in] Ein Zeiger auf die Meldung für die das Formular geladen werden soll.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, kopiert aus der Nachricht **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft, bereitstellen, die Informationen zum Status der Nachricht.
    
 _ulMessageFlags_
  
> [in] Eine Bitmaske aus Flags, die aus der Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft kopiert, die bieten weitere Informationen zum Status der Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular wurde erfolgreich geladen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer rufen Sie die **IPersistMessage::Load** -Methode, um ein Formular für eine vorhandene Nachricht zu laden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

 **Load** wird nur aufgerufen, wenn ein Formular in einem der folgenden Zustände wird: 
  
- [Nicht initialisiert](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Wenn ein Formular Viewer **Load** anruft, während das Formular in jedem anderen Zustand befindet, gibt die Methode E_UNEXPECTED zurück. 
  
Wenn Ihr Formular einen Verweis auf eine aktive Nachricht Website als derjenigen, die in **Load**übergeben wird, lassen Sie die ursprüngliche Website, da sie nicht mehr verwendet werden. Der Zeiger auf die Nachricht-Website und die Nachricht der Parameter _pMessageSite_ und _pMessage_ gespeichert, und rufen beide Objekte [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) Methoden, um ihre Referenzzähler erhöhen. 
  
Nachdem **AddRef** abgeschlossen ist, speichern Sie die Eigenschaften der Parameter _UlMessageStatus_ und _UlMessageFlags_ in das Formular. Übergang zu seinem [normalen](normal-state.md) Zustand Formulars vor dem anzeigen, und Benachrichtigen der registrierten Viewer durch ihre [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen. 
  
Wenn keine Fehler auftreten, geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Status „Nicht initialisiert“](uninitialized-state.md)
  
[Status „HandsOffAfterSave“](handsoffaftersave-state.md)
  
[Status „HandsOffFromNormal“](handsofffromnormal-state.md)
  
[Formularstatus](form-states.md)


[IPersistStorage](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream:: Load](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile:: Load](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

