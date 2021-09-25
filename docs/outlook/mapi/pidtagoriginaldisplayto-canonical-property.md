---
title: PidTagOriginalDisplayTo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9948062ea3835f8177fa50d676c6e8094bdb0706
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575029"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a>PidTagOriginalDisplayTo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzeigenamen der primären (An)-Empfänger der ursprünglichen Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W  <br/> |
|Kennung:  <br/> |0x0074  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften enthalten eine durch Semikolons getrennte ASCII-Liste. Sie wird von MAPI bereitgestellt und direkt aus **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) kopiert, wenn ein Übermittlungs- oder Unzustellbarkeitsbericht oder ein gelesener oder nicht gelesener Bericht generiert wird. Diese Eigenschaft kann in anderen Nachrichten vorhanden sein, wie durch ihre Nachrichtenklassen definiert.
  
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

