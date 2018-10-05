---
title: PidTagSearchRecipientEmailBcc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387748"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>PidTagSearchRecipientEmailBcc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicodezeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen der Empfänger in der **BCC** -Zeile von nicht gesendeten Nachrichten im Store abgefragt wird. 
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Kennung:  <br/> |0x0EA8  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Access:  <br/> |Suche  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur relevant, die Nachrichten auf den Speicher, die nicht gesendet wurden, da Nachrichten, die gesendet oder empfangen wurde keine BCC-Informationen enthalten.
  
> [!NOTE]
> Diese MAPI-Einschränkung Tag verwendet, wenn die Suche nach e-Mail-Adressen oder Anzeigenamen, die die Nachricht als eine Blindkopie gesendet wird, möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen. Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
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

