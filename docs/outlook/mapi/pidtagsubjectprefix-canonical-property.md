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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: be2d30f511540b2eb7aa6e55531753811aaa580d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795239"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>PidTagSubjectPrefix (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Betreffpräfix, der in der Regel eine Aktion für eine Nachricht wie angibt "Firmware:" für die Weiterleitung. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Bezeichner:  <br/> |0x003D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden für alle Objekte, die Meldung empfohlen. 
  
Das Betreffpräfix besteht aus einem oder mehreren alphanumerische Zeichen, gefolgt von einem Doppelpunkt und ein Leerzeichen (die Teil des Präfixes sind). Es muss nicht vor dem Doppelpunkt nicht alphanumerischen Zeichen enthalten. Fehlen ein Präfix kann von dieser Eigenschaft nicht festgelegt oder eine leere Zeichenfolge dargestellt werden. 
  
Wenn diese Eigenschaften explizit festgelegt sind, die Zeichenfolge kann beliebig lang sein und beliebige alphanumerischen Zeichen verwenden, aber eine Teilzeichenfolge am Anfang der Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) muss übereinstimmen. Wenn diese Eigenschaften nicht vom Absender festgelegt sind und berechnet werden müssen, werden ihre Inhalte eingegrenzte. Die Regel für das Präfix computing besteht darin, dass **PR_SUBJECT** mit einem, zwei oder drei Buchstaben beginnen müssen (alphabetische nur) gefolgt von einem Doppelpunkt und einem Leerzeichen. Wenn eine solche eine Teilzeichenfolge am Anfang des **PR_SUBJECT**gefunden wird, es dann wird die Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang des **PR_SUBJECT**). Andernfalls, bleiben diese Eigenschaften nicht festgelegt. 
  
Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollte als Teil der Implementierung des [IMAPIProp::SaveChanges](imapiprop-savechanges.md) berechnet werden. Ein Client sollte [IMAPIProp::GetProps](imapiprop-getprops.md) nicht für ihre Werte aufgefordert werden, bis sie gespeichert wurden durch einen Aufruf von **IMAPIProp::SaveChanges** . 
  
Subject-Eigenschaften in der Regel kleine Zeichenfolgen von weniger als 256 Zeichen sind, und eine Nachricht Speicheranbieter ist nicht verpflichtet, die OLE- **IStream** -Schnittstelle auf diese unterstützen. Ein Client sollte immer Zugriff über die Schnittstelle **IMAPIProp** zuerst versuchen, und greifen auf **IStream** nur, wenn **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

