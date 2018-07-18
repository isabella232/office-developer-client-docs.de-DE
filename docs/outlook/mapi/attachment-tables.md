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
ms.openlocfilehash: 2fd79cfe18e7d39f26563c87b8fb15553bf32ddf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791324"
---
# <a name="attachment-tables"></a>Anlagentabellen

**Betrifft**: Outlook 
  
Eine Anlagentabelle enthält Informationen zu allen Attachment-Objekte, die eine gesendete Nachricht oder eine Nachricht verfasst zugeordnet sind. 
  
Nur Anlagen, die durch einen Aufruf an die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode gespeichert wurden, sind in der Tabelle enthalten. Anlagentabellen Zeichenfolgeneigenschaften Nachricht implementiert und von Clientanwendungen und Transportanbieter verwendet werden. 
  
Eine Anlagentabelle kann durch Aufrufen der folgenden zugegriffen werden:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft anfordern.
    
Anlagentabellen sind dynamisch.
  
Nachricht Anbieter sind nicht erforderlich, zur Unterstützung ihrer Anlagentabellen sortieren. Wenn Sortieren nicht unterstützt wird, muss die Tabelle in der Order by-Renderingposition präsentiert werden – die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft.
  
Nachricht Anbieter sind zur Unterstützung von Einschränkungen für ihre Anlagentabellen auch nicht erforderlich. Anbieter, die keine für Einschränkungen Unterstützung zurück MAPI_E_NO_SUPPORT aus ihrer Implementierung von [Methode IMAPITable:: Restrict](imapitable-restrict.md) und [IMAPITable](imapitable-findrow.md).
  
Anlagentabellen können klein sein. Es gibt nur vier Spalten in der Spalte erforderlich:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** ist Nontransmittable und enthält einen Wert zur eindeutigen Identifizierung einer Anlage in einer Nachricht. Diese Eigenschaft wird häufig als Index auf die Zeilen der Tabelle verwendet. **PR_ATTACH_NUM** hat kurzen Lebensdauer. Es ist nur gültig, während die Nachricht mit Anlage geöffnet ist. Der Wert ist immer konstant bleiben, solange die Anlagentabelle geöffnet ist. 
  
 **PR_INSTANCE_KEY** ist in fast jeder Tabelle erforderlich. Es wird verwendet, um eine bestimmte Zeile eindeutig zu identifizieren. 
  
 **PR_RECORD_KEY** wird häufig verwendet, um ein Objekt zu Vergleichszwecken eindeutig zu identifizieren. Im Gegensatz zu **PR_ATTACH_NUM**hat **PR_RECORD_KEY** im selben Bereich als eine langfristige Eintrags-ID an. verfügbar und gültig bleibt auch nach die Nachricht geschlossen und erneut geöffnet wird. Weitere Informationen zur Verwendung der Datensatzschlüssel in MAPI finden Sie unter [MAPI-Datensatz und Suche Schlüssel](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** gibt an, wie eine Anlage in einer Nachricht rich-Text angezeigt werden soll. Es kann festgelegt werden, auf einen Offset in Zeichen, mit dem ersten Zeichen des Nachrichteninhalts wie gespeichert, in dem **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft zu offset 0 ist, oder auf-1 (0xFFFFFFFF), was bedeutet, dass die Anlage nicht innerhalb der Nachricht gerendert werden sollen Text überhaupt. Festlegen von nicht **PR_RENDERING_POSITION** ist auch eine Option aus. 
  
Beim Renderingposition eine Anlagentabelle sortiert wird, wird Sie von der Nachricht Informationsdienst wie einen Wert mit Vorzeichen (PT_LONG) behandelt. Aus diesem Grund werden Anlagen mit Rendering Positionen-1 vor der Anlagen mit Rendering Positionen sortiert, die gültige Offsets widerspiegeln. 
  
Weitere Informationen zum Rendern einer Anlage in einer nur-Text-Nachricht finden Sie unter [Rendern einer Anlage im Nur-Text](rendering-an-attachment-in-plain-text.md). 
  
Informationen über das Rendern einer Anlage in formatierten Text wie Rich Text Format (RTF) finden Sie unter [Rendern einer Anlage im RTF-Text](rendering-an-attachment-in-rtf-text.md).
  
Sind einige der Eigenschaften, die Nachricht Anbieter häufig in einer Anlagentabelle enthalten, da sie leicht sind zu berechnen oder abgerufen werden soll:
  
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

