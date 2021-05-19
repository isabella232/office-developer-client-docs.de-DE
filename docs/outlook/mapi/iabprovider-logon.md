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
  
Stellt eine Verbindung mit einer aktiven Sitzung fest.
  
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
  
> [in] Ein Zeiger auf das Supportobjekt des Adressbuchanbieters.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster für das Anmeldedialogfeld, das von der **Logon-Methode** angezeigt wird, sofern zulässig. Der  _ulUIParam-Parameter_ enthält den Wert des Parameters mit demselben Namen, der im vorherigen Aufruf der [MAPILogonEx-Funktion](mapilogonex.md) an MAPI Übergeben wurde. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Sitzungsprofils.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
AB_NO_DIALOG 
  
> Der Anbieter sollte während der Anmeldung kein Dialogfeld anzeigen. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Anbieter ein Dialogfeld anzeigen, in dem der Benutzer zur Eingabe fehlender Konfigurationsinformationen aufgefordert wird.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **die erfolgreiche** Rückgabe der Anmeldung, möglicherweise bevor der Anmeldevorgang abgeschlossen ist. 
    
MAPI_UNICODE 
  
> Alle Zeichenfolgen sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format vorliegen.
    
 _lpulcbSecurity_
  
> [in, out] Ein Zeiger auf die Größe der Sicherheitsanmeldeinformationenstruktur in Bytes, auf die der  _lppbSecurity-Parameter_ verweist. Bei der Eingabe muss der Wert ungleich Null sein. bei der Ausgabe muss der Wert null sein. In beiden Fällen müssen die Zeiger gültig sein. 
    
 _lppbSecurity_
  
> [in, out] Ein Zeiger auf einen Zeiger auf Sicherheitsanmeldeinformationen. Bei der Eingabe muss der Wert ungleich Null sein. bei der Ausgabe muss der Wert null sein. In beiden Fällen muss der Zeiger gültig sein.
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [MAPIERROR-Struktur.](mapierror.md) Der  _Parameter lppMAPIError_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
 _lppABLogon_
  
> [out] Ein Zeiger auf einen Zeiger auf das Anmeldeobjekt des Anbieters.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eine Verbindung zu einer aktiven Sitzung wurde erfolgreich hergestellt.
    
MAPI_E_FAILONEPROVIDER 
  
> Der Anbieter kann sich nicht anmelden, aber MAPI kann sich weiterhin bei den anderen Anbietern im Nachrichtendienst anmelden, zu dem der Anbieter gehört. 
    
MAPI_E_UNCONFIGURED 
  
> Der Anbieter verfügt über nicht ausreichende Informationen, um die Anmeldung abschließen zu können. MAPI ruft die Nachrichtendiensteintragsfunktion des Anbieters auf.
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Locale-Informationen des Clients konfiguriert.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Anmeldedialogfeld. 
    
## <a name="remarks"></a>Hinweise

Verbindungen werden mit jedem Adressbuchanbieter im Sitzungsprofil hergestellt, wenn ein Client die [IMAPISession::OpenAddressBook-Methode](imapisession-openaddressbook.md) aufruft. **OpenAddressBook** ruft dann die Anmeldemethode jedes **Anbieters** auf. 
  
Der Profilname, auf den der  _lpszProfileName-Parameter_ verweist, wird im Zeichensatz des Clients des Benutzers angezeigt, wie durch das Vorhandensein oder Fehlen des MAPI_UNICODE-Flag im  _ulFlags-Parameter_ angegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie in der Implementierung der **Logon-Methode** die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) auf, um einen eindeutigen Bezeichner oder eine [MAPIUID-Struktur zu](mapiuid.md) registrieren. Jedes Ihrer Objekte verfügt über einen Eintragsbezeichner, der diese **MAPIUID enthält.** MAPI verwendet die **MAPIUID,** um einem Objekt mit seinem Anbieter zu entsprechen. Wenn ein Client beispielsweise die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, um einen Messagingbenutzer zu öffnen, untersucht **OpenEntry** den **MAPIUID-Teil** der Eingabe-ID, der übergeben wurde, und passt ihn mit einer **MAPIUID** ab, die von einem Adressbuchanbieter registriert wurde. 
  
Wenn sich ein Client mehr als einmal bei Ihrem Anbieter anmeldet, sollten Sie für jede Anmeldung eine andere **MAPIUID** registrieren. Durch das Registrieren **eindeutiger MAPIUID-Strukturen** kann MAPI Anforderungen ordnungsgemäß an die entsprechende Anbieterinstanz weiterrouten. Möglicherweise möchten Sie jedoch, dass jedes Anmeldeobjekt eine **MAPIUID gemeinsam verwendet.** In diesem Fall müssen Sie in der Lage sein, das Routing selbst zu verarbeiten, anstatt sich auf MAPI zu verlassen. Weitere Informationen zum Erstellen einer **MAPIUID** finden Sie unter [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
  
Das Supportobjekt, das MAPI an Ihre **Logon-Methode** im  _lpMAPISup-Parameter_ übergibt, bietet Zugriff auf viele der Methoden, die in der [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) enthalten sind. MAPI erstellt ein Supportobjekt, das an Ihren Anbietertyp angepasst ist. Wenn Sie sich beispielsweise beim Herstellen der Verbindung bei einem zugrunde liegenden Messagingsystem oder Verzeichnisdienst anmelden müssen, können Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) aufrufen, um Sicherheitsanmeldeinformationen für diese bestimmte Anmeldesitzung abzurufen. 
  
Wenn **die Anmeldung** erfolgreich ist, stellen Sie sicher, dass Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) des Supportobjekts aufrufen, um die Referenzanzahl zu erhöhen. Auf diese Weise kann ihr Anbieter den Supportobjektzeiger für den Rest der Sitzung halten. Wenn Sie diese **AddRef-Methode nicht** aufrufen, wird ihr Anbieter von MAPI entladen. 
  
Sie können den im  _lpszProfileName-Parameter_ übergebenen Profilnamen in Fehlerdialogfelder, Anmeldebildschirme oder andere Benutzeroberflächen integrieren. Um den Profilnamen zu verwenden, kopieren Sie ihn in den speicher, den Sie zugewiesen haben. 
  
Erstellen Sie ein Anmeldeobjekt, und geben Sie einen Zeiger auf das Objekt im  _lppABLogon-Parameter_ zurück. MAPI verwendet dieses Anmeldeobjekt, um Aufrufe der Methoden in Ihrer [IABLogon-Implementierung zu](iablogoniunknown.md) machen. 
  
Wenn Sie während der Anmeldung ein Kennwort benötigen, zeigen Sie ein Anmeldedialogfeld nur an, wenn AB_NO_DIALOG nicht festgelegt ist. Wenn der Benutzer den Anmeldevorgang abbricht,  geben Sie in der Regel durch Klicken auf die Schaltfläche Abbrechen im Dialogfeld die MAPI_E_USER_CANCEL **Von Logon zurück.**
  
Wenn sich ein Adressbuchanbieter nicht anmelden kann, deaktiviert MAPI in der Regel den Nachrichtendienst, zu dem der fehlerhafte Anbieter gehört, d. h. MAPI versucht nicht, Verbindungen für einen der anderen Anbieter herzustellen, die während der restlichen Sitzungsdauer zum Dienst gehören. Wenn Ihr Anbieter jedoch keine Verbindung herstellen kann und Sie den gesamten Dienst nicht deaktivieren möchten, geben Sie entweder MAPI_E_FAILONEPROVIDER oder MAPI_E_UNCONFIGURED. MAPI deaktiviert nicht den Nachrichtendienst, zu dem der Anbieter gehört. 
  
Geben MAPI_E_FAILONEPROVIDER zurück, wenn ein Fehler auftritt, der nicht schwerwiegend genug ist, um zu verhindern, dass die anderen Anbieter im Nachrichtendienst Verbindungen herstellen. Geben MAPI_E_UNCONFIGURED zurück, wenn die erforderlichen Konfigurationsinformationen im Profil fehlen und Sie kein Dialogfeld anzeigen können, um den Benutzer zur Eingabeaufforderung aufforderen. MAPI antwortet, indem die Einstiegspunktfunktion ihres Anbieters mit MSG_SERVICE_CONFIGURE als  _ulContext-Parameter_ festgelegt wird, um dem Dienst die Möglichkeit zu geben, sich entweder programmgesteuert oder mithilfe eines Eigenschaftenblatts zu konfigurieren. Nach Abschluss der Funktion für den Nachrichtendiensteintragspunkt wird die Anmeldung von MAPI noch nicht abgeschlossen. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

