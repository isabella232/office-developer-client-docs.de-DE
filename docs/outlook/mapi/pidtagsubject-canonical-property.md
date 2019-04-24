---
title: Kanonische PidTagSubject-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339256"
---
# <a name="pidtagsubject-canonical-property"></a>Kanonische PidTagSubject-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vollständigen Betreff einer Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Kennung:  <br/> |0x0037  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen. 
  
Diese Eigenschaften sind immer der vollständige Betrefftext, also die Verkettung des Präfix und des normalisierten betreffs. Wenn kein Präfix vorliegt, sollte der normalisierte Betreff mit dem Betreff übereinstimmen. Ein Nachrichtenspeicher oder Transportanbieter verwendet beide Eigenschaften und **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md))-Eigenschaften, um den normalisierten Betreff mithilfe der unter **PR_NORMALIZED_SUBJECT** beschriebenen Regel zu berechnen ([ PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
Die Subject-Eigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicher Anbieter ist nicht dazu verpflichtet, die **IStream** -Schnittstelle zu unterstützen. Der Client sollte immer versuchen, zuerst über die **IMAPIProp** -Schnittstelle zuzugreifen, und nur dann auf **IStream** zurückgreifen, wenn **MAPI_E_NOT_ENOUGH_MEMORY** wird. 
  
Bei einem Bericht enthält diese Eigenschaft den Betreff der ursprünglichen Nachricht, der eine Zeichenfolge vorausgeht, die angibt, was mit der Nachricht passiert ist.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

