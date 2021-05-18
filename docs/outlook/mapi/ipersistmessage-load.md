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
  
> [in] Ein Zeiger auf die Nachrichtenwebsite, damit das Formular geladen wird.
    
 _pMessage_
  
> [in] Ein Zeiger auf die Nachricht, für die das Formular geladen werden soll.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske mit client- oder anbieterdefinierten Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert werden, die Informationen über den Status der Nachricht bereitstellen.
    
 _ulMessageFlags_
  
> [in] Eine Bitmaske mit Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert wurde, die weitere Informationen zum Status der Nachricht bereitstellen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich geladen.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IPersistMessage::Load-Methode** auf, um ein Formular für eine vorhandene Nachricht zu laden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

 **Load** wird nur aufgerufen, wenn sich ein Formular in einem der folgenden Zustände befindet: 
  
- [Nicht initialisiert](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Wenn ein **Formularanzeiger Load aufruft,** während sich das Formular in einem anderen Zustand befindet, gibt die Methode E_UNEXPECTED. 
  
Wenn Ihr Formular einen Verweis auf eine andere aktive Nachrichtenwebsite als die an **Load** übergebene enthält, geben Sie die ursprüngliche Website frei, da sie nicht mehr verwendet wird. Store die Zeiger auf die Nachrichtenwebsite und -nachricht von den _Parametern pMessageSite_ und _pMessage_ aus und rufen die [IUnknown::AddRef-Methoden](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) beider Objekte auf, um ihre Referenzanzahl zu erhöhen. 
  
Speichern Sie nach Abschluss von **AddRef** die Eigenschaften aus den  _Parametern ulMessageStatus_ und  _ulMessageFlags_ im Formular. Überwechseln Sie das Formular in den [Status Normal,](normal-state.md) bevor es angezeigt wird, und benachrichtigen Sie registrierte Viewer, indem Sie ihre [IMAPIViewAdviseSink::OnNewMessage-Methoden](imapiviewadvisesink-onnewmessage.md) aufrufen. 
  
Wenn keine Fehler auftreten, geben Sie S_OK. 
  
## <a name="see-also"></a>Siehe auch



[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Nicht initialisierter Status](uninitialized-state.md)
  
[HandsOffAfterSave-Status](handsoffaftersave-state.md)
  
[HandsOffFromNormal-Status](handsofffromnormal-state.md)
  
[Formularzustände](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

