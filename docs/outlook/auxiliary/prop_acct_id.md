---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner, der eindeutig innerhalb des Profils ein Konto in der das Konto erstellt wird.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791189"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Gibt einen Bezeichner, der eindeutig innerhalb des Profils ein Konto in der das Konto erstellt wird.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Bezeichner:  <br/> |0x0001  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Eigenschafts-Tag:  <br/> |0x00010003  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md). Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
Diese Eigenschaft unterscheidet sich von [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) , dessen Wert nur für alle Konten innerhalb dieses Profil, in dem das Konto erstellt wurde, eindeutig, sind während die **Eigenschaft\_ACCT_MINI_UID** eindeutig identifiziert den Account innerhalb und außerhalb des Profils ein, in dem das Konto erstellt wurde. Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil wechselt und andere Menge von Konten, **PROP_ACCT_ID** möglicherweise kann Konflikte mit einem Konto im Profil des zweiten Computer und **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil können eindeutig zu identifizieren. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

