---
title: PidTagInstanceKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ee989d8a4258be510a6019211ce8c41ecc5ae68f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620072"
---
# <a name="pidtaginstancekey-canonical-property"></a>PidTagInstanceKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der eine Zeile in einer Tabelle eindeutig identifiziert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_INSTANCE_KEY  <br/> |
|Kennung:  <br/> |0x0FF6  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Tabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist ein binärer Wert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert. Es ist eine erforderliche Spalte in den meisten Tabellen. Wenn eine Zeile in zwei Ansichten enthalten ist, gibt es zwei verschiedene Instanzschlüssel. Der Instanzschlüssel einer Zeile kann sich bei jedem Öffnen der Tabelle unterscheiden, bleibt jedoch konstant, während die Tabelle geöffnet ist. Zeilen, die während der Verwendung einer Tabelle hinzugefügt wurden, verwenden keinen zuvor verwendeten Instanzschlüssel. 
  
Verwenden Sie die **Eigenschaften PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), um alle Zeilen einer Erweiterung zu korrelieren. Verwenden Sie **PR_INSTANCE_KEY,** um eine bestimmte Instanz innerhalb der Erweiterung zu suchen. 
  
Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird für jede Instanz der Erweiterung, d. h. für jeden Wert dieser Eigenschaft, eine Zeile erstellt. Jede Zeile hat einen  eindeutigen Wert für die PR_INSTANCE_KEY-Eigenschaft, während alle anderen Spalten während der Erweiterung ihre ursprünglichen Werte beibehalten. 
  
In einer kategorisierten Sortierung einer Tabelle können Zeilen, die nicht den tatsächlichen Daten entsprechen, dem Ergebnis der Sortierung hinzugefügt werden. Jede solche Zeile verfügt wie alle Zeilen in allen Tabellen über einen eigenen eindeutigen Instanzschlüssel. 
  
 **PR_INSTANCE_KEY** wird auch in Tabellenereignisbenachrichtigungen verwendet. Die **propIndex-** und **propPrior-Elemente** der [TABLE_NOTIFICATION](table_notification.md) Struktur sind [SPropValue-Strukturen,](spropvalue.md) die **PR_INSTANCE_KEY** Werte enthalten. Das **propIndex-Element** gibt die Zeile an, die hinzugefügt oder geändert wurde. Das **propPrior-Element** gibt die Zeile vor der hinzugefügten oder geänderten Zeile an (**PR_NULL** eine Änderung an der ersten Zeile angibt). 
  
Dieser Wert wird nicht als Teil der Anzeigetabelle kopiert. 
  
 **PR_INSTANCE_KEY** ist eine [MAPIUID-Struktur.](mapiuid.md) Alle Instanzschlüssel können direkt als binäre Werte verglichen werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
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

