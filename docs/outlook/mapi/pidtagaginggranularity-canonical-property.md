---
title: PidTagAgingGranularity (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 09a79a68d7619ded9edf3ec4ac67733bdec1e32c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794071"
---
# <a name="pidtagaginggranularity-canonical-property"></a>PidTagAgingGranularity (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Stellt die Zeiteinheit, die verwendet wird, bei der Bestimmung der Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_AGING_GRANULARITY  <br/> |
|Bezeichner:  <br/> |0x36EE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |0  <br/> |**PR_AGING_PERIOD** ist in der Anzahl von Monaten definiert.  <br/> |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD** ist in die Anzahl der Wochen definiert.  <br/> |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD** ist in der Anzahl der Tage definiert.  <br/> |
   
Die Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird, wird durch die beiden Eigenschaften [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) und **PR_AGING_GRANULARITY**bestimmt. **PR_AGING_PERIOD** stellt die Anzahl der Einheiten, die das Element im Ordner bleibt, bevor es archiviert wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

