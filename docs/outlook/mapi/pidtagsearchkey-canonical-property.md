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
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595391"
---
# <a name="pidtagsearchkey-canonical-property"></a>PidTagSearchKey (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären vergleichbaren Schlüssel, der für eine Suche korrelierte Objekte identifiziert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x300B  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft bietet eine Verfolgung für verknüpfte Objekte, wie Nachrichtenkopien, und suchen unerwünschte vorkommen, wie etwa doppelte Empfänger erleichtert.
  
MAPI verwendet spezielle Regeln zum Erstellen von Search-Schlüssel für Empfänger der Nachricht. Die suchen-Taste wird durch Verketten den Adresstyp (in Großbuchstaben) gebildet Doppelpunkt ":", die e-Mail-Adresse in kanonische Form und abschließendes Null-Zeichen. Kanonische Form hier bedeutet, dass die Groß-/Kleinschreibung beachtet Adressen werden in die Groß-/Kleinschreibung angezeigt und Adressen, die Groß-/ nicht Kleinschreibung in Großbuchstaben umgewandelt werden. Dies ist wichtig, können Sie die Korrelation zwischen Nachrichten zu erhalten.
  
Für die Message-Objekte ist diese Eigenschaft über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode unmittelbar nach Erstellung der Nachricht verfügbar. Bei anderen Objekten ist es nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zur Verfügung. Da diese Eigenschaft schreibgeschützt ist, ist es unzuverlässig über **GetProps** erhalten, bis das Gespräch **SaveChanges** Commit für alle Werte festgelegt oder geändert werden, von der [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode ausgeführt hat. 
  
Für Profile stellt MAPI auch einen hartcodiert und Profilabschnitt mit dem Namen **MUID_PROFILE_INSTANCE**, und diese Eigenschaft als ihre einzige Eigenschaft bereit. Dieser Schlüssel ist sichergestellt, dass für alle Profile jemals erstellten eindeutig sein und dürfen zuverlässiger als die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft, die kann, beispielsweise gelöscht und neu erstellt, mit dem gleichen Namen.
  
In der folgenden Tabelle werden die wichtigen Unterschiede zwischen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und diese Eigenschaft zusammengefasst.
  
|**Merkmale**|PR_ENTRYID ***|PR_RECORD_KEY ***|PR_SEARCH_KEY ***|
|:-----|:-----|:-----|:-----|
|Erforderlich für Attachment-Objekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Auf Ordnerobjekten erforderlich  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachricht Store-Objekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Klicken Sie auf Status Objekte erforderlich  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Vom Client erstellbare  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Bevor Sie **SaveChanges** verfügbar <br/> |Je nach anbieterimplementierung  <br/> |Je nach anbieterimplementierung  <br/> |Für Nachrichten, Ja. Für andere hängt die Implementierung des Anbieters.  <br/> |
|Geändert in einen Kopiervorgang  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Vom Client beim Kopieren eines veränderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Unique innerhalb...  <br/> |Weltweit  <br/> |Providerinstanz  <br/> |Weltweit  <br/> |
|Binär (mit Memcmp) vergleichbar.  <br/> |Nein – [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) verwenden <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagResponsibility (kanonische Eigenschaft)](pidtagresponsibility-canonical-property.md)
  
[PidTagStoreRecordKey (kanonische Eigenschaft)](pidtagstorerecordkey-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

