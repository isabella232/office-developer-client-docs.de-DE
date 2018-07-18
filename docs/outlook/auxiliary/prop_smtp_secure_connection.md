---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Gibt den Typ des verschlüsselten Verbindungstyp für SMTP-Konto verwenden.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791202"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Gibt den Typ des verschlüsselten Verbindungstyp für SMTP-Konto verwenden.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Bezeichner:  <br/> |0x020A  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_DWORD  <br/> |
|Eigenschafts-Tag:  <br/> |0x020A0003  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert kann eine der folgenden Konstanten sein. Ihren Werten finden Sie unter [Konstanten (Konto Management-API)](constants-account-management-api.md) . 
  
|**Konstanten**|**Beschreibung**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Verwenden Sie keine Verschlüsselung.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Verschlüsselung Secure Socket Layer (SSL) verwenden.  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Verschlüsselung und Authentifizierung-Protokoll (Transport Layer Security, TLS) verwenden.  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Automatisch erkennen Sie und die Verschlüsselungsmethode vom Mailserver unterstützt.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

