---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412527"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Formular an.
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Formulars.
    
 _lpMsgStore_
  
> [in] Ein Zeiger auf den Nachrichtenspeicher, der den Ordner enthält, auf den der  _lpParentFolder-Parameter_ verweist. 
    
 _lpParentFolder_
  
> [in] Ein Zeiger auf den Ordner, in dem die dem  _ulMessageToken-Parameter zugeordnete_ Nachricht erstellt wurde. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf die im Formular angezeigte Nachricht verwendet werden soll. Der  _lpInterface-Parameter_ muss NULL oder IID_IMessage. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle [IMessage](imessageimapiprop.md)verwendet wird. 
    
 _ulMessageToken_
  
> [in] Das Token, das der nachricht zugeordnet ist, die im Formular angezeigt werden soll. Der _ulMessageToken-Parameter_ muss auf den Inhalt des _lpulMessageToken-Parameters_ aus dem vorherigen Aufruf von [IMAPISession::P repareForm festgelegt werden.](imapisession-prepareform.md)
    
 _lpMessageSent_
  
> [in] Reserviert; muss NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie und ob die Nachricht gespeichert wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_NEW_MESSAGE 
  
> Die Nachricht wurde nie gespeichert (d. h., die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) wurde nie aufgerufen). 
    
MAPI_POST_MESSAGE 
  
> Die Nachricht sollte im übergeordneten Ordner gespeichert werden. Die Nachricht wird nicht zum Senden verarbeitet, sondern stattdessen im Ordner bereitgestellt. Wenn dieses Flag nicht festgelegt ist, wird die Nachricht in den Posteingang kopiert und zum Senden verarbeitet. 
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske mit **Flags,** die aus der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft der Nachricht kopiert wurden, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. Die Flags enthalten Informationen zum Status der Nachricht. 
    
 _ulMessageFlags_
  
> [in] Eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. Diese Flags enthalten weitere Informationen zum Status der Nachricht. 
    
 _ulAccess_
  
> [in] Ein Flag, das die Berechtigungsstufe für die Nachricht angibt, die im Formular angezeigt wird. Diese Informationen werden aus der **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) der Nachricht kopiert, die dem Token im  _ulMessageToken-Parameter zugeordnet_ ist. 
    
 _lpszMessageClass_
  
> [in] Ein Zeiger auf die Nachrichtenklasse der Nachricht, die im Formular angezeigt wird, der aus der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der Nachricht kopiert wird, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich angezeigt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::ShowForm-Methode** zeigt ein Nachrichtenformular an, das von der **IMAPISession::P repareForm-Methode vorbereitet** wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie sollten nur einen einzigen Verweis auf die Nachricht haben, die im _lpMessage-Parameter_ der **PrepareForm-Methode** übergeben wird. 
  
Beachten Sie, dass Formularimplementierung andere Fehlerwerte als die von MAPI dokumentierten zurückgeben kann. Wenn Sie diese Fehlerwerte verwenden können, um die Fehlerbedingung genauer zu bestimmen, tun Sie dies. Behandeln Sie andernfalls diese Fehler so, wie Sie MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPISession::ShowForm-Methode** zusammen mit der **PrepareForm-Methode,** um eine Nachricht in einem modalen Formular zu zeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

