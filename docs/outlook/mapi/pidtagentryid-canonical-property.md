---
title: Kanonische PidTagEntryId-Eigenschaft
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
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328588"
---
# <a name="pidtagentryid-canonical-property"></a>Kanonische PidTagEntryId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine MAPI-Eintrags-ID zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ENTRYID  <br/> |
|Kennung:  <br/> |0X0fff dar  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft identifiziert ein Objekt für **OpenEntry** zum Instanziieren und ermöglicht den Zugriff auf alle Eigenschaften über die entsprechende abgeleitete Schnittstelle von **IMAPIProp**. 
  
Diese Eigenschaft ist eine der Basis Adresseigenschaften für alle Messagingbenutzer. 
  
Diese Eigenschaft kann einen langfristigen oder einen kurzfristigen Bezeichner enthalten. Kurzfristige Bezeichner sind einfacher und schneller zu konstruieren, sind jedoch in ihrem Umfang und ihrer Dauer begrenzt, in der Regel für die aktuelle Sitzung und Workstation. Sie werden häufig für Objekte temporärer Art wie Tabellenzeilen oder Dialogfeld Einträge verwendet und dann abgebrochen. Langfristige Bezeichner werden für Objekte mit einer breiteren und langlebigen Art verwendet. 
  
Diese Eigenschaft steht immer über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode nach dem ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode zur Verfügung. Einige Dienstanbieter können diese sofort nach der Instanziierung zur Verfügung stellen. Der Anbieter muss immer eine langfristige Eintrags-ID aus **** GetProps zurückgeben. Um einen kurzfristigen Bezeichner zu langfristig zu konvertieren, öffnen Sie daher einfach das Objekt, und rufen Sie dessen this-Eigenschaft **** über GetProps ab. 
  
In der folgenden Tabelle sind wichtige Unterschiede zwischen dieser Eigenschaft, **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) zusammengefasst. 
  
|**Merkmal**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Attachment-Objekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderliche Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicher Objekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Erstellt von Client  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor dem Aufruf **** von SaveChanges <br/> |Abhängig von der Anbieterimplementierung  <br/> |Abhängig von der Anbieterimplementierung  <br/> |Für Nachrichten, ja. Für andere ist abhängig von der Anbieterimplementierung.  <br/> |
|Geändert in einem Kopiervorgang  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Nach einer Kopie nach dem Client änderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig innerhalb  <br/> |Ganze Welt  <br/> |Anbieterinstanz  <br/> |Ganze Welt  <br/> |
|Vergleichbare Binärdatei (wie bei memcmp)  <br/> |Keine Verwendung [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Gibt das Schema und die Methoden an, die zum Anfordern von Verfügbarkeitsinformationen für Benutzer und Ressourcen verwendet werden.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagstoreentryid (-Eigenschaft](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

