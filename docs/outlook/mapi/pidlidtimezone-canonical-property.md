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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793884"
---
# <a name="pidlidtimezone-canonical-property"></a>PidLidTimeZone (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt Informationen über die Zeitzone einer Besprechungsserie.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |LID_TIME_ZONE  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Meeting  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000000C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt, wenn die **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft nicht festgelegt ist, aber die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md))-Eigenschaft ist TRUE und **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md))-Eigenschaft lautet FALSE. Das untere Wort gibt einen Index in einer Tabelle, die Informationen zur Zeitzone enthält. Die obere Wort ist nur das höchste Bit gelesen werden. Wenn dieses Bit gesetzt ist, klicken Sie dann berücksichtigt die Zeitzone auf die verwiesen wird nicht, dass Sommerzeit (Ziel), andernfalls die neuen Sommerzeitregeln Datumsangaben in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) beschrieben ausgeführt wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

