---
title: Anlagentabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c21c8a27d8cf7fa65951e8ef784a203dafbd057
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605188"
---
# <a name="attachment-tables"></a>Anlagentabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anlagentabelle enthält Informationen zu allen Anlagenobjekten, die einer gesendeten Nachricht oder einer Nachricht in der Komposition zugeordnet sind. 
  
In der Tabelle sind nur Anlagen enthalten, die über einen Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht gespeichert wurden. Anlagentabellen werden von Nachrichtenspeicheranbietern implementiert und von Clientanwendungen und Transportanbietern verwendet. 
  
Sie können auf eine Anlagentabelle zugreifen, indem Sie eine der folgenden Optionen aufrufen:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), anfordern der **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft.
    
Anlagentabellen sind dynamisch.
  
Nachrichtenspeicheranbieter müssen die Sortierung nach ihren Anlagentabellen nicht unterstützen. Wenn die Sortierung nicht unterstützt wird, muss die Tabelle in der reihenfolge dargestellt werden, indem die Position gerendert wird – die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) -Eigenschaft.
  
Nachrichtenspeicheranbieter müssen auch keine Einschränkungen für ihre Anlagentabellen unterstützen. Anbieter, die keine Einschränkungen unterstützen, geben MAPI_E_NO_SUPPORT aus ihren Implementierungen von [IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::FindRow](imapitable-findrow.md)zurück.
  
Anlagentabellen können klein sein; Der erforderliche Spaltensatz enthält nur vier Spalten:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** nicht transparent ist und einen Wert zum eindeutigen Identifizieren einer Anlage innerhalb einer Nachricht enthält. Diese Eigenschaft wird häufig als Index in den Zeilen der Tabelle verwendet. **PR_ATTACH_NUM** hat eine kurze Lebensdauer; sie ist nur gültig, während die Nachricht, die die Anlage enthält, geöffnet ist. Ihr Wert bleibt garantiert konstant, solange die Anlagentabelle geöffnet ist. 
  
 **PR_INSTANCE_KEY** ist in fast jeder Tabelle erforderlich. Es wird verwendet, um eine bestimmte Zeile eindeutig zu identifizieren. 
  
 **PR_RECORD_KEY** wird häufig verwendet, um ein Objekt zu Vergleichszwecken eindeutig zu identifizieren. Im Gegensatz **zu PR_ATTACH_NUM** hat **PR_RECORD_KEY** denselben Bereich wie ein langfristiger Eintragsbezeichner. sie bleibt auch nach dem Schließen und erneuten Öffnen der Nachricht verfügbar und gültig. Weitere Informationen zur Verwendung von Datensatzschlüsseln in der MAPI finden Sie unter [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** gibt an, wie eine Anlage in einer Rich-Text-Nachricht angezeigt werden soll. Es kann auf einen Offset in Zeichen festgelegt werden, wobei das erste Zeichen des Nachrichteninhalts, wie in der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft gespeichert, offset 0 oder -1 (0xFFFFFFFF) ist, was angibt, dass die Anlage überhaupt nicht innerhalb des Nachrichtentexts gerendert werden soll. Es ist auch eine Option, **PR_RENDERING_POSITION** nicht festzulegen. 
  
Wenn eine Anlagentabelle nach Renderingposition sortiert wird, behandelt der Nachrichtenspeicheranbieter sie als signierten Wert (PT_LONG). Daher werden Anlagen mit Renderingpositionen von -1 vor Anlagen mit Renderingpositionen sortiert, die gültige Offsets darstellen. 
  
Weitere Informationen zum Rendern einer Anlage in einer Nur-Text-Nachricht finden Sie unter [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md). 
  
Informationen zum Rendern einer Anlage in formatiertem Text, z. B. RTF (Rich Text Format), finden Sie unter [Rendern einer Anlage in RTF-Text.](rendering-an-attachment-in-rtf-text.md)
  
Einige der Eigenschaften, die Nachrichtenspeicheranbieter häufig in eine Anlagentabelle einschließen, da sie einfach zu berechnen oder abzurufen sind, sind:
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

