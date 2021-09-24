---
title: PidTagSearchRecipientEmailCc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56df6fc294bc75b178a9c03a4aa9df240525863e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550449"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a>PidTagSearchRecipientEmailCc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die in der Liste der E-Mail-Adressen  oder Anzeigenamen von Empfängern abgefragt wird, die in der CC-Nachrichtenzeile des Speichers adressiert sind. 
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_RECIP_EMAIL_CC_W  <br/> |
|Kennung:  <br/> |0x0EA7  <br/> |
|Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Suche  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

> [!NOTE]
> Dieses MAPI-Einschränkungstag, das beim Suchen nach E-Mail-Adressen oder Anzeigenamen verwendet wird, an die die Nachricht als Kopie gesendet wird, ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. Sie können es ihrem Code hinzufügen, indem Sie den folgenden Wert verwenden: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`
  
### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

