---
title: PidTagAttachPathname (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327230"
---
# <a name="pidtagattachpathname-canonical-property"></a>PidTagAttachPathname (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vollqualifizierten Pfad und Dateinamen einer Anlage.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Kennung:  <br/> |0x3708  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Anlagenunterobjekte diese Eigenschaften verfügbar machen. Wenn Sie sie festlegen, wird angegeben, dass die Anlagendaten nicht in der Nachricht enthalten sind, aber auf einem allgemeinen Dateiserver verfügbar sind. Diese Eigenschaften sind in Verbindung mit allen **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Flags erforderlich, die anlage durch Verweis angeben: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** oder **ATTACH_BY_REF_ONLY**. 
  
Jedes Verzeichnis oder jeder Dateiname ist auf einen Namen mit acht Zeichen und eine Erweiterung mit drei Zeichen beschränkt. Der Allgemeine Pfad ist auf 256 Zeichen beschränkt. Legen Sie für eine Plattform, die lange Dateinamen unterstützt, diese Eigenschaften und PR_ATTACH_LONG_PATHNAME **(** [PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) fest. 
  
Clientanwendungen sollten in den meisten Fällen eine universelle Benennungskonvention (Universal Naming Convention, UNC) verwenden, wenn die Datei freigegeben wird, und einen absoluten Pfad verwenden, wenn die Datei lokal ist.
  
MAPI funktioniert nur mit Pfaden und Dateinamen im ANSI-Zeichensatz. Clients, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen sie vor dem Aufrufen von MAPI in ANSI konvertieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

