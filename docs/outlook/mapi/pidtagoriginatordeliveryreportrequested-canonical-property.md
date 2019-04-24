---
title: Kanonische PidTagOriginatorDeliveryReportRequested-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356301"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>Kanonische PidTagOriginatorDeliveryReportRequested-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nachrichtenabsender einen Übermittlungsbericht für einen bestimmten Empfänger vom Messagingsystem anfordert, bevor die Nachricht im Nachrichtenspeicher abgelegt wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Kennung:  <br/> |0x0023  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird verwendet, um das Messagingsystem bei der Verarbeitung zugestellter Nachrichten zu leiten. In diesem Fall muss die Nachricht auch die **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([pidtagoriginatornondeliveryreportrequested (](pidtagoriginatornondeliveryreportrequested-canonical-property.md))-Eigenschaft auf false festlegen.
  
Das Festlegen der **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** -Eigenschaft für eine Nachricht stellt eine Möglichkeit dar, um Übermittlungsstatusberichte für alle Empfänger anzufordern. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

