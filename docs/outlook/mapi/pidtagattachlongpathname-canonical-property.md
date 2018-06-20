---
title: Kanonische PidTagAttachLongPathname-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a2230f2c2b1d4793c425694f76bb79fb7284c479
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794088"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Kanonische PidTagAttachLongPathname-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einer Anlage voll qualifizierte lange Pfad- und Dateiname. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Bezeichner:  <br/> |0x370D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind anwendbar, wenn Sie einen der Werte der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft verwenden, die Anlage per Verweis angeben: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY _REF_ONLY**. Plattformen, die Unterstützung von langen Dateinamen fest **PR_ATTACH_LONG_PATHNAME** oder zugeordnete Eigenschaften und **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) Eigenschaften beim Senden und **PR_ATTACH_LONG_PATHNAME sollten überprüfen **oder Eigenschaften zuerst beim empfangen. 
  
Die Clientanwendung sollte legen diese Eigenschaften einer vorgeschlagenen lange Pfad und Dateinamen für verwendet werden, wenn das Hostsystem Empfangen einer Nachricht lange Dateinamen unterstützt. Festlegen dieser Eigenschaften gibt an, dass die Anlagedaten nicht mit der Nachrichten enthalten ist, aber auf einem gemeinsamen Dateiserver verfügbar ist. 
  
Im Gegensatz zu den Verzeichnissen und Dateinamen von **PR_ATTACH_PATHNAME**bereitgestellt sind diese Verzeichnisse und Dateinamen nicht auf ein Verzeichnis acht Zeichen oder Filename plus Erweiterung aus drei Zeichen beschränkt. Stattdessen kann jede Verzeichnis oder Filename werden bis zu 256 Zeichen lange, einschließlich Name, Erweiterung und Trennzeichen Zeitraum. Jedoch ist der gesamte Pfad auf 256 Zeichen beschränkt. 
  
Clients sollten in den meisten Fällen eine universelle Benennungskonvention (UNC) verwenden, wenn die Datei gemeinsam verwendet wird und einen absoluten Pfad verwenden sollte, wenn die Datei lokal ist.
  
MAPI-funktioniert nur mit Pfaden und Dateinamen des ANSI-Zeichensatz. Clientanwendungen, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.
    
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

