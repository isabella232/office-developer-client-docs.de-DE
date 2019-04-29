---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53b2733dbf38d680027dc00ecf5513f384e46660
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417308"
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

_lpMAPISup_: [in] Zeiger auf das Unterstützungsobjekt des Transportanbieters für Rückruffunktionen in MAPI für diese Sitzung. Dieses Objekt bleibt gültig, bis der Transportanbieter es freigibt.
    
_ulUIParam_: [in] Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der _ulUIParam_ -Parameter kann ungleich NULL sein, beispielsweise, wenn das LOGON_SETUP-Flag im _lpulFlags_ -Parameter festgelegt ist. 
    
_lpszProfileName_: [in] Zeiger auf den Profilnamen des Benutzers. Der _lpszProfileName_ -Parameter wird hauptsächlich verwendet, wenn ein Dialogfeld angezeigt werden muss. 
    
_lpulFlags_: [in, out] Bitmaske von Flags, die Steuern, wie die Anmeldesitzung eingerichtet wird. Die folgenden Flags können für die Eingabe durch den MAPI-Spooler festgelegt werden:
    
  - LOGON_NO_CONNECT: das Benutzerkonto meldet sich bei diesem Transportanbieter zu anderen Zwecken als dem Senden und empfangen von Nachrichten an. Der Transportanbieter sollte nicht versuchen, Verbindungen zu anderen Messagingsystemen herzustellen.
        
  - LOGON_NO_DIALOG: Es sollte kein Dialog Feld angezeigt werden, auch wenn die aktuell gespeicherten Benutzeranmeldeinformationen ungültig oder unzureichend für die Anmeldung sind.
        
  - LOGON_NO_INBOUND: der Transportanbieter muss nicht für den Empfang von Nachrichten initialisieren und eingehende Nachrichten nicht akzeptieren. Der MAPI-Spooler kann die [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode später zum Signalisieren des Transportanbieters verwenden, um die Verarbeitung eingehender Nachrichten zu ermöglichen. 
        
  - LOGON_NO_OUTBOUND: der Transportanbieter muss nicht zum Senden von Nachrichten initialisieren, da der MAPI-Spooler keines bereitstellt. Wenn eine Clientanwendung während der Zusammensetzung einer Nachricht eine Verbindung mit einem Remoteanbieter benötigt, damit die [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methodenaufrufe durchführen können, sollte der Transportanbieter die Verbindung herstellen. Der MAPI-Spooler kann **TransportNotify** verwenden, um den Transportanbieter zu signalisieren, wenn ausgehende Vorgänge beginnen können. 
      
  - MAPI_UNICODE: die übergebene Zeichenfolge für den Profilnamen ist im Unicode-Format. Wenn das MAPI\_-Unicode-Flag nicht festgelegt ist, wird die Zeichenfolge im ANSI-Format.
      
    Die folgenden Flags können für die Ausgabe vom Transportanbieter festgelegt werden:
      
  - LOGON_SP_IDLE: fordert, dass der MAPI-Spooler häufig die [IXPLogon:: idle](ixplogon-idle.md) -Methode des Transportanbieters für die Leerlaufverarbeitung aufruft. 
      
  - LOGON_SP_POLL: fordert, dass der MAPI-Spooler häufig die [IXPLogon::P-oll](ixplogon-poll.md) -Methode für das zurückgegebene Logon-Objekt aufruft, um nach Nachrichten zu suchen. Wenn dieses Flag nicht festgelegt ist, prüft der MAPI-Spooler nur, ob neue Nachrichten vorhanden sind, wenn der Transportanbieter die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode verwendet, um dem Spooler mitzuteilen, dass neue Nachrichten verarbeitet werden müssen. Ein Transportanbieter wird effektiv zu nur-senden, indem dieses Flag nicht festgelegt und der MAPI-Spooler des Nachrichtenempfangs nicht benachrichtigt wird. 
      
  - LOGON_SP_RESOLVE: fordert, dass der MAPI-Spooler alle Nachrichten Adressen für Empfänger auflöst, die von diesem Transportanbieter nicht unterstützt werden. Daher kann der Transportanbieter einen Antwortpfad für alle Empfänger erstellen.
      
  - MAPI_UNICODE: die zurückgegebenen Zeichenfolgen in der [MAPIERROR](mapierror.md) -Struktur, sofern vorhanden, im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
_lppMAPIError_: [out] Zeiger auf einen Zeiger auf die zurückgeGebene **MAPIERROR** -Struktur, sofern vorhanden, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll. 
    
_lppXPLogon_: [out] Zeiger auf den Zeiger auf das zurückgegebene Transportanbieter-Anmeldeobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK: der Aufruf war erfolgreich und hat den erwarteten Wert zurückgegeben.
    
MAPI_E_FAILONEPROVIDER: dieser Anbieter kann sich nicht anmelden, aber dieser Fehler sollte den Dienst nicht deaktivieren. 
    
MAPI_E_UNCONFIGURED: das Profil enthält nicht genügend Informationen für die Anmeldung. MAPI Ruft die Einstiegspunktfunktion des Anbieters auf.
    
MAPI_E_UNKNOWN_CPID: der Anbieter kann die Codeseite des Clients nicht unterstützen.
    
MAPI_E_UNKNOWN_LCID: der Anbieter kann die Gebietsschemainformationen des Clients nicht unterstützen.
    
MAPI_E_USER_CANCEL: der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IXPProvider:: TransportLogon** -Methode auf, um eine Anmeldesitzung für einen Benutzer einzurichten. 
  
Die meisten Transportanbieter verwenden die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode, die mit dem Support-Objekt bereitgestellt wird, auf das durch den _lpMAPISup_ -Parameter zum Speichern und Abrufen von Benutzeridentitätsinformationen, Serveradressen und Anmeldeinformationen verwiesen wird. Mithilfe von **OpenProfileSection**kann ein Transportanbieter beliebige Informationen speichern und eine Anmeldung einer bestimmten Ressource zuordnen. Ein Anbieter kann beispielsweise **OpenProfileSection** verwenden, um den Kontonamen und das Kennwort für eine bestimmte Sitzung sowie alle Servernamen oder anderen erforderlichen Informationen zu speichern, die für den Zugriff auf Ressourcen für diese Sitzung erforderlich sind. MAPI blendet Informationen aus einer Ressource außerhalb des Zugriffs aus. Der Profil Abschnitt, der über _lpMAPISup_ zur Verfügung gestellt wird, wird vom MAPI-Spooler verwaltet, sodass Daten, die sich auf diesen Benutzerkontext beziehen, von Daten für andere Contexts getrennt werden. 
  
Der Transportanbieter muss die **IUnknown:: AddRef** -Methode für das Support-Objekt aufrufen und eine Kopie des Zeigers auf dieses Objekt als Teil des Anbieter Anmelde Objekts aufbewahren. 
  
Der Profilanzeige Name in _lpszProfileName_ wird bereitgestellt, damit der Transportanbieter ihn in Fehlermeldungen oder Anmelde Dialogfeldern verwenden kann. Wenn der Anbieter diesen Namen beibehält, muss er in den vom Anbieter reservierten Speicher kopiert werden. 
  
Transport Anbieter, die eng mit anderen Dienstanbietern verbunden sind, müssen möglicherweise zusätzliche Aufgaben bei der Anmeldung ausführen, um die für Vorgänge zwischen Companion-Anbietern erforderlichen guten Anmeldeinformationen zu erstellen.
  
In der Regel werden Transportanbieter geöffnet, wenn der Benutzer sich zuerst bei einem Profil anmeldet. Da sich die erste Anmeldung an einem Profil im Allgemeinen vor der Anmeldung an einem Nachrichtenspeicher befindet, ruft der MAPI-Spooler normalerweise **TransportLogon** mit den LOGON_NO_INBOUND-und LOGON_NO_OUTBOUND-Flags auf, die in _lpulFlags_festgelegt sind. Wenn die entsprechenden Nachrichtenspeicher später in der Profil Sitzung verfügbar sind, ruft der MAPI-Spooler **TransportNotify** auf, um ein-und ausgehende Vorgänge für den Transportanbieter zu initiieren. 
  
Durch das Übergeben des LOGON_NO_CONNECT-Flags in _lpulFlags_ wird der Offlinebetrieb des Transportanbieters signalisiert. Dieses Flag gibt an, dass keine externen Verbindungen hergestellt werden sollen. Wenn der Transportanbieter keine Sitzung ohne externe Verbindung herstellen kann, sollte er einen Fehlerwert für die Anmeldung zurückgeben. 
  
Ein Transportanbieter sollte das LOGON_SP_IDLE-Flag in _lpulFlags_ zum Zeitpunkt der Initialisierung festlegen, wenn es darauf ausgelegt ist, die Zeit zu verwenden, die sonst im Leerlauf verwendet wird. Dieser Zeitpunkt wird häufig verwendet, um automatische Vorgänge wie automatisches Herunterladen von Nachrichten, Herunterladen von Nachrichten oder zeitgesteuerte Nachrichtenübermittlung zu behandeln. Wenn dieses Flag festgelegt ist, ruft der MAPI-Spooler **Leerlauf** auf, wenn die Systemleerlaufzeit eintritt, um solche Vorgänge zu initiieren. Der MAPI-Spooler ruft **Leerlauf** nicht in festgelegten Intervallen auf. Sie wird vielmehr nur während der tatsächlichen Leerlaufzeit aufgerufen. Daher sollten Anbieter nicht bei jeder Annahme darüber arbeiten, wie häufig ihre **Leerlauf** Methoden aufgerufen werden. Anbieter, die Leerlauf Vorgänge unterstützen, sollten in Ihrem Anbietereigenschaften Blatt eine Konfigurationsbenutzeroberfläche bereitstellen. 
  
Wenn die Transportanbieter Anmeldung erfolgreich ist, sollte der Anbieter im _lppXPLogon_ -Parameter einen Zeiger auf ein LOGON-Objekt zurückgeben. Der MAPI-Spooler verwendet dieses Objekt für zusätzlichen Anbieter Zugriff. Wenn **TransportLogon** ein Anmeldedialogfeld anzeigt und der Benutzer die Anmeldung normalerweise abbricht, indem er im Dialogfeld auf die Schaltfläche **Abbrechen** klickt, sollte der Anbieter MAPI_E_USER_CANCEL zurückgeben. 
  
Bei den meisten Fehlerwerten, die von **TransportLogon**zurückgegeben werden, deaktiviert MAPI die Nachrichtendienste, zu denen der Anbieter gehört. MAPI Ruft für den Rest der MAPI-Sitzung keine Anbieter auf, die zu diesem Dienst gehören. Wenn **TransportLogon** hingegen den MAPI_E_FAILONEPROVIDER-Fehlerwert aus der Anmeldung zurückgibt, wird der Nachrichtendienst, zu dem der Anbieter gehört, nicht deaktiviert. **TransportLogon** sollte MAPI_E_FAILONEPROVIDER zurückgeben, wenn ein Fehler auftritt, der die Deaktivierung des Diensts für den Rest der Sitzung nicht zulässt. 
  
Wenn ein Anbieter MAPI_E_UNCONFIGURED von seiner Anmeldung zurückgibt, ruft MAPI die Nachrichtendienst-Eintrags Funktion des Anbieters auf und wiederholt die Anmeldung. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren. Wenn der Client sich entschieden hat, eine Benutzeroberfläche für die Anmeldung zuzulassen, kann der Dienst sein Konfigurationseigenschaften Blatt anzeigen, damit der Benutzerkonfigurationsinformationen eingeben kann. 
  
Wenn der Anbieter feststellt, dass alle erforderlichen Informationen nicht im Profil sind, sollte er MAPI_E_UNCONFIGURED zurückgeben, damit MAPI die Einstiegspunktfunktion des Anbieters für den Nachrichtendienst aufruft. 
  
## <a name="see-also"></a>Siehe auch

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

