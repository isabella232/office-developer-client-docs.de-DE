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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309618"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert ein überarbeitete Formular zurück in der Nachricht, von der es geladen oder erstellt wurde.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Parameter

 _pMessage_
  
> in Ein Zeiger auf die Nachricht.
    
 _fSameAsLoad_
  
> in TRUE, um anzugeben, dass die Nachricht, auf die von _pMessage_ verwiesen wird, die Nachricht ist, von der das Formular geladen oder erstellt wurde; andernfalls FALSE. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich gespeichert.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IPersistMessage:: Save** -Methode auf, um ein überarbeitete Formular zurück in die Nachricht zu speichern, aus der es geladen oder erstellt wurde. 
  
 **Save** sollte nur aufgerufen werden, wenn sich das Formular im [Normal](normal-state.md) Zustand befindet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichern Sie die gespeicherten Änderungen nicht. der Aufrufer muss die Änderungen übernehmen. Nehmen Sie keine Änderungen an den Eigenschaften vor, die zur Nachricht des Formulars gehören, außer während des **Save** -Aufrufs. 
  
Wenn _fSameAsLoad_ auf true festgelegt ist, können Sie die Änderungen an der vorhandenen Nachricht des Formulars speichern. Wenn _fSameAsLoad_ auf false festgelegt ist, müssen Sie alle Eigenschaften aus der ursprünglichen Nachricht in die Nachricht kopieren, die von _pMessage_ vor dem Speichern ausgeführt wird. Verwenden Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode der ursprünglichen Nachricht, um die Eigenschaften zu kopieren. 
  
Wenn alle Eigenschaften kopiert wurden, geben Sie den Status [noscribble](noscribble-state.md) ein. Wenn keine Fehler auftreten, geben Sie S_OK zurück. Geben Sie andernfalls den Fehler aus der fehlgeschlagenen Aktion zurück. 
  
Wenn **Save** aufgerufen wird, wenn sich das Formular in einem anderen Status als normal befindet, geben Sie E_UNEXPECTED zurück. 
  
Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation zu den [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) -Methoden. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formular Status](form-states.md)

