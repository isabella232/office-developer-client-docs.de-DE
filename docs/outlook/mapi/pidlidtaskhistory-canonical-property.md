---
title: Kanonische Pidlidtaskhistory (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303010"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Kanonische Pidlidtaskhistory (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Typ der letzten Änderung an der Aufgabe an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskHistory  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x0000811A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft festgelegt ist, muss die **dispidTaskLastUpdate** ([pidlidtasklastupdate (](pidlidtasklastupdate-canonical-property.md))-Eigenschaft auch auf die aktuelle Uhrzeit festgelegt werden. In der folgenden Tabelle sind die Werte der **dispidTaskHistory** -Eigenschaft aufgeführt, die in der Reihenfolge der niedrigeren Priorität aufgelistet sind. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000004  <br/> |Die **dispidTaskDueDate** ([pidlidtaskduedate (](pidlidtaskduedate-canonical-property.md))-Eigenschaft wurde geändert.  <br/> |
|0x00000003  <br/> |Eine andere Eigenschaft wurde geändert.  <br/> |
|0x00000001  <br/> |Der Aufgabenempfänger hat diese Aufgabe akzeptiert.  <br/> |
|0x00000002  <br/> |Der Aufgabenempfänger hat diese Aufgabe abgelehnt.  <br/> |
|0x00000005  <br/> |Die Aufgabe wurde einem Aufgabenempfänger zugewiesen.  <br/> |
|0x00000000  <br/> |Es wurden keine Änderungen vorgenommen.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

