---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True, Wenn das Konto ein Exchange Konto ist.
ms.openlocfilehash: 67562acbb7ee5c29948d9e2dd7bfdbf9a7623135
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631167"
---
# <a name="prop_acct_is_exch"></a>PROP_ACCT_IS_EXCH

True, Wenn das Konto ein Exchange Konto ist.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0014  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Eigenschaftstag:  <br/> |0x00140003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY** zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

