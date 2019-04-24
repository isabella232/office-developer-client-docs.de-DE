---
title: Kanonische Pidtagrecipientproposedstarttime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8815728adce809641586c4da5beb4c9fad735507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283142"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a>Kanonische Pidtagrecipientproposedstarttime (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine vorgeschlagene Startzeit einer Besprechung an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_PROPOSEDSTARTTIME  <br/> |
|Kennung:  <br/> |0x5FE3  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Transport Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([pidtagrecipientproposed (](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf true festgelegt ist, gibt der Wert dieser Eigenschaft den Wert an, der vom Teilnehmer angefordert wird, um den Wert des **dispidApptStartWhole** festzulegen ([ Pidlidappointmentstartwhole (](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft für das Besprechungsobjekt oder Exception-Objekt einer einzelnen Instanz.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
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

