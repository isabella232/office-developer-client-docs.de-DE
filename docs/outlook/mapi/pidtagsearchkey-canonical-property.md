---
title: Kanonische Pidtagsearchkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345465"
---
# <a name="pidtagsearchkey-canonical-property"></a>Kanonische Pidtagsearchkey (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären-vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x300B  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft stellt eine Ablaufverfolgung für verwandte Objekte wie Nachrichtenkopien bereit und erleichtert das Auffinden unerwünschter Vorkommnisse wie doppelter Empfänger.
  
MAPI verwendet bestimmte Regeln zum Erstellen von Such Schlüsseln für Nachrichtenempfänger. Der Suchschlüssel wird durch Verkettung des Adresstyps (in Großbuchstaben), des Doppelpunktzeichens ":", der e-Mail-Adresse in kanonischer Form und des abschließenden NULL-Zeichens gebildet. Kanonische Form hier bedeuten, dass die Groß-/Kleinschreibung vertrauliche Adressen in der richtigen Groß-/Kleinschreibung angezeigt werden und Adressen, bei denen die Groß-/Kleinschreibung nicht beachtet wird, in Großbuchstaben umgewandelt werden. Dies ist wichtig, um Korrelationen zwischen Nachrichten beizubehalten.
  
Bei Message-Objekten ist diese Eigenschaft über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode unmittelbar nach der Erstellung der Nachricht verfügbar. Für andere Objekte ist Sie nach dem ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode verfügbar. Da diese Eigenschaft veränderbar ist, ist es unzuverlässig, Sie über getProps abzurufen, bis ein **SaveChanges** -Aufruf alle Werte festgelegt hat, die von der [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode gesetzt oder geändert wurden. **** 
  
Bei Profilen liefert MAPI auch einen hartcodierten Profil Abschnitt namens **MUID_PROFILE_INSTANCE**mit dieser Eigenschaft als einzelne Eigenschaft. Dieser Schlüssel ist unter allen jemals erstellten Profilen eindeutig und kann zuverlässiger sein als die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft, die beispielsweise gelöscht und mit demselben Namen neu erstellt werden kann.
  
In der folgenden Tabelle sind wichtige Unterschiede zwischen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.
  
|**Merkmal**|PR_ENTRYID * * * *|PR_RECORD_KEY * * * *|PR_SEARCH_KEY * * * *|
|:-----|:-----|:-----|:-----|
|Erforderlich für Attachment-Objekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderliche Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicher Objekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Erstellbarer Client  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor **SaveChanges** <br/> |Abhängig von der Anbieterimplementierung  <br/> |Abhängig von der Anbieterimplementierung  <br/> |Für Nachrichten, ja. Für andere ist es von der Anbieterimplementierung abhängig.  <br/> |
|Geändert in einem Kopiervorgang  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Nach einer Kopie nach dem Client änderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Innerhalb von...  <br/> |Ganze Welt  <br/> |Anbieterinstanz  <br/> |Ganze Welt  <br/> |
|Vergleichbare Binärdatei (wie bei memcmp)  <br/> |No--verwenden Sie [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagresponsibility (-Eigenschaft](pidtagresponsibility-canonical-property.md)
  
[Kanonische Pidtagstorerecordkey (-Eigenschaft](pidtagstorerecordkey-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

