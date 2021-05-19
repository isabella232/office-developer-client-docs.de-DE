---
title: PidTagSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345465"
---
# <a name="pidtagsearchkey-canonical-property"></a>PidTagSearchKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binär-vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x300B  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft bietet eine Ablaufverfolgung für verwandte Objekte, z. B. Nachrichtenkopien, und erleichtert die Suche nach unerwünschten Vorkommen, z. B. doppelten Empfängern.
  
MAPI verwendet bestimmte Regeln zum Erstellen von Suchschlüsseln für Nachrichtenempfänger. Der Suchschlüssel wird durch Verkettung des Adresstyps (in Großbuchstaben), des Doppelpunktzeichens ":", der E-Mail-Adresse in kanonischer Form und des beendenden Nullzeichens gebildet. Das kanonische Formular bedeutet hier, dass groß-/kleinschreibungssensitive Adressen im richtigen Fall angezeigt werden, und Adressen, die nicht groß-/kleinschreibungsempfindlich sind, werden in Großbuchstaben konvertiert. Dies ist wichtig, um Korrelationen zwischen Nachrichten zu erhalten.
  
Für Nachrichtenobjekte steht diese Eigenschaft über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) unmittelbar nach der Nachrichtenerstellung zur Verfügung. Für andere Objekte steht sie nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode zur](imapiprop-savechanges.md) Verfügung. Da diese Eigenschaft änderbar ist, ist es unzuverlässig, sie über **GetProps** zu erhalten, bis ein **SaveChanges-Aufruf** werte festgelegt oder von der [IMAPIProp::SetProps-Methode geändert](imapiprop-setprops.md) hat. 
  
Für Profile bietet MAPI auch einen hart codierten Profilabschnitt namens **MUID_PROFILE_INSTANCE**, mit dieser Eigenschaft als einzelne Eigenschaft. Dieser Schlüssel ist unter allen profilen, die jemals erstellt wurden, eindeutig und kann zuverlässiger sein als die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft, die beispielsweise gelöscht und mit demselben Namen neu erstellt werden kann.
  
In der folgenden Tabelle werden wichtige Unterschiede zwischen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.
  
|**Merkmal**|PR_ENTRYID****|PR_RECORD_KEY****|PR_SEARCH_KEY****|
|:-----|:-----|:-----|:-----|
|Erforderlich für Anlagenobjekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicherobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Nach Client anknabel  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor **SaveChanges** <br/> |Hängt von der Anbieterimplementierung ab  <br/> |Hängt von der Anbieterimplementierung ab  <br/> |Bei Nachrichten ja. Für andere hängt es von der Anbieterimplementierung ab.  <br/> |
|In einem Kopiervorgang geändert  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Vom Client nach einer Kopie ändernd  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig in ...  <br/> |Gesamte Welt  <br/> |Anbieterinstanz  <br/> |Gesamte Welt  <br/> |
|Binär vergleichbar (wie bei memcmp)  <br/> |Nein – Verwenden von [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagResponsibility (kanonische Eigenschaft)](pidtagresponsibility-canonical-property.md)
  
[PidTagStoreRecordKey (kanonische Eigenschaft)](pidtagstorerecordkey-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

