---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407165"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0001  <br/> |
|Eigenschafts:  <br/> |PT_LONG  <br/> |
|Property-Tag:  <br/> |0x00010003  <br/> |
|Access  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**zurück. 
  
Diese Eigenschaft unterscheidet sich von [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) dadurch, dass ihr Wert nur unter allen Konten innerhalb dieses Profils eindeutig ist, in dem das Konto erstellt wurde, während **Prop\_ACCT_MINI_UID** das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde. Wenn eine Nachricht mit diesen Eigenschaften auf einen zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten Sätzen wechselt, kann **PROP_ACCT_ID** möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen, und **PROP_ACCT_MINI_UID** das ursprüngliche Konto kann eindeutig im ursprünglichen Profil identifiziert werden. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

