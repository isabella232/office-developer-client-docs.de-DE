---
title: PidTagAccessLevel (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331997"
---
# <a name="pidtagaccesslevel-canonical-property"></a>PidTagAccessLevel (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Zugriffsebene des Clients auf das Objekt an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACCESS_LEVEL  <br/> |
|Kennung:  <br/> |0x0FF7  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Eigenschaften der Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für den Client. Dies muss einer der folgenden Werte sein:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Schreibgeschützt  <br/> |
|0x00000001  <br/> |Ändern  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

