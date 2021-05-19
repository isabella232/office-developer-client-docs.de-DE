---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Gibt einen Kontobezeichner zurück, der für alle Outlook ist.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409433"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

Gibt einen Kontobezeichner zurück, der für alle Outlook ist.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0003  <br/> |
|Eigenschaftstyp:  <br/> |PT_LONG  <br/> |
|Eigenschaftstag:  <br/> |0x00030003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md) Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**. 
  
Diese Eigenschaft ist anders als [PROP_ACCT_ID,](prop_acct_id.md) da ihr Wert das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde, eindeutig identifiziert, während **PROP_ACCT_ID** nur zwischen allen Konten innerhalb dieses profils, in dem das Konto erstellt wurde, eindeutig ist. Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten angezeigt wird, kann **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren. Die **PROP_ACCT_ID** kann jedoch möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen. 
  
## <a name="see-also"></a>Siehe auch

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

