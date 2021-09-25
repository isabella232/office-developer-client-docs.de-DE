---
title: Kanonische PidTagReportText-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 09bd3bdf-28d6-432c-9213-562a9a271adc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 94a951f06458cd24b50797e24d727b2f3bcaad8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591549"
---
# <a name="pidtagreporttext-canonical-property"></a>Kanonische PidTagReportText-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält optionalen Text für einen vom Messagingsystem generierten Bericht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPORT_TEXT, PR_REPORT_TEXT_A, PR_REPORT_TEXT_W  <br/> |
|Kennung:  <br/> |0x1001  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der Regel wird der in diesen Eigenschaften enthaltene Text als Reaktion auf einen Übermittlungs- oder Unzustellbarkeitsbericht oder einen gelesenen oder nicht gelesenen Bericht generiert, der vom zugrunde liegenden Messagingsystem empfangen wurde, aber nicht selbst Text ist, der über dieses System übertragen wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
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

