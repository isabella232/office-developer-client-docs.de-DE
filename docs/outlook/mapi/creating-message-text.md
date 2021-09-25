---
title: Erstellen eines Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20f9201c3aab95735bf2c11a2951dd3052e61b66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551723"
---
# <a name="creating-message-text"></a>Erstellen eines Nachrichtentexts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl einige Nachrichten nur aus einer Empfängerliste und einer Betreffzeile bestehen, besteht der Inhalt der meisten Nachrichten, insbesondere IPM. Notieren Sie Nachrichten, enthält Text. Nachrichtentext kann einfach oder formatiert sein und wird in drei Eigenschaften gespeichert: **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Ihr Client nur textbasiert ist, legen Sie **PR \_ BODY** fest. Wenn Sie formatierten Text im Rich-Text-Format (RTF) unterstützen, legen Sie abhängig vom verwendeten Nachrichtenspeicheranbieter entweder **PR_RTF_COMPRESSED** nur oder sowohl **PR_RTF_COMPRESSED** als auch **PR \_ BODY** fest. Wenn ein RTF-fähiger Client einen RTF-fähigen Nachrichtenspeicher verwendet, wird **nur PR_RTF_COMPRESSED** festgelegt. Wenn ein RTF-fähiger Client einen nicht RTF-fähigen Nachrichtenspeicher verwendet, werden beide Eigenschaften festgelegt. Wenn Ihr Client HTML unterstützt, legen Sie die **eigenschaft PR_HTML** fest. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Ermitteln, ob Ihr Nachrichtenspeicher rich-Text-Format unterstützt
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers auf, um die **eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) abzurufen.
    
2. Suchen Sie nach dem STORE_RTF_OK Bit. Wenn STORE_RTF_OK festgelegt ist, unterstützt der Nachrichtenspeicheranbieter RTF-Text. Wenn er nicht festgelegt ist, unterstützt der Nachrichtenspeicheranbieter nur Nur-Text.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Ermitteln, ob Ihr Nachrichtenspeicher HTML unterstützt
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers auf, um die **PR_STORE_SUPPORT_MASK-Eigenschaft** abzurufen. 
    
2. Suchen Sie nach dem STORE_HTML_OK Bit. Wenn STORE_HTML_OK festgelegt ist, unterstützt der Nachrichtenspeicheranbieter HTML-Text. 
    
## <a name="set-pr_rtf_compressed"></a>Festlegen \_ von PR-RTF_COMPRESSED
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) der Nachricht auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen, IID_IStream als Schnittstellenbezeichner anzugeben und das MAPI_CREATE-Flag festzulegen. 
    
2. Rufen Sie die [WrapCompressedRTFStream-Funktion](wrapcompressedrtfstream.md) auf, und übergeben Sie das flag STORE_UNCOMPRESSED_RTF, wenn das STORE_UNCOMPRESSED_RTF Bit in der eigenschaft PR_STORE_SUPPORT_MASK des **Nachrichtenspeichers** festgelegt ist. 
    
3. Geben Sie den ursprünglichen Datenstrom frei, indem Sie seine ** IUnknown::Release ** -Methode aufrufen. 
    
4. Rufen Sie entweder ** IStream::Write ** oder **IStream::CopyTo** auf, um den Nachrichtentext in den von **WrapCompressedRTFStream zurückgegebenen** Datenstrom zu schreiben.
    
5. Rufen Sie die **Commit-** und **Release-Methoden** für den von der **OpenProperty-Methode zurückgegebenen** Datenstrom auf. 
    
Wenn der Nachrichtenspeicheranbieter RTF unterstützt, haben Sie nun alle erforderlichen Schritte ausgeführt. Sie können vom Nachrichtenspeicheranbieter abhängig sein, um die Synchronisierung des Nachrichteninhalts und der Formatierung zu verarbeiten und bei Bedarf die **PR \_ BODY-Eigenschaft** zu erstellen. RTF-fähige Nachrichtenspeicher rufen [RTFSync](rtfsync.md) auf, um die Synchronisierung zu verarbeiten. Wenn das \_ RTF-SYNC_BODY_CHANGED-Flag auf TRUE festgelegt ist, wird die **PR_BODY-Eigenschaft** vom Anbieter neu kompiliert. 
  
Wenn Ihr Nachrichtenspeicheranbieter RTF nicht unterstützt, müssen Sie auch Nicht-RTF-Nachrichteninhalte hinzufügen, indem Sie die **eigenschaft PR_BODY** festlegen. 
  
## <a name="set-pr_html"></a>Festlegen PR_HTML
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_HTML-Eigenschaft** mit der **IStream-Schnittstelle** zu öffnen. 
    
2. Rufen **Sie IStream::Write** auf, um die Nachrichtentextdaten in den von **OpenProperty zurückgegebenen** Datenstrom zu schreiben. 
    
3. Rufen **Sie IStream::Commit** und **IUnknown::Release** im Stream auf, um die Änderungen zu übernehmen und den Arbeitsspeicher freizugeben. 
    
## <a name="set-pr_body"></a>Festlegen PR_BODY
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_BODY-Eigenschaft** mit der **IStream-Schnittstelle** zu öffnen. 
    
2. Rufen **Sie IStream::Write** auf, um die Nachrichtentextdaten in den von **OpenProperty zurückgegebenen** Datenstrom zu schreiben. 
    
3. Rufen Sie die [RTFSync-Funktion](rtfsync.md) auf, um den Text mit der Formatierung zu synchronisieren. Da es sich um eine neue Nachricht handelt, legen Sie die Flags RTF_SYNC_RTF_CHANGED und RTF_SYNC_BODY_CHANGED fest, um anzugeben, dass sich sowohl die RTF- als auch die Nur-Text-Version des Nachrichtentexts geändert haben. **RTFSync** legt mehrere verwandte Eigenschaften fest, die der Nachrichtenspeicheranbieter benötigt, z. **B. PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), und schreibt sie in die Nachricht.
    
4. Rufen **Sie IStream::Commit** und **IUnknown::Release** im Stream auf, um die Änderungen zu übernehmen und den Arbeitsspeicher freizugeben. 
    

