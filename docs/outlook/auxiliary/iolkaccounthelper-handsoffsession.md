---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Gibt das MAPI-Sitzung-Objekt, das von IOlkAccountHelper::GetMapiSession zurückgegeben wurde.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791081"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Gibt das MAPI-Sitzung-Objekt, das von - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)zurückgegeben wurde.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Wenn die Implementierung von **IOlkAccountHelper** eigene MAPI-Sitzung, die in **IOlkAccountHelper::GetMapiSession**zurückgegeben wird erstellt, müssen Sie hier die Sitzung freigeben und geben Sie S_OK zurück.  <br/> |
|E_NOTIMPL  <br/> |Wenn die Implementierung von **IOlkAccountHelper** eigene MAPI-Sitzung nicht selbst erstellt haben, müssen Sie nur E_NOTIMPL zurückgeben. In diesem Fall ist dies der einzige unterstützte Rückgabewert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

