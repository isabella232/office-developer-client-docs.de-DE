---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.
ms.openlocfilehash: b98b736f98bb1f66a3c8e4a3bf852f2bc9c037f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601142"
---
# <a name="prop_smtp_auth_method"></a>PROP_SMTP_AUTH_METHOD

Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Kennung:  <br/> |0x0208  <br/> |
|Eigenschaftentyp:  <br/> |PT_DWORD  <br/> |
|Eigenschaftstag:  <br/> |0x02080003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert ist eine Bitmaske der folgenden Konstanten. Siehe [Konstanten (Kontoverwaltungs-API)](constants-account-management-api.md) für deren Werte. 
  
- **SMTP_AUTH_SAME_AS_POP** bedeutet, dieselben Anmeldeinformationen wie mein eingehender E-Mail-Server zu verwenden, wie von [PROP_INET_USER](prop_inet_user.md) und [PROP_INET_PASSWORD](prop_inet_password.md)bereitgestellt.
    
- **SMTP_AUTH_USER_PASS** bedeutet die Verwendung der Anmeldeinformationen, die von [PROP_SMTP_USER](prop_smtp_user.md) und [PROP_SMTP_PASSWORD](prop_smtp_password.md)bereitgestellt werden.
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** bedeutet, dass der Benutzer aufgefordert wird, sich vor dem Senden von E-Mails beim Server für eingehende E-Mails anzumelden. 
    
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

