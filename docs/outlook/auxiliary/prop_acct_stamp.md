---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Gibt den Kontostempel zurück.
ms.openlocfilehash: 1b3cd56b3f7c395391a3b91e8d16f5403ba39e95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551975"
---
# <a name="prop_acct_stamp"></a>PROP_ACCT_STAMP

Gibt den Kontostempel zurück.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x000D  <br/> |
|Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschaftstag:  <br/> |0x000D001F  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY** zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

