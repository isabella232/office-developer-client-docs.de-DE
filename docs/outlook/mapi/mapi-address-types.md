---
title: MAPI-Adresstypen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 80e933f5723746dbaeb39271cc813eb0ea56a705
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571185"
---
# <a name="mapi-address-types"></a>MAPI-Adresstypen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Jeder messaging Benutzer ist einen Adresstyp einer Zeichenfolge beschreibt das Format der Adresse des Benutzers, die in der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist zugeordnet. Ordnen Sie Adresstypen Adressformate. D. h., können Sie anhand des Empfängers Adresstyp, Clientanwendungen wie eine Adresse für den Empfänger formatiert bestimmen. 
  
Beispielsweise die `SMTP` Adresstyp gibt die standardmäßige Internet-Adresse: 
  
 `username@companyname.com.`
  
Und, die `EX` Adresstyp gibt eine Exchange Server-Adresse. 
  
Alle Einträge im Adressbuch müssen einen gültige Adresstyp verfügen. Clients müssen die Benutzer an einer Adresse Geben Sie beim Erstellen eines Typs des benutzerdefinierten Empfänger, die von der Adressbuchanbieter nicht unterstützt. Für die Einträge, die sie unterstützen, sind von adressbuchanbietern implementierte erforderlich, um gültige Adresstypen angeben. 
  
MAPI nur einen Adresstyp definiert: MAPIPDL, die für persönliche Verteilerliste steht.
  
Um eine Liste der in der Sitzung von alle Transportanbieter unterstützten Adresstypen erhalten möchten, rufen Sie Clientanwendungen die **IMAPISession::EnumAdrTypes** -Methode. Weitere Informationen finden Sie unter [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

