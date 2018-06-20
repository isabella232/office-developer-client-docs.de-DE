---
title: Kanonische PidTagRtfSyncBodyCrc-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa144ca93e8fad9b9b5a5da1ee457e5cc3bbd841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795021"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a>Kanonische PidTagRtfSyncBodyCrc-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält das Kontrollkästchen zyklischer Redundanz (CRC) für den Nachrichtentext berechnet.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RTF_SYNC_BODY_CRC  <br/> |
|Bezeichner:  <br/> |0 x 1006  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Funktion [RTFSync](rtfsync.md) berechnet das CRC mithilfe von nur die Zeichen, die sie für die Nachricht erzielt werden hält. Beispielsweise sind einige Leerzeichen und Sonderzeichen ignoriert CRC ausgelassen. 
  
Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft. Diese Eigenschaften werden von der Funktion **RTFSync** verwendet und nicht direkt von Clientanwendungen verwendet werden sollen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.
    
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

