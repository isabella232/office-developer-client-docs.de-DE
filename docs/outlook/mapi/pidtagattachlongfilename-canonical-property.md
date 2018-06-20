---
title: Kanonische PidTagAttachLongFilename-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0debee5d480c4ea0c0a8fb4b54d9fa5d92a45987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794098"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>Kanonische PidTagAttachLongFilename-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einer Anlage langer Dateiname und Erweiterung, ohne Pfad. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Bezeichner:  <br/> |0x3707  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften beziehen sich auf die Werte ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE und ATTACH_BY_REF_ONLY der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft. Plattformen, die lange Dateinamen unterstützen sollte Festlegen der **PR_ATTACH_LONG_FILENAME** und die Eigenschaften **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) beim Senden, und überprüfen **PR_ATTACH_LONG_FILENAME** zuerst bei empfangen. 
  
Die Clientanwendung sollte diese Eigenschaft auf einen vorgeschlagenen langen Dateinamen verwendet werden, wenn der Hostcomputer Empfangen einer Nachricht lange Dateinamen unterstützt festlegen. **PR_ATTACH_LONG_FILENAME** kann verwendet werden, als einen Dateinamen für die Anlage speichern und die Erweiterung Filename angeben, wenn die Eigenschaft **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) nicht verfügbar ist. 
  
Im Gegensatz zu den Dateinamen von **PR_ATTACH_FILENAME**bereitgestellt wird ist dieser Name nicht auf ein Dateiname acht Zeichen und einer Erweiterung aus drei Zeichen beschränkt. In diesem Fall kann es bis zu 256 Zeichen lange, einschließlich des Punkts Dateiname, Erweiterung und Trennzeichen sein. 
  
MAPI funktioniert nur mit Dateinamen im ANSI-Zeichensatz. Clientanwendungen, die Dateinamen in einem OEM-Zeichensatz verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.
    
[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für das Darstellen von Voicemail- und Sprachnachrichten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mmapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

