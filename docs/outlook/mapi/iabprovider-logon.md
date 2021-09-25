---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c502d3ba8b956a6c3c83bbed6e1e17d9f11fd97b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616894"
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
  
> [in] Ein Zeiger auf das Supportobjekt des Adressbuchanbieters.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für das Dialogfeld "Anmeldung", das von der **Anmeldemethode** angezeigt wird(sofern zulässig). Der  _ulUIParam-Parameter_ enthält den Wert des Parameters mit demselben Namen, der im vorherigen Aufruf der [MAPILogonEx-Funktion](mapilogonex.md) an die MAPI übergeben wurde. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Sitzungsprofils.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung durchgeführt wird. Die folgenden Flags können festgelegt werden:
    
AB_NO_DIALOG 
  
> Der Anbieter sollte während der Anmeldung kein Dialogfeld anzeigen. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Anbieter ein Dialogfeld anzeigen, in dem der Benutzer zur Eingabe fehlender Konfigurationsinformationen aufgefordert wird.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die erfolgreiche Rückgabe der **Anmeldung,** möglicherweise bevor der Anmeldevorgang abgeschlossen ist. 
    
MAPI_UNICODE 
  
> Alle Zeichenfolgen sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format vorliegen.
    
 _lpulcbSecurity_
  
> [in, out] Ein Zeiger auf die Größe der Sicherheitsanmeldeinformationsstruktur in Byte, auf die der  _Parameter "lppbSecurity"_ verweist. Bei der Eingabe muss der Wert ungleich Null sein. bei der Ausgabe muss der Wert Null sein. In beiden Fällen müssen die Zeiger gültig sein. 
    
 _lppbSecurity_
  
> [in, out] Ein Zeiger auf einen Zeiger auf Sicherheitsanmeldeinformationen. Bei der Eingabe muss der Wert ungleich Null sein. bei der Ausgabe muss der Wert Null sein. In beiden Fällen muss der Zeiger gültig sein.
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [MAPIERROR-Struktur.](mapierror.md) Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
 _lppABLogon_
  
> [out] Ein Zeiger auf einen Zeiger auf das Anmeldeobjekt des Anbieters.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eine Verbindung mit einer aktiven Sitzung wurde erfolgreich hergestellt.
    
MAPI_E_FAILONEPROVIDER 
  
> Der Anbieter kann sich nicht anmelden, die MAPI kann sich jedoch weiterhin bei den anderen Anbietern im Nachrichtendienst anmelden, zu dem der Anbieter gehört. 
    
MAPI_E_UNCONFIGURED 
  
> Der Anbieter verfügt über unzureichende Informationen, um die Anmeldung abzuschließen. DIE MAPI ruft die Nachrichtendienst-Eintragsfunktion des Anbieters auf.
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codepage des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Anmeldedialogfeld. 
    
## <a name="remarks"></a>Bemerkungen

Verbindungen werden mit jedem Adressbuchanbieter im Sitzungsprofil hergestellt, wenn ein Client die [IMAPISession::OpenAddressBook-Methode](imapisession-openaddressbook.md) aufruft. **OpenAddressBook** ruft dann die **Anmeldemethode** jedes Anbieters auf. 
  
Der Profilname, auf den der  _Parameter lpszProfileName_ verweist, wird im Zeichensatz des Clients des Benutzers angezeigt, wie durch das Vorhandensein oder Fehlen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ angegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie in der Implementierung der **Anmeldemethode** die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) auf, um einen eindeutigen Bezeichner oder eine [MAPIUID-Struktur](mapiuid.md) zu registrieren. Jedes Ihrer Objekte verfügt über einen Eintragsbezeichner, der diese **MAPIUID** enthält. DIE MAPI verwendet die **MAPIUID,** um ein Objekt mit seinem Anbieter zuzuordnen. Wenn ein Client beispielsweise die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, um einen Messagingbenutzer zu öffnen, überprüft **OpenEntry** den **MAPIUID-Teil** des übergebenen Eintragsbezeichners und gleicht ihn mit einer **MAPIUID ab, die** von einem Adressbuchanbieter registriert wurde. 
  
Wenn sich ein Client mehrmals bei Ihrem Anbieter anmeldet, können Sie für jede Anmeldung eine andere **MAPIUID** registrieren. Durch das Registrieren eindeutiger **MAPIUID-Strukturen** kann MAPI Anforderungen ordnungsgemäß an die entsprechende Anbieterinstanz weiterleiten. Möglicherweise möchten Sie jedoch, dass jedes Anmeldeobjekt eine **MAPIUID** gemeinsam verwendet. In diesem Fall müssen Sie das Routing selbst durchführen können, anstatt sich auf die MAPI zu verlassen. Weitere Informationen zum Erstellen einer **MAPIUID** finden Sie unter [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
  
Das Supportobjekt, das MAPI an Ihre **Anmeldemethode** im  _LpMAPISup-Parameter_ übergibt, bietet Zugriff auf viele der Methoden, die in der [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) enthalten sind. MAPI erstellt ein Supportobjekt, das an ihren Anbietertyp angepasst wird. Wenn Sie sich beispielsweise beim Herstellen der Verbindung bei einem zugrunde liegenden Messagingsystem oder Verzeichnisdienst anmelden müssen, können Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) aufrufen, um Sicherheitsanmeldeinformationen für diese bestimmte Anmeldesitzung abzurufen. 
  
Wenn **die Anmeldung** erfolgreich ist, müssen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) des Supportobjekts aufrufen, um die Referenzanzahl zu erhöhen. Dadurch kann ihr Anbieter den Supportobjektzeiger für den Rest der Sitzung beibehalten. Wenn Sie diese **AddRef-Methode** nicht aufrufen, entlädt MAPI den Anbieter. 
  
Sie können den im Parameter  _lpszProfileName übergebenen_ Profilnamen in Fehlerdialogfelder, Anmeldebildschirme oder andere Benutzeroberflächen einschließen. Um den Profilnamen zu verwenden, kopieren Sie ihn in den Speicher, den Sie zugewiesen haben. 
  
Erstellen Sie ein Anmeldeobjekt, und geben Sie im  _Parameter "lppABLogon"_ einen Zeiger darauf zurück. MAPI verwendet dieses Anmeldeobjekt, um Aufrufe der Methoden in Ihrer [IABLogon-Implementierung](iablogoniunknown.md) auszuführen. 
  
Wenn Sie während der Anmeldung ein Kennwort benötigen, zeigen Sie nur dann ein Anmeldedialogfeld an, wenn das AB_NO_DIALOG-Kennzeichen nicht festgelegt ist. Wenn der Benutzer den Anmeldevorgang abbricht, geben Sie in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld MAPI_E_USER_CANCEL aus der **Anmeldung** zurück.
  
Wenn sich ein Adressbuchanbieter nicht anmelden kann, deaktiviert MAPI in der Regel den Nachrichtendienst, zu dem der fehlerhafte Anbieter gehört, d. h., die MAPI versucht nicht, Verbindungen für einen der anderen Anbieter herzustellen, die für die restliche Lebensdauer der Sitzung zum Dienst gehören. Wenn Ihr Anbieter jedoch keine Verbindung herstellen kann und Sie nicht den gesamten Dienst deaktivieren möchten, geben Sie entweder MAPI_E_FAILONEPROVIDER oder MAPI_E_UNCONFIGURED zurück. Die MAPI deaktiviert nicht den Nachrichtendienst, zu dem der Anbieter gehört. 
  
Geben Sie MAPI_E_FAILONEPROVIDER zurück, wenn ein Fehler auftritt, der nicht schwerwiegend genug ist, um zu verhindern, dass die anderen Anbieter im Nachrichtendienst Verbindungen herstellen. Geben Sie MAPI_E_UNCONFIGURED zurück, wenn die erforderlichen Konfigurationsinformationen im Profil fehlen und Sie kein Dialogfeld anzeigen können, um den Benutzer aufzufordern. Die MAPI antwortet, indem sie die Nachrichtendienst-Einstiegspunktfunktion Ihres Anbieters aufruft, wobei MSG_SERVICE_CONFIGURE als  _ulContext-Parameter_ festgelegt ist, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren, entweder programmgesteuert oder mithilfe eines Eigenschaftenblatts. Wenn die Nachrichtendienst-Einstiegspunktfunktion abgeschlossen ist, versucht MAPI die Anmeldung erneut. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

