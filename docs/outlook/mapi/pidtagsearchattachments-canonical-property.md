---
title: Kanonische PidTagSearchAttachments-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 008dd69f5e31b601b678a4346880e6b3c89a0f39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795107"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Kanonische PidTagSearchAttachments-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Unicodezeichenfolge, die im Anlageninhalt für den Speicher abgefragt wird.
  
## 

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Bezeichner:  <br/> |0x0EA5  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Suchen  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

> [!NOTE]
> Diese MAPI-Einschränkung Tag verwendet bei der Suche für Anlageninhalt, möglicherweise nicht in der Headerdatei zum Herunterladen definiert werden, die Sie besitzen. Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.
    
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

