---
title: Kanonische pidlidappointmentauxiliaryflags (-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345430"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Kanonische pidlidappointmentauxiliaryflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Bit-Feld an, das den Hilfs-Status des Objekts beschreibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptAuxFlags  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x00008207  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nicht erforderlich. Im folgenden finden Sie die einzelnen Flags, die festgelegt werden können.
  
C (auxApptFlagCopied, 0x00000001)
  
> Dieses Flag gibt an, dass das Calendar-Objekt aus einem anderen Kalenderordner kopiert wurde.
    
R (auxApptFlagForceMtgResponse, 0x00000002)
  
> Dieses Flag für eine Besprechungsanfrage gibt an, dass der Client oder Server eine Besprechungsantwort zurück an den Organisator senden soll, wenn eine Antwort ausgewählt wird.
    
F (auxApptFlagForwarded, 0x00000004)
  
> Dieses Flag für eine Besprechungsanfrage gibt an, dass es weitergeleitet wurde (einschließlich der Weiterleitung durch den Organisator), statt eine Einladung des Organisators zu sein.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

