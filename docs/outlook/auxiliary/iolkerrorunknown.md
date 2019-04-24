---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321854"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Enthält zusätzliche Informationen zum letzten Fehler.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](iolkerrorunknown-getlasterror.md) <br/> |Ruft eine Meldungszeichenfolge für den angegebenen Fehler ab.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle bietet zusätzliche Informationen zu einem Fehler in [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)und [IOlkAccount](iolkaccount.md). Es ist auch die Basisschnittstelle für **IOlkAccountManager**, **IOlkAccountNotify**und **IOlkAccount**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

