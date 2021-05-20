---
title: Erstellen eines Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428004"
---
# <a name="creating-message-text"></a>Erstellen eines Nachrichtentexts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl einige Nachrichten nur aus einer Empfängerliste und einer Betreffzeile besteht, ist der Inhalt der meisten Nachrichten, insbesondere IPM. Hinweismeldungen, einschließlich Text. Nachrichtentext kann einfach oder formatiert sein und wird in drei Eigenschaften gespeichert: **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Ihr Client Nur-Text-basiert ist, legen Sie **PR \_ BODY .** Wenn Sie formatierten Text im Rich Text Format (RTF) unterstützen, legen Sie **entweder nur PR_RTF_COMPRESSED** oder sowohl **PR_RTF_COMPRESSED** als auch **PR \_ BODY** fest, je nach dem verwendeten Nachrichtenspeicheranbieter. Wenn ein RTF-bewusster Client einen RTF-benachrichtigungsspeicher verwendet, wird nur **PR_RTF_COMPRESSED** verwendet. Wenn ein RTF-bewusster Client einen Nicht-RTF-bewussten Nachrichtenspeicher verwendet, werden beide Eigenschaften festgelegt. Wenn Ihr Client HTML unterstützt, legen Sie die **PR_HTML.** 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Ermitteln, ob ihr Nachrichtenspeicher das Rich-Text-Format unterstützt
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers auf, um die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft abzurufen.
    
2. Suchen Sie nach dem STORE_RTF_OK Bit. Wenn STORE_RTF_OK festgelegt ist, unterstützt der Nachrichtenspeicheranbieter RTF-Text. Wenn sie nicht festgelegt ist, unterstützt der Nachrichtenspeicheranbieter nur Nur-Text.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Ermitteln, ob Ihr Nachrichtenspeicher HTML unterstützt
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers auf, um die **PR_STORE_SUPPORT_MASK** abzurufen. 
    
2. Suchen Sie nach dem STORE_HTML_OK Bit. Wenn STORE_HTML_OK festgelegt ist, unterstützt der Nachrichtenspeicheranbieter HTML-Text. 
    
## <a name="set-pr_rtf_compressed"></a>Festlegen von \_ PR-RTF_COMPRESSED
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) der Nachricht auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen, IID_IStream als Schnittstellenbezeichner anzugeben und das MAPI_CREATE festlegen. 
    
2. Rufen Sie [die WrapCompressedRTFStream-Funktion](wrapcompressedrtfstream.md) auf, und übergeben Sie das STORE_UNCOMPRESSED_RTF-Flag, wenn das STORE_UNCOMPRESSED_RTF-Bit in der PR_STORE_SUPPORT_MASK des Nachrichtenspeichers **festgelegt** ist. 
    
3. Geben Sie den ursprünglichen Datenstrom frei, indem Sie die ** IUnknown::Release ** -Methode aufrufen. 
    
4. Rufen Sie entweder ** IStream::Write ** oder **IStream::CopyTo auf,** um den Nachrichtentext in den Stream zu schreiben, der von **WrapCompressedRTFStream zurückgegeben wird.**
    
5. Rufen Sie **die Commit-** **und Release-Methoden** für den Stream auf, der von der **OpenProperty-Methode zurückgegeben** wird. 
    
Wenn der Nachrichtenspeicheranbieter zu diesem Zeitpunkt RTF unterstützt, haben Sie alles erforderliche getan. Sie können darauf angewiesen sein, dass der Nachrichtenspeicheranbieter die Synchronisierung von Nachrichteninhalten und -formatierungen über die Synchronisierung und die Erstellung der **PR \_ BODY-Eigenschaft** bei Bedarf abarbeite. RTF-benachrichtigungsspeicher rufen [RTFSync auf,](rtfsync.md) um die Synchronisierung zu verarbeiten. Wenn das RTF-SYNC_BODY_CHANGED auf TRUE festgelegt ist, wird der Anbieter die PR_BODY \_ neu kompensieren.  
  
Wenn Ihr Nachrichtenspeicheranbieter RTF nicht unterstützt, müssen Sie auch Nicht-RTF-Nachrichteninhalte hinzufügen, indem Sie die PR_BODY **festlegen.** 
  
## <a name="set-pr_html"></a>Festlegen PR_HTML
  
1. Rufen Sie [die IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_HTML** mit der **IStream-Schnittstelle zu** öffnen. 
    
2. Rufen **Sie IStream::Write auf,** um die Nachrichtentextdaten in den von OpenProperty zurückgegebenen **Datenstrom zu schreiben.** 
    
3. Rufen **Sie IStream::Commit und** **IUnknown::Release** im Datenstrom auf, um die Änderungen zu übertragen und den Arbeitsspeicher frei zu geben. 
    
## <a name="set-pr_body"></a>Festlegen PR_BODY
  
1. Rufen Sie [die IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_BODY** mit der **IStream-Schnittstelle zu** öffnen. 
    
2. Rufen **Sie IStream::Write auf,** um die Nachrichtentextdaten in den von OpenProperty zurückgegebenen **Datenstrom zu schreiben.** 
    
3. Rufen Sie die [RTFSync-Funktion](rtfsync.md) auf, um den Text mit der Formatierung zu synchronisieren. Da es sich um eine neue Nachricht handelt, legen Sie sowohl die RTF_SYNC_RTF_CHANGED als auch RTF_SYNC_BODY_CHANGED fest, um anzugeben, dass sich sowohl die RTF- als auch die Nur-Text-Version des Nachrichtentexts geändert hat. **RTFSync** setzt mehrere verwandte Eigenschaften, die der **Nachrichtenspeicheranbieter** benötigt, z. B. PR_RTF_IN_SYNC ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), und schreibt sie in die Nachricht.
    
4. Rufen **Sie IStream::Commit und** **IUnknown::Release** im Datenstrom auf, um die Änderungen zu übertragen und den Arbeitsspeicher frei zu geben. 
    

