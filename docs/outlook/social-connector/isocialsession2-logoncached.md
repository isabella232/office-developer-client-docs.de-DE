---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.
ms.openlocfilehash: 880484db2d5233e9a8bfe9cfd734d33d826dd4e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583016"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> [in] Eine Zeichenfolge, die leer sein kann oder die Anmeldeinformationen enthält, abhängig vom Kontext, in dem der OSC **LogonCached aufruft.**
    
_userName_
  
> [in] Eine Zeichenfolge, die den Benutzernamen enthält.
    
_password_
  
> [in] Eine Zeichenfolge, die das Kennwort des Benutzers enthält.
    
_connectOut_
  
> [out] Eine undurchsichtige Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Diese Methode wird nur für die Authentifizierung aufgerufen, wenn **useLogonCached** in den von [ISocialProvider::GetCapabilities zurückgegebenen](isocialprovider-getcapabilities.md) **Funktionen-XML** auf **"true"** festgelegt ist.
  
Der Outlook Connector für soziale Netzwerke (OSC) ruft **LogonCached auf** und übergibt eine leere Zeichenfolge für _connectIn-_ und nicht leere _Benutzernamen-_ und _Kennwortzeichenfolgen._ Der Anbieter verwendet  _"userName"_ und  _"password",_ um sich beim sozialen Netzwerk anzumelden, und gibt einen undurchsichtigen  _connectOut-Parameter_ an osc zurück, wenn die Authentifizierung erfolgreich ist. Wenn die Authentifizierung fehlschlägt, gibt der Anbieter den OSC_E_LOGON_FAILURE Fehler an osc zurück. 
  
Der  _connectOut-Parameter_ ist eine undurchsichtige Zeichenfolge für osc und wird bei nachfolgenden Versuchen des OSC, sich beim sozialen Netzwerk anzumelden, an den  _parameter connectIn_ übergeben. Der Anbieter sollte alle Anmeldeinformationen in der  _connectOut-Zeichenfolge_ platzieren, die vom Anbieter über Verbindungen hinweg vom OSC gespeichert werden soll. Der OSC interpretiert die Zeichenfolge nicht in _connectOut_ und verschlüsselt die Zeichenfolge aus Sicherheitsgründen, bevor sie in der Windows-Registrierung gespeichert wird.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

