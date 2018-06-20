---
title: Kanonische PidTagDeliveryPoint-Eigenschaft
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
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794310"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Kanonische PidTagDeliveryPoint-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt die Art der funktionalen Entität, mit der eine Nachricht wurde oder wird an den Empfänger übermittelt wurde. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DELIVERY_POINT  <br/> |
|Bezeichner:  <br/> |0x0C07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann genau einen der folgenden Werte aufweisen: 
  
MAPI_MH_DP_ML 
  
> An eine Verteilerliste gesendet, die wiederum die Nachricht an mehrere Empfänger verteilen kann eine Übermittlung zeigen.
    
MAPI_MH_DP_MS 
  
> An einen Nachrichtenspeicher anstatt direkt an einen Empfänger übermittelt.
    
MAPI_MH_DP_OTHER_AU 
  
> Eine Access Organizational Unit (AU) als eine physische Bereitstellung Access Einheit (PDAU), wie ein FAX System zugestellt.
    
MAPI_MH_DP_PDAU 
  
> An eine physische Bereitstellung Access Einheit wie eine human postalische Netzbetreiber übermittelt wurden.
    
MAPI_MH_DP_PDS_PATRON 
  
> An ein physisches Delivery System Leser, wie eine herkömmliche postalische Postfach übermittelt wurden.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Übermittelt eine private Benutzer-Agent (UA), wie ein Client in einem internen messaging-System.
    
MAPI_MH_DP_PUBLIC_UA 
  
> An eine öffentliche Benutzer-Agent oder öffentlichen Dienstanbieter übermittelt wurden.
    
Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, d. h., einem MAPI-Client. 
  
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

