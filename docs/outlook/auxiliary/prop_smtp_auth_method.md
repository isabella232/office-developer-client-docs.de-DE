---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode für das SMTP-Konto an.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326502"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Gibt die Authentifizierungsmethode für das SMTP-Konto an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Kennung:  <br/> |0x0208  <br/> |
|Eigenschafts:  <br/> |PT_DWORD  <br/> |
|Property-Tag:  <br/> |0x02080003  <br/> |
|Access  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert ist eine Bitmaske der folgenden Konstanten. Ihre Werte finden Sie unter [Constants (Account Management API)](constants-account-management-api.md) . 
  
- **SMTP_AUTH_SAME_AS_POP** ist die Verwendung derselben Anmeldeinformationen wie mein Posteingangsserver, wie von [PROP_INET_USER](prop_inet_user.md) und [PROP_INET_PASSWORD](prop_inet_password.md)bereitgestellt.
    
- **SMTP_AUTH_USER_PASS** ist die Verwendung der Anmeldeinformationen, die von [PROP_SMTP_USER](prop_smtp_user.md) und [PROP_SMTP_PASSWORD](prop_smtp_password.md)bereitgestellt werden.
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** : fordert den Benutzer auf, sich vor dem Senden von e-Mails beim Posteingangsserver anzumelden. 
    
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

