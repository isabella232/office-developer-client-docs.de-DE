---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem parameter userID übereinstimmen.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434795"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem _parameter userID übereinstimmen._ 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_userId_
  
> [in] Eine Benutzer-ID des sozialen Netzwerks, eine SMTP-Adresse oder ein Anzeigename einer Person.
    
_result_
  
> [out] Eine XML-Zeichenfolge, die eine oder mehrere Personen darstellt, die den vom parameter userId angegebenen  _Identifikationsinformationen_ entsprechen. 
    
## <a name="remarks"></a>Hinweise

Wenn eine oder mehrere Personen mit der **FindPerson-Anforderung** übereinstimmen, gibt diese Methode die Informationen für diese Personen im  _Ergebnisparameter_ zurück. Die  Ergebnis-XML-Zeichenfolge muss der Schemadefinition für Freunde **entsprechen,** wie sie im Schema für die Erweiterbarkeit des Outlook Social Connector (OSC) definiert ist. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

