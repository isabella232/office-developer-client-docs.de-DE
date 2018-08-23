---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 311d055e0a319ec26cdc4eba5ac3b50dc9e63d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565179"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Zusätzliche Informationen zu den letzten Fehler.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Ruft eine Meldungszeichenfolge für den angegebenen Fehler.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Schnittstelle stellt zusätzliche Informationen zu einem Fehler in [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)und [IOlkAccount](iolkaccount.md). Es ist außerdem die Basis-Schnittstelle für **IOlkAccountManager**, **IOlkAccountNotify**und **IOlkAccount**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

