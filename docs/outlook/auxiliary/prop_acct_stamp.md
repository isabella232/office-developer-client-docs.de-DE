---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Gibt den Kontostempel zurück.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408250"
---
# <a name="prop_acct_stamp"></a>PROP_ACCT_STAMP

Gibt den Kontostempel zurück.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x000D  <br/> |
|Eigenschaftstyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschaftstag:  <br/> |0x000D001F  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md) Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

