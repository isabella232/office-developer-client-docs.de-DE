---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialisiert den Anbieter Outlook Connector für soziale Netzwerke (SOCIAL Connector, OSC).
ms.openlocfilehash: 4e41c78c016358c205f860345bee6cdcf3ba06e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608865"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Initialisiert den Anbieter Outlook Connector für soziale Netzwerke (SOCIAL Connector, OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameter

_socialProviderInterfaceVersion_
  
> [in] Die Version der OSC-Anbieterschnittstellen, die vom OSC erwartet wird.
    
_languageTag_
  
> [in] Das IETF-Sprachtag (Internet Engineering Task Force), definiert durch [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647],](https://www.ietf.org/rfc/rfc4647.txt)das die aktuelle Outlook Sprache der Benutzeroberfläche darstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Versionsformat für den  _parameter socialProviderInterfaceVersion_ ist  _X_. _xxxx_, wobei  _X_ die Hauptversion und  _xxxx_ die Nebenversion des OSC ist. For Office 2013, check for the major version being 15. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

