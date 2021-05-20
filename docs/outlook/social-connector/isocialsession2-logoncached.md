---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436622"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> [in] Eine Zeichenfolge, die leer sein kann oder die Anmeldeinformationen enthält, abhängig vom Kontext, in dem das OSC **LogonCached aufruft.**
    
_userName_
  
> [in] Eine Zeichenfolge, die den Benutzernamen enthält.
    
_password_
  
> [in] Eine Zeichenfolge, die das Kennwort des Benutzers enthält.
    
_connectOut_
  
> [out] Eine undurchsichtige Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>Hinweise

Diese Methode wird nur für die Authentifizierung aufgerufen, wenn  **useLogonCached** in den von ISocialProvider zurückgegebenen Funktionen-XML als **true** festgelegt [ist::GetCapabilities](isocialprovider-getcapabilities.md).
  
Der Outlook Social Connector (OSC) ruft **LogonCached** auf und übergibt eine leere Zeichenfolge für _connectIn-_ und nicht leere _UserName-_ und _Kennwortzeichenfolgen._ Der Anbieter verwendet  _userName_ und  _Kennwort,_ um sich beim sozialen Netzwerk zu anmelden, und gibt einen undurchsichtigen  _connectOut-Parameter_ an die OSC zurück, wenn die Authentifizierung erfolgreich ist. Wenn bei der Authentifizierung ein Fehler auftritt, gibt der OSC_E_LOGON_FAILURE-Fehler an das Betriebssystem zurück. 
  
Der  _connectOut-Parameter_ ist eine undurchsichtige Zeichenfolge an das OSC und wird bei nachfolgenden Versuchen des OSC, sich beim sozialen Netzwerk zu melden, an den  _connectIn-Parameter_ übergeben. Der Anbieter sollte alle Anmeldeinformationen in der  _connectOut-Zeichenfolge_ platzieren, die vom Anbieter über verbindungen hinweg vom OSC gespeichert werden soll. Das OSC interpretiert die Zeichenfolge nicht in _connectOut_ und verschlüsselt die Zeichenfolge aus Sicherheitsgründen, bevor sie in der Windows gespeichert wird.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

