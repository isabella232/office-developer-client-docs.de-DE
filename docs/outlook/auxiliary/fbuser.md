---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790930"
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

## <a name="members"></a>Members

_m_cbEid_
  
> Die Länge des Eintrags-ID des e-Mail-Benutzers dargestellt durch die [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) -Schnittstelle. 
    
_m_lpEid_
  
> Die Eintrags-ID des e-Mail-Benutzers dargestellt durch die **IMailUser** -Schnittstelle. 
    
_m_ulReserved_
  
> Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
_m_pwszReserved_
  
> Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
## <a name="see-also"></a>Siehe auch

- [Über die Frei/Gebucht-API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

