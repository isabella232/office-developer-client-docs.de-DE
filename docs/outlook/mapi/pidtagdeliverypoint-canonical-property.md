---
title: Kanonische Pidtagdeliverypoint (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360879"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Kanonische Pidtagdeliverypoint (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Art der funktionalen Entität an, anhand derer eine Nachricht an den Empfänger übermittelt wurde oder wäre. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELIVERY_POINT  <br/> |
|Kennung:  <br/> |0x0C07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann genau einen der folgenden Werte haben: 
  
MAPI_MH_DP_ML 
  
> An eine Verteilerliste zuGestellt, ein Zustellungs Punkt, der die Nachricht wiederum an viele Empfänger verteilen kann.
    
MAPI_MH_DP_MS 
  
> Wird an einen Nachrichtenspeicher anstatt direkt an einen Empfänger überMittelt.
    
MAPI_MH_DP_OTHER_AU 
  
> Wird an eine andere Zugriffseinheit (AU) als eine physische Zustellungs Zugriffseinheit (PDAU) (beispielsweise ein FAX) übermittelt.
    
MAPI_MH_DP_PDAU 
  
> An eine physische Zustellungs Einheit übermittelt, beispielsweise einen menschlichen postalischen Spediteur.
    
MAPI_MH_DP_PDS_PATRON 
  
> An einen Systembenutzer für physische Zustellungen, wie ein herkömmliches Post Postfach, übermittelt.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Wird an einen privaten Benutzer-Agent (UA), beispielsweise einen Client in einem internen Messagingsystem, übermittelt.
    
MAPI_MH_DP_PUBLIC_UA 
  
> An einen öffentlichen Benutzer-Agent oder einen öffentlichen Dienstanbieter übermittelt.
    
Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, also ein MAPI-Client. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

