---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d52907f93ee6c33884df41a67fad15fc2133902
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596232"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt, ob ein Formular eigene Nachrichtenkonflikte behandeln kann. Eine Nachricht ist in Konflikt, wenn sie gleichzeitig von mehreren Benutzern bearbeitet wurde. Dies kann bei Nachrichten in öffentlichen Ordnern passieren.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameter

 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske mit Flags, die aus der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) einer Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske von clientdefinierten oder vom Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft einer Nachricht kopiert werden, die zusätzliche Informationen zum Status der Nachricht bereitstellt.
    
 _szMessageClass_
  
> [in] Eine Zeichenfolge, die die Nachrichtenklasse der Nachricht benennt.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die Nachricht enthält. Der  _pFolderFocus-Parameter_ kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (z. B. wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular behandelt keine eigenen Nachrichtenkonflikte.
    
S_FALSE 
  
> Das Formular verarbeitet eigene Nachrichtenkonflikte, oder die Nachricht, für die Informationen übergeben wurden, befindet sich nicht in Konflikt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::IsInConflict-Methode** auf, um zu ermitteln, ob ein bestimmtes Formular keine eigenen Nachrichtenkonflikte behandelt. **IsInConflict** überprüft die Bitmasken in den  _Parametern ulMessageFlags_ und  _ulMessageStatus_ auf das Vorhandensein eines Konfliktkennzeichens. Wenn ein Konfliktkennzeichen festgelegt ist, löst **IsInConflict** die im parameter  _szMessageClass_ übergebene Nachrichtenklasse auf und gibt S_OK zurück, wenn das Formular seine eigenen Konflikte nicht behandelt. **IsInConflict** gibt S_FALSE zurück, wenn das Formular seine eigenen Konflikte behandelt. 
  
Ein Formular, das seine eigenen Konflikte nicht behandelt, muss mithilfe der [IMAPIFormMgr::LoadForm-Methode](imapiformmgr-loadform.md) geöffnet werden und kann ein vorhandenes Formularobjekt nicht wiederverwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Clientanwendungen haben in der Regel Konflikte zu bewältigen, wenn die Anwendungen von einer Nachricht zur nächsten oder vorherigen Nachricht in einem Ordner wechseln. Wenn eine Nachricht in Konflikt steht, aber der Formularserver für diese Nachricht Konflikte behandeln kann, sollte die Clientanwendung ihren üblichen Code zum Anzeigen der nächsten oder vorherigen Nachricht ausführen. Wenn der Formularserver Konflikte nicht behandeln kann, sollte die Clientanwendung so fortgesetzt werden, als ob die Nachrichtenklasse der nächsten oder vorherigen Nachricht nicht bekannt wäre. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

