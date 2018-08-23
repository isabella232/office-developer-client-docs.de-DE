---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.
ms.openlocfilehash: edfc9980445fcc2e111045650667d93bffa94153
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565137"
---
# <a name="fbuser"></a>FBUser

Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.
  
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
  
> Die Länge des Eintrags-ID des e-Mail-Benutzers dargestellt durch die [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) -Schnittstelle. 
    
_m_lpEid_
  
> Die Eintrags-ID des e-Mail-Benutzers dargestellt durch die **IMailUser** -Schnittstelle. 
    
_m_ulReserved_
  
> Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
_m_pwszReserved_
  
> Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
## <a name="see-also"></a>Siehe auch

- [Informationen zur Frei/Gebucht-API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

