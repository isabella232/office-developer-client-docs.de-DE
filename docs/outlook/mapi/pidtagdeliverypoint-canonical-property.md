---
title: PidTagDeliveryPoint (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439422"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>PidTagDeliveryPoint (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Art der funktionalen Entität an, mit der eine Nachricht an den Empfänger übermittelt wurde oder hätte. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELIVERY_POINT  <br/> |
|Kennung:  <br/> |0x0C07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann genau einen der folgenden Werte haben: 
  
MAPI_MH_DP_ML 
  
> An eine Verteilerliste zugestellt, ein Zustellungspunkt, der die Nachricht wiederum an viele Empfänger verteilen kann.
    
MAPI_MH_DP_MS 
  
> An einen Nachrichtenspeicher anstatt direkt an einen Empfänger zugestellt.
    
MAPI_MH_DP_OTHER_AU 
  
> Wird an eine andere Zugriffseinheit (Access Unit, AU) als eine physische Zustellungszugriffseinheit (PHYSICAL Delivery Access Unit, PDAU) übermittelt, z. B. ein FAX-System.
    
MAPI_MH_DP_PDAU 
  
> An eine physische Zustellungszugriffseinheit, z. B. ein menschliches Postunternehmen, zugestellt.
    
MAPI_MH_DP_PDS_PATRON 
  
> Zugestellt an einen physischen Systempatron, z. B. ein herkömmliches Postpostfach.
    
MAPI_MH_DP_PRIVATE_UA 
  
> An einen privaten Benutzer-Agent (PRIVATE User Agent, UA) übermittelt, z. B. an einen Client in einem eigenen Messagingsystem.
    
MAPI_MH_DP_PUBLIC_UA 
  
> An einen öffentlichen Benutzer-Agent oder öffentlichen Dienstanbieter übermittelt.
    
Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, d. h. ein MAPI-Client. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

