---
title: Kanonische PidTag7BitDisplayName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4ae7645e45efb461ac53b6718569d909cec76504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794027"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a>Kanonische PidTag7BitDisplayName-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine 7-Bit-ASCII-Darstellung der messaging dem Namen des Benutzers an. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W  <br/> |
|Bezeichner:  <br/> |0x39FF  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften ordnen Sie die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in eine 7-Bit-Zeichensatz. Einige Messagingsysteme wie Internet und bestimmte x. 400-Links sind auf die 128-7-Bit-ASCII-Code Zeichensatz beschränkt. Gateways für die messaging-Systemen können die Leistung verbessern, indem Aufrufen der [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) -Methode zum Abrufen dieser direkt-Eigenschaft, wodurch zusätzliche Verarbeitung für die Konvertierung von Code zu vermeiden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zu Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Ein Client-Kommunikation mit einem NSPI-Server verarbeitet.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet den Reihenfolge und Datenfluss, die zum Übertragen von Daten zwischen Client und Server verwendet wird.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

