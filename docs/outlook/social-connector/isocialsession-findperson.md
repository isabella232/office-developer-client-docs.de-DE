---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Ruft eine Zeichenfolge, die eine oder mehrere Personen darstellt, die den Benutzer-ID-Parameter entsprechen.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795983"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Ruft eine Zeichenfolge, die eine oder mehrere Personen darstellt, die den _Benutzer-ID_ -Parameter entsprechen. 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_userId_
  
> [in] Eine Benutzer-ID für soziale Netzwerke, SMTP-Adresse oder Anzeigename den Namen einer Person.
    
_Ergebnis_
  
> [out] Eine XML-Zeichenfolge, die eine oder mehrere Personen darstellt, die durch den _Benutzer-ID_ -Parameter angegebenen Informationen zur Identifizierung entsprechen. 
    
## <a name="remarks"></a>Bemerkungen

Wenn eine oder mehrere Personen die Anforderung **FindPerson** übereinstimmen, gibt diese Methode die Informationen für die Personen in der _Result_ -Parameters. Die _resultierende_ XML-Zeichenfolge muss der Schemadefinition für **Freunde**, gemäß Definition im Schema für Outlook Social Connector (OSC)-Erweiterbarkeit des Providers entsprechen. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

