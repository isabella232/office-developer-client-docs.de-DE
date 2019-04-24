---
title: Kanonische Pidlidtaskassigner (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340089"
---
# <a name="pidlidtaskassigner-canonical-property"></a>Kanonische Pidlidtaskassigner (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Benennt den Benutzer, dem die Aufgabe zuletzt zugewiesen wurde. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskDelegator  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x00008121  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Aufgabe nicht zugewiesen wurde, wird diese Eigenschaft nicht festgelegt. Da der Client diese Eigenschaft festlegt, nachdem der Aufgabenempfänger eine Aufgabenanforderung erhalten hat, wird die Eigenschaft nicht für die Kopie der Aufgabe des Aufgaben beauftragten festgelegt. Wenn der Client einen Aufgaben beauftragten aus der Liste Aufgaben Verteiler in der **dispidTaskMyDelegators** ([pidlidtaskassigners (](pidlidtaskassigners-canonical-property.md))-Eigenschaft hinzufügt oder daraus entfernt, muss die **dispidTaskDelegator** ([pidlidtaskassigner (](pidlidtaskassigner-canonical-property.md))-Eigenschaft auf den hinzugefügten Wert festgelegt werden. oder entfernter Aufgaben Versender.
  
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

