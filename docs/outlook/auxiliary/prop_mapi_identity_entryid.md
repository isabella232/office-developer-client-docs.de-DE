---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Ruft ab oder legt die Address Book Eintrags-ID für das Konto.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400348"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Ruft ab oder legt die Address Book Eintrags-ID für das Konto.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0 x 2002  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschafts-Tag:  <br/> |0x20020102  <br/> |
|Access:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Hinweise

 **Eigenschaft\_MAPI\_Identität\_ENTRYID** voraussichtlich nicht auf jedem Konto vorhanden sein. Beispielsweise könnte ein Exchange-Konto haben **Eigenschaft\_MAPI\_Identität\_ENTRYID** festgelegt und nicht [Eigenschaft\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), während für ein SMTP/POP3-Konto die Situation umgekehrt wurde. **Eigenschaft\_MAPI_IDENTITY_ENTRYID** gibt eine Eintrags-ID, die auf den Wert von _LppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)zurückgegebene ähnlich ist. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

