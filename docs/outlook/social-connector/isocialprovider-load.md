---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialisiert den Anbieter Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795977"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Initialisiert den Anbieter Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameter

_socialProviderInterfaceVersion_
  
> [in] Die Version des von der OSC erwartet OSC-Provider-Schnittstellen.
    
_languageTag_
  
> [in] Der Internet Engineering Task Force (IETF) Sprach-Tag, definiert durch [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), die die Sprache der Benutzeroberfläche von Outlook darstellt.
    
## <a name="remarks"></a>Hinweise

Das Versionsformat für den Parameter _SocialProviderInterfaceVersion_ ist _X_. _Xxxx_, wobei _X_ der Hauptversion und _Xxxx_ ist die Nebenversion der die OSC. Überprüfen Sie für Office 2013 für die Hauptversion wird 15. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

