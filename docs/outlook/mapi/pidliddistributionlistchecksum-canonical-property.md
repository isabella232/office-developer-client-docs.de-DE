---
title: Kanonische Pidliddistributionlistchecksum (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357610"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a>Kanonische Pidliddistributionlistchecksum (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Prüfsumme für die 32-Bit-zyklische Redundanzprüfung (CRC-32) für eine persönliche Verteilerliste an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidDLChecksum  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long-ID (Deckel):  <br/> |0x0000804C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft kann verwendet werden, um zu bestimmen, wann die **dispidDLMembers** ([pidliddistributionlistmembers (](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft aktualisiert wurde, ohne die anderen Mitgliedereigenschaften der persönlichen Verteilerliste zu aktualisieren, indem der CRC-32 auf dem vorhandenen Wert von **dispidDLMembers** und vergleicht diesen mit dem Wert der **dispidDLChecksum** -Eigenschaft. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

