---
title: Kanonische Pidtagattachlongpathname (-Eigenschaft
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
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339368"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Kanonische Pidtagattachlongpathname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vollqualifizierten Long-Pfad und Dateinamen einer Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Kennung:  <br/> |0x370D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften sind anwendbar, wenn Sie einen der Werte der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft verwenden, die die Anlage anhand des Verweises anzeigen: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY _REF_ONLY**. Plattformen, die lange Dateinamen unterstützen, sollten sowohl **PR_ATTACH_LONG_PATHNAME** -als auch zugehörige Eigenschaften und **PR_ATTACH_PATHNAME** ([pidtagattachpathname (](pidtagattachpathname-canonical-property.md))-Eigenschaften beim Senden festlegen und PR_ATTACH_LONG_PATHNAME überprüfen. ** **oder zugeordnete Eigenschaften beim Empfang. 
  
Die Clientanwendung sollte diese Eigenschaften auf einen vorgeschlagenen Long-Pfad und Dateinamen festlegen, die verwendet werden sollen, wenn der Hostcomputer, der eine Nachricht empfängt, lange filenames unterstützt. Durch Festlegen dieser Eigenschaften wird angegeben, dass die Anlagendaten nicht in der Nachricht enthalten sind, aber auf einem gemeinsamen Dateiserver verfügbar sind. 
  
Im Gegensatz zu den von **PR_ATTACH_PATHNAME**bereitgestellten Verzeichnissen und Dateinamen sind diese Verzeichnisse und filenames nicht auf ein Verzeichnis oder einen filename mit acht Zeichen und eine Erweiterung mit drei Zeichen beschränkt. Stattdessen kann jedes Verzeichnis oder jeder Dateiname bis zu 256 Zeichen lang sein, einschließlich des Namens, der Erweiterung und des Trenn Zeitraums. Der Gesamt Pfad ist jedoch auf 256 Zeichen beschränkt. 
  
Clients sollten in den meisten Fällen eine Universal Naming Convention (UNC) verwenden, wenn die Datei freigegeben ist, und einen absoluten Pfad verwenden, wenn die Datei lokal ist.
  
MAPI kann nur mit Pfaden und Dateinamen im ANSI-Zeichensatz verwendet werden. Client Anwendungen, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren. 
  
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

