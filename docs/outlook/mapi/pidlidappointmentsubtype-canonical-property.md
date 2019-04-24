---
title: Kanonische Pidlidappointmentsubtype (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345416"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Kanonische Pidlidappointmentsubtype (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Ereignis ganztägig ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptSubType  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x00008215  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, ob das Ereignis ein ganztägiges Ereignis ist, wie vom Benutzer angegeben. Der Wert TRUE gibt an, dass das Ereignis ein ganztägiges Ereignis ist, in dem die Startzeit und die Endzeit Mitternacht sein müssen, damit die Dauer ein Vielfaches von 24 Stunden ist und mindestens 24 Stunden beträgt. Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Ereignis kein ganztägiges Ereignis ist. Der Client oder Server darf den Wert nicht als TRUE ableiten, wenn ein Benutzer ein Ereignis erstellt, das 24 Stunden dauert, auch wenn das Ereignis um Mitternacht beginnt und endet.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

