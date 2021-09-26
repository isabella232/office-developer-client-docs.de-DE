---
title: PidTagSubjectPrefix (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c2bece089bc985111695f5bb54098d3fc6c4f0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624454"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>PidTagSubjectPrefix (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Betreffpräfix, das in der Regel eine Aktion für eine Nachricht angibt, z. B. "FW: " für die Weiterleitung. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Kennung:  <br/> |0x003D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen. 
  
Das Betreffpräfix besteht aus einem oder mehreren alphanumerischen Zeichen, gefolgt von einem Doppelpunkt und einem Leerzeichen (die Teil des Präfixes sind). Es darf keine nicht alphanumerischen Zeichen vor dem Doppelpunkt enthalten. Das Fehlen eines Präfixes kann durch eine leere Zeichenfolge oder durch diese Eigenschaft dargestellt werden, die nicht festgelegt wird. 
  
Wenn diese Eigenschaften explizit festgelegt werden, kann die Zeichenfolge eine beliebige Länge haben und alphanumerische Zeichen verwenden, muss jedoch mit einer Teilzeichenfolge am Anfang der **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) -Eigenschaft übereinstimmen. Wenn diese Eigenschaften nicht vom Absender festgelegt werden und berechnet werden müssen, sind deren Inhalte eingeschränkter. Die Regel zum Berechnen des Präfixes ist, dass **PR_SUBJECT** mit einem, zwei oder drei Buchstaben (nur alphabetisch) gefolgt von einem Doppelpunkt und einem Leerzeichen beginnen muss. Wenn eine solche Teilzeichenfolge am Anfang von **PR_SUBJECT** gefunden wird, wird sie zur Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang von **PR_SUBJECT**). Andernfalls bleiben diese Eigenschaften nicht festgelegt. 
  
Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollten als Teil der [IMAPIProp::SaveChanges-Implementierung](imapiprop-savechanges.md) berechnet werden. Ein Client sollte [IMAPIProp::GetProps](imapiprop-getprops.md) erst dann zur Eingabe seiner Werte auffordern, wenn ein Commit durch einen **IMAPIProp::SaveChanges-Aufruf** ausgeführt wurde. 
  
Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die OLE **IStream-Schnittstelle** für sie zu unterstützen. Ein Client sollte immer zuerst versuchen, über die **IMAPIProp-Schnittstelle** auf **IStream** zuzugreifen, wenn **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

