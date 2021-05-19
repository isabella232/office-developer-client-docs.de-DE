---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421284"
---
# <a name="prop_smtp_secure_connection"></a>PROP_SMTP_SECURE_CONNECTION

Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Kennung:  <br/> |0x020A  <br/> |
|Eigenschaftstyp:  <br/> |PT_DWORD  <br/> |
|Eigenschaftstag:  <br/> |0x020A0003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert kann eine der folgenden Konstanten sein. Ihre Werte finden Sie unter [Konstanten (Kontoverwaltungs-API).](constants-account-management-api.md) 
  
|**Constants**|**Beschreibung**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Verwenden Sie keine Verschlüsselung.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Verwenden Sie ssl-Verschlüsselung (Secure Socket Layer).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Verwenden Sie das TLS-Verschlüsselungs- und -Authentifizierungsprotokoll (Transport Layer Security).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Automatische Erkennung und Verwendung der vom E-Mail-Server unterstützten Verschlüsselungsmethode.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

