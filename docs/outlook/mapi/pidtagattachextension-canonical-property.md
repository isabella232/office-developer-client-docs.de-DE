---
title: Kanonische Pidtagattachextension (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319761"
---
# <a name="pidtagattachextension-canonical-property"></a>Kanonische Pidtagattachextension (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Dateinamenerweiterung, die den Dokumenttyp einer Anlage angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W  <br/> |
|Kennung:  <br/> |0x3703  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden von der Clientanwendung zum Zeitpunkt der Übermittlung festgelegt. 
  
Das Messagingsystem verwendet **PR_ATTACH_EXTENSION** beim Konvertieren von Nachrichtenanlagen (in-Route-Konvertierung) oder beim Starten von Anwendungen basierend auf Anlagen in empfangenen Nachrichten. Wenn der sendende Client keinen Wert für diese Eigenschaften bereitstellt, ist der Nachrichtenspeicher, der die Anlage verarbeitet, nicht dazu verpflichtet, Sie zu generieren. Der empfangende Client sollte zunächst nach **PR_ATTACH_EXTENSION**suchen, und falls nicht angegeben, sollte die Dateinamenerweiterung aus der **PR_ATTACH_FILENAME** ([pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) oder PR_ATTACH_LONG_FILENAME der Anlage analysiert werden. ** **([Pidtagattachlongfilename (](pidtagattachlongfilename-canonical-property.md))-Eigenschaft. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

