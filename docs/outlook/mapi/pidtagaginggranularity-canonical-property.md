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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325585"
---
# <a name="pidtagaginggranularity-canonical-property"></a>PidTagAgingGranularity (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Zeiteinheit dar, die zum Bestimmen der Dauer verwendet wird, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AGING_GRANULARITY  <br/> |
|Kennung:  <br/> |0x36EE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Hinweise

Die möglichen Werte **für PR_AGING_GRANULARITY** können einer der folgenden Sein: 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |0  <br/> |**PR_AGING_PERIOD** wird in der Anzahl der Monate definiert.  <br/> |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD** wird in der Anzahl der Wochen definiert.  <br/> |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD** wird in der Anzahl der Tage definiert.  <br/> |
   
Die Dauer, die ein Element in einem Ordner verbleibt, bevor das Element archiviert [wird,](pidtagagingperiod-canonical-property.md) wird durch zwei Eigenschaften bestimmt: PR_AGING_PERIOD **und PR_AGING_GRANULARITY**. **PR_AGING_PERIOD** gibt die Anzahl der Zeiteinheiten an, die das Element im Ordner verbleibt, bevor es archiviert wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

