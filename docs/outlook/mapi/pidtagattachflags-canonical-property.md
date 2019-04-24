---
title: Kanonische Pidtagattachflags (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339333"
---
# <a name="pidtagattachflags-canonical-property"></a>Kanonische Pidtagattachflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags für eine Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Kennung:  <br/> |0x3714  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird für die MHTML-Unterstützung verwendet. 
  
Eine oder mehrere der folgenden Flags können für die **PR_ATTACH_FLAGS** -Bitmaske festgelegt werden: 
  
ATT_INVISIBLE_IN_HTML 
  
> Gibt an, dass diese Anlage für HTML-Rendering-Anwendungen nicht verfügbar ist und in Multipurpose Internet Mail Extensions (MIME)-Verarbeitung ignoriert werden sollte. 
    
ATT_INVISIBLE_IN_RTF 
  
> Gibt an, dass diese Anlage nicht für Anwendungen verfügbar ist, die im Rich-Text-Format (RTF) gerendert werden und von MAPI ignoriert werden sollten.
    
Wenn die **PR_ATTACH_FLAGS** -Eigenschaft NULL oder abwesend ist, ist die Anlage von allen Anwendungen verarbeitet werden. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

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

