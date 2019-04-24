---
title: Kanonische Pidtagmessagerecipients (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355685"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Kanonische Pidtagmessagerecipients (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle mit Einschränkungen, die auf eine Inhaltstabelle angewendet werden können, um nach Nachrichten zu suchen, die Empfänger-unter Objekte enthalten, die die Einschränkungen erfüllen. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Kennung:  <br/> |0x0E12  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden. Als Eigenschaft vom Typ **PT_OBJECT**kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden. Auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den **IID_IMAPITable** -Schnittstellenbezeichner anzufordern. Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber Sie kann Sie optional melden oder nicht, wenn Sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode aufrufen. 
  
Diese Eigenschaft kann für SubObject-Einschränkungen verwendet werden, indem Sie Sie in der [SSubRestriction](ssubrestriction.md) -Struktur angibt. Dadurch kann ein Client die Ansicht eines Containers auf Nachrichten mit Empfängern begrenzen, die bestimmte Kriterien erfüllen. Eine Nachricht kann angezeigt werden, wenn mindestens eine Zeile in der Empfängertabelle, also ein Empfänger, der SubObject-Einschränkung entspricht. 
  
 **Hinweis** Die Verwendung von SubObject-Einschränkungs Ergebnissen entspricht einem [IMAPISession:: OpenEntry](imapisession-openentry.md) -Aufruf für jede Nachricht in der Tabelle. Abhängig von der Clientanwendung und der Anzahl der zu durchsuchenden Nachrichten kann dies die Leistung beeinträchtigen. 
  
Die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft und diese Eigenschaft ähneln der Verwendung. Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen: 
  
|**Eigenschaft**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))  <br/> |Inhaltstabelle  <br/> |
|**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Hierarchietabelle  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([Pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabelle mit zugeordneten Inhalten  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))  <br/> |Attachment-Tabelle  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Empfängertabelle  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

