---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Meldet sich mithilfe der formularbasierten Authentifizierung an der Website für soziale Netzwerke an.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335364"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Meldet sich mithilfe der formularbasierten Authentifizierung an der Website für soziale Netzwerke an.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> in Eine Zeichenfolge, die **null**ist, eine URL zu einem Anmeldeformular im Web oder eine Zeichenfolge, die Anmeldeinformationen enthält, je nach Kontext im Anmeldeprozess, wenn diese Methode aufgerufen wird.
    
_Verbindung_
  
> Out Eine Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>Bemerkungen

Der Outlook Connector für soziale Netzwerke (OSC) Ruft die **LogonWeb** -Methode nur auf, wenn der Anbieter angibt, dass die formularbasierte Authentifizierung unterstützt wird. Der Anbieter gibt an, dass die formularbasierte Authentifizierung erforderlich ist, indem **useLogonWebAuth** als **true** im XML for **Capabilities**festgelegt wird. Wenn der Anbieter **useLogonWebAuth** als **false**festlegt, verwendet der osc die Standardauthentifizierung und ruft die [ISocialSession:: Login](isocialsession-logon.md) -Methode auf. 
  
Bei der Anmeldung an einem sozialen Netzwerkstandort mithilfe der formularbasierten Authentifizierung müssen Sie die Methoden **LogonWeb** und [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) in einer bestimmten Reihenfolge aufrufen: 
  
1. OSC ruft **LogonWeb** zum ersten Mal auf und übergibt **null** an den __ Parameter connectin. 
    
2. Der Anbieter löst den OSC_E_AUTH_ERROR-Fehler an den OSC aus.
    
3. Der OSC ruft **GetLogonUrl**.
    
4. Der Anbieter gibt die entsprechende URL an eine Anmeldeseite in der **GetLogonUrl** -Methode zurück. 
    
5. OSC verwendet die von **GetLogonUrl** zurückgegebene URL, um die formularbasierte Anmeldeseite anzuzeigen. 
    
6. Der OSC ruft dann **LogonWeb** ein zweites Mal auf, wobei die URL an das Anmeldeformular im __ Parameter connectin übergeben wird. 
    
7. Wenn die Authentifizierung erfolgreich ist, gibt der Anbieter Anmeldeinformationen im __ Parameter Connecting an den osc zurück. Wenn die Authentifizierung fehlschlägt, löst der Anbieter den OSC_E_AUTH_ERROR-Fehler an den OSC aus. 
    
Wenn der OSC-Anbieter die Anmeldung mithilfe zwischengespeicherter Anmeldeinformationen unterstützt, gibt er **useLogonCached** als **true** im **Capabilities** -XML an. Der Anbieter sollte alle Anmeldeinformationen in der _Verbindungs_ Zeichenfolge platzieren, die der osc über Verbindungen speichern möchte. OSC interpretiert die _Verbindungs_ Zeichenfolge nicht. Nachdem OSC überprüft hat, dass **useLogonCached** auf **true**festgelegt ist, verschlüsselt der osc die Zeichenfolge vor dem Speichern in der Windows-Registrierung. OSC übergibt diese Zeichenfolge an den __ Parameter connectin bei nachfolgenden Anmeldeversuchen beim sozialen Netzwerk durch Aufrufen von [ISocialSession2:: LogonCached](isocialsession2-logoncached.md). 
  
Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Formularbasierte Authentifizierung](forms-based-authentication.md)

