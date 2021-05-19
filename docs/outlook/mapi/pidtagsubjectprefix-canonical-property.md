---
title: PidTagSubjectPrefix (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339228"
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
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen. 
  
Das Betreffpräfix besteht aus einem oder mehreren alphanumerischen Zeichen, gefolgt von einem Doppelpunkt und einem Leerzeichen (die Teil des Präfixes sind). Er darf keine nichtalphanumerischen Zeichen vor dem Doppelpunkt enthalten. Das Fehlen eines Präfixes kann durch eine leere Zeichenfolge dargestellt werden oder durch diese Eigenschaft, die nicht festgelegt wird. 
  
Wenn diese Eigenschaften explizit festgelegt werden, kann die Zeichenfolge eine beliebige Länge haben und alphanumerische Zeichen verwenden, sie muss jedoch mit einer Teilzeichenfolge am Anfang der **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft übereinstimmen. Wenn diese Eigenschaften nicht vom Absender festgelegt werden und berechnet werden müssen, sind ihre Inhalte eingeschränkter. Die Regel zum Berechnen des Präfixes **ist, dass PR_SUBJECT** mit einem, zwei oder drei Buchstaben (nur alphabetisch) gefolgt von einem Doppelpunkt und einem Leerzeichen beginnen muss. Wenn eine solche Teilzeichenfolge am Anfang von **PR_SUBJECT** gefunden wird, wird sie dann zur Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang PR_SUBJECT **).** Andernfalls bleiben diese Eigenschaften nicht festgelegt. 
  
Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollten als Teil der [IMAPIProp::SaveChanges-Implementierung berechnet](imapiprop-savechanges.md) werden. Ein Client sollte [IMAPIProp::GetProps](imapiprop-getprops.md) erst dann zur Eingabe seiner Werte aufrufen, wenn er von einem **IMAPIProp::SaveChanges-Aufruf ausgeführt** wurde. 
  
Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die OLE **IStream-Schnittstelle** für sie zu unterstützen. Ein Client sollte immer zuerst den Zugriff über die **IMAPIProp-Schnittstelle** versuchen und nur dann auf **IStream** zugreifen, **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

