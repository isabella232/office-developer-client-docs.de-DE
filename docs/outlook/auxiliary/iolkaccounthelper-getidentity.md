---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Ruft den Profilnamen eines Kontos ab.
ms.openlocfilehash: d24f108aa4227ce8fe38e46b48a8f56a0eb29cdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625686"
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
  
> [in] [out] Der Profilname.
    
_pcch_
  
> [in] [out] Enthält beim Aufrufen dieser Methode die Größe (in Anzahl der Zeichen) von  _pwszIdentity,_ die zugewiesen wurde. Enthält bei der Rückgabe die tatsächliche Länge des zurückgegebenen Profilnamens, einschließlich des 0-endenden Zeichens. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OUTOFMEMORY  <br/> |Der zurückgegebene Profilname ist länger als die Größe von  _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ ist NULL.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn  _pwszIdentity_ zu klein ist, um den Profilnamen zu speichern, wird er bei der Rückgabe nicht festgelegt, und  _pcch_ verweist auf die für  _pwszIdentity_ erforderliche Größe.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

