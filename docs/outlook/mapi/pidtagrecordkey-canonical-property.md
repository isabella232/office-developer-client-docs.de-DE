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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401699"
---
# <a name="pidtagrecordkey-canonical-property"></a>PidTagRecordKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären vergleichbaren eindeutigen Bezeichner für ein bestimmtes Objekt an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECORD_KEY  <br/> |
|Kennung:  <br/> |0x0FF9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft erleichtert das Auffinden Verweise auf ein Objekt, wie eine Zeile in einer Inhaltstabelle suchen. Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. Verwenden Sie die Eintrags-ID für diesen Zweck.
  
Eine Anlage Unterobjekts sollten innerhalb einer Nachricht von dieser Eigenschaft eindeutig identifiziert werden. Dieser Bezeichner ist das einzige Anlage Merkmal garantiert gleich bleiben, nachdem die Meldung geschlossen und erneut geöffnet wird. Der Anbieter muss diese Eigenschaft in allen Sitzungen, um sicherzustellen, dass diese Garantie beibehalten.
  
Für Ordner enthält diese Eigenschaft einen Schlüssel in der Ordner-Hierarchie-Tabelle verwendet. In der Regel ist dies den gleichen Wert wie, die durch die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) bereitgestellt.
  
Für Nachrichtenspeicher ist diese Eigenschaft der **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))-Eigenschaft identisch.
  
In einem Message Store-Objekt sollten diese Eigenschaft für alle Anbieter eindeutig sein. Eine Möglichkeit, dies ist den Wert der Eigenschaft **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) für den Speicher (eindeutig für diesen Anbietertyp) mit einer [GUID](guid.md) -Struktur oder einen anderen Wert für den bestimmten Nachrichtenspeicher eindeutig zu kombinieren. 
  
Diese Eigenschaft ist immer über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode verfügbar. Einige Anbieter können sie sofort nach der Instanziierung zur Verfügung. 
  
Ein Client oder Dienstanbieter kann Werte aus dieser Eigenschaft mithilfe von Memcmp vergleichen. Dies ist nicht möglich, für die Eintrags-ID-Werte. Jedoch ist diese Eigenschaft Sicherheit innerhalb der gleichen Nachrichtenspeicher eindeutig sein oder address Book Container. zwei Objekte aus unterschiedlichen Containern können den gleichen Wert dieser Eigenschaft aufweisen.
  
Eine Unterscheidung zwischen den Schlüsseln Datensatz, und suchen Sie ist, dass der Datensatzschlüssel speziell für das Objekt ist, während die suchen-Taste auf andere Objekte kopiert werden kann. Beispielsweise zwei Kopien des Objekts können den gleichen Wert **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) haben jedoch unterschiedliche Werte für diese Eigenschaft aufweisen müssen.
  
In der folgenden Tabelle werden die wichtigen Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) und diese Eigenschaft zusammengefasst. 
  
|**Merkmale**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Attachment-Objekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Auf Ordnerobjekten erforderlich  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachricht Store-Objekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Klicken Sie auf Status Objekte erforderlich  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Vom Client erstellbare  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Vor einem Aufruf von **SaveChanges** verfügbar <br/> |Vielleicht  <br/> |Vielleicht  <br/> |Nachrichten Ja andere vielleicht  <br/> |
|Geändert in einen Kopiervorgang  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Von einem Client beim Kopieren eines veränderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Unique innerhalb...  <br/> |Weltweit  <br/> |Providerinstanz  <br/> |Weltweit  <br/> |
|Binär (mit Memcmp) vergleichbar.  <br/> |Nein – verwenden Sie **IMAPISupport:: CompareEntryIDs** <br/> |Ja  <br/> |Ja  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

