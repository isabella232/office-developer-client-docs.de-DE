---
title: Kanonische PidTagDeliveryPoint-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 736d98fd779d9e22553ac076f7f6a4deaacc1597
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566738"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Kanonische PidTagDeliveryPoint-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Art der funktionalen Entität an, mit der eine Nachricht an den Empfänger übermittelt wurde oder worden wäre. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELIVERY_POINT  <br/> |
|Kennung:  <br/> |0x0C07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann genau einen der folgenden Werte haben: 
  
MAPI_MH_DP_ML 
  
> Wird an eine Verteilerliste übermittelt, ein Zustellungspunkt, der die Nachricht wiederum an viele Empfänger verteilen kann.
    
MAPI_MH_DP_MS 
  
> Wird an einen Nachrichtenspeicher statt direkt an einen Empfänger übermittelt.
    
MAPI_MH_DP_OTHER_AU 
  
> Wird an eine Zugriffseinheit (ACCESS Unit, AU) geliefert, die keine physische Übermittlungszugriffseinheit (Physical Delivery Access Unit, PDAU) ist, z. B. ein FAX-System.
    
MAPI_MH_DP_PDAU 
  
> Wird an eine physische Zustelleinheit, z. B. einen netzbetreiber, geliefert.
    
MAPI_MH_DP_PDS_PATRON 
  
> Wird an einen Empfänger des physischen Zustellungssystems, z. B. ein herkömmliches Postpostfach, übermittelt.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Wird an einen privaten Benutzer-Agent (UA) übermittelt, z. B. an einen Client in einem internen Messagingsystem.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Wird an einen öffentlichen Benutzer-Agent oder öffentlichen Dienstanbieter übermittelt.
    
Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, d. h. ein MAPI-Client. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

