---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405898"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine Anlage. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameter

 _ulAttachmentNum_
  
> [in] Indexnummer der zu öffnenden Anlage, wie in der **eigenschaft PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) der Anlage gespeichert. Diese Indexnummer identifiziert die Anlage in der Nachricht eindeutig und ist nur im Kontext der Nachricht gültig.
    
 _lpInterface_
  
> [in] Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf die Anlage verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle der Anlage oder **IAttach** zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuert, wie die Anlage geöffnet wird. Die folgenden Kennzeichen können festgelegt werden: 
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass die Anlage mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte die Anlage mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützten Zugriff verfügt, sollte die Anlage mit schreibgeschützten Zugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openAttach** die erfolgreiche Rückgabe, möglicherweise bevor die Anlage vollständig für den aufrufenden Client verfügbar ist. Wenn die Anlage nicht verfügbar ist, kann ein nachfolgender Aufruf der Anlage zu einem Fehler führen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Anlagen werden standardmäßig mit schreibgeschützten Zugriffen geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
 _lppAttach_
  
> [out] Zeiger auf einen Zeiger auf die geöffnete Anlage.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich geöffnet.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::OpenAttach-Methode** öffnet die Anlage einer Nachricht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Öffnen einer Anlage müssen Sie zugriff auf die Anlagennummer oder **die PR_ATTACH_NUM** haben. Rufen [Sie IMessage::GetAttachmentTable](imessage-getattachmenttable.md) auf, um die Anlagentabelle der Nachricht abzurufen und die Zeile zu suchen, die die zu öffnende Anlage darstellt. Weitere [Informationen finden Sie unter Öffnen](opening-an-attachment.md) einer Anlage. 
  
Versuchen Sie nicht, eine Anlage mehrmals zu öffnen. Die Ergebnisse sind nicht definiert und hängen vom Nachrichtenspeicheranbieter ab.
  
Sie können anfordern, dass die Anlage im Lese-/Schreibmodus anstelle des standardmäßigen schreibgeschützten Modus geöffnet wird. Ob die Anlage tatsächlich im Lese-/Schreibmodus geöffnet wird, liegt jedoch beim Nachrichtenspeicheranbieter. Sie können entweder versuchen, die Anlage zu ändern, einen möglichen Fehler zu behandeln, oder die Zugriffsebene überprüfen, die gewährt wurde, indem Sie die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft der Anlage abrufen, sofern diese verfügbar ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Wird verwendet, um  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI verwendet die **IMessage::OpenAttach-Methode,** um Anlagenobjekte zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

