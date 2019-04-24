---
title: Kanonische Pidtagoriginalsensitivity (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341230"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>Kanonische Pidtagoriginalsensitivity (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vom Absender der ersten Version einer Nachricht zugewiesenen Vertraulichkeits Wert, die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|Kennung:  <br/> |0x002E  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung sollte diese Eigenschaft auf den gleichen Wert wie die **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))-Eigenschaft festlegen, wenn die Nachricht zum ersten Mal übermittelt wird. Sie sollte nicht nachträglich geändert werden.
  
Diese Eigenschaft wird vom Transportanbieter verwendet, um die Vertraulichkeit von kopierten Einträgen zu schützen. Sie ermöglicht es beispielsweise, die Änderung des ursprünglichen Nachrichtentexts in einer Weiterleitung von zu blockieren oder auf eine Nachricht zu antworten, die ursprünglich **SENSITIVITY_PRIVATE**markiert wurde.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

