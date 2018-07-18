---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True, wenn das Konto ein Exchange-Konto ist.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791176"
---
# <a name="propacctisexch"></a>PROP_ACCT_IS_EXCH

True, wenn das Konto ein Exchange-Konto ist.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x0014  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Eigenschafts-Tag:  <br/> |0x00140003  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md). Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

