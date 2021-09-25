---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4ce90548a39ce33c795f68e513f3c178131b50b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591269"
---
# <a name="rtfsync"></a>RTFSync

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, dass der RTF-Nachrichtentext (Rich Text Format) mit der Nur-Text-Version übereinstimmt. Es ist erforderlich, diese Funktion vor dem Lesen der RTF-Version und nach dem Ändern der RTF-Version aufzurufen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |RTF-fähige Clientanwendungen und Nachrichtenspeicheranbieter  <br/> |
   
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
  
> [in] Bitmaske mit Flags, die verwendet werden, um anzugeben, dass sich die RTF- oder Nur-Text-Version der Nachricht geändert hat. Die folgenden Flags können festgelegt werden:
    
  - RTF_SYNC_BODY_CHANGED: Die Nur-Text-Version der Nachricht wurde geändert.
      
  - RTF_SYNC_RTF_CHANGED: Die RTF-Version der Nachricht wurde geändert.
    
  Alle anderen Bits im  _ulFlags-Parameter_ sind für die zukünftige Verwendung reserviert. 
    
_lpfMessageUpdated_
  
> [out] Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht vorhanden ist. TRUE, wenn eine aktualisierte Nachricht vorhanden ist, andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) -Eigenschaft fehlt oder FALSE ist, sollte vor dem Lesen der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft die **RTFSync-Funktion** aufgerufen werden, wobei das RTF_SYNC_BODY_CHANGED Flag festgelegt ist. 
  
Wenn das flag STORE_RTF_OK nicht in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED Flag aufgerufen werden, nachdem **PR_RTF_COMPRESSED** geändert wurde. 
  
Wenn sowohl **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) als **auch PR_RTF_COMPRESSED** geändert wurden, sollte die **RTFSync-Funktion** mit beiden festgelegten Flags aufgerufen werden. 
  
Wenn der Wert des  _lpfMessageUpdated-Parameters_ auf TRUE festgelegt ist, sollte die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die Nachricht aufgerufen werden. Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert. 
  
Nachrichtenspeicheranbieter können **RTFSync** verwenden, um die **eigenschaften PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert zu halten. 
  
Weitere Informationen finden Sie unter [Unterstützen von RTF-Text für Nachrichten Store Anbieter](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

