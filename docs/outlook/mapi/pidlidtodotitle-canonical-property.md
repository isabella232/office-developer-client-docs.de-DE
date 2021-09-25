---
title: PidLidToDoTitle (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b93ff05c13ab9801e9830e36aeecdf942e53d233
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583639"
---
# <a name="pidlidtodotitle-canonical-property"></a>PidLidToDoTitle (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält benutzerdefinierten Text, um dieses Nachrichtenobjekt in einer konsolidierten Aufgabenliste zu identifizieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidToDoTitle  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A4  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft darf nicht für eine Aufgabe festgelegt werden. Um eine leere Eigenschaft anzugeben, legen Sie diese Eigenschaft nicht auf die leere Zeichenfolge fest, sondern löschen Sie sie. 
  
Wenn ein Nachrichtenobjekt gekennzeichnet wird und die Eigenschaft nicht vorhanden ist, sollte ein Client den Wert von **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) in diese Eigenschaft schreiben.
  
Wenn diese Eigenschaft in einer konsolidierten Aufgabenliste nicht vorhanden ist, sollte ein Client den Wert der **PR_NORMALIZED_SUBJECT-Eigenschaft** ersetzen, wenn diese Eigenschaft in der Aufgabenliste angezeigt wird. 
  
Wenn der Client in einem Nachrichtenentwurfsobjekt Absenderflags implementiert, sollte diese Eigenschaft auf denselben Wert wie **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) festgelegt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[PidTagNormalizedSubject (kanonische Eigenschaft)](pidtagnormalizedsubject-canonical-property.md)
  
[Kanonische PidLidFlagRequest-Eigenschaft](pidlidflagrequest-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

