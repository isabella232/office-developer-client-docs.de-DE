---
title: PidTagAgingPeriod (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9628cbde8bf136f4be4536e26ee9c2624cdea05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595329"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagAgingPeriod (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Anzahl der Zeiteinheiten dar, die verwendet werden, um die Zeitdauer zu bestimmen, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AGING_PERIOD  <br/> |
|Kennung:  <br/> |0x36EC  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Zeitdauer, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird, wird durch zwei Eigenschaften bestimmt: **PR_AGING_PERIOD** und **[PR_AGING_GRANULARITY.](pidtagaginggranularity-canonical-property.md)** **PR_AGING_GRANULARITY** stellt die Zeiteinheit dar, in der **PR_AGING_PERIOD** ausgedrückt wird, wenn diese Zeitdauer bestimmt wird. 
  
Die möglichen Werte für **PR_AGING_GRANULARITY** können einer der folgenden Werte sein: 
  
****

|**Name**|**Beschreibung**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** wird in der Anzahl der Monate definiert.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** wird in mehreren Wochen definiert.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** wird in der Anzahl der Tage definiert.  <br/> |
   
Wenn beispielsweise ein Ordner ein Element nur archiviert, nachdem sich das Element zwei Wochen lang im Ordner befindet, ist **PR_AGING_GRANULARITY** **AG_WEEKS** und **PR_AGING_PERIOD** 2. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen bereit.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

