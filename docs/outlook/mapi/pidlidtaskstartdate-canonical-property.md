---
title: Kanonische Pidlidtaskstartdate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316681"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Kanonische Pidlidtaskstartdate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Datum, an dem der Benutzer erwartet, dass die Aufgabe beginnen soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskStartDate  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x00008104  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn dieser Eigenschaftswert Links ist, hat der Vorgang kein Startdatum. Der Wert "0x5AE980E0" (1.525.252.320) bedeutet auch, dass der Vorgang kein Startdatum hat. Wenn der Vorgang ein Startdatum hat, muss der Wert eine Zeitkomponente von Mitternacht aufweisen, und die Eigenschaften **dispidTaskDueDate** ([Pidlidtaskduedate (](pidlidtaskduedate-canonical-property.md)) und **dispidCommonStart** ([pidlidcommonstart (](pidlidcommonstart-canonical-property.md)) müssen ebenfalls festgelegt werden.
  
Diese Eigenschaft wird von der Informations Kennzeichnungs Protokoll Spezifikation und der aufgabenbezogenen Objekt Protokoll Spezifikation in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)gemeinsam genutzt.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidLidTaskDueDate-Eigenschaft](pidlidtaskduedate-canonical-property.md)
  
[Kanonische PidLidCommonStart-Eigenschaft](pidlidcommonstart-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

