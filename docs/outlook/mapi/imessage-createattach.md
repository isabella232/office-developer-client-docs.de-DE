---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572089"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine neue Anlage.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Zeiger auf die Schnittstelle-ID (IID), das die Schnittstelle für verwendet werden, um Zugriff auf die Nachricht darstellt. Bei Übergabe von NULL führt der Nachricht Standardschnittstelle oder **IMessage**, zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die steuert, wie das Attachment-Objekt erstellt wird. Das folgende Flag kann festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **CreateAttach** erfolgreich, möglicherweise beendet, bevor die Anlage vollständig an den aufrufenden Client verfügbar ist. Wenn die Anlage nicht möglich ist, kann nachfolgende aufrufen es ein Laufzeitfehler. 
    
 _lpulAttachmentNum_
  
> [out] Zeiger auf eine Indexnummer, die das neu erstellte Attachment-Objekt identifiziert. Diese Nummer gilt nur, wenn die Nachricht geöffnet wird und die Grundlage für die Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft bildet.
    
 _lppAttach_
  
> [out] Zeiger auf einen Zeiger auf das Objekt Anlage öffnen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anlage wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::CreateAttach** -Methode erstellt eine neue Anlage in einer Nachricht. Die neue Anlage und Eigenschaften, die für sie festgelegt sind sind nicht verfügbar, bis ein Client die Anlage [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode und die Nachricht **IMAPIProp::SaveChanges** -Methode aufgerufen wurde. 
  
Die Anlage Anzahl auf den _LpulAttachmentNum_ ist eindeutig und nur im Kontext der Nachricht gültig. D. h., können zwei Anlagen in zwei verschiedene Nachrichten die gleiche Anzahl haben, während zwei Anlagen in die gleiche Nachricht ist nicht möglich. 
  
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)

