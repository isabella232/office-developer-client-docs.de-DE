---
title: Kanonische Pidtagattachtag (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361082"
---
# <a name="pidtagattachtag-canonical-property"></a>Kanonische Pidtagattachtag (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen ASN. 1-Objektbezeichner, der die Anwendung angibt, die eine Anlage bereitgestellt hat. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_TAG  <br/> |
|Kennung:  <br/> |0x370A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft identifiziert die Anwendung, die die Anlage ursprünglich generiert hat.
  
 **Hinweis** Die Eigenschaften **PR_ATTACH_ENCODING** ([Pidtagattachencoding (](pidtagattachencoding-canonical-property.md)) und **PR_ATTACH_TAG** sollten nicht verwechselt werden. Sie sind nicht gekoppelt oder verknüpft. **PR_ATTACH_ENCODING** identifiziert den Algorithmus, der zum Transformieren der Daten in einer Anlage verwendet wird. "Object" hat eine viel allgemeinere Bedeutung in der Term-Objekt-ID und in der X. 400-Verwendung als bei der objektorientierten Programmierung. 
  
Die Objekt-ID-Syntax und die Sample-Objekt-IDs werden in der MAPIOID definiert. H-Headerdatei. Werte für **PR_ATTACH_TAG** sind nicht auf diejenigen beschränkt, die in MAPIOID definiert sind. H. 
  
Vollständige Informationen zu diesen Objektbezeichnern finden Sie in der Dokumentation zu ASN. 1, X. 208 und X. 209. Der Objektbezeichner befindet sich im Application-Reference-Element der FTBP-Umgebung (File Transfer Body Teil). 
  
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



[Kanonische Pidtagattachmimetag (-Eigenschaft](pidtagattachmimetag-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

