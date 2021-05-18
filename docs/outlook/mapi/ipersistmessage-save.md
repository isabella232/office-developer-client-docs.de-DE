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
  
Speichert ein überarbeitetes Formular in der Nachricht zurück, aus der es geladen oder erstellt wurde.
  
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
  
> [in] TRUE, um anzugeben, dass die Nachricht, auf die  _pMessage_ verweist, die Nachricht ist, aus der das Formular geladen oder erstellt wurde. Andernfalls FALSE. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich gespeichert.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IPersistMessage::Save-Methode** auf, um ein überarbeitetes Formular wieder in der Nachricht zu speichern, aus der es geladen oder erstellt wurde. 
  
 **Speichern** sollte nur aufgerufen werden, wenn sich das Formular im [Normalzustand](normal-state.md) befindet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nehmen Sie keinen Commit für die gespeicherten Änderungen vor. Es liegt am Aufrufer, die Änderungen zu commiten. Nehmen Sie nie Änderungen an den Eigenschaften vor, die zur Nachricht des Formulars gehören, außer während des **Save-Aufrufs.** 
  
Wenn  _fSameAsLoad_ auf TRUE festgelegt ist, können Sie die Änderungen an der vorhandenen Nachricht des Formulars speichern. Wenn  _fSameAsLoad_ auf FALSE festgelegt ist, müssen Sie alle Eigenschaften aus der ursprünglichen Nachricht in die Nachricht kopieren, auf die  _pMessage_ verweist, bevor Sie das Speichern ausführen. Verwenden Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) der ursprünglichen Nachricht, um die Eigenschaften zu kopieren. 
  
Wenn alle Eigenschaften kopiert wurden, geben Sie den [Status NoScribble](noscribble-state.md) ein. Wenn keine Fehler auftreten, geben Sie S_OK. Andernfalls geben Sie den Fehler aus der fehlgeschlagenen Aktion zurück. 
  
Wenn **Save** aufgerufen wird, wenn sich das Formular in einem anderen Zustand als Normal befindet, geben Sie E_UNEXPECTED. 
  
Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation zu den [IPersistStorage-Methoden.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formularzustände](form-states.md)

