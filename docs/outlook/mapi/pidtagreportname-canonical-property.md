---
title: Kanonische PidTagReportName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d6f5608aaf6a48680f61156463892eb9831333b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591556"
---
# <a name="pidtagreportname-canonical-property"></a>Kanonische PidTagReportName-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Anzeigenamen für den Empfänger, der Berichte für diese Nachricht erhalten soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W  <br/> |
|Kennung:  <br/> |0x003A  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Empfänger, den der Absender delegiert hat, um berichte zu empfangen, die für diese Nachricht generiert wurden.
  
Eine Clientanwendung, die Berichte an einen anderen Benutzer weiterleiten muss, sollte diese Eigenschaften zum Zeitpunkt der Nachrichtenübermittlung festlegen. Wenn sie nicht festgelegt sind, werden die Berichte an den Absender der Nachricht gesendet.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

