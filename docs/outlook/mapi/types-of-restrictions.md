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
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416286"
---
# <a name="types-of-restrictions"></a>Arten von Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele Arten von Einschränkungen, die sich auf bestimmte Spalten konzentrieren. Von allen Tabellenimplementierungen wird erwartet, dass Einschränkungen für die Spalten im aktuellen Spaltensatz unterstützt werden. Zum Hinzufügen von Wert können Tabellen implementierer jedoch auch Einschränkungen basierend auf Objekteigenschaften unterstützen, die derzeit nicht in der Tabellenansicht enthalten sind.
  
Einige Einschränkungen können mithilfe einer Einschränkung kombiniert werden, die einen logischen **AND**-, **OR-** oder **NOT-Vorgang** ausführt. Die meisten Eigenschaftseinschränkungen müssen beispielsweise mit vorhandenen Einschränkungen mithilfe von **AND-Einschränkungen verbunden** werden. Es gibt einige Ausnahmen, z. B. wenn die in der Eigenschaftseinschränkung verwendete Eigenschaft die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaft ist oder wenn es sich um eine erforderliche Spalte in einer Tabelle handelt. Ein Client, der Einschränkungen beim Erstellen seiner Ansicht eingrenzt, sollte Einschränkungen mit seinen Eigenschaftseinschränkungen verwenden, da MAPI nicht anbegrenzt, wie Dienstanbieter Eigenschaftseinschränkungen auswerten sollten, wenn keine Eigenschaft vorhanden ist. Es ist sinnvoll und empfohlen, dass Dienstanbieter die Einschränkung nicht erfüllen, es gibt jedoch keine Anforderungen. 
  
Eine Einschränkung wird mithilfe der [SRestriction-Datenstruktur](srestriction.md) definiert, die eine Vereinigung speziellerer Einschränkungsstrukturen und einen Indikator für den Typ der Struktur enthält, die in der Union enthalten ist. 
  
Jede der spezialisierten Einschränkungsstrukturen in der Union stellt eine andere Art von Einschränkung dar. Die Arten von Einschränkungen und die zugehörigen Datenstrukturen sind:
  
|**Art der Einschränkung**|**Zugeordnete Datenstruktur**|**Beschreibung**|
|:-----|:-----|:-----|
|Compare-Eigenschaft  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Vergleicht zwei Eigenschaften desselben Typs.  <br/> |
|**UND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Führt einen logischen **AND-Vorgang** für zwei oder mehr Einschränkungen aus.  <br/> |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Führt einen logischen **OR-Vorgang** für zwei oder mehr Einschränkungen aus.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Führt einen logischen **NOT-Vorgang** für zwei oder mehr Einschränkungen aus.  <br/> |
|Inhalt  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Sucht nach angegebenen Daten.  <br/> |
|Eigenschaft  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Gibt einen bestimmten Eigenschaftswert als Kriterien für den Abgleich an. Kann z. B. verwendet werden, um nach einem bestimmten Anlagentyp zu suchen.  <br/> |
|Bitmaske  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Wendet eine Bitmaske auf eine PT_LONG an, um in der Regel zu bestimmen, ob bestimmte Kennzeichen festgelegt sind.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Testet die Größe einer Eigenschaft mithilfe von standardmäßigen relationalen Operatoren.  <br/> |
|Exist  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Testet, ob ein Objekt einen Wert für eine Eigenschaft hat.  <br/> |
|Unterobjekt  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Wird zum Durchsuchen von Unterobjekten oder Objekten verwendet, auf die nicht mit einem Eintragsbezeichner zugegriffen werden kann, z. B. Empfänger und Anlagen. Kann z. B. verwendet werden, um nach Nachrichten für einen bestimmten Empfänger zu suchen.  <br/> |
|Kommentar  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Ordnet ein Objekt einer Reihe benannter Eigenschaften zu.  <br/> |
   
Einige Einschränkungen verwenden reguläre Ausdrücke, und MAPI unterstützt eine eingeschränkte Form der Notation regulärer Ausdrücke in der Formatvorlage, die viele Textanwendungen verwendet.
  
Die Kommentareinschränkung wird von Clients verwendet, die Einschränkungen auf dem Datenträger speichern, um anwendungsspezifische Informationen mit der Einschränkung zu speichern. Beispielsweise kann ein Client, der den Namen einer benannten Eigenschaft, die in einer Eigenschaftseinschränkung verwendet wird, speichern, dies mit einer Kommentareinschränkung tun. Das Speichern des Namens ist in einer Eigenschaftseinschränkung nicht möglich. Die [SPropertyRestriction-Datenstruktur](spropertyrestriction.md) enthält nur das Eigenschaftstag. Kommentareinschränkungen werden von [IMAPITable::Restrict](imapitable-restrict.md) ignoriert, da sie keine Auswirkungen auf die Zeilen haben, die von [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden, nachdem ein **Restrict-Aufruf** ausgeführt wurde. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

