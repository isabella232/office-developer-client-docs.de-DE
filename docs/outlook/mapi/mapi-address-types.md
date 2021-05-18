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
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405436"
---
# <a name="mapi-address-types"></a>MAPI-Adresstypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jedem Messagingbenutzer ist ein Adresstyp zugeordnet, eine Zeichenzeichenfolge, die das Format der Adresse des Benutzers beschreibt, das in der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist. Adresstypen werden Adressformaten zuordnung. Das heißt, durch Einen Blick auf den Adresstyp eines Empfängers können Clientanwendungen bestimmen, wie eine Adresse formatiert wird, die für den Empfänger geeignet ist. 
  
Der Adresstyp gibt  `SMTP` z. B. die Standard-Internetadresse an: 
  
 `username@companyname.com.`
  
Und der `EX` Adresstyp gibt eine adresse Exchange Server an. 
  
Alle Adressbucheinträge müssen einen gültigen Adresstyp haben. Clients müssen von ihren Benutzern einen Adresstyp angeben, wenn sie einen benutzerdefinierten Empfängertyp erstellen, der vom Adressbuchanbieter nicht unterstützt wird. Für die von ihnen unterstützten Einträge müssen Adressbuchanbieter gültige Adresstypen angeben. 
  
MAPI definiert nur einen Adresstyp: MAPIPDL, der für persönliche Verteilerliste steht.
  
Um eine Liste der Adresstypen zu erhalten, die von allen Transportanbietern in der Sitzung unterstützt werden, rufen Clientanwendungen die **IMAPISession::EnumAdrTypes-Methode** auf. Weitere Informationen finden Sie unter [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

