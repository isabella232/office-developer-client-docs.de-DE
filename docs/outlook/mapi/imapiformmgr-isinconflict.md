---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412884"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt, ob ein Formular eigene Nachrichten Konflikte verarbeiten kann. Eine Nachricht ist in Konflikt, wenn Sie von mehreren Benutzern gleichzeitig bearbeitet wurde. Dies kann mit Nachrichten in öffentlichen Ordnern geschehen.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameter

 _ulMessageFlags_
  
> in Ein Zeiger auf eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer Nachricht kopiert werden, die den aktuellen Status der Nachricht angibt.
    
 _ulMessageStatus_
  
> in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft einer Nachricht kopiert werden, die zusätzliche Informationen zum Status der Nachricht bereitstellt.
    
 _szMessageClass_
  
> in Eine Zeichenfolge, die die Nachrichtenklasse der Nachricht benennt.
    
 _pFolderFocus_
  
> in Ein Zeiger auf den Ordner, der die Nachricht enthält. Der _pFolderFocus_ -Parameter kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (beispielsweise, wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular verarbeitet keine eigenen Nachrichten Konflikte.
    
S_FALSE 
  
> Das Formular verarbeitet eigene Nachrichten Konflikte, oder die Nachricht, für die Informationen übergeben wurden, ist nicht in Konflikt.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: IsInConflict** -Methode auf, um zu ermitteln, ob ein bestimmtes Formular eigene Nachrichten Konflikte nicht verarbeitet. **IsInConflict** überprüft die Bitmasken in den Parametern _ulMessageFlags_ und _ulMessageStatus_ auf das vorhanden sein eines Konflikt Kennzeichens. Wenn ein Konflikt-Flag festgelegt ist, löst **IsInConflict** die Nachrichtenklasse, die im Parameter _szMessageClass_ übergeben wird, und gibt S_OK zurück, wenn das Formular Ihre eigenen Konflikte nicht behandelt. **IsInConflict** gibt S_FALSE zurück, wenn das Formular eigene Konflikte behandelt. 
  
Ein Formular, das seine eigenen Konflikte nicht behandelt, muss mithilfe der [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) -Methode geöffnet werden und kann kein vorhandenes Form-Objekt wieder verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Client Anwendungen müssen in der Regelkonflikte bewältigen, wenn die Anwendungen von einer Nachricht zur nächsten oder zur vorherigen Nachricht in einem Ordner wechseln. Wenn eine Nachricht in Konflikt steht, aber der Formularserver für diese Nachricht Konflikte verarbeiten kann, sollte die Clientanwendung den üblichen Code zum Anzeigen der nächsten oder vorherigen Nachricht ausführen. Wenn der Formularserver Konflikte nicht verarbeiten kann, sollte die Clientanwendung fortgesetzt werden, als ob Sie die Nachrichtenklasse der nächsten oder vorherigen Nachricht nicht kennen würde. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md)
  
[Kanonische Pidtagmessagestatus (-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

