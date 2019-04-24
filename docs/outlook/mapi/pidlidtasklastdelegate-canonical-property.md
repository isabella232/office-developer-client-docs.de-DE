---
title: Kanonische Pidlidtasklastdelegate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355671"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a>Kanonische Pidlidtasklastdelegate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Benennt den Benutzer, dem die Aufgabe zuletzt zugewiesen oder zugewiesen wurde. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskLastDelegate  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x00008125  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Vor dem Senden einer Aufgabenanfrage legt der Client diese Eigenschaft auf den Namen des Aufgaben beauftragten fest. Vor dem Senden einer Aufgaben Antwort legt der Client diese Eigenschaft auf den Namen des Aufgabenempfängers fest.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt die Eigenschaftensatz Definition und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
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

