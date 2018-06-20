---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791111"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Stellt einen Rückruf an dem Client für Änderungen an einem Konto an.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Bereitgestellt von:  <br/> | Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Benachrichtigen](iolkaccountnotify-notify.md) <br/> |Benachrichtigt den Client von Änderungen an das angegebene Konto.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Schnittstelle wird an [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) übergeben, beim Einrichten von Benachrichtigungen. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

