---
title: PidTagResourceType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56f14488812842d5e9fe63ae228c325059ebe679
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575091"
---
# <a name="pidtagresourcetype-canonical-property"></a>PidTagResourceType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der angibt, der Dienstanbietertyp.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_TYPE  <br/> |
|Kennung:  <br/> |0x3E03  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

