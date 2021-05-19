---
title: PidLidToDoTitle (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339942"
---
# <a name="pidlidtodotitle-canonical-property"></a>PidLidToDoTitle (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält benutzerspezifikationsfähigen Text, um dieses Nachrichtenobjekt in einer konsolidierten To-Do-Liste zu identifizieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidToDoTitle  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x000085A4  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft darf nicht für einen Vorgang festgelegt werden. Wenn Sie eine leere Eigenschaft angeben möchten, legen Sie diese Eigenschaft nicht auf die leere Zeichenfolge, sondern löschen Sie sie. 
  
Wenn ein Nachrichtenobjekt kennzeichnend ist und die Eigenschaft nicht vorhanden ist, sollte ein Client den Wert **von PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) in diese Eigenschaft schreiben.
  
Wenn diese Eigenschaft nicht vorhanden ist, sollte ein Client in einer konsolidierten To-Do-Liste den Wert der **PR_NORMALIZED_SUBJECT-Eigenschaft** ersetzen, wenn diese Eigenschaft in der To-Do-Liste angezeigt wird. 
  
Wenn der Client Absenderflags implementiert, sollte diese Eigenschaft bei einem Nachrichtenentwurfsobjekt auf denselben Wert wie **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) festgelegt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[PidTagNormalizedSubject (kanonische Eigenschaft)](pidtagnormalizedsubject-canonical-property.md)
  
[Kanonische PidLidFlagRequest-Eigenschaft](pidlidflagrequest-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

