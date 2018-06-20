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
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792748"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Betrifft**: Outlook 
  
Das Formular benachrichtigt, einen Vorgang abgeschlossen wurde. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameter

_pMessage_
  
> [in] Ein Zeiger auf die neu gespeicherte Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
E_INVALIDARG 
  
> Der Parameter _pMessage_ ist NULL, und das Formular ist entweder im Zustand [HandsOffFromNormal](handsofffromnormal-state.md) oder [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> Das Formular ist nicht in einem der folgenden Zustände:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Hinweise

Die **IPersistMessage::SaveCompleted** -Methode wird aufgerufen, von einem Formular-Viewer, um das Formular zu benachrichtigen, das alle ausstehende Änderungen gespeichert wurden. **SaveCompleted** sollte aufgerufen werden, nur, wenn das Formular in einem der folgenden Zustände befindet: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Es gibt mehrere mögliche Aktionen, die die **SaveCompleted** -Methode ausführen können, je nach der Botschaft Zeigerparameter enthält und welche Zustand die Nachricht befindet. Jedoch bei eine Aktion erfolgreich ist, immer speichern Sie dem aktuellen Status der Nachricht, die auf der _pMessage_ -Parameter verweist und Übergang das Formular in den [normalen](normal-state.md) Zustand. 
  
In der folgenden Tabelle werden die Bedingungen, die die Aktionen betreffen, die Sie, in der Implementierung der **SaveCompleted ergreifen sollten**beschrieben.
  
|**Bedingung**|**Aktion**|
|:-----|:-----|
|Der Parameter _pMessage_ ist NULL und der _fSameAsLoad_ -Parameter der [IPersistMessage::Save](ipersistmessage-save.md) -Methode auf TRUE festgelegt ist.  <br/> |Rufen Sie die [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) -Methode des alle registrierten Viewer, markieren Sie das Formular als clean und return S_OK zurück.  <br/> |
|Der Parameter _pMessage_ ist NULL und der _fSameAsLoad_ -Parameter der **IPersistMessage::Save** -Methode auf FALSE festgelegt ist.  <br/> |Geben Sie S_OK zur�ck.  <br/> |
|Das Formular befindet sich im HandsOffFromNormal Zustand.  <br/> |Freigeben Sie die aktuelle Nachricht, und Ersetzen Sie ihn mit der Meldung über den Parameter _pMessage_ . Rufen Sie die Ersatznachricht [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode, und geben Sie S_OK zurück.  <br/> |
|Das Formular befindet sich im HandsOffAfterSave Zustand.  <br/> |Rufen Sie die **IMAPIViewAdviseSink::OnSaved** -Methode des alle registrierten Viewer, markieren Sie das Formular als clean und return S_OK zurück.  <br/> |
|Das Formular befindet sich im [NoScribble](noscribble-state.md) Zustand.  <br/> |Freigeben Sie die aktuelle Nachricht, und Ersetzen Sie ihn mit der Meldung von _pMessage_. Rufen Sie die Ersatznachricht **IUnknown:: AddRef** -Methode. Rufen Sie die **IMAPIViewAdviseSink::OnSaved** -Methode des alle registrierten Viewer, markieren Sie das Formular als clean und return S_OK zurück.  <br/> |
|Das Formular befindet sich in einem der Zustände HandsOff und der _pMessage_ -Parameter auf NULL festgelegt ist.  <br/> |E_INVALIDARG zurück.  <br/> |
|Das Formular befindet sich in eine andere als die HandsOff Zustände oder der NoScribble Zustand.  <br/> |E_UNEXPECTED zurückgeben.  <br/> |
   
Weitere Informationen zum Speichern von Speicherobjekte finden Sie unter Dokumentation für die [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) oder [:: SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) -Methoden. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)


[Formular Staaten](form-states.md)


[IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[:: SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)

