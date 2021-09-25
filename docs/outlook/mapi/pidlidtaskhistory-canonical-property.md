---
title: Kanonische PidLidTaskHistory-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0e666e4ddcd72a50f3bcefdbfb2339d33d0123bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583688"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Kanonische PidLidTaskHistory-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Typ der Änderung an, die zuletzt an der Aufgabe vorgenommen wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskHistory  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000811A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Wert dieser Eigenschaft festgelegt ist, muss die **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) -Eigenschaft auch auf die aktuelle Uhrzeit festgelegt werden. In der folgenden Tabelle sind die Werte der **dispidTaskHistory-Eigenschaft** aufgeführt, die in der Reihenfolge der abnehmenden Priorität aufgelistet sind. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000004  <br/> |Die **Eigenschaft dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) wurde geändert.  <br/> |
|0x00000003  <br/> |Eine andere Eigenschaft wurde geändert.  <br/> |
|0x00000001  <br/> |Der Aufgabenempfänger hat diese Aufgabe akzeptiert.  <br/> |
|0x00000002  <br/> |Der Aufgabenempfänger hat diese Aufgabe abgelehnt.  <br/> |
|0x00000005  <br/> |Die Aufgabe wurde einem Aufgabenempfänger zugewiesen.  <br/> |
|0x00000000  <br/> |Es wurden keine Änderungen vorgenommen.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Aufgabenzuweisungen und Aufgabenaktualisierungen modellieren.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

