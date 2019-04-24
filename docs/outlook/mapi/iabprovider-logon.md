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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348783"
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
  
> in Ein Zeiger auf das Support Objekt des Adressbuch Anbieters.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster für das Anmeldedialogfeld, das von der **Anmelde** Methode angezeigt wird, falls zulässig. Der Parameter _ulUIParam_ enthält den Wert des Parameters mit demselben Namen, der an MAPI im vorherigen Aufruf der [MAPILogonEx](mapilogonex.md) -Funktion übergeben wurde. 
    
 _lpszProfileName_
  
> in Ein Zeiger auf den Namen des Sitzungs Profils.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Ausführung der Anmeldung steuert. Die folgenden Flags können festgelegt werden:
    
AB_NO_DIALOG 
  
> Der Anbieter sollte während der Anmeldung kein Dialogfeld anzeigen. Wenn dieses Flag nicht festgelegt ist, kann der Anbieter ein Dialogfeld anzeigen, in dem der Benutzer nach fehlenden Konfigurationsinformationen gefragt wird.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die erfolgreiche Rückgabe der **Anmeldung** , bevor der Anmeldevorgang abgeschlossen ist. 
    
MAPI_UNICODE 
  
> Alle Zeichenfolgen sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format sein.
    
 _lpulcbSecurity_
  
> [in, out] Ein Zeiger auf die Größe der Sicherheitsanmeldeinformationen, auf die durch den _lppbSecurity_ -Parameter verwiesen wird, in Bytes. Bei der Eingabe muss der Wert ungleich NULL sein. bei der Ausgabe muss der Wert NULL sein. In beiden Fällen müssen die Zeiger gültig sein. 
    
 _lppbSecurity_
  
> [in, out] Ein Zeiger auf einen Zeiger auf Sicherheitsanmeldeinformationen. Bei der Eingabe muss der Wert ungleich NULL sein. bei der Ausgabe muss der Wert NULL sein. In beiden Fällen muss der Zeiger gültig sein.
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll. 
    
 _lppABLogon_
  
> Out Ein Zeiger auf einen Zeiger auf das Anmeldeobjekt des Anbieters.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eine Verbindung mit einer aktiven Sitzung wurde erfolgreich hergestellt.
    
MAPI_E_FAILONEPROVIDER 
  
> Der Anbieter kann sich nicht anmelden, aber MAPI kann sich weiterhin bei den anderen Anbietern im Nachrichtendienst anmelden, zu dem der Anbieter gehört. 
    
MAPI_E_UNCONFIGURED 
  
> Der Anbieter verfügt nicht über genügend Informationen, um die Anmeldung abzuschließen. MAPI Ruft die Nachrichtendienst-Eintrags Funktion des Anbieters auf.
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im Anmeldedialogfeld geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Verbindungen werden mit jedem Adressbuchanbieter im Sitzungsprofil hergestellt, wenn ein Client die [IMAPISession:: openaddressbook](imapisession-openaddressbook.md) -Methode aufruft. **Openaddressbook** ruft dann die **Anmelde** Methode jedes Anbieters auf. 
  
Der Profilname, auf den durch den _lpszProfileName_ -Parameter verwiesen wird, wird im Zeichensatz des Clients des Benutzers angezeigt, der durch das vorhanden sein oder Fehlen des MAPI_UNICODE-Kennzeichens im _ulFlags_ -Parameter angegeben wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie in der Implementierung der **Anmelde** Methode die [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode auf, um einen eindeutigen Bezeichner oder eine [MAPIUID](mapiuid.md) -Struktur zu registrieren. Jedes Objekt verfügt über eine Eintrags-ID, die diese **MAPIUID**enthält. MAPI verwendet die **MAPIUID** , um ein Objekt mit seinem Anbieter abzugleichen. Wenn ein Client beispielsweise die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode aufruft, um einen Messagingbenutzer zu öffnen, unterSucht OpenEntry den **** **MAPIUID** -Teil des Eintrags Bezeichners, der übergeben wurde, und vergleicht ihn mit einem **MAPIUID** , der von einem registrierten Adressbuchanbieter. 
  
Wenn sich ein Client mehr als einmal bei Ihrem Anbieter anmeldet, können Sie für jede Anmeldung eine andere **MAPIUID** registrieren. Das Registrieren eindeutiger **MAPIUID** -Strukturen ermöglicht MAPI das ordnungsgemäße Weiterleiten von Anforderungen an die entsprechende Anbieterinstanz. Möglicherweise möchten Sie jedoch, dass jedes Logon-Objekt eine **MAPIUID**. In diesem Fall müssen Sie in der Lage sein, das Routing selbst zu behandeln, statt sich auf MAPI zu verlassen. Weitere Informationen zum Erstellen eines **MAPIUID**finden Sie unter Registrieren von [eindeutigen Bezeichnern des Dienstanbieters](registering-service-provider-unique-identifiers.md).
  
Das Unterstützungsobjekt, das MAPI an Ihre **Anmelde** Methode im _lpMAPISup_ -Parameter übergibt, ermöglicht den Zugriff auf viele der Methoden, die in der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle enthalten sind. MAPI erstellt ein Support Objekt, das an den Anbietertyp angepasst wird. Wenn Sie sich beispielsweise bei einem zugrunde liegenden Messagingsystem oder Verzeichnisdienst anmelden müssen, wenn Sie Ihre Verbindung herstellen, können Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode aufrufen, um Sicherheitsanmeldeinformationen für diese bestimmte Anmeldesitzung abzurufen. 
  
Wenn die **Anmeldung** erfolgreich ist, stellen Sie sicher, dass Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode des Support-Objekts aufrufen, um den Verweiszähler zu erhöhen. Auf diese Weise kann der Anbieter den Support Objektzeiger für den Rest der Sitzung aufbewahren. Wenn Sie diese **AddRef** -Methode nicht aufrufen, wird der Anbieter von MAPI entladen. 
  
Sie können den im Parameter _lpszProfileName_ übergebenen Profilnamen in Fehler Dialogfeldern, Anmeldebildschirmen oder anderen Benutzeroberflächen angeben. Um den Profilnamen zu verwenden, kopieren Sie ihn in den Speicher, den Sie zugeordnet haben. 
  
Erstellen Sie ein LOGON-Objekt, und geben Sie im _lppABLogon_ -Parameter einen Zeiger darauf zurück. MAPI verwendet dieses Logon-Objekt, um Aufrufe der Methoden in der [IABLogon](iablogoniunknown.md) -Implementierung durchzuführen. 
  
Wenn Sie während der Anmeldung ein Kennwort anfordern, zeigen Sie nur dann ein Anmeldedialogfeld an, wenn das AB_NO_DIALOG-Flag nicht festgelegt ist. Wenn der Benutzer den Anmeldevorgang abbricht, indem er in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld MAPI_E_USER_CANCEL von der **Anmeldung**zurückgibt.
  
Wenn sich ein Adressbuchanbieter nicht anmelden kann, deaktiviert MAPI in der Regel den Nachrichtendienst, zu dem der fehlerhafte Anbieter gehört, d. h., MAPI versucht nicht, Verbindungen für andere Anbieter herzustellen, die für den Rest der Sitzung zum Dienst gehören. Leben. Wenn Ihr Anbieter jedoch keine Verbindung herstellen kann und Sie den gesamten Dienst nicht deaktivieren möchten, geben Sie entweder MAPI_E_FAILONEPROVIDER oder MAPI_E_UNCONFIGURED zurück. Der Nachrichtendienst, zu dem der Anbieter gehört, wird von MAPI nicht deaktiviert. 
  
Geben Sie MAPI_E_FAILONEPROVIDER zurück, wenn ein Fehler auftritt, der nicht schwer genug ist, um zu verhindern, dass die anderen Anbieter im Nachrichtendienst Verbindungen herstellen. Geben Sie MAPI_E_UNCONFIGURED zurück, wenn die erforderlichen Konfigurationsinformationen im Profil fehlen, und Sie können kein Dialogfeld anzeigen, um den Benutzer aufzufordern. MAPI antwortet, indem er die Einstiegspunktfunktion des Anbieters für den Nachrichtendienst aufruft, wobei MSG_SERVICE_CONFIGURE als _ulContext_ -Parameter festgelegt ist, um dem Dienst die Möglichkeit zu geben, sich selbst programmgesteuert oder mithilfe eines Eigenschaftenblatts zu konfigurieren. Wenn die Nachrichtendienst-Einstiegspunktfunktion beendet wurde, versucht MAPI die Anmeldung erneut. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

