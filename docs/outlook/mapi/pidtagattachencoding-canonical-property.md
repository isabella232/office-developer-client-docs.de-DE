---
title: PidTagAttachEncoding (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cdeb432e20f2779bbb625566108551748b48a01f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794103"
---
# <a name="pidtagattachencoding-canonical-property"></a>PidTagAttachEncoding (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
ASN. 1 Objektbezeichner, der angibt, die Codierung für eine Anlage enthält. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Bezeichner:  <br/> |0x3702  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt den Algorithmus zum Transformieren der Daten in einer Anlage.
  
 **Hinweis** Die **PR_ATTACH_ENCODING** und **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) Eigenschaften darf nicht verwechselt werden. Sie werden nicht verbunden oder verwandte. **PR_ATTACH_TAG** identifiziert die Anwendung, die die Anlage ursprünglich erzeugt hat. "Objekt" hat eine sehr viel allgemeine Bedeutung in den Begriff Objektbezeichner und x. 400-, als im objektorientiertes Programmieren. 
  
Die Objekt-ID zu Syntax und Beispiel-Objekt-IDs werden in der MAPIOID definiert. H-Headerdatei. Werte für **PR_ATTACH_ENCODING** sind nicht auf den in MAPIOID definierten beschränkt. H. Angefügte Macintosh-Dateien können beispielsweise einen Bezeichner wie MacBinary verwenden. 
  
Umfassende Informationen zu diesen Objektbezeichner finden Sie in der Dokumentation auf ASN. 1, X.208 und X.209. Die Objekt-ID wird im Application-Referenz-Element der Umgebung FTBP (File Transfer Body Part) gefunden. 
  
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



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

