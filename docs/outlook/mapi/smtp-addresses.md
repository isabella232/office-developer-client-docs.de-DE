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
  
Das Format der SMTP-e-Mail-Adressen ist in RFC 822 definiert. MAPI-Komponenten sollten jede Adresse behandeln, die diesem Standard entspricht. Es gibt jedoch eine bestimmte Form der RFC 822-Adresse, die die MAPI-Adressen am besten codiert:
  
 _Anzeigename_ **\<** _e-Mail-Adresse_**\>**
  
Die eckigen Klammern sind als Literale enthalten. Leerzeichen sind in Anzeige Namen gebräuchlich. Sie müssen nicht zitiert werden. Eine typische Adresse könnte wie diese aussehen, die zu einem der Mitverfasser von RFC 1521 gehört:
  
Nathaniel Borenstein \<NSB@bellcore.com\>
  
Wenn der Anzeigename Zeichen enthält, die eine besondere Bedeutung in SMTP-Adressen wie \< oder @ haben, sollte der gesamte Anzeigename in doppelte Anführungszeichen eingeschlossen werden. Wenn die Gesamtlänge der e-Mail-Adresse und der Anzeigename bei ausgehenden e-Mails 255 Zeichen überschreitet, sollte der Anzeigename gelöscht werden.
  
Die Teile einer SMTP-Adresse werden wie folgt in MAPI-Eigenschaften zugeordnet:
  
|**SMTP-Adresskomponente**|**MAPI-Eigenschaft**|
|:-----|:-----|
| _Anzeigename_ für alle Empfänger  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _Anzeigename_ für vom-Feld  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Anzeigename_ für Absenderfeld  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _e-Mail-Adresse_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implizit, immer "SMTP"  <br/> |**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))  <br/> |
   
Wenn kein Anzeigename für eine Adresse bei eingehenden e-Mails vorhanden ist, sollte stattdessen die gesamte e-Mail-Adresse verwendet werden. Der Adresstyp ist immer SMTP.
  
Empfänger Eigenschaften werden aus der Empfängertabelle der MAPI-Nachricht entnommen. Absender Eigenschaften werden aus der Nachricht selbst entnommen.
  

