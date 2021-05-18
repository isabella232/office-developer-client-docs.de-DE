---
title: PidNameRightsManagementLicense (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315022"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>PidNameRightsManagementLicense (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert die Verwendungslizenz für die E-Mail-Nachricht mit verwalteten Rechten zwischen.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |Keine  <br/> |
|Eigenschaftensatz:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Eigenschaftsname:  <br/> |DRMLicense  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Sicheres Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die Eigenschaft in einer E-Mail-Nachricht mit verwalteten Rechten vorhanden ist, muss der erste Wert dieser mehreren binären Eigenschaft die komprimierte ZLIB-Lizenz (wie in [RFC1950]) angegeben für die E-Mail-Nachricht mit verwalteten Rechten enthalten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

