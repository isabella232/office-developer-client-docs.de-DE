---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die dem parameter userID entsprechen.
ms.openlocfilehash: 789f98dcc8e4b09a230d148644f60a2fbf1c3328
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594916"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die dem  _parameter userID_ entsprechen. 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameter

_userId_
  
> [in] Eine Benutzer-ID, SMTP-Adresse oder der Anzeigename einer Person im sozialen Netzwerk.
    
_result_
  
> [out] Eine XML-Zeichenfolge, die eine oder mehrere Personen darstellt, die den durch den  _parameter userId_ angegebenen Identifikationsinformationen entsprechen. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine oder mehrere Personen mit der **FindPerson-Anforderung** übereinstimmen, gibt diese Methode die Informationen für diese Personen im  _Ergebnisparameter_ zurück. Die ERGEBNIS-XML-Zeichenfolge muss der Schemadefinition für **Freunde** entsprechen, wie sie im Schema für die Osc-Anbietererweiterung (Social Connector) Outlook.  
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

