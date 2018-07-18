---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Gibt ein Konto-ID, die Outlook-Profilen eindeutig ist.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791190"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Gibt ein Konto-ID, die Outlook-Profilen eindeutig ist.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0 x 0003  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Eigenschafts-Tag:  <br/> |0x00030003  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md). Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
Diese Eigenschaft unterscheidet sich von [PROP_ACCT_ID](prop_acct_id.md) , dessen Wert das Konto innerhalb und außerhalb der Profil, in dem das Konto erstellt wurde, eindeutig identifiziert wird, während **PROP_ACCT_ID** nur für alle Konten in diesem Profil eine eindeutig ist. in dem das Konto erstellt wurde. Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil und andere Menge von Konten wechselt, kann das ursprüngliche Konto im ursprünglichen Profil von **PROP_ACCT_MINI_UID** eindeutig identifizieren. **PROP_ACCT_ID** können jedoch möglicherweise über ein Konto im Profil des zweiten Computer Konflikt steht. 
  
## <a name="see-also"></a>Siehe auch

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

