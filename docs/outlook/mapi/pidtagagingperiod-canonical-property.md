---
title: PidTagAgingPeriod (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1fd1b06bbaa10c2d7c71ee4c161fd6a980da1865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794059"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagAgingPeriod (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Stellt die Anzahl der Einheiten, die verwendet werden, um die Dauer zu ermitteln, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird.
  
## 

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_AGING_PERIOD  <br/> |
|Bezeichner:  <br/> |0x36EC  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird, wird durch die beiden Eigenschaften **PR_AGING_PERIOD** und **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** bestimmt. **PR_AGING_GRANULARITY** stellt die Zeiteinheit, in der **PR_AGING_PERIOD** ausgedrückt wird, wenn diese Zeitdauer zu bestimmen. 
  
Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein. 
  
****

|**Name**|**Beschreibung**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** ist in der Anzahl von Monaten definiert.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** ist in die Anzahl der Wochen definiert.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** ist in der Anzahl der Tage definiert.  <br/> |
   
Beispielsweise, wenn ein Ordner Archive eines Elements, nachdem das Element in den Ordner für zwei Wochen zu löschen, und klicken Sie dann auf **PR_AGING_GRANULARITY** wurde ist **AG_WEEKS** und **PR_AGING_PERIOD** 2. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen an.
    
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

