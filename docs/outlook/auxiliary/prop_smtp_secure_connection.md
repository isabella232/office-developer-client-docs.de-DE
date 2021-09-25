---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.
ms.openlocfilehash: eb267e71f63bd02dc0268e06f62b288f56e4db11
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592732"
---
# <a name="prop_smtp_secure_connection"></a>PROP_SMTP_SECURE_CONNECTION

Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Kennung:  <br/> |0x020A  <br/> |
|Eigenschaftentyp:  <br/> |PT_DWORD  <br/> |
|Eigenschaftstag:  <br/> |0x020A0003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert kann eine der folgenden Konstanten sein: Siehe [Konstanten (Kontoverwaltungs-API)](constants-account-management-api.md) für deren Werte. 
  
|**Constants**|**Beschreibung**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Verwenden Sie keine Verschlüsselung.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Verwenden Sie ssl-Verschlüsselung (Secure Socket Layer).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Verwenden Sie TLS-Verschlüsselungs- und Authentifizierungsprotokoll (Transport Layer Security).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Automatisches Erkennen und Verwenden der vom E-Mail-Server unterstützten Verschlüsselungsmethode.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

