---
title: PidLidTaskAcceptanceState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331290"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>PidLidTaskAcceptanceState (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Annahmestatus des Vorgangs an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskDelegValue  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Lange ID (LID):  <br/> |0x0000812A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

In der folgenden Tabelle sind die möglichen Werte für diese Eigenschaft aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Die Aufgabe wird nicht zugewiesen.  <br/> |
|0x00000001  <br/> |Der Annahmestatus des Vorgangs ist unbekannt.  <br/> |
|0x00000002  <br/> |Der Aufgabenbef?hnte hat den Vorgang angenommen. Dieser Wert wird festgelegt, wenn der Client eine Vorgangsakzeptanz verarbeitet.  <br/> |
|0x00000003  <br/> |Der Aufgabenbef?hnte hat den Vorgang abgelehnt. Dieser Wert wird festgelegt, wenn der Client eine Vorgangsabweisung verarbeitet.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

