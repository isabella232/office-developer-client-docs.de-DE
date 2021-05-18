---
title: PidTagMessageSubmissionId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329400"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a>PidTagMessageSubmissionId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Id des Nachrichtenübertragungssystems (Message Transfer System, MTS) für den Nachrichtenübertragungs-Agent (Message Transfer Agent, MTA).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_SUBMISSION_ID  <br/> |
|Kennung:  <br/> |0x0047  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird vom MTA nach erfolgreichem Abschluss der Nachrichtenübermittlung zurückgegeben. Jeder zukünftige Kontakt mit dem MTA in Bezug auf diese Nachricht, z. B. das Anfordern eines Abbruchs, verwendet den MTS-Bezeichner in dieser Eigenschaft.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

