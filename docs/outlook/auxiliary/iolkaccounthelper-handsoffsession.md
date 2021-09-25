---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Gibt das MAPI-Sitzungsobjekt frei, das von IOlkAccountHelper::GetMapiSession zurückgegeben wurde.
ms.openlocfilehash: 3909d65d516d2b2da8e215bf5504e0ab64faa374
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617118"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Gibt das MAPI-Sitzungsobjekt frei, das zurückgegeben wurde – [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Wenn Ihre Implementierung von **IOlkAccountHelper** eine eigene MAPI-Sitzung erstellt, die in **IOlkAccountHelper::GetMapiSession** zurückgegeben wird, müssen Sie die Sitzung hier freigeben und S_OK zurückgeben.  <br/> |
|E_NOTIMPL  <br/> |Wenn Ihre Implementierung von **IOlkAccountHelper** keine eigene MAPI-Sitzung erstellt hat, dürfen Sie nur E_NOTIMPL zurückgeben. In diesem Fall ist dies der einzige unterstützte Rückgabewert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

