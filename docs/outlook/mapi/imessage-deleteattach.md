---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 76b5be70415588e56b4743489faf5b73050a34fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620793"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht eine Anlage.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulAttachmentNum_
  
> [in] Indexnummer der zu löschenden Anlage. Dies ist der Wert für die **eigenschaft PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) der Anlage.
    
 _ulUIParam_
  
> [in] Behandeln Sie das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das ATTACH_DIALOG-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das ATTACH_DIALOG Flag in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die die Anzeige einer Benutzeroberfläche steuern. Das folgende Kennzeichen kann festgelegt werden:
    
ATTACH_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich gelöscht.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::D eleteAttach-Methode** löscht eine Anlage aus einer Nachricht heraus. 
  
Eine gelöschte Anlage wird erst endgültig gelöscht, wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie vor dem Aufrufen von **DeleteAttach** die **IUnknown::Release-Methode** für die Anlage und jeden ihrer Datenströme auf. 
  
Da das Löschen einer Anlage ein langwieriger Prozess sein kann, stellt **DeleteAttach** den Mechanismus bereit, der eine Statusanzeige anzeigt. Sie können die Anzeige einer Statusanzeige anfordern, indem Sie einen Zeiger an Ihre [IMAPIProgress übergeben: IUnknown-Implementierung](imapiprogressiunknown.md) oder NULL, wenn Sie keine Implementierung haben. Sie müssen auch ein Fensterhandle im  _ulUIParam-Parameter_ und das ATTACH_DIALOG-Flag im  _ulFlags-Parameter_ angeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMessage::D eleteAttach-Methode,** um die ausgewählte Anlage zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

