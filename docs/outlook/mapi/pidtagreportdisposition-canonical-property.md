---
title: PidTagReportDisposition (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 62d5b04086e45b6b3d2cfa960472010827d60d6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794967"
---
# <a name="pidtagreportdisposition-canonical-property"></a>PidTagReportDisposition (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt den Empfangsbestätigungsstatus für Nachrichten, die Empfangsbestätigungen anfordern. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W  <br/> |
|Bezeichner:  <br/> |0 x 0080  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die folgenden Werte sind gültig:
  
- "gelöscht"
    
- "verarbeitet"
    
- "verteilt"
    
- "verweigert."
    
- "failed"
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
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

