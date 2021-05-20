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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436209"
---
# <a name="rtfsync"></a>RTFSync

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, dass der Rich Text Format (RTF)-Nachrichtentext der Nur-Text-Version entspricht. Sie müssen diese Funktion aufrufen, bevor Sie die RTF-Version lesen und die RTF-Version ändern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |RTF-bewusste Clientanwendungen und Nachrichtenspeicheranbieter  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parameter

_lpMessage_
  
> [in] Zeiger auf die zu aktualisierende Nachricht.
    
_ulFlags_
  
> [in] Bitmaske von Flags, die verwendet werden, um die RTF- oder Nur-Text-Version der Nachricht anzugeben, hat sich geändert. Die folgenden Kennzeichen können festgelegt werden:
    
  - RTF_SYNC_BODY_CHANGED: Die Nur-Text-Version der Nachricht wurde geändert.
      
  - RTF_SYNC_RTF_CHANGED: Die RTF-Version der Nachricht wurde geändert.
    
  Alle anderen Bits im  _ulFlags-Parameter_ sind für die zukünftige Verwendung reserviert. 
    
_lpfMessageUpdated_
  
> [out] Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht vor liegt. TRUE, wenn eine aktualisierte Nachricht vor liegt, andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) -Eigenschaft fehlt oder FALSE ist, vor dem Lesen der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft sollte die **RTFSync** -Funktion mit dem flag set RTF_SYNC_BODY_CHANGED aufgerufen werden. 
  
Wenn das STORE_RTF_OK in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft nicht festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED-Flag nach dem Ändern von **PR_RTF_COMPRESSED aufgerufen werden.** 
  
Wenn sowohl **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) als **auch** PR_RTF_COMPRESSED geändert wurden, sollte die **RTFSync-Funktion** mit beiden Flags aufgerufen werden. 
  
Wenn der Wert des  _Parameters lpfMessageUpdated_ auf TRUE festgelegt ist, sollte die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die Nachricht aufgerufen werden. Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert. 
  
Nachrichtenspeicheranbieter können **RTFSync** verwenden, um die eigenschaften **PR_BODY** und **PR_RTF_COMPRESSED** zu synchronisieren. 
  
Weitere Informationen finden Sie unter [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

