---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True, wenn das Konto ein Exchange-Konto ist.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418232"
---
# <a name="propacctisexch"></a>PROP_ACCT_IS_EXCH

True, wenn das Konto ein Exchange-Konto ist.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0014  <br/> |
|Eigenschafts:  <br/> |PT_LONG  <br/> |
|Property-Tag:  <br/> |0x00140003  <br/> |
|Access  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

