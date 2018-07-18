---
title: Öffnen des Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793312"
---
# <a name="opening-message-text"></a>Öffnen des Nachrichtentexts

**Betrifft**: Outlook 
  
Der Text einer Nachricht gespeichert ist entweder in seiner **PR\_BODY** Eigenschaft oder **PR\_RTF\_komprimierte** Eigenschaft. Weitere Informationen finden Sie unter **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR\_RTF\_komprimierte** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Wenn Sie die Rich Text Format (RTF) unterstützen, öffnen **PR\_RTF_COMPRESSED**. Wenn Sie keine RTF unterstützen, öffnen **PR\_BODY**. Der Text einer Nachricht kann werden große unabhängig davon, ob es formatiert ist, verwenden Sie **IMAPIProp::OpenProperty** , um diese Eigenschaften zu öffnen. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Anzeigen formatierter Nachrichtentext
  
1. Wenn Sie einen bewusst nicht RTF-Nachrichtenspeicher verwenden, wie durch die Abwesenheit des STORE_RTF_OK-Flags in den Speicher **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft angegeben:
    
    1. Rufen Sie die Nachricht **IMAPIProp::GetProps** -Methode zum Abrufen der **PR_RTF_IN_SYNC** -Eigenschaft. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) und **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Rufen Sie RTFSync, um die Nachricht PR_BODY-Eigenschaft mit der **PR_RTF_COMPRESSED** -Eigenschaft zu synchronisieren. Weitere Informationen finden Sie unter [RTFSync](rtfsync.md), **PR_BODY**und **PR_RTF_COMPRESSED**. Übergeben Sie die RTF_SYNC_BODY_CHANGED kennzeichnen, wenn die Aufrufs zum Abrufen von **PR_RTF_IN_SYNC** ist fehlgeschlagen, da die Eigenschaft nicht vorhanden ist, oder es ist auf FALSE festgelegt. 
        
    3. Wenn **RTFSync** den Wert TRUE zurückgegeben, was bedeutet, dass Änderungen vorgenommen wurden – rufen Sie die Nachricht **IMAPIProp::SaveChanges** -Methode, um sie dauerhaft zu speichern. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Speichern Sie unabhängig davon, ob Sie eine RTF-fähigen Nachricht verwenden:
    
    1. Rufen Sie **IMAPIProp::OpenProperty** , um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.
        
    2. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, rufen Sie **OpenProperty** , um die **PR_BODY** -Eigenschaft zu öffnen. 
        
    3. Rufen Sie die **WrapCompressedRTFStream** -Funktion, um eine nicht komprimierten Version der komprimierten RTF-Daten zu erstellen, falls verfügbar. Weitere Informationen finden Sie unter [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Kopieren des formatierten Texts aus dem Stream an der entsprechenden Stelle in das Nachrichtenformular. 
    
### <a name="to-display-plain-message-text"></a>Einfache Meldungstext angezeigt.
  
1. Rufen Sie die Nachricht **IMAPIProp::GetProps** -Methode zum Abrufen der **PR_BODY** -Eigenschaft. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Wenn **GetProps** entweder PT_ERROR für den Eigenschaftentyp in der Eigenschaft Wert Struktur oder MAPI_E_NOT_ENOUGH_MEMORY zurückgibt, rufen Sie die Nachricht **IMAPIProp::OpenProperty** -Methode. Übergeben Sie **PR_BODY** als Eigenschafts-Tag und IID_IStream als Schnittstellenbezeichner. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Kopieren Sie die nur-Text aus dem Stream an der entsprechenden Stelle in das Nachrichtenformular. 
    

