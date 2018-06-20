---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich bei der Website für soziale Netzwerke mithilfe von Anmeldeinformationen.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796002"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Meldet sich bei der Website für soziale Netzwerke mithilfe von Anmeldeinformationen.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> [in] Eine Zeichenfolge, die kann leer sein oder enthält die Anmeldeinformationen, je nach den Kontext, in dem die OSC **LogonCached**anruft.
    
_userName_
  
> [in] Eine Zeichenfolge, die den Benutzernamen enthält.
    
_password_
  
> [in] Eine Zeichenfolge, die das Kennwort des Benutzers enthält.
    
_connectOut_
  
> [out] Eine opake Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>Hinweise

Diese Methode ist für die Authentifizierung nur aufgerufen, wenn **UseLogonCached** in die **Funktionen** von [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)zurückgegebenen XML-Daten als **true** festgelegt ist.
  
Outlook Social Connector (OSC) **LogonCached**aufruft, und eine leere Zeichenfolge für _ConnectIn_ und nicht leeren Zeichenfolgen für _Benutzername_ und _Kennwort_ übergibt. Der Anbieter _Benutzernamen_ und das _Kennwort_ zur Anmeldung bei dem sozialen Netzwerk verwendet und gibt einen undurchsichtiger _ConnectOut_ -Parameter ist die Authentifizierung erfolgreich die OSC zurück. Wenn Authentifizierung ein Fehler auftritt, gibt der Anbieter den OSC_E_LOGON_FAILURE Fehler an das osc bilden. 
  
Der Parameter _ConnectOut_ ist eine opake Zeichenfolge an die OSC und auf nachfolgenden Versuche an den Parameter _ConnectIn_ durch die OSC zur Anmeldung bei dem sozialen Netzwerk übergeben. Der Anbieter sollte keine Anmeldeinformationen in der Zeichenfolge _ConnectOut_ platzieren, die der Anbieter das osc bilden, um Verbindungen zu speichern möchte. Das osc bilden kann nicht die Zeichenfolge in _ConnectOut_interpretieren und verschlüsselt die Zeichenfolge aus Sicherheitsgründen vor dem Speichern in der Windows-Registrierung.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2: IUnknown](isocialsession2iunknown.md)

