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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
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
  
> in Ein Zeiger auf die neu gespeicherte Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich ausgeführt.
    
E_INVALIDARG 
  
> Der _pMessage_ -Parameter ist NULL, und das Formular befindet sich im [Status "handsofffromnormal](handsofffromnormal-state.md) -oder [HandsOffAfterSave](handsoffaftersave-state.md) -Zustand. 
    
E_UNEXPECTED 
  
> Das Formular befindet sich nicht in einem der folgenden Status:
    
   - Status "handsofffromnormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Bemerkungen

Die **IPersistMessage:: SaveCompleted** -Methode wird von einem Formular Betrachter aufgerufen, um das Formular zu benachrichtigen, dass alle ausstehenden Änderungen gespeichert wurden. **SaveCompleted** sollte nur aufgerufen werden, wenn sich das Formular in einem der folgenden Zustände befindet: 
  
- Status "handsofffromnormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Es gibt verschiedene mögliche Aktionen, die von der **SaveCompleted** -Methode ausgeführt werden können, je nachdem, was der Nachrichten Zeigerparameter enthält und in welchem Zustand sich die Nachricht befindet. Wenn eine Aktion jedoch erfolgreich ist, speichern Sie immer den aktuellen Status der Nachricht, auf die der _pMessage_ -Parameter zeigt, und wechseln Sie in den [normalen](normal-state.md) Status des Formulars. 
  
In der folgenden Tabelle werden die Bedingungen beschrieben, die sich auf die Aktionen auswirken, die Sie bei der Implementierung von **SaveCompleted**ausführen sollten.
  
|**Bedingung**|**Aktion**|
|:-----|:-----|
|Der _pMessage_ -Parameter ist NULL, und der _fSameAsLoad_ -Parameter der [IPersistMessage:: Save](ipersistmessage-save.md) -Methode ist auf true festgelegt.  <br/> |Rufen Sie die [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved-Methode aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.  <br/> |
|Der _pMessage_ -Parameter ist NULL, und der _fSameAsLoad_ -Parameter der **IPersistMessage:: Save** -Methode ist auf false festgelegt.  <br/> |Geben Sie S_OK zur�ck.  <br/> |
|Das Formular befindet sich im Status "handsofffromnormal-Zustand.  <br/> |Geben Sie die aktuelle Nachricht frei, und ersetzen Sie Sie durch die Nachricht, auf die durch den _pMessage_ -Parameter verwiesen wird. Rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode der Ersatznachricht auf, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich im HandsOffAfterSave-Zustand.  <br/> |Rufen Sie die **IMAPIViewAdviseSink::** onsaved-Methode aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich im [noscribble](noscribble-state.md) -Zustand.  <br/> |Geben Sie die aktuelle Nachricht frei, und ersetzen Sie Sie durch die Nachricht, auf die von _pMessage_verwiesen wird. Rufen Sie die **IUnknown:: AddRef** -Methode der Ersatznachricht auf. Rufen Sie die **IMAPIViewAdviseSink::** onsaved-Methode aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich in einem der HandsOff-Zustände, und der _pMessage_ -Parameter ist auf NULL festgelegt.  <br/> |E_INVALIDARG zurückgeben.  <br/> |
|Das Formular befindet sich in einem anderen Status als einem der HandsOff-Zustände oder im noScribble-Zustand.  <br/> |E_UNEXPECTED zurückgeben.  <br/> |
   
Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation zu den [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) -oder [IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) -Methoden. 
  
## <a name="see-also"></a>Siehe auch

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Formular Status](form-states.md)
