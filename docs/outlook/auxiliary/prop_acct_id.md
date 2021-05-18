---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils, in dem das Konto erstellt wird, eindeutig identifiziert.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407165"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils, in dem das Konto erstellt wird, eindeutig identifiziert.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0001  <br/> |
|Eigenschaftstyp:  <br/> |PT_LONG  <br/> |
|Eigenschaftstag:  <br/> |0x00010003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md) Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
Diese Eigenschaft ist anders als [PROP_ACCT_MINI_UID,](prop_acct_mini_uid.md) da ihr Wert nur für alle Konten innerhalb des Profils eindeutig ist, in dem das Konto erstellt wurde, während **PROP \_ ACCT_MINI_UID** das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde, eindeutig identifiziert. Wenn eine Nachricht mit diesen Eigenschaften auf einen zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten streift, kann **PROP_ACCT_ID** möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen, und **PROP_ACCT_MINI_UID** kann das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

