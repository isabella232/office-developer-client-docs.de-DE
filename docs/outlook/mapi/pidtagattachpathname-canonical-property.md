---
title: Kanonische PidTagAttachPathname-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b7e0c174f0b31522cffbb4761ab64a50267874be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794113"
---
# <a name="pidtagattachpathname-canonical-property"></a>Kanonische PidTagAttachPathname-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einer Anlage vollqualifizierten Pfad und Dateinamen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Bezeichner:  <br/> |0x3708  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Anlage Unterobjekte diese Eigenschaften verfügbar machen. Das Festlegen dieser gibt an, dass die Anlagedaten nicht mit der Nachrichten enthalten ist, aber auf einem gemeinsamen Dateiserver verfügbar ist. Diese Eigenschaften sind in Verbindung mit einem der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) Flags, die angeben, Anlage per Verweis erforderlich: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY_REF_ NUR**. 
  
Jedes Verzeichnis oder eine Datei ist auf einen Namen für die acht Zeichen und einer Erweiterung aus drei Zeichen beschränkt. Der gesamte Pfad ist auf 256 Zeichen beschränkt. Legen Sie für eine Plattform, die lange Dateinamen unterstützt diese Eigenschaften und die **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
-Clientanwendungen sollten in den meisten Fällen eine universelle Benennungskonvention (UNC) verwenden, wenn die Datei gemeinsam verwendet wird und einen absoluten Pfad verwenden sollte, wenn die Datei lokal ist.
  
MAPI-funktioniert nur mit Pfaden und Dateinamen des ANSI-Zeichensatz. Clients, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI. 
  
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



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

