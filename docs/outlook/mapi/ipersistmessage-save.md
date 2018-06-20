---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792736"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Betrifft**: Outlook 
  
Speichert eine überarbeitete Formular an die Nachricht aus der es geladen oder erstellt wurde.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Parameter

 _pMessage_
  
> [in] Ein Zeiger auf die Nachricht.
    
 _fSameAsLoad_
  
> [in] True, um anzugeben, dass die Nachricht, auf das verwiesen ist durch _pMessage_ die Nachricht aus der das Formular geladen oder erstellt wurde. andernfalls, FALSE. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular wurde erfolgreich gespeichert.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IPersistMessage::Save** -Methode, um ein überarbeiteten Formular wieder auf die Nachricht zu speichern, von dem er geladen oder erstellt wurde. 
  
 **Speichern Sie** sollte nur aufgerufen werden, wenn das Formular in seinem [normalen](normal-state.md) Zustand befindet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Übernehmen Sie die gespeicherten Änderungen nicht; Es liegt an den Anrufer an die Änderungen zu übernehmen. Nehmen Sie Änderungen an den Eigenschaften, die während des Anrufs **Speichern** auf das Formular Nachricht außer gehören nie vor. 
  
Wenn _fSameAsLoad_ auf TRUE festgelegt ist, können Sie die Änderungen auf dem Formular vorhandene Nachricht speichern. Wenn _fSameAsLoad_ auf FALSE festgelegt ist, müssen Sie alle Eigenschaften aus der ursprünglichen Nachricht in der Meldung von _pMessage_ vor dem Speichern kopieren. Verwenden Sie die ursprüngliche Nachricht [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um die Eigenschaften zu kopieren. 
  
Wenn alle Eigenschaften kopiert wurden, geben Sie den Status [NoScribble](noscribble-state.md) . Wenn keine Fehler auftreten, geben Sie S_OK zurück. Anderenfalls zurückgegeben Sie Fehler, der von der fehlgeschlagenen Aktion. 
  
Wenn **Speichern** aufgerufen wird, wenn das Formular in einem anderen Status als Normal befindet, zurückgeben Sie E_UNEXPECTED. 
  
Weitere Informationen zum Speichern von Speicherobjekte finden Sie in der Dokumentation zu den Methoden [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)


[Formular Staaten](form-states.md)

