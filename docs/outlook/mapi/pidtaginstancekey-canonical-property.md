---
title: Kanonische Pidtaginstancekey (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358511"
---
# <a name="pidtaginstancekey-canonical-property"></a>Kanonische Pidtaginstancekey (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der eine Zeile in einer Tabelle eindeutig identifiziert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_INSTANCE_KEY  <br/> |
|Kennung:  <br/> |0x0FF6  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Tabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist ein Binärwert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert. In den meisten Tabellen ist es eine erforderliche Spalte. Wenn eine Zeile in zwei Ansichten enthalten ist, gibt es zwei verschiedene Instanzenschlüssel. Der Instanzschlüssel einer Zeile kann sich bei jedem Öffnen der Tabelle unterscheiden, bleibt jedoch konstant, während die Tabelle geöffnet ist. Zeilen, die hinzugefügt werden, während eine Tabelle verwendet wird, verwenden Sie keinen zuvor verwendeten Instanzschlüssel. 
  
Verwenden Sie die Eigenschaften **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md)), um alle Zeilen einer Erweiterung zu korrelieren. Verwenden Sie **PR_INSTANCE_KEY** , um eine bestimmte Instanz innerhalb der Erweiterung zu suchen. 
  
Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird für jede Erweiterungs Instanz, also für jeden Wert dieser Eigenschaft, eine Zeile erstellt. Jede Zeile hat einen eindeutigen Wert für die **PR_INSTANCE_KEY** -Eigenschaft, während alle anderen Spalten ihre ursprünglichen Werte während der Erweiterung behalten. 
  
In einer kategorisierten Sortierung einer Tabelle können Zeilen, die nicht den tatsächlichen Daten entsprechen, dem Ergebnis der Sortierung hinzugefügt werden. Jede solche Zeile hat, wie alle Zeilen in allen Tabellen, ihren eigenen eindeutigen Instanzschlüssel. 
  
 **PR_INSTANCE_KEY** wird auch in Tabellenereignis Benachrichtigungen verwendet. Die **propIndex** -und **propPrior** -Elemente der [TABLE_NOTIFICATION](table_notification.md) -Struktur sind [SPropValue](spropvalue.md) -Strukturen mit **PR_INSTANCE_KEY** -Werten. Das **propIndex** -Element gibt die Zeile an, die hinzugefügt oder geändert wurde. Das **propPrior** -Element gibt die Zeile vor der hinzugefügten oder geänderten Zeile an (**PR_NULL** gibt eine Änderung der ersten Zeile an). 
  
Dieser Wert wird nicht als Teil der Anzeigetabelle kopiert. 
  
 **PR_INSTANCE_KEY** ist eine [MAPIUID](mapiuid.md) -Struktur. Alle Instanzenschlüssel können direkt als Binärwerte verglichen werden. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
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

