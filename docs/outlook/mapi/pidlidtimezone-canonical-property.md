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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389925"
---
# <a name="pidlidtimezone-canonical-property"></a>PidLidTimeZone (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen über die Zeitzone einer Besprechungsserie.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |LID_TIME_ZONE  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Meeting  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000000C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt, wenn die **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft nicht festgelegt ist, aber die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md))-Eigenschaft ist TRUE und **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md))-Eigenschaft lautet FALSE. Das untere Wort gibt einen Index in einer Tabelle, die Informationen zur Zeitzone enthält. Die obere Wort ist nur das höchste Bit gelesen werden. Wenn dieses Bit gesetzt ist, klicken Sie dann berücksichtigt die Zeitzone auf die verwiesen wird nicht, dass Sommerzeit (Ziel), andernfalls die neuen Sommerzeitregeln Datumsangaben in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) beschrieben ausgeführt wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

