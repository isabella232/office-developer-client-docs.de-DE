---
title: Kanonische Pidtagrecordkey (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355265"
---
# <a name="pidtagrecordkey-canonical-property"></a>Kanonische Pidtagrecordkey (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen, Binär-vergleichbaren Bezeichner für ein bestimmtes Objekt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECORD_KEY  <br/> |
|Kennung:  <br/> |0x0FF9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft erleichtert das Auffinden von Verweisen auf ein Objekt, wie beispielsweise die Suche nach der Zeile in einer Inhaltstabelle. Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. Verwenden Sie dazu die Eintrags-ID.
  
Ein Attachment-Unterobjekt sollte innerhalb einer Nachricht durch diese Eigenschaft eindeutig identifiziert werden. Dieser Bezeichner ist das einzige Anlagen Merkmal, das garantiert bleiben muss, nachdem die Nachricht geschlossen und erneut geöffnet wurde. Der Informationsspeicher Anbieter muss diese Eigenschaft in allen Sitzungen aufbewahren, um diese Garantie sicherzustellen.
  
Bei Ordnern enthält diese Eigenschaft einen Schlüssel, der in der Ordner Hierarchietabelle verwendet wird. In der Regel ist dies derselbe Wert wie der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft.
  
Für Nachrichtenspeicher ist diese Eigenschaft mit der **PR_STORE_RECORD_KEY** ([pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))-Eigenschaft identisch.
  
In einem Nachrichtenspeicherobjekt sollte diese Eigenschaft für alle Speicheranbieter eindeutig sein. Eine Möglichkeit hierfür besteht darin, den Wert der **PR_MDB_PROVIDER** ([pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))-Eigenschaft für den Store (eindeutig für diesen Anbietertyp) mit einer [GUID](guid.md) -Struktur oder einem anderen Wert zu kombinieren, der eindeutig für den jeweiligen Nachrichtenspeicher ist. 
  
Diese Eigenschaft steht immer über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode nach dem ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode zur Verfügung. Einige Anbieter können diese sofort nach der Instanziierung zur Verfügung stellen. 
  
Ein Client oder Dienstanbieter kann Werte dieser Eigenschaft mithilfe von memcmp vergleichen. Dies ist für Eintrags-ID-Werte nicht möglich. Diese Eigenschaft ist jedoch garantiert innerhalb desselben Nachrichtenspeichers oder Adressbuch Containers eindeutig. zwei Objekte aus unterschiedlichen Containern können denselben Wert dieser Eigenschaft aufweisen.
  
Eine Unterscheidung zwischen dem Record-und dem Suchschlüssel besteht darin, dass der Record-Schlüssel spezifisch für das Objekt ist, wohingegen der Suchschlüssel in andere Objekte kopiert werden kann. Beispielsweise können zwei Kopien des Objekts denselben **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Wert aufweisen, aber Sie müssen unterschiedliche Werte für diese Eigenschaft aufweisen.
  
In der folgenden Tabelle sind wichtige Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst. 
  
|**Merkmal**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Attachment-Objekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderliche Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicher Objekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Erstellbarer Client  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor einem Aufruf von **SaveChanges** <br/> |Leicht  <br/> |Leicht  <br/> |Nachrichten ja andere vielleicht  <br/> |
|Geändert in einem Kopiervorgang  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Von einem Client nach einer Kopie änderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Innerhalb von...  <br/> |Ganze Welt  <br/> |Anbieterinstanz  <br/> |Ganze Welt  <br/> |
|Vergleichbare Binärdatei (wie bei memcmp)  <br/> |No--verwenden Sie **IMAPISupport:: CompareEntryIDs** <br/> |Ja  <br/> |Ja  <br/> |
   
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

