---
title: Kanonische Pidlidtodotitle (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339942"
---
# <a name="pidlidtodotitle-canonical-property"></a>Kanonische Pidlidtodotitle (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält benutzerspezifischen Text, um dieses Nachrichtenobjekt in einer konsolidierten Aufgabenliste zu identifizieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidToDoTitle  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x000085A4  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft darf für einen Vorgang nicht festgelegt werden. Um eine leere Eigenschaft anzugeben, legen Sie diese Eigenschaft nicht auf die Zeichenfolge der Länge 0 (null), sondern stattdessen löschen. 
  
Wenn ein Message-Objekt gekennzeichnet wird und die Eigenschaft nicht vorhanden ist, sollte der Wert von **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) in diese Eigenschaft geschrieben werden.
  
Wenn diese Eigenschaft in einer konsolidierten Aufgabenliste nicht vorhanden ist, sollte der Wert der **PR_NORMALIZED_SUBJECT** -Eigenschaft durch einen Client ersetzt werden, wenn diese Eigenschaft in der Aufgabenliste angezeigt wird. 
  
Bei einem Entwurfsnachrichten Objekt sollte diese Eigenschaft auf den gleichen Wert wie **dispidRequest** ([pidlidflagrequest (](pidlidflagrequest-canonical-property.md)) festgelegt werden, wenn der Client Absender-Flags implementiert.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagNormalizedSubject-Eigenschaft](pidtagnormalizedsubject-canonical-property.md)
  
[Kanonische PidLidFlagRequest-Eigenschaft](pidlidflagrequest-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

