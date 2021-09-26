---
title: Kanonische PidTagSearchKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 59d604d347ff0788c5075a828a42ef47cb3b6212
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624510"
---
# <a name="pidtagsearchkey-canonical-property"></a>Kanonische PidTagSearchKey-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen mit Binärdaten vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x300B  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft stellt eine Ablaufverfolgung für verwandte Objekte bereit, z. B. Nachrichtenkopien, und erleichtert das Auffinden unerwünschter Vorkommen, z. B. doppelter Empfänger.
  
DIE MAPI verwendet bestimmte Regeln zum Erstellen von Suchschlüsseln für Nachrichtenempfänger. Der Suchschlüssel wird durch Verketten des Adresstyps (in Großbuchstaben), des Doppelpunktzeichens ":", der E-Mail-Adresse in kanonischer Form und des endenden NULL-Zeichens gebildet. Die kanonische Form bedeutet hier, dass Adressen, bei denen groß- und kleingeschrieben wird, im richtigen Fall angezeigt werden und Adressen, bei denen die Groß-/Kleinschreibung nicht beachtet wird, in Großbuchstaben konvertiert werden. Dies ist wichtig, um Die Korrelationen zwischen Nachrichten zu erhalten.
  
Für Nachrichtenobjekte steht diese Eigenschaft über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) unmittelbar nach der Nachrichtenerstellung zur Verfügung. Für andere Objekte ist sie nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) verfügbar. Da diese Eigenschaft veränderbar ist, ist es unzuverlässig, sie über **GetProps** abzurufen, bis für einen **SaveChanges-Aufruf** ein Commit für von der [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) festgelegte oder geänderte Werte ausgeführt wurde. 
  
Für Profile stellt MAPI auch einen hartcodierten Profilabschnitt mit dem Namen **MUID_PROFILE_INSTANCE** bereit, wobei diese Eigenschaft als einzelne Eigenschaft gilt. Dieser Schlüssel ist garantiert für alle erstellten Profile eindeutig und kann zuverlässiger als die **eigenschaft PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) sein, die z. B. mit demselben Namen gelöscht und neu erstellt werden kann.
  
In der folgenden Tabelle werden wichtige Unterschiede zwischen den **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.
  
|**Merkmal**|PR_ENTRYID|PR_RECORD_KEY|PR_SEARCH_KEY|
|:-----|:-----|:-----|:-----|
|Erforderlich für Anlagenobjekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicherobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Erstellbar nach Client  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor **SaveChanges** <br/> |Hängt von der Anbieterimplementierungen ab.  <br/> |Hängt von der Anbieterimplementierungen ab.  <br/> |Bei Nachrichten: Ja. Bei anderen hängt dies von der Anbieterimplementierung ab.  <br/> |
|In einem Kopiervorgang geändert  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Nach einer Kopie vom Client veränderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig innerhalb ...  <br/> |Gesamte Welt  <br/> |Anbieterinstanz  <br/> |Gesamte Welt  <br/> |
|Binär vergleichbar (wie bei memcmp)  <br/> |Nein -- verwenden Sie [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagResponsibility-Eigenschaft](pidtagresponsibility-canonical-property.md)
  
[Kanonische PidTagStoreRecordKey-Eigenschaft](pidtagstorerecordkey-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

