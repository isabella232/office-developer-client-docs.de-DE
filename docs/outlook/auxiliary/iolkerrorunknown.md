---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 60e5a6f7400a3bb7ab2df1fc25cc2c469af29418
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617083"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Stellt zusätzliche Informationen zum letzten Fehler bereit.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](iolkerrorunknown-getlasterror.md) <br/> |Ruft eine Meldungszeichenfolge für den angegebenen Fehler ab.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle enthält zusätzliche Informationen zu einem Fehler in [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)und [IOlkAccount](iolkaccount.md). Es ist auch die Basisschnittstelle für **IOlkAccountManager**, **IOlkAccountNotify** und **IOlkAccount**. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)

