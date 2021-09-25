---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Gibt einen Kontobezeichner zurück, der für Outlook Profile eindeutig ist.
ms.openlocfilehash: bcfede8ad2716bd09ec1abd3420b7e61777f4a0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625630"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

Gibt einen Kontobezeichner zurück, der für Outlook Profile eindeutig ist.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0003  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Eigenschaftstag:  <br/> |0x00030003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md)ab. Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY** zurück. 
  
Diese Eigenschaft unterscheidet sich von [PROP_ACCT_ID](prop_acct_id.md) darin, dass ihr Wert das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde, eindeutig identifiziert, während **PROP_ACCT_ID** nur unter allen Konten innerhalb dieses Profils eindeutig ist, in dem das Konto erstellt wurde. Wenn eine Nachricht mit diesen Eigenschaften auf einen zweiten Computer mit einem anderen Outlook Profil und verschiedenen Kontengruppen übertragen wird, können **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren. **PROP_ACCT_ID** können jedoch möglicherweise einen Konflikt mit einem Konto im Profil des zweiten Computers verursachen. 
  
## <a name="see-also"></a>Siehe auch

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

