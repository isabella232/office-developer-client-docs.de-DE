---
title: PidNameAcceptLanguage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e1f03e7834a4a67ce7ea61b2e4eaac6ea02a597
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579320"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>PidNameAcceptLanguage (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen [RFC3282] Accept-Language Headerfeldwert.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |Acceptlanguage  <br/> |
|Eigenschaftensatz:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Eigenschaftenname:  <br/> |Accept-Language  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um den Wert dieser Eigenschaft festzulegen, sollten MIME-Clients (Multipurpose Internet Message Extensions) ein Accept-Language Headerfeld mit dem gewünschten Wert schreiben. MIME-Clients können stattdessen ein X-Accept-Language-Headerfeld schreiben. MIME-Leser sollten den Wert eines der beiden Kopfzeilenfelder in den Wert dieser Eigenschaft kopieren. Wenn beide Kopfzeilenfelder vorhanden sind, sollten MIME-Leser das Accept-Language Kopfzeilenfeld verwenden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

