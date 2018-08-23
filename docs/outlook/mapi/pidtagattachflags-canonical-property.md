---
title: PidTagAttachFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bf92e62dc572a81b6e0aab4cb1b0fc8afe97800d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573096"
---
# <a name="pidtagattachflags-canonical-property"></a>PidTagAttachFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Bitmaske aus Flags für eine Anlage enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Kennung:  <br/> |0x3714  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird verwendet, für die MHTML-Unterstützung. 
  
Für die Bitmaske **PR_ATTACH_FLAGS** kann eine oder mehrere der folgenden Werte festgelegt werden: 
  
ATT_INVISIBLE_IN_HTML 
  
> Gibt an, dass diese Anlage nicht verfügbar für HTML-Rendering Clientanwendungen ist und sollte in Multipurpose Internet Mail Extensions (MIME) Verarbeitung ignoriert werden. 
    
ATT_INVISIBLE_IN_RTF 
  
> Gibt an, dass diese Anlage ist nicht verfügbar für Clientanwendungen Rendern in Rich Text Format (RTF) und MAPI ignoriert werden soll.
    
Wenn die **PR_ATTACH_FLAGS** -Eigenschaft gleich NULL ist oder nicht vorhanden ist, ist die Anlage von allen Anwendungen verarbeitet werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
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

