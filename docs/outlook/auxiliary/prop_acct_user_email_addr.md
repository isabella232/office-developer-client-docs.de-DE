---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Gibt die E-Mail-Adresse für das Konto an.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436776"
---
# <a name="prop_acct_user_email_addr"></a>PROP_ACCT_USER_EMAIL_ADDR

Gibt die E-Mail-Adresse für das Konto an.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x000C  <br/> |
|Eigenschaftstyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschaftstag:  <br/> |0x000C001F  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

 **PROP_ACCT_USER_EMAIL_ADDR** wird nicht für jedes Konto erwartet. Beispielsweise könnte ein Exchange-Konto PROP_MAPI_IDENTITY_ENTRYID [](prop_mapi_identity_entryid.md) aber nicht PROP_ACCT_USER_EMAIL_ADDR **haben,** während für ein SMTP/POP3-Konto die Situation umgekehrt wird.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

