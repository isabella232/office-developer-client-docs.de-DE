---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322155"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Stellt Hilfsfunktionen in der aktuellen MAPI-Sitzung zum Verwalten von Konten bereit.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Platzhalter1](iolkaccounthelper-placeholder1.md) <br/> | *Dieses Element ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Ruft den Profilnamen eines Kontos ab.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Konto-Manager.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Gibt das MAPI-Sitzungsobjekt frei, das von [IOlkAccountHelper zurückgegeben wurde::GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Schnittstelle wird beim Initialisieren des Konto-Managers an [IOlkAccountManager::Init](iolkaccountmanager-init.md) übergeben. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

