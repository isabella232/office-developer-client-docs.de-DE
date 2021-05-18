---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert einen Benutzer, für den Frei/Gebucht-Daten verfügbar sind oder nicht.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317661"
---
# <a name="fbuser"></a>FBUser

Identifiziert einen Benutzer, für den Frei/Gebucht-Daten verfügbar sind oder nicht.
  
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
  
> Die Länge der Eintrags-ID des E-Mail-Benutzers, dargestellt durch die [IMailUser-Schnittstelle.](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) 
    
_m_lpEid_
  
> Die Eintrags-ID des E-Mail-Benutzers, dargestellt durch die **IMailUser-Schnittstelle.** 
    
_m_ulReserved_
  
> Dieser Parameter ist für die Outlook reserviert und wird nicht unterstützt.
    
_m_pwszReserved_
  
> Dieser Parameter ist für die Outlook reserviert und wird nicht unterstützt.
    
## <a name="see-also"></a>Siehe auch

- [Informationen zur Frei/Gebucht-API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

