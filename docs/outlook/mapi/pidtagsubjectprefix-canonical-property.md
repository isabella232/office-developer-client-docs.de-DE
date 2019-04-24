---
title: Kanonische Pidtagsubjectprefix (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339228"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Kanonische Pidtagsubjectprefix (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Betreff-Präfix, der in der Regel eine Aktion für eine Nachricht angibt, beispielsweise "FW:" für die Weiterleitung. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Kennung:  <br/> |0x003D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen. 
  
Das Betreff-Präfix besteht aus einem oder mehreren alphanumerischen Zeichen, gefolgt von einem Doppelpunkt und einem Raum (die Teil des Präfixes sind). Sie darf keine nicht alphanumerische Zeichen vor dem Doppelpunkt enthalten. Das Fehlen eines Präfixes kann durch eine leere Zeichenfolge oder durch diese Eigenschaft nicht festgelegt werden. 
  
Wenn diese Eigenschaften explizit festgelegt werden, kann die Zeichenfolge eine beliebige Länge aufweisen und alphanumerische Zeichen verwenden, aber Sie muss mit einer Teilzeichenfolge am Anfang der **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft übereinstimmen. Wenn diese Eigenschaften nicht vom Absender festgelegt werden und berechnet werden müssen, sind deren Inhalte eingeschränkter. Die Regel zum Berechnen des Präfixes ist, dass **PR_Subject** mit einem, zwei oder drei Buchstaben (nur alphabetisch) beginnen muss, gefolgt von einem Doppelpunkt und einem Leerzeichen. Wenn eine solche Teilzeichenfolge am Anfang von **PR_Subject**gefunden wird, wird Sie die Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang von **PR_Subject**). Andernfalls bleiben diese Eigenschaften unverändert. 
  
Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollten als Teil der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Implementierung berechnet werden. Ein Client sollte [IMAPIProp::](imapiprop-getprops.md) GetProps für seine Werte erst auffordern, nachdem er von einem **IMAPIProp:: SaveChanges** -Aufruf übergeben wurde. 
  
Die Subject-Eigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicher Anbieter ist nicht verpflichtet, die OLE **IStream** -Schnittstelle darauf zu unterstützen. Ein Client sollte immer versuchen, zuerst über die **IMAPIProp** -Schnittstelle zuzugreifen, und nur dann auf **IStream** zurückgreifen, wenn **MAPI_E_NOT_ENOUGH_MEMORY** wird. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

