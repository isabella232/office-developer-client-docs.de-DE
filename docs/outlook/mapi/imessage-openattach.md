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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792515"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Die Indexnummer der Anlage für das Öffnen, wie in der Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft gespeichert. Diese Indexnummer eindeutig identifiziert die Anlage in der Nachricht und ist nur im Kontext der Nachricht gültig.
    
 _lpInterface_
  
> [in] Zeiger auf die Schnittstelle-ID (IID), das die Schnittstelle für den Zugriff auf die Anlage verwendet werden darstellt. Bei Übergabe von NULL führt der Anlage Standardschnittstelle oder **IAttach**, zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die steuert, wie die Anlage geöffnet wird. Die folgenden Kennzeichen können festgelegt werden: 
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass die Anlage mit den maximale Netzwerkberechtigungen für den Benutzer und die maximale Anwendung Clientzugriff zulässig geöffnet werden. Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Attachment-Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client schreibgeschützten Zugriff hat, sollte die Anlage mit schreibgeschützten Zugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenAttach** erfolgreich, möglicherweise beendet, bevor die Anlage vollständig an den aufrufenden Client verfügbar ist. Wenn die Anlage nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Anlagen mit schreibgeschützten Zugriff geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lppAttach_
  
> [out] Zeiger auf einen Zeiger auf die Anlage öffnen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anlage wurde erfolgreich geöffnet.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::OpenAttach** -Methode wird ein e-Mail-Anlage geöffnet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Anlage zu öffnen, benötigen Sie Zugriff auf die Anlage Nummer oder **PR_ATTACH_NUM** -Eigenschaft. Rufen Sie [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) zum Abrufen der Nachricht Anlagentabelle, und suchen Sie die Zeile, die die Anlage geöffnet werden soll. Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md) . 
  
Versuchen Sie nicht, öffnen Sie eine Anlage mehrmals; die Ergebnisse sind nicht definiert und die Nachricht Speicheranbieter abhängig.
  
Sie können anfordern, dass die Anlage im Lese-/Schreibmodus anstelle der Standardmodus schreibgeschützt geöffnet werden. Bis zu der Nachricht Informationsdienst jedoch ist, ob die Anlage tatsächlich im Lese-/Schreibmodus geöffnet werden. Sie können entweder Versuch, ändern die Anlage Vorbereitung auf mögliche Ausfälle behandeln oder Überprüfen Sie die Zugriffsebene, die durch die Anlage **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft, abrufen, falls verfügbar erteilt wurde. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp verwendet, um  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI (engl.) wird die **IMessage::OpenAttach** -Methode verwendet, um Attachment-Objekte zu öffnen,  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

