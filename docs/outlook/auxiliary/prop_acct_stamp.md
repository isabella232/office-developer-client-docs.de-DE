---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Gibt den Stempel Konto zurück.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791199"
---
# <a name="propacctstamp"></a>PROP_ACCT_STAMP

Gibt den Stempel Konto zurück.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x000d  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_UNICODE  <br/> |
|Eigenschafts-Tag:  <br/> |0x000D001F  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md). Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

