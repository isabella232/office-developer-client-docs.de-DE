---
title: Kanonische Pidlidtaskassigners (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303066"
---
# <a name="pidlidtaskassigners-canonical-property"></a>Kanonische Pidlidtaskassigners (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Stapel von Einträgen, die Aufgaben Verteiler darstellen. Der letzte Aufgaben beauftragte wird oben im Stapel angezeigt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskMyDelegators  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x00008117  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Client eine Aufgabenanfrage erhält, fügt er an diese Eigenschaft an, welche Struktur in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)definiert ist, ein Eintrag, der den Absender der Aufgabe darstellt. Wenn der Client eine Aufgaben Ablehnung erhält, entfernt der Client den Eintrag letzter Aufgaben-Absender aus dieser Eigenschaft. Wenn der Client eine Aufgaben Antwort sendet, sendet der Client ihn an den zuletzt im Wert dieser Eigenschaft aufgeführten Aufgaben Beauftragten.
  
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

