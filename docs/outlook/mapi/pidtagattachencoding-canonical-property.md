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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345493"
---
# <a name="pidtagattachencoding-canonical-property"></a>PidTagAttachEncoding (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen ASN.1-Objektbezeichner, der die Codierung für eine Anlage angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Kennung:  <br/> |0x3702  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft identifiziert den Algorithmus, der zum Transformieren der Daten in einer Anlage verwendet wird.
  
 **Hinweis** Die **eigenschaften PR_ATTACH_ENCODING** **und PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) sollten nicht verwechselt werden. Sie sind nicht gekoppelt oder verwandt. **PR_ATTACH_TAG** identifiziert die Anwendung, die die Anlage ursprünglich generiert hat. "Object" hat im Begriff Objektbezeichner und in X.400 eine viel allgemeinere Bedeutung als in der objektorientierten Programmierung. 
  
Die Objektbezeichnersyntax und Beispielobjektbezeichner sind in der MAPIOID definiert. H-Headerdatei. Die Werte **für PR_ATTACH_ENCODING** sind nicht auf die werte beschränkt, die in MAPIOID.H definiert sind. Angefügte Macintosh-Dateien können beispielsweise einen Bezeichner wie MacBinary verwenden. 
  
Ausführliche Informationen zu diesen Objektbezeichnern finden Sie in der Dokumentation zu ASN.1, X.208 und X.209. Der Objektbezeichner befindet sich im Anwendungsreferenzelement der FTBP(File Transfer Body Part)-Umgebung. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

