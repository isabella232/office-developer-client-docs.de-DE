---
title: PidTagAttachEncoding (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9716af43b65b8bbc9b1d2c3b8b0b3d549b635afd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583583"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft identifiziert den Algorithmus, der zum Transformieren der Daten in einer Anlage verwendet wird.
  
 **Hinweis** Die **Eigenschaften PR_ATTACH_ENCODING** und **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) sollten nicht verwechselt werden. Sie sind nicht gekoppelt oder miteinander verbunden. **PR_ATTACH_TAG** identifiziert die Anwendung, die die Anlage ursprünglich generiert hat. "Objekt" hat im Ausdruck "Objektbezeichner" und in X.400 eine viel allgemeinere Bedeutung als bei der objektorientierten Programmierung. 
  
Die Objektbezeichnersyntax und Die Beispielobjektbezeichner sind im MAPIOID definiert. H-Headerdatei. Werte für **PR_ATTACH_ENCODING** sind nicht auf die in MAPIOID.H definierten Werte beschränkt. Beispielsweise können angefügte Macintosh-Dateien einen Bezeichner wie MacBinary verwenden. 
  
Vollständige Informationen zu diesen Objektbezeichnern finden Sie in der Dokumentation zu ASN.1, X.208 und X.209. Der Objektbezeichner befindet sich im Anwendungsreferenzelement der FTBP-Umgebung (File Transfer Body Part). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

