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
  
Einige Nachrichten bestehen zwar aus nichts mehr als eine Empfängerliste und eine Betreffzeile, der Inhalt der meisten Nachrichten, insbesondere IPM. Hinweis Nachrichten, einschließlich Text. Nachrichtentext kann einfach oder formatiert sein und in drei Eigenschaften gespeichert werden: **PR\_-Body** ([pidtagbody (](pidtagbody-canonical-property.md)) **,\_PR-HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Ihr Client nur-Text-basiert ist, legen Sie **PR\_**-Text fest. Wenn Sie formatierten Text im Rich-Text-Format (RTF) unterstützen, legen Sie je nach verwendetem Nachrichtenspeicher Anbieter entweder **PR_RTF_COMPRESSED** oder sowohl **PR_RTF_COMPRESSED** als auch **PR\_-Body**fest. Wenn ein RTF-fähiger Client einen RTF-fähigen Nachrichtenspeicher verwendet, wird nur **PR_RTF_COMPRESSED** festgelegt. Wenn ein RTF-fähiger Client einen nicht-RTF-fähigen Nachrichtenspeicher verwendet, werden beide Eigenschaften festgelegt. Wenn Ihr Client HTML unterstützt, legen Sie die **PR_HTML** -Eigenschaft fest. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Bestimmen, ob der Nachrichtenspeicher Rich-Text-Format unterstützt
  
1. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers auf, um die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft abzurufen.
    
2. Überprüfen Sie das STORE_RTF_OK-Bit. Wenn STORE_RTF_OK festgelegt ist, unterstützt der Nachrichtenspeicher Anbieter RTF-Text. Wenn Sie nicht festgelegt ist, unterstützt der Nachrichtenspeicher Anbieter nur-Text.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Bestimmen, ob der Nachrichtenspeicher HTML unterstützt
  
1. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers auf, um die **PR_STORE_SUPPORT_MASK** -Eigenschaft abzurufen. 
    
2. Überprüfen Sie das STORE_HTML_OK-Bit. Wenn STORE_HTML_OK festgelegt ist, unterstützt der Nachrichtenspeicher Anbieter HTML-Text. 
    
## <a name="set-prrtfcompressed"></a>Festlegen von\_PR-RTF_COMPRESSED
  
1. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode der Nachricht auf, um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen und IID_IStream als Schnittstellenbezeichner anzugeben und das MAPI_CREATE-Flag festzulegen. 
    
2. Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion auf, und übergeben Sie das STORE_UNCOMPRESSED_RTF-Flag, wenn das STORE_UNCOMPRESSED_RTF-Bit in der **PR_STORE_SUPPORT_MASK** -Eigenschaft des Nachrichtenspeichers festgelegt ist. 
    
3. Geben Sie den ursprünglichen Datenstrom durch Aufrufen der * * IUnknown:: Release * *-Methode frei. 
    
4. Rufen Sie entweder * * IStream:: Write * * oder **IStream:: CopyTo** auf, um den Nachrichtentext in den von **WrapCompressedRTFStream**zurückgegebenen Stream zu schreiben.
    
5. Rufen Sie die Methoden **Commit** und **Release** für den Stream auf, der von der **OpenProperty** -Methode zurückgegeben wird. 
    
Wenn der Nachrichtenspeicher Anbieter RTF unterstützt, haben Sie jetzt alle erforderlichen Schritte ausgeführt. Sie können davon abhängen, ob der Nachrichtenspeicher Anbieter die Synchronisierung des Nachrichteninhalts und die Formatierung und **die\_PR-Body** -Eigenschaft bei Bedarf erstellt. RTF-fähige Nachrichtenspeicher rufen [RTFSync](rtfsync.md) auf, um die Synchronisierung zu behandeln. Wenn das RTF\_-SYNC_BODY_CHANGED-Flag auf true festgelegt ist, berechnet der Anbieter die **PR_BODY** -Eigenschaft neu. 
  
Wenn der Nachrichtenspeicher Anbieter RTF nicht unterstützt, müssen Sie auch nicht-RTF-Nachrichteninhalte hinzufügen, indem Sie die **PR_BODY** -Eigenschaft festlegen. 
  
## <a name="set-prhtml"></a>PR_HTML festlegen
  
1. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode auf, um die **PR_HTML** -Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. 
    
2. Rufen Sie **IStream:: Write** auf, um die Nachrichten Textdaten in den von **OpenProperty**zurückgegebenen Stream zu schreiben. 
    
3. Rufen Sie **IStream:: Commit** und **IUnknown:: Release** für den Stream ab, um die Änderungen zu übernehmen und den Arbeitsspeicher freizugeben. 
    
## <a name="set-prbody"></a>PR_BODY festlegen
  
1. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode auf, um die **PR_BODY** -Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. 
    
2. Rufen Sie **IStream:: Write** auf, um die Nachrichten Textdaten in den von **OpenProperty**zurückgegebenen Stream zu schreiben. 
    
3. Rufen Sie die [RTFSync](rtfsync.md) -Funktion auf, um den Text mit der Formatierung zu synchronisieren. Da es sich um eine neue Nachricht handelt, legen Sie sowohl die RTF_SYNC_RTF_CHANGED-als auch die RTF_SYNC_BODY_CHANGED-Flags fest, um anzugeben, dass sowohl die RTF-als auch die nur-Text-Version des Nachrichtentexts geändert wurde. **RTFSync** legt mehrere verwandte Eigenschaften fest, die der Nachrichtenspeicher Anbieter benötigt, beispielsweise **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md)), und schreibt diese in die Nachricht.
    
4. Rufen Sie **IStream:: Commit** und **IUnknown:: Release** für den Stream ab, um die Änderungen zu übernehmen und den Arbeitsspeicher freizugeben. 
    

