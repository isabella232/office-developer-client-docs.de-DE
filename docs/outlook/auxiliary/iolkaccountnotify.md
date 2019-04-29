---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412499"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Stellt dem Client einen Rückruf für Änderungen an einem Konto bereit.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Bereitgestellt von:  <br/> | Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Benachrichtigen](iolkaccountnotify-notify.md) <br/> |Benachrichtigt den Client über Änderungen am angegebenen Konto.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird an [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md) beim Einrichten von Benachrichtigungen übergeben. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

