---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Ruft den Profilnamen eines Kontos ab.
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791091"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Ruft den Profilnamen eines Kontos ab.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccountHelper](iolkaccounthelper.md).
  
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
  
> [in] [out] Beim Aufrufen dieser Methode enthält die Größe (in Anzahl von Zeichen) der _PwszIdentity_ , der zugeordnet wurde. Bei der Rückgabe enthält die tatsächliche Länge, einschließlich des Zeichens 0 zum Abbruch des Namens zurückgegebene Profil. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OUTOFMEMORY  <br/> |Der zurückgegebene Profilname ist länger als die Größe der _PwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _Pcch_ ist NULL.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn _PwszIdentity_ zu klein, um den Profilnamen enthalten ist, wird bei der Rückgabe nicht festgelegt werden, und _Pcch_ verweist auf die Größe für _PwszIdentity_erforderlich.
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

