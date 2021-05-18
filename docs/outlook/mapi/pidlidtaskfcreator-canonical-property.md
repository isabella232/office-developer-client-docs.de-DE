---
title: PidLidTaskFCreator (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303080"
---
# <a name="pidlidtaskfcreator-canonical-property"></a>PidLidTaskFCreator (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass die Aufgabe ursprünglich vom aktuellen Benutzer- oder Benutzer-Agent erstellt wurde, anstatt eine Aufgabenanforderung zu verarbeiten.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskFCreator  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Lange ID (LID):  <br/> |0x0000811E  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Client legt diese Eigenschaft auf TRUE fest, wenn der Benutzer die Aufgabe erstellt, und auf FALSE, wenn die Aufgabe von einem anderen Benutzer zugewiesen wird. Wenn diese Eigenschaft nicht mehr verwendet wird, wird der Wert TRUE angenommen.
  
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

