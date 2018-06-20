---
title: Kanonische PidTagMessageSubmissionId-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3286e9e666d59997693df636263cb04f7b767d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794635"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a>Kanonische PidTagMessageSubmissionId-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine System (MTS) ID für die Message Transfer Agent (MTA).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MESSAGE_SUBMISSION_ID  <br/> |
|Bezeichner:  <br/> |0x0047  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von der MTA nach dem erfolgreichen Abschluss der Nachrichtenübermittlung zurückgegeben. Alle zukünftiger Kontakt mit dem MTA zu im Zusammenhang mit dieser Nachricht, wie etwa anfordernde Abbruch wird die MTS-ID in dieser Eigenschaft verwendet.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

