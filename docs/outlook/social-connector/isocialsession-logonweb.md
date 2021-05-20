---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Meldet sich mithilfe der formularbasierten Authentifizierung am Standort des sozialen Netzwerks an.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430336"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Meldet sich mithilfe der formularbasierten Authentifizierung am Standort des sozialen Netzwerks an.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> [in] Eine Zeichenfolge, die **null** ist, eine URL zu einem Anmeldeformular im Web oder eine Zeichenfolge, die Anmeldeinformationen enthält, abhängig vom Kontext im Anmeldeprozess, wenn diese Methode aufgerufen wird.
    
_connectOut_
  
> [out] Eine Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>Hinweise

Die Outlook Social Connector (OSC) ruft die **LogonWeb-Methode** nur auf, wenn der Anbieter angibt, dass er die formularbasierte Authentifizierung unterstützt. Der Anbieter gibt an, dass eine formularbasierte Authentifizierung erforderlich ist, indem **useLogonWebAuth** in der XML für Funktionen als **true** **angegeben wird.** Wenn der Anbieter **useLogonWebAuth** als **false** fest legt, verwendet das OSC die Standardauthentifizierung und ruft die [ISocialSession::Logon-Methode](isocialsession-logon.md) auf. 
  
Die Anmeldung bei einem Standort für soziale Netzwerke mithilfe der formularbasierten Authentifizierung umfasst das Aufrufen der **Methoden LogonWeb** und [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) in einer bestimmten Reihenfolge: 
  
1. Das OSC ruft **das erste Mal LogonWeb** auf und übertut **null** an den _connectIn-Parameter._ 
    
2. Der Anbieter löst den fehler OSC_E_AUTH_ERROR osC aus.
    
3. Der OSC ruft als nächstes **GetLogonUrl auf.**
    
4. Der Anbieter gibt die entsprechende URL zu einer Anmeldeseite in der **GetLogonUrl-Methode** zurück. 
    
5. Das OSC verwendet die von **GetLogonUrl** zurückgegebene URL zum Anzeigen der formularbasierten Anmeldeseite. 
    
6. Das OSC ruft dann ein zweites **Mal LogonWeb** auf, und übergeben die URL an das Anmeldeformular im _connectIn-Parameter._ 
    
7. Wenn die Authentifizierung erfolgreich ist, gibt der Anbieter Anmeldeinformationen im  _connectOut-Parameter_ an das OSC zurück. Wenn die Authentifizierung fehlschlägt, löst der Anbieter den OSC_E_AUTH_ERROR-Fehler an das OSC aus. 
    
Wenn der OSC-Anbieter die Anmeldung mithilfe zwischengespeicherter Anmeldeinformationen unterstützt, gibt er **useLogonCached** als **true** im Xml-Funktionen **an.** Der Anbieter sollte alle Anmeldeinformationen in der  _connectOut-Zeichenfolge_ platzieren, die vom Anbieter über verbindungen hinweg vom OSC gespeichert werden soll. Das OSC interpretiert die _connectOut-Zeichenfolge nicht._ Nachdem die OSC überprüft hat, dass **useLogonCached** **true** ist, verschlüsselt das OSC die Zeichenfolge aus Sicherheitsgründen, bevor sie in der Registrierung Windows wird. Das OSC übergibt diese Zeichenfolge an den _connectIn-Parameter_ bei nachfolgenden Versuchen, sich beim sozialen Netzwerk durch Aufrufen von [ISocialSession2::LogonCached zu anmelden.](isocialsession2-logoncached.md) 
  
Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Formularbasierte Authentifizierung](forms-based-authentication.md)

