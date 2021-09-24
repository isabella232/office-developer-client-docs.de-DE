---
title: PidNameRightsManagementLicense (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd5503901e50c3b7f44d567aa09b3b6306639343
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550876"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>PidNameRightsManagementLicense (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert die Verwendungslizenz für die E-Mail-Nachricht mit verwalteten Rechten zwischen.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |Keines  <br/> |
|Eigenschaftensatz:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Eigenschaftenname:  <br/> |DRMLicense  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Sicheres Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Eigenschaft in einer E-Mail-Nachricht mit verwalteten Rechten vorhanden ist, muss der erste Wert dieser mehreren binären Eigenschaft die komprimierte Verwendungslizenz für die E-Mail-Nachricht mit verwalteten Rechten enthalten (wie in [RFC1950]angegeben).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von nachrichten mit verwalteten Rechten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

