---
title: Kanonische PidLidAppointmentSubType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b9b1b4615893418374b98403e7d519d3f632d07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591892"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Kanonische PidLidAppointmentSubType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Ereignis den ganzen Tag ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptSubType  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008215  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt an, ob es sich bei dem Ereignis um ein ganztägiges Ereignis handelt, wie vom Benutzer angegeben. Der Wert TRUE gibt an, dass es sich bei dem Ereignis um ein ganztägiges Ereignis handelt. In diesem Fall müssen Startzeit und Endzeit Mitternacht sein, damit die Dauer ein Vielfaches von 24 Stunden und mindestens 24 Stunden beträgt. Der Wert FALSE oder das Fehlen dieser Eigenschaft weist darauf hin, dass es sich bei dem Ereignis nicht um ein ganztägiges Ereignis handelt. Der Client oder Server darf den Wert nicht als TRUE ableiten, wenn ein Benutzer ein Ereignis erstellt, das 24 Stunden dauert, auch wenn das Ereignis um Mitternacht beginnt und endet.
  
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

