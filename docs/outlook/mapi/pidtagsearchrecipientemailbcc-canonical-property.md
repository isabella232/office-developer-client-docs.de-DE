---
title: PidTagSearchRecipientEmailBcc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 364ccc1428585a005135c13180231285df3ffcaa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563301"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>PidTagSearchRecipientEmailBcc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die in der Liste der E-Mail-Adressen oder Anzeigenamen von Empfängern abgefragt wird, die in der **BCC-Zeile** nicht gesendeter Nachrichten im Speicher adressiert sind. 
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Kennung:  <br/> |0x0EA8  <br/> |
|Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Zugriff:  <br/> |Suche  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist nur für Nachrichten im Speicher relevant, die nicht gesendet wurden, da Nachrichten, die gesendet oder empfangen wurden, keine BCC-Informationen enthalten.
  
> [!NOTE]
> Dieses MAPI-Einschränkungstag, das bei der Suche nach E-Mail-Adressen oder Anzeigenamen verwendet wird, an die die Nachricht als blinde Kopie gesendet wird, ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. Sie können es ihrem Code hinzufügen, indem Sie den folgenden Wert verwenden: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
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

