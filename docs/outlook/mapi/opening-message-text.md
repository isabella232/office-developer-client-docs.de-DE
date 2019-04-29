---
title: Öffnen des Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407536"
---
# <a name="opening-message-text"></a>Öffnen des Nachrichtentexts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Text einer Nachricht wird in seiner **PR\_-Body** -Eigenschaft oder **PR\_-RTF\_** -komprimierten Eigenschaft gespeichert. Weitere Informationen finden Sie unter **PR\_-Textkörper** ([pidtagbody (](pidtagbody-canonical-property.md)), **\_PR-HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) und **PR\_-\_RTF-Komprimierung** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Sie das Rich-Text-Format (RTF) unterstützen, öffnen Sie **PR\_RTF_COMPRESSED**. Wenn Sie RTF nicht unterstützen, öffnen **Sie\_PR Body**. Da der Text einer Nachricht groß sein kann, unabhängig davon, ob Sie formatiert ist, verwenden Sie **IMAPIProp:: OpenProperty** , um diese Eigenschaften zu öffnen. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>So zeigen Sie formatierten Nachrichtentext an
  
1. Wenn Sie einen nicht-RTF-fähigen Nachrichtenspeicher verwenden, wie durch das Fehlen des STORE_RTF_OK-Flags in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Stores angegeben:
    
    1. Rufen Sie die **IMAPIProp::** GetProps-Methode der Nachricht auf, um die **PR_RTF_IN_SYNC** -Eigenschaft abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::](imapiprop-getprops.md) GetProps und **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md)).
        
    2. Rufen Sie RTFSync auf, um die PR_BODY-Eigenschaft der Nachricht mit der **PR_RTF_COMPRESSED** -Eigenschaft zu synchronisieren. Weitere Informationen finden Sie unter [RTFSync](rtfsync.md), **PR_BODY**und **PR_RTF_COMPRESSED**. Geben Sie das RTF_SYNC_BODY_CHANGED-Flag zurück, wenn der Aufruf von **PR_RTF_IN_SYNC** fehlgeschlagen ist, weil die Eigenschaft nicht vorhanden ist oder auf false festgelegt ist. 
        
    3. Wenn **RTFSync** zurückgegeben wird, was bedeutet, dass Änderungen vorgenommen wurden, rufen Sie die **IMAPIProp:: SaveChanges** -Methode der Nachricht auf, um Sie dauerhaft zu speichern. Weitere Informationen finden Sie unter [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
2. Unabhängig davon, ob Sie einen RTF-fähigen Nachrichtenspeicher verwenden oder nicht:
    
    1. Rufen Sie **IMAPIProp:: OpenProperty** auf, um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen. Weitere Informationen finden Sie unter [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.
        
    2. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, rufen **** Sie OpenProperty auf, um die **PR_BODY** -Eigenschaft zu öffnen. 
        
    3. Rufen Sie die **WrapCompressedRTFStream** -Funktion auf, um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, sofern verfügbar. Weitere Informationen finden Sie unter [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Kopieren Sie den formatierten Text aus dem Stream an die entsprechende Stelle im Nachrichtenformular. 
    
### <a name="to-display-plain-message-text"></a>So zeigen Sie reinen Nachrichtentext an
  
1. Rufen Sie die **IMAPIProp::** GetProps-Methode der Nachricht auf, um die **PR_BODY** -Eigenschaft abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::](imapiprop-getprops.md)GetProps.
    
2. Wenn **** GetProps entweder PT_ERROR für den Eigenschaftentyp in der Eigenschaftswert Struktur oder MAPI_E_NOT_ENOUGH_MEMORY zurückgibt, rufen Sie die **IMAPIProp:: OpenProperty** -Methode der Nachricht auf. Übergibt **PR_BODY** als Property-Tag und IID_IStream als Schnittstellenbezeichner. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Kopieren Sie den nur-Text aus dem Stream an die entsprechende Stelle im Nachrichtenformular. 
    

