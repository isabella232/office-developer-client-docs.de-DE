---
title: Arten von Einschränkungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85cf254c9ea23ecbd6f311ba012d2e048a0b2a6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572445"
---
# <a name="types-of-restrictions"></a>Arten von Einschränkungen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Es gibt viele Arten von Einschränkungen, einige, den Fokus auf bestimmte Spalten. Alle Tabelle Implementierungen sind zur Unterstützung von Einschränkungen für die Spalten in der aktuellen Spalte Gruppe erwartet. Jedoch können Wert Tabelle Implementierer auch unterstützen Einschränkungen basierend auf Objekteigenschaften, die derzeit nicht in der Tabellenansicht sind.
  
Einige Einschränkungen können mit einer Einschränkung, die eine logische **und**, **oder**oder **nicht** ausführt kombiniert werden. Beispielsweise die meisten-Eigenschaft, die mit Einschränkungen verknüpft werden müssen **und** Einschränkungen von Einschränkungen vorhanden. Es gibt einige Ausnahmen, z. B., wenn die Eigenschaft in der eigenschaftseinschränkung, die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaft ist oder wenn es sich um eine erforderliche Spalte in einer Tabelle ist. Ein Client erstellen Einschränkungen zur Begrenzung der Ansicht verwenden sollte Einschränkungen mit den Suchkriterien in Eigenschaft vorhanden sein, da MAPI nicht festlegt, wie Dienstanbieter Suchkriterien in Eigenschaft ausgewertet werden soll, wenn eine Eigenschaft nicht vorhanden ist. Es ist angemessen und empfohlen, Dienstanbieter die Einschränkung Fehler, aber es keine Anforderungen sind. 
  
Eine Einschränkung wird mithilfe der [SRestriction](srestriction.md) -Datenstruktur, die eine Vereinigung von speziellere Einschränkung Strukturen und ein Indikator vom Typ der Union-Struktur enthält definiert. 
  
Jede Struktur spezialisierte Einschränkung in der Union stellt eine andere Art von Einschränkung. Die Arten von Einschränkungen und ihre zugehörigen Datenstrukturen sind:
  
|**Typ der Einschränkung**|**Struktur der zugehörigen Daten**|**Beschreibung**|
|:-----|:-----|:-----|
|Vergleichen-Eigenschaft  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Vergleicht zwei Eigenschaften des gleichen Typs.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Führt eine logische **AND** -Operation mit zwei oder mehr Einschränkungen.  <br/> |
|**ODER** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Führt eine logische **OR** -Operation für zwei oder mehr Einschränkungen.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Führt eine logische **NOT** -Operation für zwei oder mehr Einschränkungen.  <br/> |
|Inhalt  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Sucht angegebene Daten.  <br/> |
|Eigenschaft  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Gibt den Wert einer bestimmten Eigenschaft als Kriterium für den Abgleich. Kann beispielsweise verwendet werden für einen bestimmten Typ Anlage suchen.  <br/> |
|Bitmaske  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Eine Bitmaske gilt in der Regel zu einer Eigenschaft PT_LONG, um festzustellen, ob bestimmte Flags festgelegt sind.  <br/> |
|Größe  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Die Größe einer Eigenschaft über die standardmäßigen relationale Operatoren getestet.  <br/> |
|Vorhanden  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Überprüft, ob ein Objekt einen Wert für eine Eigenschaft verfügt.  <br/> |
|Unterobjekt  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Verwendet für die Suche über Unterobjekte oder -Objekten, die mit einem Eintrag Bezeichner, wie Empfänger und Anlagen nicht zugegriffen werden können. Kann beispielsweise verwendet werden nach einem bestimmten Empfänger nach Nachrichten gesucht.  <br/> |
|Kommentar  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Ordnet eine Reihe von benannten Eigenschaften ein Objekt hinzu.  <br/> |
   
Einige Einschränkungen mithilfe von regulären Ausdrücken und MAPI unterstützt eingeschränkte des regulären Ausdrucks Notation im Format, die viele Text Clientanwendungen verwendet.
  
Die Einschränkung der Kommentar wird von Clients verwendet, die auf dem Datenträger beibehalten anwendungsspezifische Informationen mit der Einschränkung Einschränkungen speichern. Beispielsweise kann ein Client, speichern den Namen einer benannten Eigenschaft verwendet, in einer eigenschaftseinschränkung mit einer Einschränkung Kommentar tun. Speichern den Namen ist nicht möglich in eine eigenschaftseinschränkung; die [SPropertyRestriction](spropertyrestriction.md) -Datenstruktur enthält das Eigenschafts-Tag. Kommentar Einschränkungen werden durch die [Methode IMAPITable:: Restrict](imapitable-restrict.md) ignoriert, sie haben keinen Einfluss auf die Zeilen von [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben wird, nachdem ein Anruf **Restrict** vorgenommen wurde. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

