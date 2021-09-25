---
title: PidTagOriginatorDeliveryReportRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3a31b767ef02e12dced9e2a43f9cdba7f2a4e220
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574945"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>PidTagOriginatorDeliveryReportRequested (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nachrichtensender einen Übermittlungsbericht für einen bestimmten Empfänger vom Messagingsystem anfordert, bevor die Nachricht im Nachrichtenspeicher abgelegt wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Kennung:  <br/> |0x0023  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird verwendet, um das Messagingsystem bei der Verarbeitung von zugestellten Nachrichten zu leiten. In diesem Fall muss die Nachricht auch die **eigenschaft PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) auf FALSE festlegen.
  
Das Festlegen der **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** Eigenschaft für eine Nachricht ist eine Möglichkeit, Übermittlungsstatusberichte für alle Empfänger anzufordern. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

