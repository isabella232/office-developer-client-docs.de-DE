---
title: PidTagDeleteAfterSubmit (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359913"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a>PidTagDeleteAfterSubmit (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn eine Clientanwendung möchte, dass MAPI die zugeordnete Nachricht nach der Übermittlung löscht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELETE_AFTER_SUBMIT  <br/> |
|Kennung:  <br/> |0x0E01  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Clientanwendung verwendet diese Eigenschaft mit der **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) -Eigenschaft, um zu steuern, was mit einer Nachricht nach dem Senden geschieht. Entweder die eine oder die andere sollte festgelegt werden, aber nicht beides. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

