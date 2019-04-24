---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316479"
---
# <a name="rtfsync"></a>RTFSync

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, dass der RTF-Nachrichten Text (Rich Text Format) mit der nur-Text-Version übereinstimmt. Diese Funktion muss aufgerufen werden, bevor die RTF-Version gelesen und die RTF-Version geändert wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |RTF-fähige Clientanwendungen und Nachrichtenspeicher Anbieter  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parameter

_lpMessage_
  
> in Zeiger auf die zu aktualisierende Nachricht.
    
_ulFlags_
  
> in Bitmaske der Flags, mit denen die RTF-oder nur-Text-Version der Nachricht angegeben wurde. Die folgenden Flags können festgelegt werden:
    
  - RTF_SYNC_BODY_CHANGED: die nur-Text-Version der Nachricht wurde geändert.
      
  - RTF_SYNC_RTF_CHANGED: die RTF-Version der Nachricht wurde geändert.
    
  Alle anderen Bits im _ulFlags_ -Parameter sind für die zukünftige Verwendung reserviert. 
    
_lpfMessageUpdated_
  
> Out Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht vorhanden ist. TRUE, wenn eine aktualisierte Nachricht vorhanden ist, andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Wenn die **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))-Eigenschaft fehlt oder false ist, bevor Sie die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft lesen, sollte die **RTFSync** -Funktion mit dem RTF_SYNC_BODY_ aufgerufen werden. GEÄNDERTer Flagsatz. 
  
Wenn das STORE_RTF_OK-Flag nicht in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED-Flag nach dem Ändern von **PR_RTF_COMPRESSED**aufgerufen werden. 
  
Wenn sowohl **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) als auch **PR_RTF_COMPRESSED** geändert wurden, sollte die **RTFSync** -Funktion mit beiden Flags festgelegt aufgerufen werden. 
  
Wenn der Wert des _lpfMessageUpdated_ -Parameters auf true festgelegt ist, sollte die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode für die Nachricht aufgerufen werden. Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert. 
  
Nachrichtenspeicher Anbieter können **RTFSync** verwenden, um die **PR_BODY** -und **PR_RTF_COMPRESSED** -Eigenschaften zu synchronisieren. 
  
Weitere Informationen finden Sie unter [Unterstützung von RTF-Text für Nachrichtenspeicher Anbieter](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

