---
title: PidTagOriginalSubject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331143"
---
# <a name="pidtagoriginalsubject-canonical-property"></a>PidTagOriginalSubject (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Betreff einer ursprünglichen Nachricht zur Verwendung in einem Bericht über die Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W  <br/> |
|Kennung:  <br/> |0x0049  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind ursprünglich auf denselben Wert wie die **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) festgelegt.
  
Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die **Ole-IStream-Schnittstelle** (Object Linking and Embedding) zu unterstützen. Der Client sollte immer zuerst den Zugriff über die **IMAPIProp-Schnittstelle** versuchen und nur dann auf **IStream** zugreifen, **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.
    
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

