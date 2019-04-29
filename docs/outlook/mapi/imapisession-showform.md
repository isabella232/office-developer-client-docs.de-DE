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
  
> in Ein Handle für das übergeordnete Fenster des Formulars.
    
 _lpMsgStore_
  
> in Ein Zeiger auf den Nachrichtenspeicher, der den Ordner enthält, auf den durch den _lpParentFolder_ -Parameter verwiesen wird. 
    
 _lpParentFolder_
  
> in Ein Zeiger auf den Ordner, in dem die dem _ulMessageToken_ -Parameter zugeordnete Nachricht erstellt wurde. 
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf die im Formular angezeigte Nachricht verwendet werden soll. Der _lpInterface_ -Parameter muss NULL oder IID_IMessage sein. Übergeben von NULL-Ergebnissen in der Standardschnittstelle, [IMessage](imessageimapiprop.md), wird verwendet. 
    
 _ulMessageToken_
  
> in Das Token, das der im Formular anzuzeigenden Nachricht zugeordnet ist. Der _ulMessageToken_ -Parameter muss auf den Inhalt des paraMeters _lpulMessageToken_ des vorherigen Aufrufs an IMAPISession festgelegt werden [::P repareform](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> in Reserviert muss NULL sein. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die Steuern, wie und ob die Nachricht gespeichert wird. Die folgenden Flags können festgelegt werden:
    
MAPI_NEW_MESSAGE 
  
> Die Nachricht wurde nie gespeichert (das heißt, Ihre [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode wurde nie aufgerufen). 
    
MAPI_POST_MESSAGE 
  
> Die Nachricht sollte im übergeordneten Ordner gespeichert werden. Die Nachricht wird nicht zum Senden verarbeitet, sondern stattdessen in den Ordner geschrieben. Wenn dieses Flag nicht festgelegt ist, wird die Nachricht in den Postausgang kopiert und zum Senden verarbeitet. 
    
 _ulMessageStatus_
  
> in Eine Bitmaske von Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der dem Token im _ulMessageToken_ -Parameter zugeordneten Nachricht kopiert werden. Die Flags enthalten Informationen zum Status der Nachricht. 
    
 _ulMessageFlags_
  
> in Eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der dem Token im _ulMessageToken_ -Parameter zugeordneten Nachricht kopiert werden. Diese Kennzeichnungen enthalten weitere Informationen zum Status der Nachricht. 
    
 _ulAccess_
  
> in Ein Flag, das die Berechtigungsstufe für die im Formular angezeigte Nachricht angibt. Diese Informationen werden aus der **PR_ACCESS** ([pidtagaccess (](pidtagaccess-canonical-property.md))-Eigenschaft der Nachricht kopiert, die dem Token im _ulMessageToken_ -Parameter zugeordnet ist. 
    
 _lpszMessageClass_
  
> in Ein Zeiger auf die Nachrichtenklasse der Nachricht, die im Formular angezeigt wird, kopiert aus der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der Nachricht, die dem Token im _ulMessageToken_ -Parameter zugeordnet ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde erfolgreich angezeigt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: ShowForm** -Methode zeigt ein Nachrichtenformular an, das von der **IMAPISession::P repareform** -Methode vorbereitet wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie sollten nur einen einzigen Verweis auf die Nachricht haben, die im _lpMessage_ -Parameter der **PrepareForm** -Methode übergeben wird. 
  
Beachten Sie, dass Formular Implementierungen andere Fehlerwerte als die unter MAPI zurückgeben können. Wenn Sie diese Fehlerwerte verwenden können, um eine genauere Ermittlung der Fehlerbedingung vorzunehmen, tun Sie dies. Andernfalls behandeln Sie diese Fehler wie MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPISession:: ShowForm** -Methode zusammen mit der **PrepareForm** -Methode, um eine Nachricht in einem modalen Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

