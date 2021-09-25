---
title: MAPI-Adresstypen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c6faae3c477c221d2395b28a7104f15621378a89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579632"
---
# <a name="mapi-address-types"></a>MAPI-Adresstypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jeder Messagingbenutzer ist einem Adresstyp zugeordnet, einer Zeichenzeichenfolge, die das Format der Adresse des Benutzers beschreibt, die in der **eigenschaft PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gespeichert ist. Adresstypen entsprechen Adressformaten. Clientanwendungen können also anhand des Adresstyps eines Empfängers bestimmen, wie eine für den Empfänger geeignete Adresse formatiert wird. 
  
Beispielsweise gibt der  `SMTP` Adresstyp die Standard-Internetadresse an: 
  
 `username@companyname.com.`
  
Und der `EX` Adresstyp gibt eine Exchange Server Adresse an. 
  
Alle Adressbucheinträge müssen einen gültigen Adresstyp aufweisen. Clients erfordern, dass ihre Benutzer einen Adresstyp angeben, wenn ein Typ von benutzerdefiniertem Empfänger erstellt wird, der vom Adressbuchanbieter nicht unterstützt wird. Für die von ihnen unterstützten Einträge müssen Adressbuchanbieter gültige Adresstypen angeben. 
  
MAPI definiert nur einen Adresstyp: MAPIPDL, der für persönliche Verteilerliste steht.
  
Um eine Liste der Adresstypen abzurufen, die von allen Transportanbietern in der Sitzung unterstützt werden, rufen Clientanwendungen die **IMAPISession::EnumAdrTypes-Methode** auf. Weitere Informationen finden Sie unter [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

