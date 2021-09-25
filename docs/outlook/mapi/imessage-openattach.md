---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fa38f1123ab3bd3c13dcad830680e16d5e6d33c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584332"
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
  
> [in] Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf die Anlage verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle der Anlage oder **IAttach** zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuert, wie die Anlage geöffnet wird. Die folgenden Flags können festgelegt werden: 
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass die Anlage mit den für den Benutzer maximal zulässigen Netzwerkberechtigungen und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte die Anlage mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützten Zugriff verfügt, sollte die Anlage mit schreibgeschütztem Zugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenAttach** die erfolgreiche Rückgabe, möglicherweise bevor die Anlage für den aufrufenden Client vollständig verfügbar ist. Wenn die Anlage nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Anlagen werden standardmäßig mit schreibgeschütztem Zugriff geöffnet, und Clients sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
 _lppAttach_
  
> [out] Zeiger auf einen Zeiger auf die geöffnete Anlage.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich geöffnet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::OpenAttach-Methode** öffnet die Anlage einer Nachricht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Anlage zu öffnen, müssen Sie Zugriff auf die Anlagennummer oder **PR_ATTACH_NUM** Eigenschaft haben. Rufen Sie [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) auf, um die Anlagentabelle der Nachricht abzurufen und die Zeile zu suchen, die die zu öffnende Anlage darstellt. Weitere Informationen finden Sie [unter "Öffnen einer Anlage".](opening-an-attachment.md) 
  
Versuchen Sie nicht, eine Anlage mehrmals zu öffnen. die Ergebnisse sind nicht definiert und vom Nachrichtenspeicheranbieter abhängig.
  
Sie können anfordern, dass die Anlage im Lese-/Schreibmodus anstelle des standardmäßigen schreibgeschützten Modus geöffnet wird. Ob die Anlage tatsächlich im Lese-/Schreibmodus geöffnet wird, hängt jedoch vom Nachrichtenspeicheranbieter ab. Sie können entweder versuchen, die Anlage zu ändern, die Behandlung möglicher Fehler vorzubereiten oder die Zugriffsebene zu überprüfen, die gewährt wurde, indem Sie die **Eigenschaft PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) der Anlage abrufen, falls verfügbar. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Verwendet für  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI verwendet die **IMessage::OpenAttach-Methode** zum Öffnen von Anlagenobjekten,  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

