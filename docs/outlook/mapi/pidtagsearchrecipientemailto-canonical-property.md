---
title: Kanonische Pidtagsearchrecipientemailto (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358919"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>Kanonische Pidtagsearchrecipientemailto (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen von Empfängern abgefragt wird, die in der **an** -Nachrichten Reihe im Speicher adressiert sind. 
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|Kennung:  <br/> |0x0EA6  <br/> |
|Eigenschafts:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Suche  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

> [!NOTE]
> Dieses MAPI-Einschränkungs, das verwendet wird, wenn Sie nach e-Mail-Adressen oder Anzeigenamen suchen, an die die Nachricht gesendet wird, wird möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. Sie können Sie dem Code hinzufügen, indem Sie den folgenden Wert verwenden: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordner Listen Konfiguration an.
    
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

