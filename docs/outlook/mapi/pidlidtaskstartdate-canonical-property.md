---
title: PidLidTaskStartDate (kanonische Eigenschaft)
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
ms.openlocfilehash: 486b1f913e7c3c76886232c48fa842e25e1f7905
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793854"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>PidLidTaskStartDate (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Das Datum, wenn der Benutzer für den Task erwartet.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskStartDate  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008104  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft nicht festgelegt lassen, hat die Aufgabe ein Startdatum keinen. Der Wert "0x5AE980E0" (1,525,252,320) bedeutet auch, dass die Aufgabe ein Startdatum nicht vorhanden ist. Wenn der Vorgang ein Startdatum hat, der Wert muss eine Zeitkomponente Mitternacht haben, und die **DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) und **DispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) Eigenschaften müssen ebenfalls festgelegt werden.
  
Diese Eigenschaft wird von der Informationszwecken kennzeichnen Protokollspezifikation gemeinsam genutzt und Task-Related Object Protokoll Specification befindet sich in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die auf Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidLidTaskDueDate-Eigenschaft](pidlidtaskduedate-canonical-property.md)
  
[Kanonische PidLidCommonStart-Eigenschaft](pidlidcommonstart-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

