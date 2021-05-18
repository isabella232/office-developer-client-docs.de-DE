---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317136"
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
  
> Der _pMessage-Parameter_ ist NULL, und das Formular befindet sich entweder im [Status HandsOffFromNormal](handsofffromnormal-state.md) oder [HandsOffAfterSave.](handsoffaftersave-state.md) 
    
E_UNEXPECTED 
  
> Das Formular hat keinen der folgenden Zustände:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Hinweise

Die **IPersistMessage::SaveCompleted-Methode** wird von einer Formularanzeige aufgerufen, um das Formular darüber zu informieren, dass alle ausstehenden Änderungen gespeichert wurden. **SaveCompleted** sollte nur aufgerufen werden, wenn sich das Formular in einem der folgenden Zustände befindet: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Es gibt mehrere mögliche Aktionen, die die **SaveCompleted-Methode** ausführen kann, je nachdem, was der Parameter für den Nachrichtenzeiger enthält und in welchem Zustand sich die Nachricht befindet. Wenn eine Aktion erfolgreich ist, speichern Sie jedoch immer den aktuellen Status der Nachricht, auf die der _pMessage-Parameter_ zeigt, und übergeben Sie das Formular in den [Status Normal.](normal-state.md) 
  
In der folgenden Tabelle werden die Bedingungen beschrieben, die sich auf die Aktionen auswirken, die Sie bei der Implementierung von **SaveCompleted ausführen sollten.**
  
|**Bedingung**|**Aktion**|
|:-----|:-----|
|Der  _pMessage-Parameter_ ist NULL, und der  _fSameAsLoad-Parameter_ der [IPersistMessage::Save-Methode](ipersistmessage-save.md) ist auf TRUE festgelegt.  <br/> |Rufen Sie [die IMAPIViewAdviseSink::OnSaved-Methode](imapiviewadvisesink-onsaved.md) aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK.  <br/> |
|Der  _pMessage-Parameter_ ist NULL, und der  _fSameAsLoad-Parameter_ der **IPersistMessage::Save-Methode** ist auf FALSE festgelegt.  <br/> |Geben Sie S_OK zur�ck.  <br/> |
|Das Formular befindet sich im Status HandsOffFromNormal.  <br/> |Geben Sie die aktuelle Nachricht frei, und ersetzen Sie sie durch die Nachricht, auf die der  _pMessage-Parameter_ verweist. Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Ersetzungsnachricht auf, und geben Sie S_OK.  <br/> |
|Das Formular befindet sich im Status HandsOffAfterSave.  <br/> |Rufen Sie **die IMAPIViewAdviseSink::OnSaved-Methode** aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK.  <br/> |
|Das Formular befindet sich im [Status NoScribble.](noscribble-state.md)  <br/> |Geben Sie die aktuelle Nachricht frei, und ersetzen Sie sie durch die Nachricht, auf die _durch pMessage verwiesen wird._ Rufen Sie die **IUnknown::AddRef-Methode der Ersetzungsnachricht** auf. Rufen Sie **die IMAPIViewAdviseSink::OnSaved-Methode** aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK.  <br/> |
|Das Formular befindet sich in einem der HandsOff-Zustände, und der  _pMessage-Parameter_ ist auf NULL festgelegt.  <br/> |Zurückgeben E_INVALIDARG.  <br/> |
|Das Formular befindet sich in einem anderen Zustand als einem der HandsOff-Zustände oder des NoScribble-Status.  <br/> |Zurückgeben E_UNEXPECTED.  <br/> |
   
Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation für die [IPersistStorage::SaveCompleted-](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) oder [IPersistFile::SaveCompleted-Methoden.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) 
  
## <a name="see-also"></a>Siehe auch

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Formularzustände](form-states.md)
