---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.
ms.openlocfilehash: 9d926b5b68fb41962946700f585d6a3629aacd25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601135"
---
# <a name="prop_mapi_identity_entryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x2002  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x20020102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **PROP \_ MAPI \_ IDENTITY \_ ENTRYID** wird nicht für jedes Konto erwartet. Beispielsweise könnte für ein Exchange Konto **PROP \_ MAPI IDENTITY \_ \_ ENTRYID** und nicht [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)festgelegt sein, während für ein SMTP/POP3-Konto die Situation umgekehrt wird. **PROP \_ MAPI_IDENTITY_ENTRYID** gibt eine Eintrags-ID zurück, die dem von  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)zurückgegebenen Wert ähnelt. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

