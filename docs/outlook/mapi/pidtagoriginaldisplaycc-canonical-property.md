---
title: Kanonische Pidtagoriginaldisplaycc (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9eb90d353705434803ff617ff2b355c7c96359b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355622"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a>Kanonische Pidtagoriginaldisplaycc (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzeigenamen aller CC-Empfänger der ursprünglichen Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W  <br/> |
|Kennung:  <br/> |0x0073  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften enthalten eine durch Semikolons getrennte Liste. Sie wird von MAPI bereitgestellt und direkt aus **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) kopiert, wenn ein Zusteller-oder Unzustellbarkeitsbericht oder ein Lese-oder nicht lesbarer Bericht generiert wird. Diese Eigenschaft kann in anderen Nachrichten gemäß der Definition durch ihre Nachrichtenklassen vorhanden sein.
  
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

