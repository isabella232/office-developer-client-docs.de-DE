---
title: PidTagReportText (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 09bd3bdf-28d6-432c-9213-562a9a271adc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7173caa7a31bc3ad11a4785b6a1498aba139de7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359192"
---
# <a name="pidtagreporttext-canonical-property"></a>PidTagReportText (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält optionalen Text für einen Bericht, der vom Messagingsystem generiert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPORT_TEXT, PR_REPORT_TEXT_A, PR_REPORT_TEXT_W  <br/> |
|Kennung:  <br/> |0x1001  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>Hinweise

In der Regel wird der in diesen Eigenschaften enthaltene Text als Antwort auf einen Zustellungs- oder Unzustellungsbericht oder einen lese- oder ungelesenen Bericht generiert, der vom zugrunde liegenden Messagingsystem empfangen wurde, ist jedoch nicht selbst Text, der über dieses System übertragen wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
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

