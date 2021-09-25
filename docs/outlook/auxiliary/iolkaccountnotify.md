---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: 1d9b659cee551140aedd4caf21d929f6df2bfc72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605386"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Stellt einen Rückruf an den Client für Änderungen an einem Konto bereit.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Bereitgestellt von:  <br/> | Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |Benachrichtigt den Client über Änderungen am angegebenen Konto.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Schnittstelle wird an [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) beim Einrichten von Benachrichtigungen übergeben. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

