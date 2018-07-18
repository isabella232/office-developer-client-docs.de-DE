---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode für die SMTP-Konto verwenden.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791206"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Gibt die Authentifizierungsmethode für die SMTP-Konto verwenden.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Bezeichner:  <br/> |0x0208  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_DWORD  <br/> |
|Eigenschafts-Tag:  <br/> |0x02080003  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert ist eine Bitmaske der folgenden Konstanten sein. Ihren Werten finden Sie unter [Konstanten (Konto Management-API)](constants-account-management-api.md) . 
  
- **SMTP_AUTH_SAME_AS_POP** bedeutet als Posteingangsserver, die dieselben Anmeldeinformationen verwenden, wie von [PROP_INET_USER](prop_inet_user.md) und [PROP_INET_PASSWORD](prop_inet_password.md)bereitgestellt.
    
- **SMTP_AUTH_USER_PASS** bedeutet, dass mit den Anmeldeinformationen von [PROP_SMTP_USER](prop_smtp_user.md) und [PROP_SMTP_PASSWORD](prop_smtp_password.md)bereitgestellt werden.
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** bedeutet, dass den Benutzer zum Server für eingehende e-Mail-Nachrichten melden Sie sich vor dem Senden von e-Mail-Nachrichten anfordern. 
    
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

