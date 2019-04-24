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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298012"
---
# <a name="mapi-address-types"></a>MAPI-Adresstypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jeder Messagingbenutzer ist einem Adresstyp zugeordnet, einer Zeichenfolge, die das Format der Adresse des Benutzers beschreibt, die in der **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist. Adresstypen werden Adressformaten zugeordnet. Das heißt, wenn Sie sich den Adresstyp eines Empfängers ansehen, können Clientanwendungen festlegen, wie eine für den Empfänger geeignete Adresse formatiert werden soll. 
  
Der `SMTP` Adresstyp gibt beispielsweise die standardmäßige Internet Adresse an: 
  
 `username@companyname.com.`
  
Und der `EX` Adresstyp gibt eine Exchange-Server Adresse an. 
  
Alle Adressbucheinträge müssen einen gültigen Adresstyp aufweisen. Die Benutzer müssen beim Erstellen eines benutzerdefinierten Empfängertyps, der vom Adressbuchanbieter nicht unterstützt wird, einen Adresstyp angeben. Für die unterstützten Einträge müssen Adressbuchanbieter gültige Adresstypen angeben. 
  
MAPI definiert nur einen Adresstyp: MAPIPDL, die für die persönliche Verteilerliste steht.
  
Um eine Liste der Adresstypen abzurufen, die von allen Transportanbietern in der Sitzung unterstützt werden, rufen Clientanwendungen die **IMAPISession:: EnumAdrTypes** -Methode auf. Weitere Informationen finden Sie unter [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).
  

