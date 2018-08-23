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
ms.openlocfilehash: 655d48d1ea937659f85e0ef7379425759ea7e256
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591359"
---
# <a name="smtp-addresses"></a>SMTP-Adressen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Das Format der SMTP-e-Mail-Adressen ist in RFC 822 definiert. MAPI-Komponenten sollte eine beliebige Adresse behandeln, die mit diesem Standard entspricht. Es ist jedoch eine bestimmte Form des RFC 822-Adresse, die am besten MAPI-Adressen codiert:
  
 _Anzeigename_ **\<** _e-Mail-Adresse_**\>**
  
Die spitzen Klammern sind als Literale enthalten. Leerzeichen sind häufig in Anzeigenamen. Sie müssen nicht in Anführungszeichen eingeschlossen werden. Eine typische Adresse sieht aus wie dieser, der eines der Coauthors der RFC 1521 gehört:
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
Wenn der angezeigte Name Zeichen enthält, die in der SMTP-Adressen, z. B. besondere Bedeutung haben \< oder @, sollte der gesamte Anzeigename in doppelte Anführungszeichen eingeschlossen werden. Ausgehende Nachrichten Wenn die Gesamtlänge des plus die e-Mail-Adresse anzuzeigen Name länger als 255 Zeichen klicken Sie auf der Anzeigenamen gelöscht werden soll.
  
Die Teile der SMTP-Adresse wie folgt in MAPI-Eigenschaften zugeordnet:
  
|**SMTP-Adresse-Komponente**|**MAPI-Eigenschaft**|
|:-----|:-----|
| _Anzeigename_ für alle Empfänger  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _Anzeigename_ für Feld  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Anzeigename_ für Feld Absender  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _e-Mail-Adresse_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implizite, immer "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Wenn kein Anzeigename für eine eingehende e-Mail-Adresse vorhanden ist, sollte die gesamte e-Mail-Adresse stattdessen verwendet werden. Der Adresstyp ist immer SMTP.
  
Empfängereigenschaften getroffen werden aus der MAPI-Nachricht Empfänger Tabelle; Absender Eigenschaften werden aus der Nachricht selbst übernommen.
  

