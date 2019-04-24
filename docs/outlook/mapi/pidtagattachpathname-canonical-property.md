---
title: Kanonische Pidtagattachpathname (-Eigenschaft
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
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327230"
---
# <a name="pidtagattachpathname-canonical-property"></a>Kanonische Pidtagattachpathname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vollqualifizierten Pfad und Dateinamen einer Anlage.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Kennung:  <br/> |0x3708  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Attachment-unter Objekte diese Eigenschaften verfügbar machen. Diese Einstellung gibt an, dass die Anlagendaten nicht in der Nachricht enthalten sind, aber auf einem gemeinsamen Dateiserver verfügbar sind. Diese Eigenschaften sind in Verbindung mit einem der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Flags erforderlich, die die Anlage anhand des Verweises anzeigen: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY_REF_ NUR**. 
  
Jedes Verzeichnis oder jeder Dateiname ist auf einen achtstelligen Namen und eine dreistellige Durchwahlnummer beschränkt. Der Gesamt Pfad ist auf 256 Zeichen beschränkt. Legen Sie für eine Plattform, die lange Dateinamen unterstützt, sowohl diese Eigenschaften als auch **PR_ATTACH_LONG_PATHNAME** ([pidtagattachlongpathname (](pidtagattachlongpathname-canonical-property.md)) fest. 
  
Client Anwendungen sollten in den meisten Fällen eine UNC (Universal Naming Convention) verwenden, wenn die Datei freigegeben ist und einen absoluten Pfad verwenden sollte, wenn die Datei lokal ist.
  
MAPI kann nur mit Pfaden und Dateinamen im ANSI-Zeichensatz verwendet werden. Clients, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von Nachrichten mit verwalteten Rechten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

