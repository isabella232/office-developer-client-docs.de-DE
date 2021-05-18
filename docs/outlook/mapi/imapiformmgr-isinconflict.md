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
  
Bestimmt, ob ein Formular eigene Nachrichtenkonflikte verarbeiten kann. Eine Nachricht ist in Konflikt, wenn sie von mehreren Benutzern gleichzeitig bearbeitet wurde. Dies kann bei Nachrichten in öffentlichen Ordnern passieren.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameter

 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske mit client- oder anbieterdefinierten **Flags,** die aus der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft einer Nachricht kopiert wurden, die zusätzliche Informationen zum Status der Nachricht enthält.
    
 _szMessageClass_
  
> [in] Eine Zeichenfolge, die die Nachrichtenklasse der Nachricht benennt.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die Nachricht enthält. Der  _pFolderFocus-Parameter_ kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (z. B. wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular kann keine eigenen Nachrichtenkonflikte verarbeiten.
    
S_FALSE 
  
> Das Formular verarbeitet eigene Nachrichtenkonflikte, oder die Nachricht, für die Informationen übergeben wurden, ist nicht in Konflikt.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::IsInConflict-Methode** auf, um zu ermitteln, ob ein bestimmtes Formular keine eigenen Nachrichtenkonflikte verarbeiten kann. **IsInConflict** überprüft die Bitmasken in den  _Parametern ulMessageFlags_ und  _ulMessageStatus_ auf das Vorhandensein eines Konfliktflags. Wenn ein Konfliktflag festgelegt ist, löst **IsInConflict** die im  _szMessageClass-Parameter_ übergebene Nachrichtenklasse auf und gibt S_OK zurück, wenn das Formular keine eigenen Konflikte verarbeiten kann. **IsInConflict** gibt S_FALSE zurück, wenn das Formular eigene Konflikte verarbeitet. 
  
Ein Formular, das keine eigenen Konflikte verarbeiten kann, muss mithilfe der [IMAPIFormMgr::LoadForm-Methode](imapiformmgr-loadform.md) geöffnet werden und kann kein vorhandenes Formularobjekt wiederverwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Clientanwendungen müssen in der Regel mit Konflikten umgehen, wenn die Anwendungen von einer Nachricht zur nächsten oder vorherigen Nachricht in einem Ordner wechseln. Wenn eine Nachricht in Konflikt steht, aber der Formularserver für diese Nachricht Konflikte verarbeiten kann, sollte die Clientanwendung ihren üblichen Code zum Anzeigen der nächsten oder vorherigen Nachricht ausführen. Wenn der Formularserver Konflikte nicht verarbeiten kann, sollte die Clientanwendung so fortfahren, als wäre ihr die Nachrichtenklasse der nächsten oder vorherigen Nachricht nicht bekannt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

