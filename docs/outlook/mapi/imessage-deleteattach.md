---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430707"
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
  
> in Index Nummer der zu löschenden Anlage. Dies ist der Wert für die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage.
    
 _ulUIParam_
  
> in Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das ATTACH_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpProgress_
  
> in Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das ATTACH_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _ulFlags_
  
> in Bitmaske von Flags, die die Anzeige einer Benutzeroberfläche steuert. Das folgende Flag kann festgelegt werden:
    
ATTACH_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich gelöscht.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::D eleteattach** -Methode löscht eine Anlage aus einer Nachricht. 
  
Eine gelöschte Anlage wird erst dann endgültig gelöscht, wenn die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie vor dem Aufrufen von **DeleteAttach**die **IUnknown:: Release** -Methode für die Anlage und alle zugehörigen Streams auf. 
  
Da das Löschen einer Anlage ein langwieriger Prozess sein kann, stellt **DeleteAttach** den Mechanismus bereit, mit dem eine Statusanzeige angezeigt wird. Sie können die Anzeige einer Statusanzeige anfordern, indem Sie einen Zeiger an Ihre [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Implementierung oder NULL übergeben, wenn Sie keine Implementierung haben. Sie müssen auch ein Fensterhandle im Parameter _ulUIParam_ und das ATTACH_DIALOG-Flag im _ulFlags_ -Parameter angeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp  <br/> |CAttachmentsDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMessage::D eleteattach** -Methode, um die ausgewählte Anlage zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

