---
title: PidLidTaskHistory (kanonische Eigenschaft)
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
ms.openlocfilehash: 6e53d91a80d7e3b3bb4bf02ff3446eb385293c6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793851"
---
# <a name="pidlidtaskhistory-canonical-property"></a>PidLidTaskHistory (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt den Typ der Änderung an, die für die Aufgabe zuletzt vorgenommen wurde.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskHistory  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000811A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft festgelegt ist, muss auch die **DispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md))-Eigenschaft auf die aktuelle Zeit festgelegt werden. In der folgenden Tabelle werden die **DispidTaskHistory** Eigenschaftenwerte, in der Reihenfolge der Priorität niedriger aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 x 00000004  <br/> |Die **DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md))-Eigenschaft geändert wurde.  <br/> |
|0 x 00000003  <br/> |Eine andere Eigenschaft geändert wurde.  <br/> |
|0x00000001  <br/> |Beauftragte für die Aufgabe angenommen für diese Aufgabe.  <br/> |
|0x00000002  <br/> |Beauftragte für die Aufgabe abgelehnt für diese Aufgabe.  <br/> |
|0 x 00000005  <br/> |Die Aufgabe wurde einer zugewiesenen Aufgabe zugewiesen.  <br/> |
|0x00000000  <br/> |Keine Änderungen vorgenommen wurden.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

