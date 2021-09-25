---
title: Kanonische PidLidAppointmentAuxiliaryFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66bbaccb056dfeba28d3016023a8093bc05927b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591969"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Kanonische PidLidAppointmentAuxiliaryFlags-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Bitfeld an, das den Hilfsstatus des Objekts beschreibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptAuxFlags  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008207  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist nicht erforderlich. Unten sind die einzelnen Kennzeichen aufgeführt, die festgelegt werden können.
  
C (auxApptFlagCopied, 0x00000001)
  
> Dieses Flag gibt an, dass das Kalenderobjekt aus einem anderen Kalenderordner kopiert wurde.
    
R (auxApptFlagForceMtgResponse, 0x00000002)
  
> Dieses Kennzeichen für eine Besprechungsanfrage gibt an, dass der Client oder Server eine Besprechungsantwort zurück an den Organisator senden soll, wenn eine Antwort ausgewählt wird.
    
F (auxApptFlagForwarded, 0x00000004)
  
> Dieses Flag in einer Besprechungsanfrage gibt an, dass sie weitergeleitet wurde (einschließlich der Weiterleitung durch den Organisator), anstatt eine Einladung des Organisators zu sein.
    
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

