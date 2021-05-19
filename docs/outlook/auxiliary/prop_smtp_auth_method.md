---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434641"
---
# <a name="prop_smtp_auth_method"></a>PROP_SMTP_AUTH_METHOD

Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Kennung:  <br/> |0x0208  <br/> |
|Eigenschaftstyp:  <br/> |PT_DWORD  <br/> |
|Eigenschaftstag:  <br/> |0x02080003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert ist eine Bitmaske der folgenden Konstanten. Ihre Werte finden Sie unter [Konstanten (Kontoverwaltungs-API).](constants-account-management-api.md) 
  
- **SMTP_AUTH_SAME_AS_POP** bedeutet die Verwendung der gleichen Anmeldeinformationen wie mein eingehender E-Mail-Server, wie von PROP_INET_USER [und](prop_inet_user.md) [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** bedeutet die Verwendung der Anmeldeinformationen, wie sie von PROP_SMTP_USER [und](prop_smtp_user.md) [PROP_SMTP_PASSWORD.](prop_smtp_password.md)
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** bedeutet, dass der Benutzer zur Anmeldung beim server für eingehende E-Mails vor dem Senden von E-Mails anfordert. 
    
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

