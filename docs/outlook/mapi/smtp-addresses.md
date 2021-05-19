---
title: SMTP-Adressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419625"
---
# <a name="smtp-addresses"></a>SMTP-Adressen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Format von SMTP-E-Mail-Adressen ist in RFC 822 definiert. MAPI-Komponenten sollten alle Adressen behandeln, die diesem Standard entsprechen. Es gibt jedoch eine bestimmte Form von RFC 822-Adresse, die MAPI-Adressen am besten codiert:
  
 _Anzeigename_ **\<** _E-Mail-Adresse_**\>**
  
Die eckigen Klammern sind als Literale enthalten. Leerstellen werden häufig in Anzeigenamen verwendet. sie müssen nicht angegeben werden. Eine typische Adresse kann wie diese aussehen, die zu einem der Mitautoren von RFC 1521 gehört:
  
Nataniel Borenstein \< nsb@bellcore.com\>
  
Wenn der Anzeigename Zeichen enthält, die in SMTP-Adressen eine besondere Bedeutung haben, z. B. oder @, sollte der gesamte Anzeigename in doppelte \< Anführungszeichen gesetzt werden. Wenn die Gesamtlänge der E-Mail-Adresse plus Anzeigename bei ausgehenden E-Mails 255 Zeichen überschreitet, sollte der Anzeigename gelöscht werden.
  
Die Teile einer SMTP-Adresszuordnung werden den MAPI-Eigenschaften wie folgt gegliedert:
  
|**SMTP-Adresskomponente**|**MAPI-Eigenschaft**|
|:-----|:-----|
| _Anzeigename_ für alle Empfänger  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _Anzeigename für_ Feld "Von"  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Anzeigename für_ das Feld "Sender"  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _E-Mail-Adresse_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implizit, immer "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Wenn für eine Adresse in eingehenden E-Mails kein Anzeigename vorhanden ist, sollte stattdessen die gesamte E-Mail-Adresse verwendet werden. Der Adresstyp ist immer SMTP.
  
Empfängereigenschaften werden aus der Empfängertabelle der #A0 übernommen. Absendereigenschaften werden aus der Nachricht selbst übernommen.
  

