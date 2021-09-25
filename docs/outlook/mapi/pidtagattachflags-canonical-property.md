---
title: PidTagAttachFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5e5a8820161cb675f07b792e0ddafeabdfb07fb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563861"
---
# <a name="pidtagattachflags-canonical-property"></a>PidTagAttachFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags für eine Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Kennung:  <br/> |0x3714  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird für die MHTML-Unterstützung verwendet. 
  
Mindestens eines der folgenden Flags kann für die **PR_ATTACH_FLAGS** Bitmaske festgelegt werden: 
  
ATT_INVISIBLE_IN_HTML 
  
> Gibt an, dass diese Anlage für HTML-Renderinganwendungen nicht verfügbar ist und bei der MIME-Verarbeitung (Multipurpose Internet Mail Extensions) ignoriert werden sollte. 
    
ATT_INVISIBLE_IN_RTF 
  
> Gibt an, dass diese Anlage für Anwendungen, die im RTF-Format (Rich Text Format) gerendert werden, nicht verfügbar ist und von MAPI ignoriert werden sollte.
    
Wenn die **PR_ATTACH_FLAGS-Eigenschaft** null oder nicht vorhanden ist, wird die Anlage von allen Anwendungen verarbeitet. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

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

