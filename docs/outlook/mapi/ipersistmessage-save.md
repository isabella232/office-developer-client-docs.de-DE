---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51fa8ddb71ba3d80c80b7e19d267fdf7da4f62ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596043"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert ein überarbeitetes Formular wieder in der Nachricht, aus der es geladen oder erstellt wurde.
  
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
  
> [in] TRUE, um anzugeben, dass die Nachricht, auf die von  _pMessage_ verwiesen wird, die Nachricht ist, aus der das Formular geladen oder erstellt wurde; andernfalls FALSE. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich gespeichert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IPersistMessage::Save-Methode** auf, um ein überarbeitetes Formular wieder in der Nachricht zu speichern, aus der es geladen oder erstellt wurde. 
  
 **"Speichern"** sollte nur aufgerufen werden, wenn sich das Formular im [Normalen-Zustand](normal-state.md) befindet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Übernehmen Sie die gespeicherten Änderungen nicht. es liegt an dem Aufrufer, die Änderungen zu übernehmen. Nehmen Sie niemals Änderungen an den Eigenschaften vor,  die zur Nachricht des Formulars gehören, außer während des Speicheraufrufs. 
  
Wenn  _fSameAsLoad_ auf TRUE festgelegt ist, können Sie die Änderungen an der vorhandenen Nachricht des Formulars speichern. Wenn  _fSameAsLoad_ auf FALSE festgelegt ist, müssen Sie alle Eigenschaften aus der ursprünglichen Nachricht in die Nachricht kopieren, auf die von pMessage verwiesen  _wird,_ bevor Sie das Speichern ausführen. Verwenden Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) der ursprünglichen Nachricht, um die Eigenschaften zu kopieren. 
  
Wenn alle Eigenschaften kopiert wurden, geben Sie den [NoScribble-Zustand](noscribble-state.md) ein. Wenn keine Fehler auftreten, geben Sie S_OK zurück. Andernfalls wird der Fehler aus der fehlgeschlagenen Aktion zurückgegeben. 
  
Wenn **Save** aufgerufen wird, wenn sich das Formular in einem anderen Zustand als Normal befindet, geben Sie E_UNEXPECTED zurück. 
  
Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation zu den [IPersistStorage-Methoden.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formularstatus](form-states.md)

