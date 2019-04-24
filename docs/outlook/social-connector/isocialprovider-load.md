---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialisiert den Outlook Social Connector (OSC)-Anbieter.
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285759"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Initialisiert den Outlook Social Connector (OSC)-Anbieter.
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameter

_socialProviderInterfaceVersion_
  
> in Die Version der OSC-Anbieterschnittstellen, die vom OSC erwartet werden.
    
_languageTag_
  
> in Das von [[rfc4646]](https://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)definierte IETF-Sprachtag (Internet Engineering Task Force), das die aktuelle Sprache der Benutzeroberfläche von Outlook darstellt.
    
## <a name="remarks"></a>Bemerkungen

Das Versionsformat für den _socialProviderInterfaceVersion_ -Parameter ist _X_. _xxxx_, wobei _X_ die Hauptversion ist und _xxxx_ die Nebenversion des osc ist. Für Office 2013 überprüfen Sie, ob die Hauptversion 15 ist. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

