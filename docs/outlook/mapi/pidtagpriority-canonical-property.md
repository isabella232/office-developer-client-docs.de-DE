---
title: Kanonische PidTagPriority-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: be32e8c8c83305ec759062c523c0567b39239178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574902"
---
# <a name="pidtagpriority-canonical-property"></a>Kanonische PidTagPriority-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die relative Priorität einer Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PRIORITY  <br/> |
|Kennung:  <br/> |0x0026  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft und die **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) -Eigenschaft sollten nicht verwechselt werden. Wichtigkeit gibt den Benutzern einen Wert an, während die Priorität die Reihenfolge oder Geschwindigkeit angibt, in der die Nachricht von der Messagingsystemsoftware gesendet werden soll. Eine höhere Priorität weist in der Regel auf höhere Kosten hin. Eine höhere Wichtigkeit wird in der Regel einer anderen Anzeige über die Benutzeroberfläche zugeordnet.
  
Die Priorität einer Berichtsnachricht sollte mit der Priorität der ursprünglichen Nachricht übereinstimmen, die gemeldet wird.
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
PRIO_NONURGENT 
  
> Die Nachricht ist nicht dringend.
    
PRIO_NORMAL 
  
> Die Nachricht hat normale Priorität.
    
PRIO_URGENT 
  
> Die Nachricht ist dringend.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

