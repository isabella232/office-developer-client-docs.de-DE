---
title: Kanonische PidTagProviderUid-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794835"
---
# <a name="pidtagprovideruid-canonical-property"></a>Kanonische PidTagProviderUid-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine **MAPIUID** Struktur des Dienstanbieters, der eine Nachricht behandelt wird. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PROVIDER_UID  <br/> |
|Bezeichner:  <br/> |0x300C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine MAPI  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von allen Dienstanbietern berechnet. Sie enthält eine [MAPIUID](mapiuid.md) Struktur zugeordnet und in der Regel hartcodierte vom Anbieter. Es wird in der Regel von einer Clientanwendung verwendet, die nur Address Book Container von einem bestimmten Anbieter bereitgestellt wird, interessiert ist. 
  
Diese Eigenschaft wird nur als ein Eintrag in der Spalte in der Tabelle Anbieter angezeigt.
  
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

