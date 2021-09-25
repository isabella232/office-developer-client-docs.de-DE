---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab5b98ce47e35c820227bea9d666904026fbd76e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579717"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Richtet eine Sitzung ein, in der sich eine Clientanwendung bei einem Transportanbieter anmeldet. 
  
```cpp
HRESULT TransportLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG FAR * lpulFlags,
  LPMAPIERROR FAR * lppMAPIError,
  LPXPLOGON FAR * lppXPLogon
);
```

## <a name="parameters"></a>Parameter

_lpMAPISup_: [in] Zeiger auf das Supportobjekt des Transportanbieters für Rückruffunktionen innerhalb der MAPI für diese Sitzung. Dieses Objekt bleibt gültig, bis der Transportanbieter es freigibt.
    
_ulUIParam_: [in] Handle to the parent window of any dialog boxes or windows this method displays. Der  _ulUIParam-Parameter_ kann ungleich NULL sein, z. B. wenn das flag LOGON_SETUP im  _lpulFlags-Parameter_ festgelegt ist. 
    
_lpszProfileName_: [in] Zeiger auf den Profilnamen des Benutzers. Der  _Parameter lpszProfileName_ wird in erster Linie verwendet, wenn ein Dialogfeld angezeigt werden muss. 
    
_lpulFlags_: [in, out] Bitmaske mit Flags, die steuert, wie die Anmeldesitzung eingerichtet wird. Die folgenden Flags können für die Eingabe durch den MAPI-Spooler festgelegt werden:
    
  - LOGON_NO_CONNECT: Das Benutzerkonto wird bei diesem Transportanbieter für andere Zwecke als die Übertragung und den Empfang von Nachrichten angemeldet. Der Transportanbieter sollte nicht versuchen, Verbindungen mit anderen Messagingsystemen herzustellen.
        
  - LOGON_NO_DIALOG: Es sollte kein Dialogfeld angezeigt werden, auch wenn die aktuell gespeicherten Benutzeranmeldeinformationen für die Anmeldung ungültig oder nicht ausreichend sind.
        
  - LOGON_NO_INBOUND: Der Transportanbieter muss für den Empfang von Nachrichten nicht initialisieren und sollte keine eingehenden Nachrichten annehmen. Der MAPI-Spooler kann später die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) verwenden, um dem Transportanbieter zu signalisieren, dass die Verarbeitung eingehender Nachrichten aktiviert wird. 
        
  - LOGON_NO_OUTBOUND: Der Transportanbieter muss nicht initialisiert werden, um Nachrichten zu senden, da der MAPI-Spooler keines bereitstellt. Wenn eine Clientanwendung während der Erstellung einer Nachricht eine Verbindung mit einem Remoteanbieter erfordert, damit [IXPLogon::AddressTypes-Methodenaufrufe](ixplogon-addresstypes.md) ausgeführt werden können, sollte der Transportanbieter die Verbindung herstellen. Der MAPI-Spooler kann **TransportNotify** verwenden, um dem Transportanbieter zu signalisieren, wann ausgehende Vorgänge beginnen können. 
      
  - MAPI_UNICODE: Die übergebene Zeichenfolge für den Profilnamen hat das Unicode-Format. Wenn das MAPI \_ UNICODE-Flag nicht festgelegt ist, hat die Zeichenfolge das ANSI-Format.
      
    Die folgenden Flags können für die Ausgabe durch den Transportanbieter festgelegt werden:
      
  - LOGON_SP_IDLE: Fordert an, dass der MAPI-Spooler häufig die [IXPLogon::Idle-Methode](ixplogon-idle.md) des Transportanbieters für die Leerlaufzeitverarbeitung aufruft. 
      
  - LOGON_SP_POLL: Fordert an, dass der MAPI-Spooler häufig die [IXPLogon::P oll-Methode](ixplogon-poll.md) für das zurückgegebene Anmeldeobjekt aufruft, um nach neuen Nachrichten zu suchen. Wenn dieses Kennzeichen nicht festgelegt ist, überprüft der MAPI-Spooler nur dann auf neue Nachrichten, wenn der Transportanbieter die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) verwendet, um den Spooler zu benachrichtigen, dass neue Nachrichten verarbeitet werden müssen. Ein Transportanbieter wird effektiv nur gesendet, indem er dieses Kennzeichen nicht festlegt und den MAPI-Spooler nicht über den Nachrichtenbeleg benachrichtigt. 
      
  - LOGON_SP_RESOLVE: Fordert an, dass der MAPI-Spooler in vollständige Adressen aller Nachrichtenadressen für Empfänger aufgelöst wird, die von diesem Transportanbieter nicht unterstützt werden. Daher kann der Transportanbieter einen Antwortpfad für alle Empfänger erstellen.
      
  - MAPI_UNICODE: Die zurückgegebenen Zeichenfolgen in der [MAPIERROR-Struktur](mapierror.md) haben ggf. das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
_lppMAPIError_: [out] Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur(** falls vorhanden), die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
_lppXPLogon_: [out] Zeiger auf den Zeiger auf das zurückgegebene Transportanbieter-Anmeldeobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK: Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_FAILONEPROVIDER: Dieser Anbieter kann sich nicht anmelden, aber dieser Fehler sollte den Dienst nicht deaktivieren. 
    
MAPI_E_UNCONFIGURED: Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. DIE MAPI ruft die Nachrichtendienst-Einstiegspunktfunktion des Anbieters auf.
    
MAPI_E_UNKNOWN_CPID: Der Anbieter kann die Codepage des Clients nicht unterstützen.
    
MAPI_E_UNKNOWN_LCID: Der Anbieter kann die Gebietsschemainformationen des Clients nicht unterstützen.
    
MAPI_E_USER_CANCEL: Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPProvider::TransportLogon-Methode** auf, um eine Anmeldesitzung für einen Benutzer einzurichten. 
  
Die meisten Transportanbieter verwenden die [IMAPISupport::OpenProfileSection-Methode,](imapisupport-openprofilesection.md) die mit dem Supportobjekt bereitgestellt wird, auf das der  _parameter lpMAPISup_ verweist, um Benutzeridentitätsinformationen, Serveradressen und Anmeldeinformationen zu speichern und abzurufen. Mithilfe von **OpenProfileSection** kann ein Transportanbieter beliebige Informationen speichern und einer Anmeldung zu einer bestimmten Ressource zuordnen. Beispielsweise kann ein Anbieter **OpenProfileSection** verwenden, um den Kontonamen und das Kennwort zu speichern, die einer bestimmten Sitzung zugeordnet sind, sowie alle Servernamen oder andere erforderliche Informationen, die für den Zugriff auf Ressourcen für diese Sitzung erforderlich sind. MapI blendet Informationen, die einer Ressource zugeordnet sind, aus dem externen Zugriff aus. Der profilabschnitt, der über  _lpMAPISup_ zur Verfügung gestellt wird, wird vom MAPI-Spooler verwaltet, sodass Daten im Zusammenhang mit diesem Benutzerkontext von Daten für andere Kontexte getrennt werden. 
  
Der Transportanbieter muss die **IUnknown::AddRef-Methode** für das Supportobjekt aufrufen und eine Kopie des Zeigers auf dieses Objekt als Teil des Anbieteranmeldeobjekts beibehalten. 
  
Der Profilanzeigename in  _lpszProfileName_ wird bereitgestellt, damit der Transportanbieter ihn in Fehlermeldungen oder Anmeldedialogfeldern verwenden kann. Wenn der Anbieter diesen Namen beibehält, muss er in den vom Anbieter zugewiesenen Speicher kopiert werden. 
  
Transportanbieter, die eng mit anderen Dienstanbietern gekoppelt sind, müssen möglicherweise zusätzliche Arbeit bei der Anmeldung ausführen, um die für Vorgänge zwischen Begleitanbietern erforderlichen guten Anmeldeinformationen zu ermitteln.
  
In der Regel werden Transportanbieter geöffnet, wenn sich der Benutzer zum ersten Mal bei einem Profil anmeldet. Da die erste Anmeldung bei einem Profil daher in der Regel vor der Anmeldung bei einem Nachrichtenspeicher erfolgt, ruft der MAPI-Spooler in der Regel **TransportLogon** mit den in  _lpulFlags_ festgelegten LOGON_NO_INBOUND- und LOGON_NO_OUTBOUND Flags auf. Später, wenn die entsprechenden Nachrichtenspeicher in der Profilsitzung verfügbar sind, ruft der MAPI-Spooler **TransportNotify** auf, um eingehende und ausgehende Vorgänge für den Transportanbieter zu initiieren. 
  
Das Übergeben des LOGON_NO_CONNECT Flags in  _lpulFlags_ signalisiert den Offlinebetrieb des Transportanbieters. Dieses Flag gibt an, dass keine externen Verbindungen hergestellt werden sollen. Wenn der Transportanbieter keine Sitzung ohne externe Verbindung herstellen kann, sollte er einen Fehlerwert für die Anmeldung zurückgeben. 
  
Ein Transportanbieter sollte das LOGON_SP_IDLE Flag in  _lpulFlags_ zur Initialisierungszeit festlegen, wenn die Zeit verwendet werden soll, die das System andernfalls im Leerlauf verbringt. Diese Zeit wird häufig für automatische Vorgänge verwendet, z. B. das automatische Herunterladen von Nachrichten, das Herunterladen von Zeitnachrichten oder die übermittlung von Zeitnachrichten. Wenn dieses Kennzeichen festgelegt ist, ruft der MAPI-Spooler **"Idle"** auf, wenn die Leerlaufzeit des Systems auftritt, um solche Vorgänge zu initiieren. Der MAPI-Spooler ruft **leer nicht in** festgelegten Intervallen auf. stattdessen wird es nur während der tatsächlichen Leerlaufzeit aufgerufen. Daher sollten Anbieter nicht davon ausgehen, wie häufig ihre **Idle-Methoden** aufgerufen werden. Anbieter, die Leerlaufzeitvorgänge unterstützen, sollten eine Konfigurationsbenutzeroberfläche dafür in ihrem Anbietereigenschaftenblatt bereitstellen. 
  
Wenn die Anmeldung des Transportanbieters erfolgreich ist, sollte der Anbieter im  _lppXPLogon-Parameter_ einen Zeiger auf ein Anmeldeobjekt zurückgeben. Der MAPI-Spooler verwendet dieses Objekt für zusätzlichen Anbieterzugriff. Wenn **TransportLogon** ein Anmeldedialogfeld anzeigt und der Benutzer die Anmeldung in der Regel abbricht, indem er im Dialogfeld auf die Schaltfläche **Abbrechen** klickt, sollte der Anbieter MAPI_E_USER_CANCEL zurückgeben. 
  
Bei den meisten von **TransportLogon** zurückgegebenen Fehlerwerten deaktiviert MAPI die Nachrichtendienste, zu denen der Anbieter gehört. MAPI ruft für den Rest der MAPI-Sitzung keine Anbieter auf, die zu diesem Dienst gehören. Wenn **TransportLogon** dagegen den MAPI_E_FAILONEPROVIDER Fehlerwert aus der Anmeldung zurückgibt, deaktiviert MAPI nicht den Nachrichtendienst, zu dem der Anbieter gehört. **TransportLogon** sollte MAPI_E_FAILONEPROVIDER zurückgeben, wenn ein Fehler auftritt, der das Deaktivieren des Diensts für den Rest der Sitzung nicht rechtfertigen kann. 
  
Wenn ein Anbieter MAPI_E_UNCONFIGURED aus seiner Anmeldung zurückgibt, ruft MAPI die Nachrichtendienst-Eintragsfunktion des Anbieters auf und versucht dann erneut, die Anmeldung auszuführen. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren. Wenn der Client eine Benutzeroberfläche für die Anmeldung zugelassen hat, kann der Dienst sein Konfigurationseigenschaftenblatt anzeigen, damit der Benutzer Konfigurationsinformationen eingeben kann. 
  
Wenn der Anbieter feststellt, dass sich nicht alle erforderlichen Informationen im Profil befinden, sollte er MAPI_E_UNCONFIGURED zurückgeben, damit die MAPI die Nachrichtendienst-Einstiegspunktfunktion des Anbieters aufruft. 
  
## <a name="see-also"></a>Siehe auch

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

