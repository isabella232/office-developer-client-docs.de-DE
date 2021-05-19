---
title: PidTagInstanceKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358511"
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
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist ein binärer Wert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert. Es handelt sich um eine erforderliche Spalte in den meisten Tabellen. Wenn eine Zeile in zwei Ansichten enthalten ist, gibt es zwei verschiedene Instanzschlüssel. Der Instanzschlüssel einer Zeile kann sich jedes Mal unterscheiden, wenn die Tabelle geöffnet wird, bleibt jedoch konstant, während die Tabelle geöffnet ist. Zeilen, die hinzugefügt werden, während eine Tabelle verwendet wird, verwenden keinen Instanzschlüssel, der zuvor verwendet wurde. 
  
Verwenden Sie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) Eigenschaften, um alle Zeilen einer Erweiterung zu korrelieren. Verwenden **PR_INSTANCE_KEY,** um eine bestimmte Instanz innerhalb der Erweiterung zu suchen. 
  
Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird für jede Instanz der Erweiterung, d. h. für jeden Wert dieser Eigenschaft, eine Zeile erstellt. Jede Zeile hat einen eindeutigen Wert für **die PR_INSTANCE_KEY-Eigenschaft,** während alle anderen Spalten während der gesamten Erweiterung ihre ursprünglichen Werte beibehalten. 
  
In einer kategorisierten Art einer Tabelle können dem Ergebnis der Sortierung Zeilen hinzugefügt werden, die nicht den tatsächlichen Daten entspricht. Jede solche Zeile verfügt wie alle Zeilen in allen Tabellen über einen eigenen eindeutigen Instanzschlüssel. 
  
 **PR_INSTANCE_KEY** wird auch in Tabellenereignisbenachrichtigungen verwendet. Die **propIndex-** **und propPrior-Elemente** der TABLE_NOTIFICATION sind [SPropValue-Strukturen,](spropvalue.md) die **PR_INSTANCE_KEY** enthalten. [](table_notification.md) Das **propIndex-Element** gibt die Zeile an, die hinzugefügt oder geändert wurde. Das **propPrior-Element** gibt die Zeile vor der hinzugefügten oder geänderten Zeile an (**PR_NULL** gibt eine Änderung an der ersten Zeile an). 
  
Dieser Wert wird nicht als Teil der Anzeigetabelle kopiert. 
  
 **PR_INSTANCE_KEY** ist eine [MAPIUID-Struktur.](mapiuid.md) Alle Instanzschlüssel können direkt als Binärwerte verglichen werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
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

