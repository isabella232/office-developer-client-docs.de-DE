---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: a663305653df1732cd4fc61daa8bd81354946c18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625672"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Stellt Hilfsfunktionen in der aktuellen MAPI-Sitzung zum Verwalten von Konten bereit.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Platzhalter1](iolkaccounthelper-placeholder1.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Ruft den Profilnamen eines Kontos ab.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Konto-Manager.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Gibt das MAPI-Sitzungsobjekt frei, das von [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)zurückgegeben wurde.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird an [IOlkAccountManager::Init](iolkaccountmanager-init.md) übergeben, wenn der Konto-Manager initialisiert wird. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

