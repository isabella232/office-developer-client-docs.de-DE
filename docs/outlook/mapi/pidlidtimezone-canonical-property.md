---
title: PidLidTimeZone (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319271"
---
# <a name="pidlidtimezone-canonical-property"></a>PidLidTimeZone (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zur Zeitzone einer Besprechungsserie an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |LID_TIME_ZONE  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Lange ID (LID):  <br/> |0x0000000C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur gelesen, wenn die **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) -Eigenschaft nicht festgelegt ist, aber wenn die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) -Eigenschaft TRUE und die **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) -Eigenschaft false ist. Der untere WORD-Wert gibt einen Index in einer Tabelle an, die Zeitzoneninformationen enthält. Aus dem oberen WORD wird nur das höchste Bit gelesen. Wenn dieses Bit festgelegt ist, wird in der referenzierten Zeitzone die Sommerzeit (Sommerzeit, Sommerzeit, Sommerzeit) nicht beobachtet, andernfalls werden die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) detaillierten Sommerzeitdaten befolgt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

