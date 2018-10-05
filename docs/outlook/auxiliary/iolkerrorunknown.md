---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384640"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Zusätzliche Informationen zu den letzten Fehler.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Ruft eine Meldungszeichenfolge für den angegebenen Fehler.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Schnittstelle stellt zusätzliche Informationen zu einem Fehler in [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)und [IOlkAccount](iolkaccount.md). Es ist außerdem die Basis-Schnittstelle für **IOlkAccountManager**, **IOlkAccountNotify**und **IOlkAccount**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

