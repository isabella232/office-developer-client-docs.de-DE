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
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795424"
---
# <a name="rtfsync"></a>RTFSync

**Betrifft**: Outlook 
  
Stellt sicher, dass der Nachrichtentext Rich Text Format (RTF), die nur-Text-Version übereinstimmt. Es ist erforderlich, das diesen Funktionsaufruf vor dem Lesen der RTF-Version und nach dem Ändern der RTF-Version. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |RTF-fähigen Clientanwendungen und Nachricht speichern-Anbieter  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parameter

_lpMessage_
  
> [in] Zeiger auf die Nachricht aktualisiert werden.
    
_ulFlags_
  
> [in] Bitmaske aus Flags verwendet, um anzugeben, die RTF oder nur-Text-Version der Nachricht wurde geändert. Die folgenden Kennzeichen können festgelegt werden:
    
  - RTF_SYNC_BODY_CHANGED: Die Textversion der Nachricht wurde geändert.
      
  - RTF_SYNC_RTF_CHANGED: Die RTF-Version der Nachricht wurde geändert.
    
  Alle anderen Bits im _UlFlags_ -Parameter sind für die zukünftige Verwendung reserviert. 
    
_lpfMessageUpdated_
  
> [out] Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht. True, wenn es eine aktualisierte Meldung, sonst FALSE ist.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Wenn die Eigenschaft **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) fehlt oder ist FALSE, bevor Sie mit der RTF_SYNC_BODY_ Lesen der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) die **RTFSync** -Funktion aufgerufen werden soll -Kennzeichens geändert. 
  
Wenn das Flag STORE_RTF_OK in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft nicht festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED-Flag festlegen, nach dem Ändern der **PR_RTF_COMPRESSED**aufgerufen werden. 
  
Wenn **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) und **PR_RTF_COMPRESSED** geändert haben, sollte die **RTFSync** -Funktion mit beiden Flags aufgerufen werden. 
  
Wenn der Wert des Parameters _LpfMessageUpdated_ auf TRUE festgelegt ist, sollte die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode für die Nachricht aufgerufen werden. Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert werden. 
  
**RTFSync** können Nachricht-Anbieter die Eigenschaften **PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert halten. 
  
Weitere Informationen finden Sie unter [Unterstützung von RTF-Text für die Nachricht-Anbieter](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

