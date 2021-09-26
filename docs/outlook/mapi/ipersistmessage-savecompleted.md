---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 53026c7b7cabd6f399300db79b441d6fee953a0d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620590"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt das Formular, dass ein Speichervorgang abgeschlossen wurde. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameter

_pMessage_
  
> [in] Ein Zeiger auf die neu gespeicherte Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
E_INVALIDARG 
  
> Der _pMessage-Parameter_ ist NULL, und das Formular befindet sich entweder im [HandsOffFromNormal-](handsofffromnormal-state.md) oder [HandsOffAfterSave-Zustand.](handsoffaftersave-state.md) 
    
E_UNEXPECTED 
  
> Das Formular befindet sich nicht in einem der folgenden Zustände:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Bemerkungen

Die **IPersistMessage::SaveCompleted-Methode** wird von einem Formularviewer aufgerufen, um das Formular darüber zu benachrichtigen, dass alle ausstehenden Änderungen gespeichert wurden. **SaveCompleted** sollte nur aufgerufen werden, wenn sich das Formular in einem der folgenden Zustände befindet: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Es gibt mehrere mögliche Aktionen, die die **SaveCompleted-Methode** ausführen kann, je nachdem, was der Nachrichtenzeigerparameter enthält und in welchem Status sich die Nachricht befindet. Wenn eine Aktion jedoch erfolgreich ist, speichern Sie immer den aktuellen Status der Nachricht, auf die der _pMessage-Parameter_ zeigt, und überführen Sie das Formular in den [Normalzustand.](normal-state.md) 
  
In der folgenden Tabelle werden die Bedingungen beschrieben, die sich auf die Aktionen auswirken, die Sie bei der Implementierung von **SaveCompleted** ausführen sollten.
  
|**Bedingung**|**Aktion**|
|:-----|:-----|
|Der  _pMessage-Parameter_ ist NULL, und der  _fSameAsLoad-Parameter_ der [IPersistMessage::Save-Methode](ipersistmessage-save.md) ist auf TRUE festgelegt.  <br/> |Rufen Sie die [IMAPIViewAdviseSink::OnSaved-Methode](imapiviewadvisesink-onsaved.md) aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.  <br/> |
|Der  _pMessage-Parameter_ ist NULL, und der  _fSameAsLoad-Parameter_ der **IPersistMessage::Save-Methode** ist auf FALSE festgelegt.  <br/> |Geben Sie S_OK zur�ck.  <br/> |
|Das Formular befindet sich im HandsOffFromNormal-Zustand.  <br/> |Geben Sie die aktuelle Nachricht frei, und ersetzen Sie sie durch die Nachricht, auf die durch den  _Parameter "pMessage"_ verwiesen wird. Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Ersetzungsnachricht auf, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich im HandsOffAfterSave-Zustand.  <br/> |Rufen Sie die **IMAPIViewAdviseSink::OnSaved-Methode** aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich im [NoScribble-Zustand.](noscribble-state.md)  <br/> |Geben Sie die aktuelle Nachricht frei, und ersetzen Sie sie durch die Nachricht, auf die  _pMessage_ verweist. Rufen Sie die **IUnknown::AddRef-Methode** der Ersetzungsnachricht auf. Rufen Sie die **IMAPIViewAdviseSink::OnSaved-Methode** aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich in einem der HandsOff-Zustände, und der  _Parameter "pMessage"_ ist auf NULL festgelegt.  <br/> |Zurückgeben E_INVALIDARG.  <br/> |
|Das Formular befindet sich in einem anderen Zustand als einem der HandsOff-Zustände oder im NoScribble-Zustand.  <br/> |Zurückgeben E_UNEXPECTED.  <br/> |
   
Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation für die Methoden [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) oder [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) 
  
## <a name="see-also"></a>Siehe auch

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Formularstatus](form-states.md)
