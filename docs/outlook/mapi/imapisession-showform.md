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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792333"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Ein Zeiger auf den Nachrichtenspeicher mit dem Ordner, auf den durch den Parameter _LpParentFolder_ verwiesen wird. 
    
 _lpParentFolder_
  
> [in] Ein Zeiger auf den Ordner, in dem die Nachricht mit dem Parameter _UlMessageToken_ verbundenen erstellt wurde. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, die verwendet werden, um die Nachricht zuzugreifen, die in dem Formular angezeigt wird. Der Parameter _LpInterface_ muss NULL oder IID_IMessage sein. Bei Übergabe von NULL führt die standard-Schnittstelle, [IMessage](imessageimapiprop.md), verwendet wird. 
    
 _ulMessageToken_
  
> [in] Das Token, das die Nachricht im Formular anzuzeigende zugeordnet ist. Der Parameter _UlMessageToken_ muss auf den Inhalt des Parameters _LpulMessageToken_ aus dem vorherigen Aufruf von [IMAPISession::PrepareForm](imapisession-prepareform.md)festgelegt sein.
    
 _lpMessageSent_
  
> [in] Reserviert. NULL muss sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, ob und wie die Nachricht gespeichert wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_NEW_MESSAGE 
  
> Die Nachricht wurde noch nie gespeichert wurde (d. h., seine [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode noch nie aufgerufen wurde). 
    
MAPI_POST_MESSAGE 
  
> Die Nachricht sollte in seinem übergeordneten Ordner gespeichert werden. Die Nachricht wird nicht für das Senden von verarbeitet, aber es wird in den Ordner bereitgestellt. Wenn dieses Flag nicht festgelegt ist, wird die Nachricht im Ordner Postausgang kopiert und für das Senden von verarbeitet wird. 
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske aus Flags, die von der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert. Die Kennzeichen liefern Informationen zu den Status der Nachricht. 
    
 _ulMessageFlags_
  
> [in] Eine Bitmaske aus Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert. Diese Flags bieten weitere Informationen zum Status der Nachricht. 
    
 _ulAccess_
  
> [in] Ein Flag, das die Berechtigungsstufe für die Nachricht gibt an, die im Formular angezeigt wird. Diese Informationen werden aus der Eigenschaft **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert. 
    
 _lpszMessageClass_
  
> [in] Ein Zeiger auf die Nachrichtenklasse der Nachricht angezeigt wird, klicken Sie im Formular aus der Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Nachricht dem Token im Parameter _UlMessageToken_ zugeordneten kopiert. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular wurde erfolgreich angezeigt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::ShowForm** -Methode zeigt ein Formular für Nachrichten, die von der **IMAPISession::PrepareForm** -Methode vorbereitet wurden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie sollten nur einen Verweis auf die Nachricht im _LpMessage_ -Parameter der **PrepareForm** -Methode übergeben haben. 
  
Beachten Sie, dass das Formular Implementierungen Fehlerwerte als derjenigen, die von MAPI dokumentiert zurückgeben können. Wenn Sie diese Fehlerwerte verwenden können, um eine genauere Bestimmung des Fehlers, dazu. Anderenfalls behandeln Sie diese Fehler wie MAPI_E_CALL_FAILED behandeln. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::ShowForm** -Methode, zusammen mit der **PrepareForm** -Methode, um eine Nachricht in ein modales Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

