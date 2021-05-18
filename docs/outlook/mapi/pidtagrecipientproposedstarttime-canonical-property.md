---
title: PidTagRecipientProposedStartTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8815728adce809641586c4da5beb4c9fad735507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283142"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a>PidTagRecipientProposedStartTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine vorgeschlagene Startzeit einer Besprechung an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_PROPOSEDSTARTTIME  <br/> |
|Kennung:  <br/> |0x5FE3  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Transportempfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist, gibt der Wert dieser Eigenschaft den Vom Teilnehmer angeforderten Wert an, der als Wert der **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft für das Besprechungsobjekt oder Ausnahmeobjekt der einzelnen Instanz festgelegt werden soll.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

