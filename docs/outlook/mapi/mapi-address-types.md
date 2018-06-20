---
title: MAPI-Adresstypen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792935"
---
# <a name="mapi-address-types"></a>MAPI-Adresstypen

  
  
**Betrifft**: Outlook 
  
Jeder messaging Benutzer ist einen Adresstyp einer Zeichenfolge beschreibt das Format der Adresse des Benutzers, die in der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist zugeordnet. Ordnen Sie Adresstypen Adressformate. D. h., können Sie anhand des Empfängers Adresstyp, Clientanwendungen wie eine Adresse für den Empfänger formatiert bestimmen. 
  
Beispielsweise die `SMTP` Adresstyp gibt die standardmäßige Internet-Adresse: 
  
 `username@companyname.com.`
  
Und, die `EX` Adresstyp gibt eine Exchange Server-Adresse. 
  
Alle Einträge im Adressbuch müssen einen gültige Adresstyp verfügen. Clients müssen die Benutzer an einer Adresse Geben Sie beim Erstellen eines Typs des benutzerdefinierten Empfänger, die von der Adressbuchanbieter nicht unterstützt. Für die Einträge, die sie unterstützen, sind von adressbuchanbietern implementierte erforderlich, um gültige Adresstypen angeben. 
  
MAPI nur einen Adresstyp definiert: MAPIPDL, die für persönliche Verteilerliste steht.
  
Um eine Liste der in der Sitzung von alle Transportanbieter unterstützten Adresstypen erhalten möchten, rufen Sie Clientanwendungen die **IMAPISession::EnumAdrTypes** -Methode. Weitere Informationen finden Sie unter [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

