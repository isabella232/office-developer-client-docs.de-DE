---
title: Kanonische Pidlidappointmentreplyname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356042"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a>Kanonische Pidlidappointmentreplyname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Benutzer an, der zuletzt auf die Besprechungsanfrage oder das Besprechungs Update Objekt geantwortet hat.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptReplyName  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x00008230  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur für einen delegierenden festgelegt, wenn ein Delegat reagiert. Der Wert ist gleich der **PR_MAILBOX_OWNER_NAME** ([pidtagmailboxownername (](pidtagmailboxownername-canonical-property.md))-Eigenschaft für den Speicher des Delegaten. Diese Eigenschaft hat keine Bedeutung für den Organisator. Weitere Informationen zu **PR_MAILBOX_OWNER_NAME**finden Sie unter Store Object Protocol, angegeben in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Stellt Datentypdefinitionen bereit.
    
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

