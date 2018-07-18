---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Gibt die Accountsendstamp zurück.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791180"
---
# <a name="propacctsendstamp"></a>PROP_ACCT_SEND_STAMP

Gibt den Konto-Stempel "Senden" zurück.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x000E  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschafts-Tag:  <br/> |0x000E001F  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md). Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

