---
title: Erstellen des Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bd840c7bef0607db37c6477bd8f4a7320a8188c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574755"
---
# <a name="creating-message-text"></a>Erstellen des Nachrichtentexts

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Obwohl einige Nachrichten von nicht mehr als eine Empfängerliste und der Betreffzeile den Inhalt der meisten Nachrichten, insbesondere IPM vorgenommen werden. Beachten Sie Nachrichten, die Text enthält. Nachricht Text kann einfache oder formatiert sein und in drei Eigenschaften gespeichert ist: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Ihr Client nur-Text-basierte ist, legen Sie **PR\_BODY**. Wenn Sie formatierten Text im Rich Text Format (RTF) unterstützen, legen Sie nur **PR_RTF_COMPRESSED** oder beide **PR_RTF_COMPRESSED** und **PR\_BODY**je nach Anbieter die Nachricht, die Sie verwenden. Wenn ein Client RTF-Unterstützung einen RTF-fähigen Nachrichtenspeicher verwendet wird, stellt er nur **PR_RTF_COMPRESSED** . Wenn ein Client RTF-Unterstützung ein RTF nicht unterstützen Nachrichtenspeichers verwendet wird, stellt er beide Eigenschaften. Wenn der Client HTML unterstützt, festlegen Sie die **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** -Eigenschaft. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Bestimmen Sie, ob Ihre Nachrichtenspeicher Rich-Text-Format unterstützt
  
1. Rufen Sie den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Überprüfen Sie das STORE_RTF_OK Bit. Wenn STORE_RTF_OK festgelegt ist, unterstützt der Nachricht Informationsdienst RTF-Text. Wenn sie nicht festgelegt ist, unterstützt der Informationsdienst Nachricht als nur-Text.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Bestimmen Sie, ob Ihre Nachrichtenspeicher HTML unterstützt
  
1. Rufen Sie den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der **PR_STORE_SUPPORT_MASK** -Eigenschaft. 
    
2. Überprüfen Sie das STORE_HTML_OK Bit. Wenn STORE_HTML_OK festgelegt ist, unterstützt der Nachricht Informationsdienst HTML-Text. 
    
## <a name="set-prrtfcompressed"></a>Legen Sie PR\_RTF_COMPRESSED
  
1. Rufen Sie die Nachricht [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_RTF_COMPRESSED** -Eigenschaft, IID_IStream als Schnittstellenbezeichner angeben und Festlegen des Flags MAPI_CREATE ist. 
    
2. Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion, die das Flag STORE_UNCOMPRESSED_RTF übergeben, wenn das STORE_UNCOMPRESSED_RTF Bit in der Nachrichtenspeicher **PR_STORE_SUPPORT_MASK** -Eigenschaft festgelegt wird. 
    
3. Geben Sie den ursprünglichen Stream durch Aufrufen seiner ** IUnknown ** Methode. 
    
4. Rufen Sie entweder ** IStream::Write ** oder **:: CopyTo** den Nachrichtentext an den Stream Schreiben von **WrapCompressedRTFStream**zurückgegeben.
    
5. Rufen Sie die **Commit** und **Release** -Methoden für das Stream-Objekt aus der **OpenProperty** -Methode zurückgegeben. 
    
Zu diesem Zeitpunkt, wenn der Nachricht Speicheranbieter RTF unterstützt, haben Sie alle durchgeführt, die erforderlich ist. Sie können richten sich nach den Speicheranbieter Nachricht, um den Nachrichteninhalt synchronisieren und die Formatierung zu behandeln und zum Erstellen der **PR\_BODY** Eigenschaft bei Bedarf. RTF-fähigen Nachrichtenspeicher Aufrufen [RTFSync](rtfsync.md) , um die Synchronisierung zu behandeln. Wenn die RTF\_SYNC_BODY_CHANGED-Flag auf TRUE festgelegt ist, wird in der Anbieter die **PR_BODY** -Eigenschaft neu berechnen. 
  
Wenn Ihre Nachricht Speicheranbieter RTF nicht unterstützt, müssen Sie auch nicht RTF-Nachrichteninhalt durch Festlegen der Eigenschaft **PR_BODY** hinzufügen. 
  
## <a name="set-prhtml"></a>Http://Schemas.Microsoft.com/mapi/proptag/0x10130102 festlegen
  
1. Rufen Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, um die **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** -Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. 
    
2. Rufen Sie **IStream::Write** zum Schreiben der Nachricht-Text-Daten in das Stream-Objekt von **OpenProperty**zurückgegeben. 
    
3. Rufen Sie **IStream:: Commit** und **IUnknown** im Stream commit der Änderungen und Speicherplatz frei. 
    
## <a name="set-prbody"></a>PR_BODY festlegen
  
1. Rufen Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, um die **PR_BODY** -Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. 
    
2. Rufen Sie **IStream::Write** zum Schreiben der Nachricht-Text-Daten in das Stream-Objekt von **OpenProperty**zurückgegeben. 
    
3. Rufen Sie die [RTFSync](rtfsync.md) -Funktion, um den Text mit der Formatierung zu synchronisieren. Da es sich um eine neue Nachricht handelt, legen Sie die RTF_SYNC_RTF_CHANGED und die RTF_SYNC_BODY_CHANGED Flags, um anzugeben, dass sowohl die RTF und nur-Text-Version von den Nachrichtentext geändert wurde. **RTFSync** wird mehrerer verwandte Eigenschaften, die der Nachricht Speicheranbieter erforderlich, wie **PR_RTF_IN_SYNC** ([PidTagRtfInSync sind](pidtagrtfinsync-canonical-property.md)) festgelegt und in der Nachricht zu schreiben.
    
4. Rufen Sie **IStream:: Commit** und **IUnknown** im Stream commit der Änderungen und Speicherplatz frei. 
    

