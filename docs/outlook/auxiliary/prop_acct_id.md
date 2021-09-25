---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.
ms.openlocfilehash: e1a4d5cd6594dc4b85b356d76b1e09c96d863364
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605330"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0001  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Eigenschaftstag:  <br/> |0x00010003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY** zurück. 
  
Diese Eigenschaft unterscheidet sich von [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) darin, dass ihr Wert nur für alle Konten innerhalb dieses Profils eindeutig ist, in dem das Konto erstellt wurde, während **PROP \_ ACCT_MINI_UID** das Konto innerhalb und außerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wurde. Wenn eine Nachricht mit diesen Eigenschaften auf einen zweiten Computer mit einem anderen Outlook-Profil und verschiedenen Kontengruppen übertragen wird, können **PROP_ACCT_ID** möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen, und **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren können. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

