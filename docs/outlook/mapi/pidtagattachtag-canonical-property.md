---
title: Kanonische PidTagAttachTag-Eigenschaft
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
ms.openlocfilehash: d8d8d32bddb98e0ac180b0898478c67297980492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794140"
---
# <a name="pidtagattachtag-canonical-property"></a>Kanonische PidTagAttachTag-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen ASN. 1 Objektbezeichner angeben die Anwendung, die eine Anlage bereitstellt. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_TAG  <br/> |
|Bezeichner:  <br/> |0x370A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft identifiziert die Anwendung, die die Anlage ursprünglich erzeugt hat.
  
 **Hinweis** Die **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) und **PR_ATTACH_TAG** Eigenschaften darf nicht verwechselt werden. Sie werden nicht verbunden oder verwandte. **PR_ATTACH_ENCODING** gibt den Algorithmus zum Transformieren der Daten in einer Anlage. "Objekt" hat eine sehr viel allgemeine Bedeutung in den Begriff Objektbezeichner und x. 400-Nutzung, als im objektorientiertes Programmieren. 
  
Die Objekt-ID zu Syntax und Beispiel-Objekt-IDs werden in der MAPIOID definiert. H-Headerdatei. Werte für **PR_ATTACH_TAG** sind nicht auf den in MAPIOID definierten beschränkt. H. 
  
Umfassende Informationen zu diesen Objektbezeichner finden Sie in der Dokumentation auf ASN. 1, X.208 und X.209. Die Objekt-ID wird in der Anwendung Verweis-Element der Datei übertragen Textkörper Teil (FTBP) Umgebung gefunden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagAttachMimeTag-Eigenschaft](pidtagattachmimetag-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

