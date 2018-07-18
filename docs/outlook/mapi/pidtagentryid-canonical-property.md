---
title: PidTagEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794367"
---
# <a name="pidtagentryid-canonical-property"></a>PidTagEntryId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine MAPI-Eintrags-ID, die zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts verwendet. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ENTRYID  <br/> |
|Bezeichner:  <br/> |0x0FFF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt ein Objekt für **OpenEntry** zum Instanziieren und ermöglicht den Zugriff auf alle seine Eigenschaften über die entsprechenden abgeleiteten Schnittstelle des **IMAPIProp**. 
  
Diese Eigenschaft ist eine der Eigenschaften für alle Benutzer messaging Basisadresse. 
  
Diese Eigenschaft kann eine langfristige oder einen kurzfristigen Bezeichner enthalten. Kurzfristige Bezeichner sind schneller und einfacher, Konstrukt, aber in deren Bereich und die Dauer, in der Regel auf der aktuellen Sitzung und Arbeitsstation beschränkt sind. Sie sind häufig verwendet, um Objekte vorübergehender Art, wie Zeilen der Tabelle oder Einträgen im Dialogfeld, und klicken Sie dann abgebrochen. Langfristige-IDs werden für eine umfassende und langfristig Art-Objekte verwendet. 
  
Diese Eigenschaft ist immer über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode verfügbar. Einige Dienstanbieter können sie sofort nach der Instanziierung zur Verfügung. Der Anbieter muss immer eine langfristige Eintrags-ID aus **GetProps**zurückgeben. Aus diesem Grund um einen kurzfristigen Bezeichner in langfristige konvertieren, einfach öffnen Sie das Objekt und seine dies abrufen-Eigenschaft über **GetProps**. 
  
In der folgenden Tabelle werden wichtige Unterschiede zwischen den diese Eigenschaft **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) zusammengefasst. 
  
|**Merkmale**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Attachment-Objekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Auf Ordnerobjekten erforderlich  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachricht Store-Objekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Klicken Sie auf Status Objekte erforderlich  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Vom Client erstellt  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Vor dem Aufruf von **SaveChanges** verfügbar <br/> |Hängt vom anbieterimplementierung  <br/> |Hängt vom anbieterimplementierung  <br/> |Für Nachrichten, Ja. Für andere hängt von anbieterimplementierung.  <br/> |
|Geändert in einen Kopiervorgang  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Vom Client beim Kopieren eines veränderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Innerhalb eindeutig  <br/> |Weltweit  <br/> |Providerinstanz  <br/> |Weltweit  <br/> |
|Binär (mit Memcmp) vergleichbar.  <br/> |Keine Verwendung [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.
    
[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Gibt an, das Schema und die Methoden, die zum Anfordern von Informationen zur Verfügbarkeit für Benutzer und Ressourcen verwendet werden.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagStoreEntryId (kanonische Eigenschaft)](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

