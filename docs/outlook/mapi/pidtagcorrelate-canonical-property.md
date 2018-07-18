---
title: PidTagCorrelate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce8573310e17e26b4e2deb4c0a0f835a6569151e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794284"
---
# <a name="pidtagcorrelate-canonical-property"></a>PidTagCorrelate (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält True, wenn der Absender einer Nachricht die Korrelations-Funktion von messaging-System anfordert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CORRELATE  <br/> |
|Bezeichner:  <br/> |0x0E0C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird verwendet, um die Korrelation eingehende Berichte mit der ursprünglichen gesendeten Nachrichten anfordern. Stößt ein Transportdienstes eine gesendete Nachricht mit **PR_CORRELATE** Set auf true festgelegt, wird die **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md))-Eigenschaft auf die Übertragung System (MTS)-ID für diese Nachricht.
  
 **PR_CORRELATE** sollte mit der messaging-Systeme, die Korrelation unterstützen von MTS Bezeichner, z. B. x. 400-verwendet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

