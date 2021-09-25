---
title: SMTP-Adressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 913df302c86742c20849fdb62e83437ad27e6d0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619729"
---
# <a name="smtp-addresses"></a>SMTP-Adressen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Format der SMTP-E-Mail-Adressen ist in RFC 822 definiert. MAPI-Komponenten sollten alle Adressen verarbeiten, die diesem Standard entsprechen. Es gibt jedoch eine bestimmte Form von RFC 822-Adresse, die MAPI-Adressen am besten codiert:
  
 _Anzeigename_ **\<** _email-address_ **\>**
  
Die spitzen Klammern sind als Literale enthalten. Leerstellen werden häufig in Anzeigenamen angezeigt. Sie müssen nicht in Anführungszeichen eingeschlossen werden. Eine typische Adresse könnte wie diese aussehen, die zu einem der Mitautoren von RFC 1521 gehört:
  
Ilsiel Borzem \<nsb@bellcore.com\>
  
Wenn der Anzeigename Zeichen enthält, die in SMTP-Adressen eine besondere Bedeutung haben, z. B. \< @, sollte der gesamte Anzeigename in doppelte Anführungszeichen eingeschlossen werden. Wenn bei ausgehenden E-Mails die Gesamtlänge der E-Mail-Adresse plus Anzeigename 255 Zeichen überschreitet, sollte der Anzeigename gelöscht werden.
  
Die Teile einer SMTP-Adresszuordnung werden den MAPI-Eigenschaften wie folgt zugeordnet:
  
|**SMTP-Adresskomponente**|**MAPI-Eigenschaft**|
|:-----|:-----|
| _Anzeigename_ für alle Empfänger  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _Anzeigename für From-Feld_  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Anzeigename_ für Absenderfeld  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _E-Mail-Adresse_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implizit, immer "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Wenn für eine Adresse bei eingehenden E-Mails kein Anzeigename vorhanden ist, sollte stattdessen die gesamte E-Mail-Adresse verwendet werden. Der Adresstyp ist immer SMTP.
  
Empfängereigenschaften werden aus der Empfängertabelle der MAPI-Nachricht übernommen. Absendereigenschaften werden der Nachricht selbst entnommen.
  

