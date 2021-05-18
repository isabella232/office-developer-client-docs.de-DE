---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326432"
---
# <a name="prop_mapi_identity_entryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2002  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x20020102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

 **PROP \_ MAPI \_ IDENTITY \_ ENTRYID** wird nicht für jedes Konto erwartet. Ein Exchange-Konto könnte z. B. **PROP \_ MAPI \_ IDENTITY \_ ENTRYID** und nicht [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)festlegen, während für ein SMTP/POP3-Konto die Situation umgekehrt wird. **PROP \_ MAPI_IDENTITY_ENTRYID** gibt eine Eintrags-ID zurück, die dem wert ähnelt, der von _lppEntryID_ in [IMAPISession::QueryIdentity zurückgegeben wird.](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx) 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

