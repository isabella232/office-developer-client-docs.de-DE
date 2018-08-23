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
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592514"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

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

