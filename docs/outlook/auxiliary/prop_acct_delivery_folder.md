---
title: PROP_ACCT_DELIVERY_FOLDER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a409c49b-b390-021e-2ec1-7a5932a0c8de
description: Stellt die Eintrags-ID des Standardzustellungsordners für das Konto dar.
ms.openlocfilehash: 1bac4890791edfe661599d383e2cb048bf4c42fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427150"
---
# <a name="prop_acct_delivery_folder"></a>PROP_ACCT_DELIVERY_FOLDER

Stellt die Eintrags-ID des Standardzustellungsordners für das Konto dar.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0019  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x00190102  <br/> |
|Zugriff:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) bzw. [IOlkAccount::SetProp](iolkaccount-setprop.md)erhalten oder festlegen.
  
Der Standardzustellungsordner ist **Posteingang**.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)

