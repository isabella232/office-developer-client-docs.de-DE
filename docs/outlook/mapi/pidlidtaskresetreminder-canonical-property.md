---
title: PidLidTaskResetReminder (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a95fc30de7511672cb27c9dd6fbc37b96e822e77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793863"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>PidLidTaskResetReminder (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt an, ob zukünftige Instanzen von Aufgabenserien Erinnerungen, benötigen, obwohl **DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) auf false festgelegt ist.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskResetReminder  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008107  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird auf TRUE festgelegt, wenn die Aufgabe Erinnerung geschlossen ist, und andernfalls auf FALSE festgelegt. Wenn nicht festgelegt, wird davon ausgegangen, dass Standardwert ist FALSE.
  
Wie in [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)angegeben gibt die **DispidReminderSet** -Eigenschaft, ob eine Erinnerung für den Vorgang festgelegt ist. Diese Eigenschaft gibt jedoch nur das Vorhandensein einer Erinnerung für eine einzelne Aufgabe an. Es kann nicht verwendet werden, als eigenständige Anwendung, um festzustellen, ob eine zukünftige Instanz einer Aufgabenserie eine Erinnerung benötigt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidLidReminderSet-Eigenschaft](pidlidreminderset-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

