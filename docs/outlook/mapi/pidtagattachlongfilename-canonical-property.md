---
title: PidTagAttachLongFilename (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00d1ce393958389e757d1729c0c8c4cdc96aff81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560935"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>PidTagAttachLongFilename (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den langen Dateinamen und die Erweiterung einer Anlage mit Ausnahme des Pfads. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Kennung:  <br/> |0x3707  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften beziehen sich auf die Werte ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE und ATTACH_BY_REF_ONLY der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft. Plattformen, die lange Dateinamen unterstützen, sollten die Eigenschaften **PR_ATTACH_LONG_FILENAME** und **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) beim Senden festlegen und beim Empfang **zuerst PR_ATTACH_LONG_FILENAME** überprüfen. 
  
Die Clientanwendung sollte diese Eigenschaft auf einen vorgeschlagenen langen Dateinamen festlegen, der verwendet werden soll, wenn der Hostcomputer, der eine Nachricht empfängt, lange Dateinamen unterstützt. **PR_ATTACH_LONG_FILENAME** kann als Dateiname zum Speichern der Anlage und zum Angeben der Dateinamenerweiterung verwendet werden, wenn die **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) -Eigenschaft nicht angegeben ist. 
  
Im Gegensatz zum von **PR_ATTACH_FILENAME** bereitgestellten Dateinamen ist dieser Name nicht auf einen achtstelligen Dateinamen und eine dreistellige Erweiterung beschränkt. Stattdessen können bis zu 256 Zeichen lang sein, einschließlich Dateiname, Erweiterung und Trennzeichen. 
  
MAPI funktioniert nur mit Dateinamen im ANSI-Zeichensatz. Clientanwendungen, die Dateinamen in einem OEM-Zeichensatz verwenden, müssen sie vor dem Aufrufen der MAPI in ANSI konvertieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von nachrichten mit verwalteten Rechten an.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für die Darstellung von Voicemail- und Faxnachrichten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mmapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

