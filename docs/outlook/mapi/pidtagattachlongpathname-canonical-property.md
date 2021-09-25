---
title: PidTagAttachLongPathname (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7183b878646a4f7171de71b042305ede8d90dab6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609943"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>PidTagAttachLongPathname (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den vollqualifizierten langen Pfad und Dateinamen einer Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Kennung:  <br/> |0x370D  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften sind anwendbar, wenn Sie einen der Werte der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft verwenden, die anlagenweise angeben: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** oder **ATTACH_BY_REF_ONLY**. Plattformen, die lange Dateinamen unterstützen, sollten beim Senden sowohl **PR_ATTACH_LONG_PATHNAME-** als auch die zugehörigen Eigenschaften und **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))-Eigenschaften festlegen und beim Empfang zuerst **PR_ATTACH_LONG_PATHNAME** oder zugeordnete Eigenschaften überprüfen. 
  
Die Clientanwendung sollte diese Eigenschaften auf einen vorgeschlagenen langen Pfad und Dateinamen festlegen, der verwendet werden soll, wenn der Hostcomputer, der eine Nachricht empfängt, lange Dateinamen unterstützt. Das Festlegen dieser Eigenschaften weist darauf hin, dass die Anlagendaten nicht in der Nachricht enthalten sind, aber auf einem gemeinsamen Dateiserver verfügbar sind. 
  
Im Gegensatz zu den von **PR_ATTACH_PATHNAME** bereitgestellten Verzeichnissen und Dateinamen sind diese Verzeichnisse und Dateinamen nicht auf ein 8-Zeichen-Verzeichnis oder einen Dateinamen sowie eine dreistellige Erweiterung beschränkt. Stattdessen kann jedes Verzeichnis oder jeder Dateiname bis zu 256 Zeichen lang sein, einschließlich Name, Erweiterung und Trennzeichen. Der Gesamtpfad ist jedoch auf 256 Zeichen beschränkt. 
  
Clients sollten in den meisten Fällen eine universelle Benennungskonvention (UNIVERSAL Naming Convention, UNC) verwenden, wenn die Datei freigegeben wird, und einen absoluten Pfad verwenden, wenn die Datei lokal ist.
  
MAPI funktioniert nur mit Pfaden und Dateinamen im ANSI-Zeichensatz. Clientanwendungen, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen sie vor dem Aufrufen der MAPI in ANSI konvertieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften von nachrichten mit verwalteten Rechten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

