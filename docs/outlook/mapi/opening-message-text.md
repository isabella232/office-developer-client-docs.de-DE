---
title: Öffnen des Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 40d12c84088748d0801649a2fca59c12e60d0b92
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625140"
---
# <a name="opening-message-text"></a>Öffnen des Nachrichtentexts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Text einer Nachricht wird entweder in der **PR \_ BODY-Eigenschaft** oder in der **PR \_ RTF \_ COMPRESSED-Eigenschaft** gespeichert. Weitere Informationen finden Sie unter **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Sie rtf (Rich Text Format) unterstützen, öffnen Sie **PR \_ RTF_COMPRESSED**. Wenn Sie RTF nicht unterstützen, öffnen Sie **PR \_ BODY**. Da der Text einer Nachricht groß sein kann, unabhängig davon, ob er formatiert ist, verwenden Sie **IMAPIProp::OpenProperty,** um diese Eigenschaften zu öffnen. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>So zeigen Sie formatierten Nachrichtentext an
  
1. Wenn Sie einen Nicht-RTF-fähigen Nachrichtenspeicher verwenden, wie durch das Fehlen des flags STORE_RTF_OK in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) des Speichers angegeben:
    
    1. Rufen Sie die **IMAPIProp::GetProps-Methode** der Nachricht auf, um die **PR_RTF_IN_SYNC-Eigenschaft** abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) und **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Rufen Sie RTFSync auf, um die PR_BODY Eigenschaft der Nachricht mit der **PR_RTF_COMPRESSED-Eigenschaft** zu synchronisieren. Weitere Informationen finden Sie unter [RTFSync](rtfsync.md), **PR_BODY** und **PR_RTF_COMPRESSED**. Übergeben Sie das flag RTF_SYNC_BODY_CHANGED, wenn der Aufruf zum Abrufen **von PR_RTF_IN_SYNC** fehlgeschlagen ist, da die Eigenschaft nicht vorhanden ist oder auf FALSE festgelegt ist. 
        
    3. Wenn **RTFSync** TRUE zurückgegeben hat , was angibt, dass Änderungen vorgenommen wurden, rufen Sie die **IMAPIProp::SaveChanges-Methode** der Nachricht auf, um sie dauerhaft zu speichern. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Unabhängig davon, ob Sie einen RTF-fähigen Nachrichtenspeicher verwenden oder nicht:
    
    1. Rufen Sie **IMAPIProp::OpenProperty** auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.
        
    2. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, rufen Sie **OpenProperty** auf, um die **PR_BODY-Eigenschaft** zu öffnen. 
        
    3. Rufen Sie die **WrapCompressedRTFStream-Funktion** auf, um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, falls verfügbar. Weitere Informationen finden Sie unter [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Kopieren Sie den formatierten Text aus dem Datenstrom an die entsprechende Stelle im Nachrichtenformular. 
    
### <a name="to-display-plain-message-text"></a>So zeigen Sie Nur-Nachrichten-Text an
  
1. Rufen Sie die **IMAPIProp::GetProps-Methode** der Nachricht auf, um die **PR_BODY-Eigenschaft** abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Wenn **GetProps** entweder PT_ERROR für den Eigenschaftstyp in der Eigenschaftswertstruktur oder MAPI_E_NOT_ENOUGH_MEMORY zurückgibt, rufen Sie die **IMAPIProp::OpenProperty-Methode** der Nachricht auf. Übergeben **Sie PR_BODY** als Eigenschaftstag und IID_IStream als Schnittstellenbezeichner. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Kopieren Sie den Nur-Text aus dem Datenstrom an die entsprechende Stelle im Nachrichtenformular. 
    

