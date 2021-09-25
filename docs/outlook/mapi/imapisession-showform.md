---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fbe1087c2d7036aeb7b02b019cf6bec84e43d139
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561530"
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
  
> [in] Ein Handle für das übergeordnete Fenster des Formulars.
    
 _lpMsgStore_
  
> [in] Ein Zeiger auf den Nachrichtenspeicher, der den Ordner enthält, auf den der  _parameter lpParentFolder_ verweist. 
    
 _lpParentFolder_
  
> [in] Ein Zeiger auf den Ordner, in dem die dem  _ulMessageToken-Parameter_ zugeordnete Nachricht erstellt wurde. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf die im Formular angezeigte Nachricht verwendet werden soll. Der  _lpInterface-Parameter_ muss NULL oder IID_IMessage sein. Wenn NULL übergeben wird, wird die Standardschnittstelle [IMessage](imessageimapiprop.md)verwendet. 
    
 _ulMessageToken_
  
> [in] Das Token, das der im Formular anzuzeigenden Nachricht zugeordnet ist. Der  _ulMessageToken_ -Parameter muss auf den Inhalt des  _lpulMessageToken_ -Parameters aus dem vorherigen Aufruf von [IMAPISession::P repareForm](imapisession-prepareform.md)festgelegt werden.
    
 _lpMessageSent_
  
> [in] Reserviert; muss NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie und ob die Nachricht gespeichert wird. Die folgenden Flags können festgelegt werden:
    
MAPI_NEW_MESSAGE 
  
> Die Nachricht wurde noch nie gespeichert (d. a. ihre [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) wurde noch nie aufgerufen). 
    
MAPI_POST_MESSAGE 
  
> Die Nachricht sollte im übergeordneten Ordner gespeichert werden. Die Nachricht wird nicht zum Senden verarbeitet, sondern stattdessen in den Ordner gestellt. Wenn dieses Kennzeichen nicht festgelegt ist, wird die Nachricht in den Postausgang kopiert und zum Senden verarbeitet. 
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske von Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft der Nachricht kopiert wurde, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. Die Flags enthalten Informationen zum Status der Nachricht. 
    
 _ulMessageFlags_
  
> [in] Eine Bitmaske von Flags, die aus der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht kopiert wurde, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. Diese Flags enthalten weitere Informationen zum Status der Nachricht. 
    
 _ulAccess_
  
> [in] Ein Kennzeichen, das die Berechtigungsstufe für die im Formular angezeigte Nachricht angibt. Diese Informationen werden aus der **eigenschaft PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) der Nachricht kopiert, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. 
    
 _lpszMessageClass_
  
> [in] Ein Zeiger auf die Nachrichtenklasse der Nachricht, die im Formular angezeigt wird, kopiert aus der **eigenschaft PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Nachricht, die dem Token im  _ulMessageToken-Parameter_ zugeordnet ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich angezeigt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::ShowForm-Methode** zeigt ein Meldungsformular an, das von der **IMAPISession::P repareForm-Methode** vorbereitet wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie sollten nur einen einzelnen Verweis auf die Nachricht haben, die im _lpMessage-Parameter_ der **PrepareForm-Methode** übergeben wird. 
  
Beachten Sie, dass Formularimplementierungen andere Fehlerwerte als die von MAPI dokumentierten zurückgeben können. Wenn Sie diese Fehlerwerte verwenden können, um die Fehlerbedingung genauer zu bestimmen, tun Sie dies. Behandeln Sie diese Fehler andernfalls so, wie Sie MAPI_E_CALL_FAILED behandeln würden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPISession::ShowForm-Methode** zusammen mit der **PrepareForm-Methode,** um eine Nachricht in einem modalen Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

