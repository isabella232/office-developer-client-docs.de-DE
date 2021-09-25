---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Ruft eine Meldungszeichenfolge für den angegebenen Fehler ab.
ms.openlocfilehash: 3a32c4bdb3bed1f98228670a5ac66f7d36f14855
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561894"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Ruft eine Meldungszeichenfolge für den angegebenen Fehler ab. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Parameter

_Hr_
  
> [in] Der nachzuschlagende Fehlercode.
    
_ppwszError_
  
> [out] Die Fehlermeldung, die  *hr*  entspricht. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)

