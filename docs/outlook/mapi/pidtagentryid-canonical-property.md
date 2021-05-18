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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328588"
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
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft identifiziert ein Objekt für **OpenEntry,** das instanziiert werden soll, und ermöglicht den Zugriff auf alle eigenschaften über die entsprechende abgeleitete Schnittstelle von **IMAPIProp**. 
  
Diese Eigenschaft ist eine der Basisadresseneigenschaften für alle Messagingbenutzer. 
  
Diese Eigenschaft kann einen langfristigen oder einen kurzfristigen Bezeichner enthalten. Kurzfristige Bezeichner sind einfacher und schneller zu erstellen, sind jedoch in Umfang und Dauer beschränkt, in der Regel auf die aktuelle Sitzung und Arbeitsstation. Sie werden häufig für Objekte temporärer Art verwendet, z. B. Tabellenzeilen oder Dialogfeldeinträge, und dann abgebrochen. Langfristige Bezeichner werden für Objekte mit einem breiteren und langlebigeren Charakter verwendet. 
  
Diese Eigenschaft ist immer über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) verfügbar. Einige Dienstanbieter können sie unmittelbar nach der Instanziierung verfügbar machen. Der Anbieter muss immer einen langfristigen Eintragsbezeichner von **GetProps zurückgeben.** Um einen kurzfristigen Bezeichner in einen langfristigen Bezeichner zu konvertieren, öffnen Sie daher einfach das Objekt und erhalten dessen Eigenschaft über **GetProps**. 
  
In der folgenden Tabelle werden wichtige Unterschiede zwischen dieser Eigenschaft **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) zusammengefasst. 
  
|**Merkmal**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Anlagenobjekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicherobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Vom Client erstellt  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor dem Aufruf **von SaveChanges** <br/> |Abhängig von der Anbieterimplementierung  <br/> |Abhängig von der Anbieterimplementierung  <br/> |Bei Nachrichten ja. Bei anderen ist dies von der Anbieterimplementierung abhängig.  <br/> |
|In einem Kopiervorgang geändert  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Vom Client nach einer Kopie ändernd  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig innerhalb  <br/> |Gesamte Welt  <br/> |Anbieterinstanz  <br/> |Gesamte Welt  <br/> |
|Binär vergleichbar (wie bei memcmp)  <br/> |Keine Verwendung [von IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordnerberechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Gibt das Schema und die Methoden an, die zum Anfordern von Verfügbarkeitsinformationen für Benutzer und Ressourcen verwendet werden.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagStoreEntryId (kanonische Eigenschaft)](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

