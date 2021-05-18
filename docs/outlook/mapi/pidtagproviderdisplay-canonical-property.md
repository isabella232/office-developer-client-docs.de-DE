---
title: PidTagProviderDisplay (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421592"
---
# <a name="pidtagproviderdisplay-canonical-property"></a>PidTagProviderDisplay (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vom Hersteller definierten Anzeigenamen für einen Dienstanbieter.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W  <br/> |
|Kennung:  <br/> |0x3006  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften und **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) werden nur für Profilabschnitte definiert, die zu Dienstanbietern gehören. Sie müssen in MAPISVC.INF vorhanden sein.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

