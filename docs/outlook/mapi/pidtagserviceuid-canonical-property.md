---
title: Kanonische PidTagServiceUid-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795176"
---
# <a name="pidtagserviceuid-canonical-property"></a>Kanonische PidTagServiceUid-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die [MAPIUID](mapiuid.md) -Struktur für einen Nachrichtendienst. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SERVICE_UID  <br/> |
|Bezeichner:  <br/> |0x3D0C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von MAPI auf Profil Section-Objekten berechnet. MAPI wird verwendet, um alle Anbieter zu gruppieren, die den Dienst angehören. Diese Eigenschaft wird als Parameter für die meisten [IMsgServiceAdmin](imsgserviceadminiunknown.md) Methoden bereitgestellt. Sie müssen nicht Mapisvc.inf angezeigt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

