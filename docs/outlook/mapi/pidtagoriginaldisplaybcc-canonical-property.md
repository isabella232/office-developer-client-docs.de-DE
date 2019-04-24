---
title: Kanonische Pidtagoriginaldisplaybcc (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355643"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a>Kanonische Pidtagoriginaldisplaybcc (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzeigenamen aller BCC-Empfänger (Blind Carbon Copy) der ursprünglichen Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W  <br/> |
|Kennung:  <br/> |0x0072  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften enthalten eine durch Semikolons getrennte Liste. Sie werden von MAPI bereitgestellt und direkt aus **PR_DISPLAY_BCC** ([pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md)) kopiert, wenn ein zugestellter oder nicht zugestellter Bericht oder ein Lese-oder nicht lesbarer Bericht generiert wird. Diese Eigenschaften sind möglicherweise in anderen Nachrichten vorhanden, wie durch ihre Nachrichtenklassen definiert.
  
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

