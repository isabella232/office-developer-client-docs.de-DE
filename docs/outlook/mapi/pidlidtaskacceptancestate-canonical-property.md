---
title: Kanonische PidLidTaskAcceptanceState-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bcd1e034e22ff4a075e089fda0dbebd4e7a7d4a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591731"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Kanonische PidLidTaskAcceptanceState-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Annahmestatus der Aufgabe an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskDelegValue  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000812A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der folgenden Tabelle sind die möglichen Werte für diese Eigenschaft aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Die Aufgabe ist nicht zugewiesen.  <br/> |
|0x00000001  <br/> |Der Annahmestatus der Aufgabe ist unbekannt.  <br/> |
|0x00000002  <br/> |Der Aufgabenempfänger hat die Aufgabe akzeptiert. Dieser Wert wird festgelegt, wenn der Client eine Aufgabenakzeptanz verarbeitet.  <br/> |
|0x00000003  <br/> |Der Vorgangsempfänger hat die Aufgabe abgelehnt. Dieser Wert wird festgelegt, wenn der Client eine Vorgangsverweigerung verarbeitet.  <br/> |
   
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

