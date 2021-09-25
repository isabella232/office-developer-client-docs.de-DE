---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert einen Benutzer, der möglicherweise Frei/Gebucht-Daten zur Verfügung hat.
ms.openlocfilehash: e3c67d8cf4e858fa6b5bdde7bb1714c5caacb484
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568040"
---
# <a name="fbuser"></a>FBUser

Identifiziert einen Benutzer, der möglicherweise Frei/Gebucht-Daten zur Verfügung hat.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a>Elemente

_m_cbEid_
  
> Die Länge der Eintrags-ID des E-Mail-Benutzers, wie sie von der [IMailUser-Schnittstelle](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) dargestellt wird. 
    
_m_lpEid_
  
> Die Eintrags-ID des E-Mail-Benutzers, dargestellt durch die **IMailUser-Schnittstelle.** 
    
_m_ulReserved_
  
> Dieser Parameter ist für Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
_m_pwszReserved_
  
> Dieser Parameter ist für Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
## <a name="see-also"></a>Siehe auch

- [Informationen zur Frei/Gebucht-API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

