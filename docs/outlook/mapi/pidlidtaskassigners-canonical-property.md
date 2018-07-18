---
title: PidLidTaskAssigners (kanonische Eigenschaft)
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
ms.openlocfilehash: 89e0b6eae35de9e40dba411afb82e19aa81fb635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793806"
---
# <a name="pidlidtaskassigners-canonical-property"></a>PidLidTaskAssigners (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen Stack von Einträgen, die Aufgabe Assigners darstellen. Die letzte Aufgabe delegierende Person wird am oberen Rand des Stapels angezeigt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskMyDelegators  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008117  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der Client eine Aufgabenanfrage erhält, fügt es an diese Eigenschaft, welche Struktur in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), ein Eintrag definiert ist, der Absender die Aufgabe darstellt. Wenn der Client eine Aufgabe Ablehnung erhält, entfernt der Client den letzten Aufgabe delegierende Person Eintrag aus dieser Eigenschaft an. Wenn der Client eine Taskantwort sendet, sendet der Client es auf die letzte Aufgabe delegierende Person, die in der Wert dieser Eigenschaft aufgelistet.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen modellieren definiert 
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

