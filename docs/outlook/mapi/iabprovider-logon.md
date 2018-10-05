---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384108"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt eine Verbindung mit einer aktiven Sitzung her.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a>Parameter

 _lpMAPISup_
  
> [in] Ein Zeiger auf die Adressbuchanbieter DSO-Objekt.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für das Dialogfeld anmelden, die die **Logon** -Methode angezeigt, wenn zulässig. Der Parameter _UlUIParam_ enthält den Wert des Parameters mit demselben Namen in der vorherigen Aufruf der Funktion [MAPILogonEx](mapilogonex.md) MAPI übergeben. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils Sitzung.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
AB_NO_DIALOG 
  
> Der Anbieter sollte kein Dialogfeld während der Anmeldung angezeigt werden. Wenn dieses Flag nicht festgelegt ist, kann der Anbieter ein Dialogfeld, um den Benutzer aufzufordern, nach fehlenden Konfigurationsinformationen anzeigen.
    
MAPI_DEFERRED_ERRORS 
  
> **Anmeldung** erfolgreich, möglicherweise vor Abschluss des Anmeldevorgangs zurückgeben können. 
    
PARAMETER MAPI_UNICODE 
  
> Alle Zeichenfolgen sollte im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format.
    
 _lpulcbSecurity_
  
> [in, out] Ein Zeiger auf die Größe der Struktur der Sicherheits-Anmeldeinformationen auf das durch den Parameter _LppbSecurity_ in Bytes. Bei der Eingabe muss der Wert ungleich NULL sein. Bei der Ausgabe muss der Wert 0 (null) sein. In beiden Fällen müssen die Zeiger gültig sein. 
    
 _lppbSecurity_
  
> [in, out] Ein Zeiger auf einen Zeiger auf Sicherheitsanmeldeinformationen. Bei der Eingabe muss der Wert ungleich NULL sein. Bei der Ausgabe muss der Wert 0 (null) sein. In beiden Fällen muss der Zeiger gültig sein.
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben. 
    
 _lppABLogon_
  
> [out] Ein Zeiger auf einen Zeiger auf das Objekt für den Anbieter anmelden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eine Verbindung mit einer aktiven Sitzung wurde erfolgreich hergestellt.
    
MAPI_E_FAILONEPROVIDER 
  
> Der Anbieter nicht anmelden kann, MAPI jedoch weiterhin die anderen Anbieter in der Nachrichtendienst anmelden zu der der Anbieter gehört. 
    
MAPI_E_UNCONFIGURED 
  
> Der Anbieter verfügt über nicht genügend Informationen für die Durchführung die Anmeldung. MAPI-Aufrufen des Anbieters Nachricht Service Eintrag-Funktion.
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht zur Unterstützung der Codeseite für den Client konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht konfiguriert, um Gebietsschemainformationen des Clients zu unterstützen.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld Anmeldung abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Verbindungen sind mit jedem Adressbuchanbieter im Profil der Sitzung eingerichtet, wenn ein Client die [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) -Methode aufruft. **OpenAddressBook** ruft dann des Anbieters **Logon** (Methode). 
  
Der Name der Benutzerprofildienst auf das durch den Parameter _LpszProfileName_ wird in den Zeichensatz des Client des Benutzers, wie durch die Anwesenheit oder Abwesenheit die Option MAPI_UNICODE im _UlFlags_ -Parameter angegeben angezeigt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie in der Implementierung der die **Logon** -Methode die [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode, um eine eindeutige ID oder [MAPIUID](mapiuid.md) -Struktur zu registrieren. Jedes Ihrer Objekte haben eine Eintrags-ID, die diese **MAPIUID**enthält. MAPI verwendet die **MAPIUID** , um ein Objekt mit seinen Provider übereinstimmen. Wenn ein Client die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode, um ein messaging-Benutzer öffnen aufruft, untersucht **OpenEntry** beispielsweise den **MAPIUID** Teil der Eintrags-ID, die übergeben wurde, und ordnet ihn einem **MAPIUID** registriert, indem ein Adressbuchanbieter. 
  
Wenn ein Client an Ihren Anbieter nur einmal anmeldet, möchten Sie möglicherweise eine unterschiedliche **MAPIUID** für jede Anmeldung registrieren. Registrieren eindeutige **MAPIUID** Strukturen ermöglicht MAPI ordnungsgemäß Anforderungen an die entsprechende authentifizierungsanbieterinstanz weitergeleitet. Sie möchten jedoch jeder Anmeldung-Objekt eine **MAPIUID**freigeben. In diesem Fall müssen Sie das routing verarbeiten werden selbst auf MAPI angewiesen. Weitere Informationen zum Erstellen einer **MAPIUID**finden Sie unter [Registrieren Service Provider eindeutige Bezeichner](registering-service-provider-unique-identifiers.md).
  
Das Support-Objekt, das MAPI an Ihre **Logon** -Methode im Parameter _LpMAPISup_ übergibt ermöglicht den Zugriff auf viele der Methoden in enthalten die [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle. MAPI erstellt ein Support-Objekt, das in den Typ des Anbieters angepasst ist. Wenn Sie müssen zur Anmeldung an einer zugrunde liegenden messaging-System oder Verzeichnisdienst, wenn Sie die Verbindung hergestellt wird, können Sie beispielsweise die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode zum Abrufen von Anmeldeinformationen für diese Sitzung bestimmte Anmeldung anrufen. 
  
Wenn die **Anmeldung** erfolgreich ist, müssen Sie unbedingt, dass Sie die des Unterstützungsobjekts [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode, um erhöht den Referenzzähler aufrufen. Auf diese Weise können vom Dienstanbieter, die auf den Support-Objektzeiger für den Rest der Sitzung enthalten soll. Wenn Sie diese **AddRef** -Methode nicht aufrufen, wird MAPI vom Dienstanbieter entfernen. 
  
Sie können den Namen des Profils im Parameter _LpszProfileName_ Fehlerdialogfelder, Anmeldefenster oder andere Elemente der Benutzeroberfläche übergeben einschließen. Um den Profilnamen zu verwenden, kopieren Sie sie in einen Speicher, die Sie bereitgestellt haben. 
  
Erstellen Sie ein Objekt Anmeldung und zurückkehren Sie einen Zeiger in der _LppABLogon_ -Parameter zu ihm. MAPI verwendet dieses Anmeldeobjekt tätigen von Anrufen an die Methoden in der Implementierung [IABLogon](iablogoniunknown.md) . 
  
Wenn Sie ein Kennwort bei der Anmeldung benötigen, ein Anmeldedialogfeld nur angezeigt, wenn das Flag AB_NO_DIALOG nicht festgelegt ist. Wenn der Benutzer des Anmeldevorgangs abbricht, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** klicken Sie im Dialogfeld zurückgeben Sie MAPI_E_USER_CANCEL aus **Anmelden**.
  
In der Regel bei der Adressbuch-Dienstanbieter nicht anmelden kann, MAPI wird deaktiviert den Dienst, der der fehlerhaften Anbieter angehört – d. h., MAPI versucht nicht, Verbindungen für andere Anbieter herzustellen, die mit dem Dienst für den Rest der der Sitzung gehören Lebensdauer. Wenn vom Dienstanbieter kann keine Verbindung herstellen, und Sie nicht den gesamten Dienst deaktivieren möchten, zurückgeben Sie MAPI_E_FAILONEPROVIDER oder MAPI_E_UNCONFIGURED aus. MAPI wird nicht den Dienst deaktivieren, zu dem der Anbieter gehört. 
  
Rückgabe MAPI_E_FAILONEPROVIDER, wenn ein Fehler auftritt, kann nicht schwerwiegend genug ist, um zu verhindern, dass die anderen Anbieter in der Nachrichtendienst Herstellen einer Verbindung. MAPI_E_UNCONFIGURED zurück, wenn die erforderlichen Konfigurationsdaten aus dem Profil nicht vorhanden ist und Sie ein Dialogfeld, um den Benutzer aufzufordern können nicht angezeigt werden. MAPI wird durch Aufrufen des Anbieters Nachricht Service Entry Point-Funktion mit MSG_SERVICE_CONFIGURE als Parameter _UlContext_ für dem Dienst selbst, entweder programmgesteuert konfigurieren kann oder Verwenden des Eigenschaftenfensters Antworten. Wenn die Nachricht Service Einstiegspunkt Funktion beendet wurde, MAPI, ein Wiederholungsversuch der Anmeldung. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

