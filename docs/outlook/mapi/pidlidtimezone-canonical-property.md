---
title: Kanonische PidLidTimeZone-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ada0ccc7844fc259cc85a33ed3bfe441f4b26a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571290"
---
# <a name="pidlidtimezone-canonical-property"></a>Kanonische PidLidTimeZone-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zur Zeitzone einer Besprechungsserie an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |LID_TIME_ZONE  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x0000000C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird nur gelesen, wenn die **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) -Eigenschaft nicht festgelegt ist, aber wenn die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) -Eigenschaft TRUE ist und die **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) -Eigenschaft FALSE ist. Das untere WORD gibt einen Index in einer Tabelle an, die Zeitzoneninformationen enthält. Aus dem oberen WORD-Element wird nur das höchste Bit gelesen. Wenn dieses Bit festgelegt ist, wird in der Zeitzone, auf die verwiesen wird, die Sommerzeit (Daylight Saving Time, DST) nicht beobachtet, andernfalls werden die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) beschriebenen DST-Datumsangaben eingehalten. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

