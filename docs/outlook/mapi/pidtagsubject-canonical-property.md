---
title: PidTagSubject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 92682661770dff7e704a8c7aac4c38e601595835
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591367"
---
# <a name="pidtagsubject-canonical-property"></a>PidTagSubject (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vollständigen Betreff einer Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Kennung:  <br/> |0x0037  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen. 
  
Diese Eigenschaften sind immer der vollständige Betrefftext, d. h. die Verkettung des Präfixes und des normalisierten Betreffs. Wenn kein Präfix vorhanden ist, sollte der normalisierte Betreff mit dem Betreff identisch sein. Ein Nachrichtenspeicher- oder Transportanbieter verwendet diese Eigenschaften und **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) -Eigenschaften, um den normalisierten Betreff mithilfe der unter **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) beschriebenen Regel zu berechnen.
  
Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die **IStream-Schnittstelle** für sie zu unterstützen. Der Client sollte immer zuerst versuchen, über die **IMAPIProp-Schnittstelle** auf **IStream** zuzugreifen, wenn **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird. 
  
Bei einem Bericht enthält diese Eigenschaft den Betreff der ursprünglichen Nachricht, der eine Zeichenfolge vorangestellt ist, die angibt, was mit der Nachricht passiert ist.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

