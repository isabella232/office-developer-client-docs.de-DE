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
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349252"
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
  
> in Index Nummer der zu öffnenden Anlage, wie in der **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage gespeichert. Diese Indexnummer identifiziert die Anlage in der Nachricht eindeutig und ist nur im Kontext der Nachricht gültig.
    
 _lpInterface_
  
> in Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die Anlage verwendet werden soll. Das übergeben von NULL-Ergebnissen in der Standardschnittstelle oder **IAttach**, die zurückgegeben wird. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die Steuern, wie die Anlage geöffnet wird. Die folgenden Flags können festgelegt werden: 
    
MAPI_BEST_ACCESS 
  
> Fordert, dass die Anlage mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Zugriff auf Clientanwendungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, muss die Anlage mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützten Zugriff hat, sollte die Anlage mit Lesezugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** das erfolgreiche zurückgeben von openattach, möglicherweise vor der vollständigen Verfügbarkeit der Anlage für den aufrufenden Client. Wenn die Anlage nicht verfügbar ist, kann durch einen nachfolgenden Aufruf eine Fehlermeldung verursacht werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Anlagen werden standardmäßig mit schreibgeschütztem Zugriff geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde. 
    
 _lppAttach_
  
> Out Zeiger auf einen Zeiger auf die offene Anlage.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich geöffnet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage:: openattach** -Methode öffnet die Anlage einer Nachricht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Öffnen einer Anlage benötigen Sie Zugriff auf die Anlagennummer oder die **PR_ATTACH_NUM** -Eigenschaft. Rufen Sie [IMessage::](imessage-getattachmenttable.md) getattachmentable auf, um die Attachment-Tabelle der Nachricht abzurufen und die Zeile zu suchen, die die zu öffnende Anlage darstellt. Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md) . 
  
Versuchen Sie nicht, eine Anlage mehrmals zu öffnen. die Ergebnisse sind nicht definiert und vom Nachrichtenspeicher Anbieter abhängig.
  
Anstelle des Standard schreibgeschützten Modus können Sie anfordern, dass die Anlage im Lese-/Schreibzugriff-Modus geöffnet wird. Ob die Anlage tatsächlich im Lese-/Schreibzugriff-Modus geöffnet wird, liegt jedoch beim Nachrichtenspeicher Anbieter. Sie können entweder versuchen, die Anlage zu ändern, die Behandlung möglicher Ausfälle vorzubereiten oder die Zugriffsebene zu überprüfen, die durch Abrufen der **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft der Anlage gewährt wurde, falls diese verfügbar ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp  <br/> |CAttachmentsDlg:: OpenItemProp  <br/> |MFCMAPI verwendet die **IMessage:: openattach** -Methode zum Öffnen von Attachment-Objekten,  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

