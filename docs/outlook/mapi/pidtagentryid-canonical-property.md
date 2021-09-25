---
title: PidTagEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 42e105ee5addca6445c3ee0ef667c873192d66e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616509"
---
# <a name="pidtagentryid-canonical-property"></a>PidTagEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen MAPI-Eintragsbezeichner, der zum Öffnen und Bearbeiten von Eigenschaften eines bestimmten MAPI-Objekts verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ENTRYID  <br/> |
|Kennung:  <br/> |0x0FFF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft identifiziert ein Objekt, das von **OpenEntry** instanziiert werden soll, und ermöglicht den Zugriff auf alle seine Eigenschaften über die entsprechende abgeleitete Schnittstelle von **IMAPIProp.** 
  
Diese Eigenschaft ist eine der Basisadresseigenschaften für alle Messagingbenutzer. 
  
Diese Eigenschaft kann entweder einen langfristigen bezeichner oder einen kurzfristigen Bezeichner enthalten. Kurzfristige Bezeichner sind einfacher und schneller zu erstellen, sind jedoch in ihrem Umfang und ihrer Dauer begrenzt, in der Regel auf die aktuelle Sitzung und Arbeitsstation. Sie werden häufig für Objekte temporärer Art, z. B. Tabellenzeilen oder Dialogfeldeinträge, verwendet und dann abgebrochen. Langfristige Bezeichner werden für Objekte mit einer umfassenderen und dauerhafteren Art verwendet. 
  
Diese Eigenschaft ist nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode immer über die IMAPIProp::GetProps-Methode](imapiprop-savechanges.md) verfügbar. [](imapiprop-getprops.md) Einige Dienstanbieter können sie unmittelbar nach der Instanziierung zur Verfügung stellen. Der Anbieter muss immer einen langfristigen Eintragsbezeichner aus **GetProps** zurückgeben. Um einen kurzfristigen Bezeichner in einen langfristigen Bezeichner zu konvertieren, öffnen Sie das Objekt, und rufen Sie seine Eigenschaft über **GetProps** ab. 
  
Die folgende Tabelle fasst wichtige Unterschiede zwischen dieser **Eigenschaft, PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) zusammen. 
  
|**Merkmal**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Anlagenobjekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicherobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Erstellt vom Client  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor dem Aufruf von **SaveChanges** <br/> |Hängt von der Implementierung des Anbieters ab.  <br/> |Hängt von der Implementierung des Anbieters ab.  <br/> |Bei Nachrichten: Ja. Für andere hängt von der Anbieterimplementierung ab.  <br/> |
|In einem Kopiervorgang geändert  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Nach einer Kopie vom Client veränderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig innerhalb  <br/> |Gesamte Welt  <br/> |Anbieterinstanz  <br/> |Gesamte Welt  <br/> |
|Binär vergleichbar (wie bei memcmp)  <br/> |Verwenden Sie [IMAPISupport nicht:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt den Abruf von Ordnerberechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden mit und Konfigurieren von Postfächern als Stellvertretungen und Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers handeln.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Gibt das Schema und die Methoden an, die zum Anfordern von Verfügbarkeitsinformationen für Benutzer und Ressourcen verwendet werden.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagStoreEntryId (kanonische Eigenschaft)](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

