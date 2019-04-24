---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Ruft den Profilnamen eines Kontos ab.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322106"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Ruft den Profilnamen eines Kontos ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Parameter

_pwszIdentity_
  
> in Out Der Profilname.
    
_pcch_
  
> in Out Beim Aufrufen dieser Methode enthält die Größe (in Zeichen) von _pwszIdentity_ , die zugeordnet wurde. Bei Rückgabe enthält die tatsächliche Länge des zurückgegebenen Profilnamens, einschließlich des 0-Abschlusszeichens. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OUTOFMEMORY  <br/> |Der zurückgegebene Profilname ist länger als die Größe von _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ ist NULL.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn _pwszIdentity_ zu klein für den Profilnamen ist, wird er bei der Rückgabe nicht festgelegt, und _pcch_ zeigt auf die für _pwszIdentity_erforderliche Größe.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

