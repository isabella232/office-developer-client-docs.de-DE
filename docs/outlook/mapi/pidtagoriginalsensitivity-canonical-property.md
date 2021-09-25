---
title: PidTagOriginalSensitivity (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 187bdd2a3255b740cf32487d3d59a7ddaa5cec6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624762"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>PidTagOriginalSensitivity (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vom Absender der ersten Version einer Nachricht zugewiesenen Vertraulichkeitswert, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|Kennung:  <br/> |0x002E  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung sollte diese Eigenschaft auf denselben Wert wie die **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) -Eigenschaft festlegen, wenn die Nachricht zum ersten Mal gesendet wird. Sie sollte nie später geändert werden.
  
Diese Eigenschaft wird vom Transportanbieter verwendet, um die Vertraulichkeit bei kopierten Einträgen zu schützen. Sie ermöglicht beispielsweise das Blockieren der Änderung des ursprünglichen Nachrichtentexts in einer Weiterleitung oder Antwort auf eine Nachricht, die ursprünglich **als SENSITIVITY_PRIVATE** markiert wurde.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
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

