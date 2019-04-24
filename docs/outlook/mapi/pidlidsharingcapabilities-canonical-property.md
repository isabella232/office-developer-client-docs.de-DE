---
title: Kanonische Pidlidsharingcapabilities (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d44851e1c863cb117eed3462eb98de87f8d1f0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358891"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a>Kanonische Pidlidsharingcapabilities (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kennzeichnet als Eigenschaft einer Freigabenachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingCaps  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Sharing  <br/> |
|Long-ID (Deckel):  <br/> |0x00008A17  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss auf einen der folgenden Werte festgelegt werden:
  
|**Wert**|**Szenario**|
|:-----|:-----|
|0x00040290  <br/> |Dieses Freigabenachrichten Objekt bezieht sich auf einen speziellen Ordner.  <br/> |
|0x000402B0  <br/> |Dieses Freigabenachrichten Objekt bezieht sich nicht auf einen speziellen Ordner.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Freigabe von Postfachordnern zwischen Clients.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

