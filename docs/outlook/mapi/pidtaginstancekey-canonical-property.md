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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bc16e88035f091a4f42a03342a70e7e3a1da5e0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794484"
---
# <a name="pidtaginstancekey-canonical-property"></a>PidTagInstanceKey (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen Wert, der eine Zeile in einer Tabelle eindeutig identifiziert. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_INSTANCE_KEY  <br/> |
|Bezeichner:  <br/> |0x0FF6  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Tabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist ein binärer Wert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert. Es ist eine erforderliche Spalte in den meisten Tabellen. Wenn eine Zeile in zwei Ansichten enthalten ist, sind zwei andere Instanzenschlüssel. Der Instanzschlüssel einer Zeile abweichen jedes Mal, wenn die Tabelle geöffnet ist, aber konstant bleiben, während die Tabelle geöffnet ist. Zeilen hinzugefügt, während eine Tabelle verwendet wird wieder einen Instanzschlüssel nicht verwenden, der zuvor verwendet wurde. 
  
Verwenden Sie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) Eigenschaften alle Zeilen der eine Erweiterung korrelieren. Verwenden Sie **PR_INSTANCE_KEY** , um eine bestimmte Instanz innerhalb der Erweiterung zu suchen. 
  
Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird eine Zeile für jeden Wert dieser Eigenschaft d. h., für jede Instanz der Erweiterung, erstellt. Jede Zeile enthält einen eindeutigen Wert für die Eigenschaft **PR_INSTANCE_KEY** , während die anderen Spalten die ursprünglichen Werte in der gesamten die Erweiterung beibehalten. 
  
Zeilen nicht entsprechend der tatsächlichen Daten können in einer kategorisierten Sortierung einer Tabelle das Ergebnis der Sortierung hinzugefügt werden. Jede Zeile eine solche wie alle Zeilen in allen Tabellen, verfügt über eine eigene eindeutige Instanz-Taste. 
  
 **PR_INSTANCE_KEY** ist auch in der Tabelle ereignisbenachrichtigungen verwendet. Die **PropIndex** und **PropPrior** Member der Struktur [TABLE_NOTIFICATION](table_notification.md) sind [SPropValue](spropvalue.md) Strukturen **PR_INSTANCE_KEY** enthalten. Das Element **PropIndex** gibt die Zeile, die hinzugefügt oder geändert wurde. Das Element **PropPrior** gibt die Zeile vor der hinzugefügte oder geänderte Zeile (**PR_NULL** gibt eine Änderung an der ersten Zeile). 
  
Dieser Wert wird nicht als Teil der Anzeige-Tabelle kopiert. 
  
 **PR_INSTANCE_KEY** ist eine [MAPIUID](mapiuid.md) -Struktur. Alle Instanzenschlüssel können direkt als Binärwerte verglichen werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
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

