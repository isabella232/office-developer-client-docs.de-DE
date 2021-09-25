---
title: Kanonische PidLidLogStart-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: df39d6619d1507e83709068bd74178f34d92231b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624874"
---
# <a name="pidlidlogstart-canonical-property"></a>Kanonische PidLidLogStart-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt das Startdatum und die Startzeit für die Journalnachricht dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidLogStart  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Log  <br/> |
|Long ID (LID):  <br/> |0x00008706  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zeit in koordinierter Weltzeit (UTC), zu der die Aktivität begonnen hat, muss der **Eigenschaft dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) entsprechen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Die Definition von Eigenschaftengruppen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Diebe zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

