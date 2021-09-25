---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Gibt den Accountsendstamp zurück.
ms.openlocfilehash: b86fb4526703802e843f3976655621c4eb676e76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601149"
---
# <a name="prop_acct_send_stamp"></a>PROP_ACCT_SEND_STAMP

Gibt den Stempel "Senden" des Kontos zurück.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x000E  <br/> |
|Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschaftstag:  <br/> |0x000E001F  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY** zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

