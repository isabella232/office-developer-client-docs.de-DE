---
title: PidLidRemoteTransport (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793770"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt an, welches Konto das Headerelement zugeordnet wird, in erster Linie auf POP belassen auf Serverfunktionen implementieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidRemoteXP  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Remote  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008F03  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Remote-Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur für Nachrichten mit einer Nachrichtenklasse IPM relevant. Remote. Microsoft Outlook behält eine Zuordnung von verschiedenen Konten, die auf einem bestimmten Speicher in einer Nachricht Ordner verknüpften Informationen (FAI) herunterladen möchten, aber es kann auch diese Informationen in der Registrierung beibehalten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

