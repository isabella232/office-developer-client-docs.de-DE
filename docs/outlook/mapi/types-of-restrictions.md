---
title: Arten von Einschränkungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3fd12f2bed213bf48db18b8dacafc8d522439140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590898"
---
# <a name="types-of-restrictions"></a>Arten von Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele Arten von Einschränkungen, von denen sich einige auf bestimmte Spalten konzentrieren. Es wird erwartet, dass alle Tabellenimplementierungen Einschränkungen für die Spalten im aktuellen Spaltensatz unterstützen. Um einen Mehrwert hinzuzufügen, können Tabellen implementierer jedoch auch Einschränkungen basierend auf Objekteigenschaften unterstützen, die sich derzeit nicht in der Tabellenansicht befinden.
  
Einige Einschränkungen können mithilfe einer Einschränkung kombiniert werden, die einen logischen **AND-,** **OR-** oder **NOT-Vorgang** ausführt. Beispielsweise müssen die meisten Eigenschaftseinschränkungen mit vorhandenen Einschränkungen verknüpft werden, die **AND-Einschränkungen** verwenden. Es gibt einige Ausnahmen, z. B. wenn die Eigenschaft, die in der Eigenschaftseinschränkung verwendet wird, die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaft ist oder wenn es sich um eine erforderliche Spalte in einer Tabelle handelt. Bei Clienterstellungseinschränkungen zum Einschränken der Ansicht sollten Einschränkungen mit den Zugehörigen Eigenschaftseinschränkungen verwendet werden, da MAPI nicht angibt, wie Dienstanbieter Eigenschaftseinschränkungen auswerten sollen, wenn keine Eigenschaft vorhanden ist. Es ist sinnvoll und wird empfohlen, dass Dienstanbieter die Einschränkung nicht bestehen, es jedoch keine Anforderungen gibt. 
  
Eine Einschränkung wird mithilfe der [SRestriction-Datenstruktur](srestriction.md) definiert, die eine Vereinigung von spezielleren Einschränkungsstrukturen und einen Indikator für den Typ der Struktur enthält, die in der Vereinigung enthalten ist. 
  
Jede der spezialisierten Einschränkungsstrukturen in der Vereinigung stellt einen anderen Einschränkungstyp dar. Die Arten von Einschränkungen und die zugehörigen Datenstrukturen sind:
  
|**Einschränkungstyp**|**Zugeordnete Datenstruktur**|**Beschreibung**|
|:-----|:-----|:-----|
|Compare-Eigenschaft  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Vergleicht zwei Eigenschaften desselben Typs.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Führt einen logischen **AND-Vorgang** für mindestens zwei Einschränkungen aus.  <br/> |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Führt einen **logischen OR-Vorgang** für mindestens zwei Einschränkungen aus.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Führt einen logischen **NOT-Vorgang** für mindestens zwei Einschränkungen aus.  <br/> |
|Inhalt  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Sucht angegebene Daten.  <br/> |
|Eigenschaft  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Gibt einen bestimmten Eigenschaftswert als Kriterien für den Abgleich an. Kann beispielsweise verwendet werden, um nach einem bestimmten Anlagentyp zu suchen.  <br/> |
|Bitmaske  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Wendet eine Bitmaske auf eine PT_LONG Eigenschaft an, in der Regel, um zu bestimmen, ob bestimmte Flags festgelegt sind.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Testet die Größe einer Eigenschaft mithilfe von relationalen Standardoperatoren.  <br/> |
|Existieren  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Überprüft, ob ein Objekt einen Wert für eine Eigenschaft aufweist.  <br/> |
|Unterobjekt  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Wird zum Durchsuchen von Unterobjekten oder Objekten verwendet, auf die nicht mit einem Eintragsbezeichner zugegriffen werden kann, z. B. Empfänger und Anlagen. Kann beispielsweise verwendet werden, um nach Nachrichten für einen bestimmten Empfänger zu suchen.  <br/> |
|Kommentar  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Ordnet ein Objekt einer Gruppe benannter Eigenschaften zu.  <br/> |
   
Einige Einschränkungen verwenden reguläre Ausdrücke, und mapi unterstützt eine begrenzte Form der Notation regulärer Ausdrücke in der Formatvorlage, die viele Textanwendungen verwendet wird.
  
Die Kommentareinschränkung wird von Clients verwendet, die Einschränkungen auf dem Datenträger speichern, um anwendungsspezifische Informationen mit der Einschränkung beizubehalten. Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft speichert, die in einer Eigenschaftseinschränkung verwendet wird, dies mit einer Kommentareinschränkung tun. Das Speichern des Namens ist in einer Eigenschaftseinschränkung nicht möglich. Die [SPropertyRestriction-Datenstruktur](spropertyrestriction.md) enthält nur das Eigenschaftstag. Kommentareinschränkungen werden von [IMAPITable::Restrict](imapitable-restrict.md) ignoriert, da sie keine Auswirkungen auf die Zeilen haben, die von [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden, nachdem ein **Restrict-Aufruf** ausgeführt wurde. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

