---
title: PidLidAppointmentAuxiliaryFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cac9c735403e6cb65dfe3111a2246a8387339339
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793338"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>PidLidAppointmentAuxiliaryFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt ein Bitfeld, das den Hilfs Status des Objekts beschreibt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidApptAuxFlags  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008207  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nicht erforderlich. Im folgenden sind die einzelnen Flags, die festgelegt werden können.
  
C (AuxApptFlagCopied, 0 x 00000001)
  
> Dieses Kennzeichen gibt an, dass das Calendar-Objekt aus einer anderen Kalenderordner kopiert wurde.
    
R (AuxApptFlagForceMtgResponse, 0 x 00000002)
  
> Dieses Kennzeichen auf eine Besprechungsanfrage gibt an, dass der Client oder Server gesendet wird eine Antwort auf Besprechungsanfrage wieder an den Organisator beim eine Antwort ausgewählt wird.
    
F (AuxApptFlagForwarded, 0 x 00000004)
  
> Dieses Flag auf eine Besprechungsanfrage bedeutet, dass sie weitergeleitet wurde (einschließlich vom Organisator weitergeleiteten), sondern wird eine Einladung aus organisieren.
    
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

