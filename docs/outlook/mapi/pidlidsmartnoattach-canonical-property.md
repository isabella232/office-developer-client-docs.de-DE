---
title: Kanonische PidLidSmartNoAttach-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 43e10652a7dccdf0da6592df0f9fc2daf5ea9bee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793789"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>Kanonische PidLidSmartNoAttach-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Stellt dar, ob die Anlagen auf eine Nachricht gelten als ausgeblendet.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidSmartNoAttach  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008514  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Laufzeit-Konfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist TRUE, wenn die Anlagen der Nachricht gelten als ausgeblendet.
  
Es gibt an, ob das Message-Objekt keine sichtbaren Anlagen Endbenutzer hat. Diese Eigenschaft kann nicht festgelegt werden; ist dies der Fall ist, wird davon ausgegangen, dass ein Standardwert FALSE.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

