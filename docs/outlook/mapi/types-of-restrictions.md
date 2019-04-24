---
title: Arten von Einschränkungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356567"
---
# <a name="types-of-restrictions"></a>Arten von Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele Arten von Einschränkungen, einige, die sich auf bestimmte Spalten konzentrieren. Es wird davon ausgegangen, dass alle Tabellen Implementierungen Einschränkungen für die Spalten in der aktuellen Spaltengruppe unterstützen. Zum Hinzufügen von Wert können Tabellen Implementierer auch Einschränkungen basierend auf Objekteigenschaften unterstützen, die derzeit nicht in der Tabellenansicht sind.
  
Einige Einschränkungen können mit einer Einschränkung kombiniert werden, die einen logischen **and**- **oder**- **Not** -Vorgang ausführt. Beispielsweise müssen die meisten Eigenschaftseinschränkungen mit exist-Einschränkungen **und** Einschränkungen verbunden werden. Es gibt einige Ausnahmen, beispielsweise wenn die Eigenschaft, die in der Eigenschaftseinschränkung verwendet wird, die **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaft oder eine erforderliche Spalte in einer Tabelle ist. Ein Client Building Einschränkungen zum Einschränken der Ansicht sollte exist-Einschränkungen mit seiner Eigenschaft Einschränkungen verwenden, da MAPI nicht angeben, wie Dienstanbieter Eigenschafteneinschränkungen auswerten sollten, wenn eine Eigenschaft nicht vorhanden ist. Es ist sinnvoll und empfehlenswert, dass Dienstanbieter die Einschränkung nicht erfüllen, aber es gibt keine Anforderungen. 
  
Eine Einschränkung wird mithilfe der [SRestriction](srestriction.md) -Datenstruktur definiert, die eine Vereinigung spezieller Einschränkungs Strukturen und einen Indikator für den in der Union enthaltenen Strukturtyp enthält. 
  
Jede der spezialisierten Einschränkungs Strukturen in der Union stellt eine andere Art von Einschränkung dar. Die Arten von Einschränkungen und die zugehörigen Datenstrukturen sind:
  
|**Art der Einschränkung**|**Zugeordnete Datenstruktur**|**Beschreibung**|
|:-----|:-----|:-----|
|Compare-Eigenschaft  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Vergleicht zwei Eigenschaften desselben Typs.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Führt eine logische **and-** Operation für zwei oder mehr Einschränkungen aus.  <br/> |
|**ODER** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Führt eine logische **or** -Operation für zwei oder mehr Einschränkungen aus.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Führt einen logischen **Not** -Vorgang für zwei oder mehr Einschränkungen aus.  <br/> |
|Inhalt  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Sucht nach angegebenen Daten.  <br/> |
|Eigenschaft  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Gibt einen bestimmten Eigenschaftswert als Kriterien für den Abgleich an. Kann beispielsweise für die Suche nach einem bestimmten Anlagentyp verwendet werden.  <br/> |
|Bitmaske  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Wendet eine Bitmaske auf eine PT_LONG-Eigenschaft an, in der Regel, um zu bestimmen, ob bestimmte Flags festgelegt sind.  <br/> |
|Größe  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Testet die Größe einer Eigenschaft mit standardmäßigen relationalen Operatoren.  <br/> |
|Existieren  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Testet, ob ein Objekt einen Wert für eine Eigenschaft aufweist.  <br/> |
|SubObject  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Wird zum Durchsuchen von Unterobjekten oder Objekten verwendet, auf die nicht mit einer Eintrags-ID wie Empfängern und Anlagen zugegriffen werden kann. Kann verwendet werden, um beispielsweise nach Nachrichten für einen bestimmten Empfänger zu suchen.  <br/> |
|Kommentar  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Ordnet ein Objekt mit einem Satz benannter Eigenschaften zu.  <br/> |
   
Einige Einschränkungen verwenden reguläre Ausdrücke, und MAPI unterstützt eine begrenzte Form von Notation für reguläre Ausdrücke in der Formatvorlage, die viele Textanwendungen verwendet wird.
  
Die Kommentar Einschränkung wird von Clients verwendet, die Einschränkungen auf dem Datenträgerspeichern, um anwendungsspezifische Informationen mit der Einschränkung beizubehalten. Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft speichert, die in einer Eigenschaftseinschränkung verwendet wird, dies mit einer Kommentar Einschränkung tun. Das Speichern des Namens ist in einer Eigenschaftseinschränkung nicht möglich; die [SPropertyRestriction](spropertyrestriction.md) -Datenstruktur enthält nur das Property-Tag. Kommentar Einschränkungen werden von [IMAPITable:: Restrict](imapitable-restrict.md) insofern ignoriert, dass Sie keine Auswirkungen auf die von [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegebenen Zeilen haben, nachdem ein **Restrict** -Aufruf ausgeführt wurde. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

