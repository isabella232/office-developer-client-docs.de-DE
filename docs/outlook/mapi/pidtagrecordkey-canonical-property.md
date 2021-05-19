---
title: PidTagRecordKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355265"
---
# <a name="pidtagrecordkey-canonical-property"></a>PidTagRecordKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen binär-vergleichbaren Bezeichner für ein bestimmtes Objekt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECORD_KEY  <br/> |
|Kennung:  <br/> |0x0FF9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft erleichtert das Suchen von Verweisen auf ein Objekt, z. B. das Suchen der Zeile in einer Inhaltstabelle. Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. verwenden Sie zu diesem Zweck die Eintrags-ID.
  
Ein Anlagenunterobjekt sollte innerhalb einer Nachricht durch diese Eigenschaft eindeutig identifiziert werden. Dieser Bezeichner ist das einzige Anlagenmerkmal, das garantiert gleich bleibt, nachdem die Nachricht geschlossen und erneut geöffnet wurde. Der Speicheranbieter muss diese Eigenschaft sitzungsübergreifend beibehalten, um diese Garantie sicherzustellen.
  
Für Ordner enthält diese Eigenschaft einen Schlüssel, der in der Ordnerhierarchietabelle verwendet wird. In der Regel ist dies der gleiche Wert wie der wert, der von der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft bereitgestellt wird.
  
Bei Nachrichtenspeichern ist diese Eigenschaft mit der **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) identisch.
  
In einem Nachrichtenspeicherobjekt sollte diese Eigenschaft für alle Speicheranbieter eindeutig sein. Eine Möglichkeit besteht in der Kombination des Werts der **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))-Eigenschaft für den Speicher (eindeutig für diesen Anbietertyp) mit einer [GUID-Struktur](guid.md) oder einem anderen wert, der für den bestimmten Nachrichtenspeicher eindeutig ist. 
  
Diese Eigenschaft ist immer über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) verfügbar. Einige Anbieter können sie unmittelbar nach der Instanziierung verfügbar machen. 
  
Ein Client oder Dienstanbieter kann Werte aus dieser Eigenschaft mithilfe von memcmp vergleichen. Dies ist für Eintragsbezeichnerwerte nicht möglich. Diese Eigenschaft ist jedoch garantiert innerhalb desselben Nachrichtenspeichers oder Adressbuchcontainers eindeutig. Zwei Objekte aus unterschiedlichen Containern können denselben Wert dieser Eigenschaft haben.
  
Ein Unterschied zwischen dem Datensatz und den Suchtasten ist, dass der Datensatzschlüssel für das Objekt spezifisch ist, während der Suchschlüssel in andere Objekte kopiert werden kann. Beispielsweise können zwei Kopien des Objekts denselben wert **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) haben, müssen jedoch unterschiedliche Werte für diese Eigenschaft haben.
  
In der folgenden Tabelle werden wichtige Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst. 
  
|**Merkmal**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Anlagenobjekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicherobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Nach Client anknabel  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor einem Aufruf von **SaveChanges** <br/> |Vielleicht  <br/> |Vielleicht  <br/> |Nachrichten Ja Andere vielleicht  <br/> |
|In einem Kopiervorgang geändert  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Von einem Client nach einer Kopie ändernd  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig in ...  <br/> |Gesamte Welt  <br/> |Anbieterinstanz  <br/> |Gesamte Welt  <br/> |
|Binär vergleichbar (wie bei memcmp)  <br/> |Nein – Verwenden von **IMAPISupport:: CompareEntryIDs** <br/> |Ja  <br/> |Ja  <br/> |
   
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

