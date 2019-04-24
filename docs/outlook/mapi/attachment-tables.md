---
title: Anlagentabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318137"
---
# <a name="attachment-tables"></a>Anlagentabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Attachment-Tabelle enthält Informationen zu allen Attachment-Objekten, die einer übermittelten Nachricht oder einer Nachricht unter Composition zugeordnet sind. 
  
Nur Anlagen, die durch einen Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht gespeichert wurden, sind in der Tabelle enthalten. Anlagen Tabellen werden von Nachrichtenspeicher Anbietern implementiert und von Clientanwendungen und Transportanbietern verwendet. 
  
Sie können auf eine Attachment-Tabelle zugreifen, indem Sie eine der folgenden aufrufen:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md), der die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft anfordert.
    
Anlagen Tabellen sind dynamisch.
  
Nachrichtenspeicher Anbieter müssen die Sortierung in ihren Anlagen Tabellen nicht unterstützen. Wenn die Sortierung nicht unterstützt wird, muss die Tabelle in der Reihenfolge nach der **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft angezeigt werden.
  
Nachrichtenspeicher Anbieter müssen auch keine Einschränkungen für Ihre Anlage Tabellen unterstützen. Anbieter, die keine Einschränkungen unterstützen, geben MAPI_E_NO_SUPPORT aus ihren Implementierungen von [IMAPITable:: Restrict](imapitable-restrict.md) und [IMAPITable:: FindRow](imapitable-findrow.md)zurück.
  
Anlagen Tabellen können klein sein; der erforderliche Spaltensatz enthält nur vier Spalten:
  
- **PR_ATTACH_NUM** ([Pidtagattachnumber (](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** ist nicht übertragbar und enthält einen Wert zum eindeutigen Identifizieren einer Anlage in einer Nachricht. Diese Eigenschaft wird häufig als Index in den Zeilen der Tabelle verwendet. **PR_ATTACH_NUM** hat eine kurze Lebensdauer; Sie ist nur gültig, wenn die Nachricht, die die Anlage enthält, geöffnet ist. Der Wert der Datei wird garantiert konstant bleiben, solange die Anlage Tabelle geöffnet ist. 
  
 **PR_INSTANCE_KEY** ist in fast jeder Tabelle erforderlich. Es wird verwendet, um eine bestimmte Zeile eindeutig zu identifizieren. 
  
 **PR_RECORD_KEY** wird häufig verwendet, um ein Objekt zu Vergleichszwecken eindeutig zu identifizieren. Im Gegensatz zu **PR_ATTACH_NUM**hat **PR_RECORD_KEY** den gleichen Bereich wie eine langfristige Eintrags-ID. Sie bleibt auch nach dem Schließen und erneuten Öffnen der Nachricht verfügbar und gültig. Weitere Informationen zur Verwendung von Daten Satz Schlüsseln in MAPI finden Sie unter [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** gibt an, wie eine Anlage in einer Rich-Text-Nachricht angezeigt werden soll. Sie kann auf einen Offset in Zeichen festgelegt werden, wobei das erste Zeichen des Nachrichteninhalts in der **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft als Offset 0 oder to-1 (0xFFFFFFFF) gespeichert wird, was darauf hinweist, dass die Anlage nicht innerhalb der Nachricht gerendert werden soll. Text überhaupt. Nicht die Einstellung **PR_RENDERING_POSITION** ist auch eine Option. 
  
Wenn eine Anlage Tabelle nach der Position des Renders sortiert wird, behandelt der Nachrichtenspeicher Anbieter Sie als einen signierten Wert (PT_LONG). Daher werden Anlagen mit Renderingposition von-1 vor Anlagen mit Wiedergabepositionen sortiert, die gültige Offsets widerspiegeln. 
  
Weitere Informationen zum Rendern einer Anlage in einer nur-Text-Nachricht finden Sie unter Rendering an [Attachment in Plain Text](rendering-an-attachment-in-plain-text.md). 
  
Informationen zum Rendern einer Anlage in formatiertem Text wie Rich-Text-Format (RTF) finden Sie unter [Rendern einer Anlage in RTF-Text](rendering-an-attachment-in-rtf-text.md).
  
Einige der Eigenschaften von Nachrichtenspeicher Anbietern sind häufig in einer Attachment-Tabelle eingeschlossen, da Sie einfach zu berechnen oder abzurufen sind:
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([Pidtagattachencoding (](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([Pidtagattachextension (](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([Pidtagattachfilename (](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([Pidtagattachlongfilename (](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([Pidtagattachpathname (](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([Pidtagattachlongpathname (](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([Pidtagattachmethod (](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([Pidtagattachtag (](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([Pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

