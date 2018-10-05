---
title: PidTagAttachExtension (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388428"
---
# <a name="pidtagattachextension-canonical-property"></a>PidTagAttachExtension (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Erweiterung, die den Dokumenttyp einer Anlage angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W  <br/> |
|Kennung:  <br/> |0x3703  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden von der Clientanwendung Zeitpunkt der Übermittlung festgelegt. 
  
Der messaging-System verwendeten **PR_ATTACH_EXTENSION** beim Konvertieren von Nachrichtenanlagen (Konvertierung in Route) oder Starten von Anwendungen basierend auf Anlagen in empfangene Nachrichten. Wenn der sendende Client keinen Wert für diese Eigenschaften bereitstellen, ist der Nachrichtenspeicher behandeln die Anlage nicht verpflichtet zum erzeugen. Der empfangende Client sollte zunächst für **PR_ATTACH_EXTENSION**überprüfen, und wenn es nicht angegeben wird, sollte die Dateinamenerweiterung aus der Anlage **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) oder **PR_ATTACH_LONG_FILENAME analysieren **-Eigenschaft ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
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

