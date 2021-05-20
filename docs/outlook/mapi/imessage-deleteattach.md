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
  
> [in] Indexnummer der zu löschende Anlage. Dies ist der Wert für die **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft der Anlage.
    
 _ulUIParam_
  
> [in] Behandeln Sie das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das ATTACH_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, ATTACH_DIALOG in _ulFlags festgelegt ist._
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die die Anzeige einer Benutzeroberfläche steuert. Das folgende Flag kann festgelegt werden:
    
ATTACH_DIALOG 
  
> Fordert die Anzeige eines Statusindikators an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich gelöscht.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::D eleteAttach-Methode** löscht eine Anlage innerhalb einer Nachricht. 
  
Eine gelöschte Anlage wird erst endgültig gelöscht, wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **vor dem Aufrufen von DeleteAttach** die **IUnknown::Release-Methode** für die Anlage und jeden ihrer Datenströme auf. 
  
Da das Löschen einer Anlage ein langwieriger Prozess sein kann, bietet **DeleteAttach** den Mechanismus, der eine Statusanzeige anzeigt. Sie können die Anzeige eines Statusindikators anfordern, indem Sie einen Zeiger an Ihre [IMAPIProgress : IUnknown-Implementierung](imapiprogressiunknown.md) oder NULL übergeben, wenn Sie über keine Implementierung verfügen. Sie müssen auch ein Fensterhandle im  _ulUIParam-Parameter_ und das ATTACH_DIALOG im  _ulFlags-Parameter_ angeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMessage::D eleteAttach-Methode,** um die ausgewählte Anlage zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

