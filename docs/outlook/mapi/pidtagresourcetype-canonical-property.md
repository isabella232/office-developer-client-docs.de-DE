---
title: Kanonische PidTagResourceType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5d494577721feba01dd9cb93f344308251a8ed33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795002"
---
# <a name="pidtagresourcetype-canonical-property"></a>Kanonische PidTagResourceType-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Wert, der angibt, der Dienstanbietertyp.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RESOURCE_TYPE  <br/> |
|Bezeichner:  <br/> |0x3E03  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
MAPI_AB 
  
> Adressbuch
    
"MAPI_AB_PROVIDER". 
  
> -Adressbuchanbieter
    
MAPI_HOOK_PROVIDER 
  
> Warteschlange Hook Anbieter
    
MAPI_PROFILE_PROVIDER 
  
> Der Provider Profile
    
MAPI_SPOOLER 
  
> Nachricht Warteschlange
    
MAPI_STORE_PROVIDER 
  
> Nachricht Speicheranbieter
    
MAPI_SUBSYSTEM 
  
> Interne MAPI-Subsystems
    
MAPI_TRANSPORT_PROVIDER 
  
> Transportdienst
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

