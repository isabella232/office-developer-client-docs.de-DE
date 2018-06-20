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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792173"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**Betrifft**: Outlook 
  
Bestimmt, ob ein Formular eine eigene Nachricht Konflikte verarbeitet werden kann. Eine Nachricht ist in Konflikt, wenn es von mehreren Benutzern gleichzeitig bearbeitet wurde. Dies kann vorkommen, auf Nachrichten in öffentlichen Ordnern.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameter

 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske aus Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer Nachricht, der angibt, den aktuellen Status der Nachricht kopiert.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, kopiert aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft einer Nachricht bereitstellt, die zusätzliche Informationen zum Status der Nachricht.
    
 _szMessageClass_
  
> [in] Eine Zeichenfolge, die die Nachricht Nachrichtenklasse bezeichnet.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die Nachricht enthält. Der Parameter _pFolderFocus_ kann NULL sein, wenn eine solche ein Ordner nicht vorhanden ist (z. B., wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular behandelt eine eigene Nachricht Konflikte nicht.
    
S_FALSE 
  
> Das Formular eine eigene Nachricht Konflikte behandelt werden, oder die Nachricht, deren Informationen übergeben wurde, ist nicht in Konflikt.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::IsInConflict** -Methode, um zu ermitteln, ob ein bestimmtes Formular eine eigene Nachricht Konflikte nicht behandelt. **IsInConflict** überprüft die Bitmasken in den _UlMessageFlags_ und _UlMessageStatus_ das Vorhandensein von ein Conflict-Flag. Wenn ein Konflikt Flag festgelegt ist, **IsInConflict** die Nachrichtenklasse in der _SzMessageClass_ -Parameter übergeben wird, aufgelöst wird und gibt S_OK zurück, wenn das Formular eine eigene Konflikte nicht behandelt. **IsInConflict** gibt S_FALSE zurück, wenn das Formular eine eigene Konflikte behandelt. 
  
Ein Formular, das nicht über einen eigenen Konflikte handhabt muss mithilfe der [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) -Methode geöffnet und kann nicht wiederverwenden ein vorhandenen Form-Objekt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Clientanwendungen weisen in der Regel für den Umgang mit Konflikte, wenn die Anwendung von einer Nachricht in der nächsten oder der vorherigen Nachricht in einem Ordner verschieben. Wenn eine Nachricht liegt ein Konflikt, aber der Server Formular für diese Nachricht Konflikte behandeln kann, sollte die Clientanwendung seine üblichen Code für die Anzeige der nächsten oder der vorherigen Nachricht ausführen. Wenn der Formular Server Konflikte nicht verarbeiten kann, sollte die Clientanwendung fortgesetzt, als wäre es der Nachrichtenklasse der nächsten oder der vorherigen Nachricht nicht bekannt war. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md)
  
[Kanonische PidTagMessageStatus-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

