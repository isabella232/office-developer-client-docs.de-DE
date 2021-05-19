---
title: Anlagentabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427443"
---
# <a name="attachment-tables"></a>Anlagentabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anlagentabelle enthält Informationen zu allen Anlagenobjekten, die einer übermittelten Nachricht oder einer Nachricht in der Komposition zugeordnet sind. 
  
In der Tabelle sind nur Anlagen enthalten, die durch einen Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht gespeichert wurden. Anlagentabellen werden von Nachrichtenspeicheranbietern implementiert und von Clientanwendungen und Transportanbietern verwendet. 
  
Auf eine Anlagentabelle kann zugegriffen werden, indem sie eine der folgenden Aufrufe aufruft:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), fordert die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft an.
    
Anlagentabellen sind dynamisch.
  
Nachrichtenspeicheranbieter müssen die Sortierung ihrer Anlagentabellen nicht unterstützen. Wenn die Sortierung nicht unterstützt wird, muss die Tabelle in der Reihenfolge dargestellt werden, indem die Position **gerendert** wird – die PR_RENDERING_POSITION ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) -Eigenschaft.
  
Nachrichtenspeicheranbieter müssen auch keine Einschränkungen für ihre Anlagentabellen unterstützen. Anbieter, die keine Einschränkungen unterstützen, geben MAPI_E_NO_SUPPORT Implementierungen von [IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::FindRow zurück.](imapitable-findrow.md)
  
Anlagentabellen können klein sein. Der erforderliche Spaltensatz enthält nur vier Spalten:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** ist nichttransmitierbar und enthält einen Wert zum eindeutigen Identifizieren einer Anlage innerhalb einer Nachricht. Diese Eigenschaft wird häufig als Index in den Zeilen der Tabelle verwendet. **PR_ATTACH_NUM** hat eine kurze Lebensdauer; sie ist nur gültig, wenn die Nachricht mit der Anlage geöffnet ist. Der Wert bleibt garantiert konstant, solange die Anlagentabelle geöffnet ist. 
  
 **PR_INSTANCE_KEY** in fast jeder Tabelle erforderlich. Es wird verwendet, um eine bestimmte Zeile eindeutig zu identifizieren. 
  
 **PR_RECORD_KEY** wird häufig verwendet, um ein Objekt für Vergleichszwecke eindeutig zu identifizieren. Im **PR_ATTACH_NUM** hat **PR_RECORD_KEY** denselben Bereich wie eine langfristige Eintrags-ID. sie bleibt verfügbar und gültig, auch nachdem die Nachricht geschlossen und erneut geöffnet wurde. Weitere Informationen zur Verwendung von Datensatzschlüsseln in MAPI finden Sie unter [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** gibt an, wie eine Anlage in einer Rich-Text-Nachricht angezeigt werden soll. Sie kann auf einen Offset in Zeichen festgelegt werden, und das erste Zeichen des Nachrichteninhalts, das in der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft gespeichert ist, wird auf -0 oder -1 (0xFFFFFFFF) versetzt, was angibt, dass die Anlage überhaupt nicht im Nachrichtentext gerendert werden soll. Das Festlegen **PR_RENDERING_POSITION** ist ebenfalls eine Option. 
  
Wenn eine Anlagentabelle nach Renderposition sortiert wird, behandelt der Nachrichtenspeicheranbieter sie als signierten Wert (PT_LONG). Aus diesem Grund werden Anlagen mit Renderingpositionen von -1 vor Anlagen mit Renderingpositionen sortiert, die gültige Offsets widerspiegeln. 
  
Weitere Informationen zum Rendern einer Anlage in einer Nur-Text-Nachricht finden Sie unter [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md). 
  
Informationen zum Rendern einer Anlage in formatierten Text wie Rich Text Format (RTF) finden Sie unter [Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md).
  
Einige der Eigenschaften, die Nachrichtenspeicheranbieter häufig in einer Anlagentabelle enthalten, da sie einfach zu berechnen oder abzurufen sind, sind:
  
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

