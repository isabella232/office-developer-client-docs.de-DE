---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Meldet sich mithilfe der formularbasierten Authentifizierung am Standort des sozialen Netzwerks an.
ms.openlocfilehash: 923838f0064d979b7901ebe269822059a75400c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563196"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Meldet sich mithilfe der formularbasierten Authentifizierung am Standort des sozialen Netzwerks an.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> [in] Eine Zeichenfolge, die **NULL** ist, eine URL zu einem Anmeldeformular im Web oder eine Zeichenfolge, die Anmeldeinformationen enthält, abhängig vom Kontext im Anmeldevorgang, wenn diese Methode aufgerufen wird.
    
_connectOut_
  
> [out] Eine Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Outlook Connector für soziale Netzwerke (OSC) ruft die **LogonWeb-Methode** nur auf, wenn der Anbieter angibt, dass er die formularbasierte Authentifizierung unterstützt. Der Anbieter gibt an, dass für **funktionen** die formularbasierte Authentifizierung erforderlich ist, indem **"useLogonWebAuth"** im XML-Code als **"true"** festgelegt wird. Wenn die Anbietersätze **"logonWebAuth"** als **"false"** verwenden, verwendet OSC die Standardauthentifizierung und ruft die [ISocialSession::Logon-Methode auf.](isocialsession-logon.md) 
  
Die Anmeldung an einem Standort für soziale Netzwerke mithilfe der formularbasierten Authentifizierung umfasst das Aufrufen der Methoden **LogonWeb** und [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) in einer bestimmten Reihenfolge: 
  
1. Der OSC ruft **LogonWeb** zum ersten Mal auf und übergibt **null** an den _connectIn-Parameter._ 
    
2. Der Anbieter löst den OSC_E_AUTH_ERROR Fehler an osc aus.
    
3. Der OSC ruft als Nächstes **GetLogonUrl auf.**
    
4. Der Anbieter gibt die entsprechende URL zu einer Anmeldeseite in der **GetLogonUrl-Methode** zurück. 
    
5. Der OSC verwendet die von **GetLogonUrl** zurückgegebene URL, um die formularbasierte Anmeldeseite anzuzeigen. 
    
6. Der OSC ruft dann **LogonWeb** ein zweites Mal auf und übergibt die URL an das Anmeldeformular im _connectIn-Parameter._ 
    
7. Wenn die Authentifizierung erfolgreich ist, gibt der Anbieter Anmeldeinformationen im  _connectOut-Parameter_ an osc zurück. Wenn die Authentifizierung fehlschlägt, löst der Anbieter den OSC_E_AUTH_ERROR Fehler an osc aus. 
    
Wenn der OSC-Anbieter die Anmeldung mit zwischengespeicherten Anmeldeinformationen unterstützt, gibt er an, dass **"useLogonCached"** in der **Funktions-XML** **"true"** ist. Der Anbieter sollte alle Anmeldeinformationen in der  _connectOut-Zeichenfolge_ platzieren, die der Anbieter von OSC über Verbindungen speichern soll. Die  _connectOut-Zeichenfolge_ wird vom OSC nicht interpretiert. Nachdem der OSC überprüft hat, ob **useLogonCached** **"true"** ist, verschlüsselt osc die Zeichenfolge aus Sicherheitsgründen, bevor sie in der Windows-Registrierung gespeichert wird. Der OSC übergibt diese Zeichenfolge an den _parameter connectIn_ bei nachfolgenden Versuchen, sich beim sozialen Netzwerk anzumelden, indem [ISocialSession2::LogonCached aufgerufen wird.](isocialsession2-logoncached.md) 
  
Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Formularbasierte Authentifizierung](forms-based-authentication.md)

