---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 23b486a91701a317f23b6dd1f0018db115f369c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579768"
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
  
> [in] Ein Zeiger auf die Nachrichtenwebsite für das zu ladende Formular.
    
 _pMessage_
  
> [in] Ein Zeiger auf die Nachricht, für die das Formular geladen werden soll.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske mit client- oder anbieterdefinierten Flags, die aus der **eigenschaft PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) der Nachricht kopiert wird und Informationen zum Status der Nachricht bereitstellt.
    
 _ulMessageFlags_
  
> [in] Eine Bitmaske mit Flags, die aus der **Eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht kopiert wurde und weitere Informationen zum Status der Nachricht bereitstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich geladen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IPersistMessage::Load-Methode** auf, um ein Formular für eine vorhandene Nachricht zu laden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

 **Laden** wird nur aufgerufen, wenn sich ein Formular in einem der folgenden Zustände befindet: 
  
- [Nicht initialisiert](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Wenn ein Formularviewer **Load** aufruft, während sich das Formular in einem anderen Zustand befindet, gibt die Methode E_UNEXPECTED zurück. 
  
Wenn Ihr Formular über einen Verweis auf eine aktive Nachrichtenwebsite verfügt, die nicht die in Load übergebene ist, geben **Sie** die ursprüngliche Website frei, da sie nicht mehr verwendet wird. Store die Zeiger auf die Nachrichtenwebsite und die Nachricht aus den _Parametern "pMessageSite"_ und _"pMessage"_ und rufen die [IUnknown::AddRef-Methoden](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) beider Objekte auf, um deren Verweisanzahl zu erhöhen. 
  
Speichern Sie nach Abschluss von **AddRef** die Eigenschaften aus den  _Parametern ulMessageStatus_ und  _ulMessageFlags_ im Formular. Überführen Sie das Formular in den [Normalzustand,](normal-state.md) bevor es angezeigt wird, und benachrichtigen Sie registrierte Benutzer, indem Sie ihre [IMAPIViewAdviseSink::OnNewMessage-Methoden](imapiviewadvisesink-onnewmessage.md) aufrufen. 
  
Wenn keine Fehler auftreten, geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Nicht initialisierter Zustand](uninitialized-state.md)
  
[HandsOffAfterSave-Zustand](handsoffaftersave-state.md)
  
[HandsOffFromNormal-Zustand](handsofffromnormal-state.md)
  
[Formularstatus](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

