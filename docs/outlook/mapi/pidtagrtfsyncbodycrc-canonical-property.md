---
title: Kanonische Pidtagrtfsyncbodycrc (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357869"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a>Kanonische Pidtagrtfsyncbodycrc (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die zyklische Redundanzprüfung (CRC), die für den Nachrichtentext berechnet wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_SYNC_BODY_CRC  <br/> |
|Kennung:  <br/> |0x1006  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die [RTFSync](rtfsync.md) -Funktion berechnet den CRC nur mit den Zeichen, die für die Nachricht als bedeutsam erachtet werden. Beispielsweise werden einige Leerraum und andere ignorierte Zeichen aus dem CRC ausgelassen. 
  
Diese Eigenschaft ist eine Hilfseigenschaft für Rich-Text-Format (RTF). Diese Eigenschaften werden von der **RTFSync** -Funktion verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

