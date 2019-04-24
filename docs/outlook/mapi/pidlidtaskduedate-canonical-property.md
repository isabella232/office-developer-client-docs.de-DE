---
title: Kanonische Pidlidtaskduedate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303325"
---
# <a name="pidlidtaskduedate-canonical-property"></a>Kanonische Pidlidtaskduedate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt das Datum dar, an dem der Benutzer erwartet, die Aufgabe abzuschließen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskDueDate  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x00008105  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Aufgabe hat kein Fälligkeitsdatum, wenn diese Eigenschaft nicht festgelegt oder auf 0x5AE980E0 (1.525.252.320) eingestellt ist. Ein Fälligkeitsdatum ist jedoch nur optional, wenn kein Startdatum in der **dispidTaskStartDate** ([pidlidtaskstartdate (](pidlidtaskstartdate-canonical-property.md))-Eigenschaft angegeben ist. Wenn der Vorgang ein Fälligkeitsdatum hat, muss der Wert eine Zeitkomponente von Mitternacht aufweisen, und die **dispidCommonEnd** ([pidlidcommonend (](pidlidcommonend-canonical-property.md))-Eigenschaft muss ebenfalls festgelegt werden. Wenn **dispidTaskStartDate** ein Startdatum hat, muss der Wert der **dispidTaskDueDate** -Eigenschaft größer oder gleich dem Wert von **dispidTaskStartDate**sein.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

