---
title: Kanonische PidTagRecordKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96e509e1348bf3996d1f73d2f7a14d4f386774f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587209"
---
# <a name="pidtagrecordkey-canonical-property"></a>Kanonische PidTagRecordKey-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen, mit Binärdaten vergleichbaren Bezeichner für ein bestimmtes Objekt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECORD_KEY  <br/> |
|Kennung:  <br/> |0x0FF9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft erleichtert das Auffinden von Verweisen auf ein Objekt, z. B. das Suchen seiner Zeile in einem Inhaltsverzeichnis. Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. verwenden Sie den Eintragsbezeichner für diesen Zweck.
  
Ein Anlagenunterobjekt sollte innerhalb einer Nachricht durch diese Eigenschaft eindeutig identifiziert werden. Dieser Bezeichner ist das einzige Anlagenmerkmal, das garantiert gleich bleibt, nachdem die Nachricht geschlossen und erneut geöffnet wurde. Der Speicheranbieter muss diese Eigenschaft sitzungsübergreifend beibehalten, um diese Garantie sicherzustellen.
  
Für Ordner enthält diese Eigenschaft einen Schlüssel, der in der Ordnerhierarchietabelle verwendet wird. In der Regel ist dies derselbe Wert wie der von der **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) bereitgestellte Wert.
  
Bei Nachrichtenspeichern ist diese Eigenschaft identisch mit der **eigenschaft PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
In einem Nachrichtenspeicherobjekt sollte diese Eigenschaft für alle Speicheranbieter eindeutig sein. Eine Möglichkeit besteht darin, den Wert der **eigenschaft PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) für den Informationsspeicher (für diesen Anbietertyp eindeutig) mit einer [GUID-Struktur](guid.md) oder einem anderen für den jeweiligen Nachrichtenspeicher eindeutigen Wert zu kombinieren. 
  
Diese Eigenschaft ist nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode immer über die IMAPIProp::GetProps-Methode](imapiprop-savechanges.md) verfügbar. [](imapiprop-getprops.md) Einige Anbieter können sie unmittelbar nach der Instanziierung verfügbar machen. 
  
Ein Client oder Dienstanbieter kann Werte aus dieser Eigenschaft mithilfe von Memcmp vergleichen. Dies ist für Eintragsbezeichnerwerte nicht möglich. Diese Eigenschaft ist jedoch garantiert innerhalb desselben Nachrichtenspeichers oder Adressbuchcontainers eindeutig. Zwei Objekte aus unterschiedlichen Containern können denselben Wert dieser Eigenschaft haben.
  
Ein Unterschied zwischen Datensatz- und Suchschlüsseln besteht darin, dass der Datensatzschlüssel für das Objekt spezifisch ist, während der Suchschlüssel in andere Objekte kopiert werden kann. Beispielsweise können zwei Kopien des Objekts denselben **wert PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) aufweisen, müssen jedoch unterschiedliche Werte für diese Eigenschaft aufweisen.
  
In der folgenden Tabelle werden wichtige Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst. 
  
|**Merkmal**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Erforderlich für Anlagenobjekte  <br/> |Nein  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Ordnerobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Nachrichtenspeicherobjekte  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Erforderlich für Statusobjekte  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|Erstellbar nach Client  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Verfügbar vor einem Aufruf von **SaveChanges** <br/> |Vielleicht  <br/> |Vielleicht  <br/> |Nachrichten ja, andere vielleicht  <br/> |
|In einem Kopiervorgang geändert  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|Von einem Client nach einer Kopie veränderbar  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|Eindeutig innerhalb ...  <br/> |Gesamte Welt  <br/> |Anbieterinstanz  <br/> |Gesamte Welt  <br/> |
|Binär vergleichbar (wie bei memcmp)  <br/> |Nein -- **verwenden Sie IMAPISupport:: CompareEntryIDs** <br/> |Ja  <br/> |Ja  <br/> |
   
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

