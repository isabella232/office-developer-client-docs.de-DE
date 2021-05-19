---
title: PidLidDistributionListOneOffMembers (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335049"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>PidLidDistributionListOneOffMembers (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Liste der einmal verwendeten EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidDLOneOffMembers  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Lange ID (LID):  <br/> |0x00008054  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese einmal verwendeten EntryIds kapseln Anzeigenamen und E-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.
  
Wenn der Client oder der Server diese Eigenschaft festlegen, muss sie mit der **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft synchronisiert werden: Für jeden Eintrag in der **dispidDLOneOffMembers-Eigenschaft** muss ein Eintrag an derselben Position in der **dispidDLMembers-Eigenschaft** vorhanden sein. 
  
Beim Festlegen **von dispidDLOneOffMembers** muss der Client oder der Server sicherstellen, dass die Gesamtgröße weniger als 15.000 Byte beträgt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

