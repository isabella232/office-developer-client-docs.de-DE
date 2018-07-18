---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Meldet sich bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795995"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Meldet sich bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameter

_connectIn_
  
> [in] Eine Zeichenfolge, die ist **null**, eine URL zu einem Formular Anmeldung auf dem Web oder eine Zeichenfolge, die Anmeldeinformationen, je nach Kontext während der Anmeldung beim Aufruf dieser Methode enthält.
    
_connectOut_
  
> [out] Eine Zeichenfolge, die Anmeldeinformationen enthält.
    
## <a name="remarks"></a>Bemerkungen

Outlook Social Connector (OSC) Ruft die **LogonWeb** -Methode nur, wenn der Anbieter gibt an, dass sie die formularbasierte Authentifizierung unterstützt. Der Anbieter gibt an, dass es formularbasierte Authentifizierung erfordert, indem **UseLogonWebAuth** als **true** in den XML-Code für **Funktionen**festlegen. Wenn der Anbieter **UseLogonWebAuth** als **false**legt fest, die OSC wird die Standardauthentifizierung verwendet und die [ISocialSession::Logon](isocialsession-logon.md) -Methode aufgerufen. 
  
Anmelden bei einer Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung umfasst das Aufrufen der Methods **LogonWeb** und [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) in einer bestimmten Reihenfolge: 
  
1. Die OSC ruft **LogonWeb** beim ersten **null** an den _ConnectIn_ -Parameter übergeben. 
    
2. Der Anbieter wird von der OSC_E_AUTH_ERROR Fehler an das osc bilden.
    
3. Die OSC-Anrufe Weiter **GetLogonUrl**.
    
4. Der Anbieter gibt die entsprechende URL zu einer Anmeldeseite in der **GetLogonUrl** -Methode zurück. 
    
5. Die OSC mithilfe den von **GetLogonUrl** zurückgegebenen URL die Anmeldeseite von formularbasierten angezeigt. 
    
6. Die OSC ruft dann **LogonWeb** ein zweites Mal die URL an das Anmeldeformular im _ConnectIn_ -Parameter übergeben. 
    
7. Wenn Authentifizierung erfolgreich ist, gibt der Anbieter Anmeldeinformationen im _ConnectOut_ -Parameter an die OSC. Wenn die Authentifizierung fehlschlägt, löst der Anbieter der OSC_E_AUTH_ERROR Fehler, der die OSC aus. 
    
Wenn der OSC-Anbieter mit zwischengespeicherten Anmeldeinformationen anmelden unterstützt, gibt **UseLogonCached** in **Funktionen** XML als **true** an. Der Anbieter sollte Anmeldeinformationen in der Zeichenfolge _ConnectOut_ tätigen, die der Anbieter das osc bilden, um Verbindungen zu speichern möchte. Das osc bilden kann nicht die Zeichenfolge _ConnectOut_ interpretieren. Nachdem die OSC überprüft hat, dass diese **UseLogonCached** auf **true**festgelegt ist, werden die OSC die Zeichenfolge für die Sicherheit vor dem Speichern in der Windows-Registrierung verschlüsselt. Die OSC übergibt diese Zeichenfolge für den Parameter _ConnectIn_ auf nachfolgenden Versuche, die durch Aufrufen von [ISocialSession2::LogonCached](isocialsession2-logoncached.md)in sozialen Netzwerken anmelden. 
  
Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Formularbasierte Authentifizierung](forms-based-authentication.md)

