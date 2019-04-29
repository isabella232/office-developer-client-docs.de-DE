---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich mithilfe zwischengespeicherter Anmeldeinformationen an der Website für soziale Netzwerke an.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436622"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Meldet sich mithilfe zwischengespeicherter Anmeldeinformationen an der Website für soziale Netzwerke an.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> in Eine Zeichenfolge, die leer sein oder die Anmeldeinformationen enthalten kann, je nachdem, in welchem Kontext der OSC **LogonCached**aufruft.
    
_userName_
  
> in Eine Zeichenfolge, die den Benutzernamen enthält.
    
_password_
  
> in Eine Zeichenfolge, die das Kennwort des Benutzers enthält.
    
_Verbindung_
  
> Out Eine undurchsichtige Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>Bemerkungen

Diese Methode wird nur für die Authentifizierung aufgerufen, wenn **useLogonCached** in den von [ISocialProvider: getCapabilities](isocialprovider-getcapabilities.md)zurückgegebenen **Capabilities-Funktionen** als **true** festgelegt ist.
  
Der Outlook Connector für soziale Netzwerke (OSC) ruft **LogonCached**auf und übergibt eine leere Zeichenfolge für _connectin_ und nicht leere _Benutzernamen_ -und _Kenn Wort_ Zeichenfolgen. Der Anbieter verwendet _username_ und _Password_ , um sich beim sozialen Netzwerk anzumelden, und gibt einen Opaque- _Verbindungs_ Parameter an den osc zurück, wenn die Authentifizierung erfolgreich ist. Wenn die Authentifizierung fehlschlägt, gibt der Anbieter den OSC_E_LOGON_FAILURE-Fehler an den OSC zurück. 
  
Der __ Parameter Connecting ist eine undurchsichtige Zeichenfolge für OSC und wird bei nachfolgenden Versuchen des osc zur Anmeldung am sozialen Netzwerk an den Parameter _connectin_ übergeben. Der Anbieter sollte alle Anmeldeinformationen in der _Verbindungs_ Zeichenfolge platzieren, die der osc über Verbindungen speichern möchte. OSC interpretiert die Zeichenfolge nicht in der _Verbindung_und verschlüsselt die Zeichenfolge aus Sicherheitsgründen, bevor Sie in der Windows-Registrierung gespeichert wird.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

