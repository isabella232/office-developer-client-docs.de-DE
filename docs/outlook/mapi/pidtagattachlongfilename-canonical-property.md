---
title: Kanonische Pidtagattachlongfilename (-Eigenschaft
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
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339326"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>Kanonische Pidtagattachlongfilename (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den langen Dateinamen und die Erweiterung einer Anlage ohne Pfad. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Kennung:  <br/> |0x3707  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften beziehen sich auf die Werte ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE und ATTACH_BY_REF_ONLY der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft. Plattformen, die lange Dateinamen unterstützen, sollten sowohl die **PR_ATTACH_LONG_FILENAME** -als auch die **PR_ATTACH_FILENAME** -Eigenschaft ([pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) beim Senden festlegen und **PR_ATTACH_LONG_FILENAME** zuerst überprüfen, wenn empfangen. 
  
Die Clientanwendung sollte diese Eigenschaft auf einen vorgeschlagenen langen Dateinamen festlegen, der verwendet werden soll, wenn der Hostcomputer, der eine Nachricht empfängt, lange filenames unterstützt. **PR_ATTACH_LONG_FILENAME** kann als Dateiname zum Speichern der Anlage und zur Angabe der Dateinamenerweiterung verwendet werden, wenn die **PR_ATTACH_EXTENSION** ([pidtagattachextension (](pidtagattachextension-canonical-property.md))-Eigenschaft nicht bereitgestellt wird. 
  
Im Gegensatz zum von **PR_ATTACH_FILENAME**bereitgestellten Dateinamen ist dieser Name nicht auf einen Namen mit acht Zeichen und eine dreistellige Erweiterung beschränkt. Stattdessen kann es bis zu 256 Zeichen lang sein, einschließlich des Datei namens, der Erweiterung und des Trenn Zeitraums. 
  
MAPI funktioniert nur mit Dateinamen im ANSI-Zeichensatz. Client Anwendungen, die Dateinamen in einem OEM-Zeichensatz verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von Nachrichten mit verwalteten Rechten an.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für die Darstellung von Voicemail und Faxnachrichten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mmapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

