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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 93f264cc91118e40f7a2869d29e7e53d404ae381
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792520"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Die Indexnummer der Anlage zu löschen. Dies ist der Wert für die Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft.
    
 _ulUIParam_
  
> [in] Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, den, die diese Methode zeigt. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag ATTACH_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter mithilfe der MAPI-Fortschritt objektimplementierung wird die Statusanzeige angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag ATTACH_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die die Anzeige einer Benutzeroberfläche steuert. Das folgende Flag kann festgelegt werden:
    
ATTACH_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an, wie der-Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anlage wurde gelöscht.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::DeleteAttach** -Methode löscht eine Anlage in einer Nachricht. 
  
Eine gelöschte Anlage wird nicht endgültig gelöscht werden, bis die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Vor dem Aufruf von **DeleteAttach**, rufen Sie die **IUnknown** -Methode für die Anlage und die einzelnen seine Datenströme. 
  
Da eine Anlage löschen Anspruch sein kann, bietet **DeleteAttach** den Mechanismus, der eine Statusanzeige wird angezeigt. Sie können die Anzeige einer Statusanzeige anfordern, übergeben Sie einen Zeiger auf Ihre [IMAPIProgress: IUnknown](imapiprogressiunknown.md) Implementierung oder NULL, wenn Sie nicht über eine Implementierung verfügen. Sie müssen auch ein Fensterhandle in der _UlUIParam_ -Parameter und das Flag ATTACH_DIALOG im _UlFlags_ -Parameter angeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI (engl.) verwendet die **IMessage::DeleteAttach** -Methode, um die ausgewählte Anlage zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

