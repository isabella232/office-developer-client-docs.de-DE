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

_lpMAPISup_: [in] Zeiger auf das Supportobjekt des Transportanbieters für Rückruffunktionen innerhalb von MAPI für diese Sitzung. Dieses Objekt bleibt gültig, bis es vom Transportanbieter veröffentlicht wird.
    
_ulUIParam_: [in] Handle to the parent window of any dialog boxes or windows this method displays. Der  _ulUIParam-Parameter_ kann nicht null sein, z. B. wenn das LOGON_SETUP im  _lpulFlags-Parameter festgelegt_ ist. 
    
_lpszProfileName_: [in] Zeiger auf den Profilnamen des Benutzers. Der  _lpszProfileName-Parameter_ wird hauptsächlich verwendet, wenn ein Dialogfeld angezeigt werden muss. 
    
_lpulFlags_: [in, out] Bitmaske von Flags, die steuert, wie die Anmeldesitzung eingerichtet wird. Die folgenden Flags können für die Eingabe durch den MAPI-Spooler festgelegt werden:
    
  - LOGON_NO_CONNECT: Das Benutzerkonto hat sich bei diesem Transportanbieter für andere Zwecke als die Übertragung und den Empfang von Nachrichten anmelden. Der Transportanbieter sollte nicht versuchen, Verbindungen mit anderen Messagingsystemen herzustellen.
        
  - LOGON_NO_DIALOG: Es sollte kein Dialogfeld angezeigt werden, auch wenn die aktuell gespeicherten Benutzeranmeldeinformationen ungültig oder für die Anmeldung nicht ausreichend sind.
        
  - LOGON_NO_INBOUND: Der Transportanbieter muss nicht für den Empfang von Nachrichten initialisieren und sollte keine eingehenden Nachrichten akzeptieren. Der MAPI-Spooler kann später die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) verwenden, um den Transportanbieter zu signalisieren, die Verarbeitung eingehender Nachrichten zu aktivieren. 
        
  - LOGON_NO_OUTBOUND: Der Transportanbieter muss nicht für das Senden von Nachrichten initialisieren, da der MAPI-Spooler keine zur Verfügung stellt. Wenn eine Clientanwendung während der Komposition einer Nachricht eine Verbindung mit einem Remoteanbieter benötigt, damit sie [IXPLogon::AddressTypes-Methodenaufrufe](ixplogon-addresstypes.md) erstellen kann, sollte der Transportanbieter die Verbindung herstellen. Der MAPI-Spooler kann **TransportNotify** verwenden, um den Transportanbieter zu signalisieren, wenn ausgehende Vorgänge beginnen können. 
      
  - MAPI_UNICODE: Die übergebene Zeichenfolge für den Profilnamen ist im Unicode-Format. Wenn das \_ MAPI-UNICODE-Flag nicht festgelegt ist, hat die Zeichenfolge das ANSI-Format.
      
    Die folgenden Flags können für die Ausgabe durch den Transportanbieter festgelegt werden:
      
  - LOGON_SP_IDLE: Fordert an, dass der MAPI-Spooler häufig die [IXPLogon::Idle-Methode](ixplogon-idle.md) des Transportanbieters für die Leerlaufzeitverarbeitung aufruft. 
      
  - LOGON_SP_POLL: Fordert an, dass der MAPI-Spooler häufig die [IXPLogon::P oll-Methode](ixplogon-poll.md) für das zurückgegebene Anmeldeobjekt aufruft, um nach neuen Nachrichten zu suchen. Wenn dieses Flag nicht festgelegt ist, überprüft der MAPI-Spooler nur auf neue Nachrichten, wenn der Transportanbieter die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) verwendet, um den Spooler zu benachrichtigen, dass neue Nachrichten zu verarbeiten sind. Ein Transportanbieter wird tatsächlich nur gesendet, indem er dieses Flag nicht festlegen und den MAPI-Spooler nicht über den Nachrichteneingang informiert. 
      
  - LOGON_SP_RESOLVE: Fordert an, dass der MAPI-Spooler alle Nachrichtenadressen für Empfänger, die von diesem Transportanbieter nicht unterstützt werden, vollständig adressiert. Daher kann der Transportanbieter einen Antwortpfad für alle Empfänger erstellen.
      
  - MAPI_UNICODE: Die zurückgegebenen Zeichenfolgen in der [MAPIERROR-Struktur](mapierror.md) sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
_lppMAPIError_: [out] Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** sofern erforderlich, die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _Parameter lppMAPIError_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
_lppXPLogon_: [out] Zeiger auf den Zeiger auf das zurückgegebene Anmeldeobjekt des Transportanbieters.
    
## <a name="return-value"></a>Rückgabewert

S_OK: Der Aufruf ist erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_FAILONEPROVIDER: Dieser Anbieter kann sich nicht anmelden, aber dieser Fehler sollte den Dienst nicht deaktivieren. 
    
MAPI_E_UNCONFIGURED: Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. MAPI ruft die Nachrichtendienst-Einstiegspunktfunktion des Anbieters auf.
    
MAPI_E_UNKNOWN_CPID: Der Anbieter kann die Codeseite des Clients nicht unterstützen.
    
MAPI_E_UNKNOWN_LCID: Der Anbieter kann die Locale-Informationen des Clients nicht unterstützen.
    
MAPI_E_USER_CANCEL: Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPProvider::TransportLogon-Methode auf,** um eine Anmeldesitzung für einen Benutzer zu erstellen. 
  
Die meisten Transportanbieter verwenden die [IMAPISupport::OpenProfileSection-Methode,](imapisupport-openprofilesection.md) die mit dem Supportobjekt bereitgestellt wird, auf das der  _lpMAPISup-Parameter_ verweist, zum Speichern und Abrufen von Benutzeridentitätsinformationen, Serveradressen und Anmeldeinformationen. Mithilfe von **OpenProfileSection** kann ein Transportanbieter beliebige Informationen speichern und einer bestimmten Ressource einer Anmeldung zuordnen. Beispielsweise kann ein Anbieter **OpenProfileSection** verwenden, um den Kontonamen und das Kennwort zu speichern, die einer bestimmten Sitzung zugeordnet sind, sowie alle Servernamen oder andere erforderliche Informationen, die für den Zugriff auf Ressourcen für diese Sitzung erforderlich sind. MAPI blendet Informationen, die einer Ressource zugeordnet sind, vor dem Zugriff außerhalb des Zugriffs aus. Der über  _lpMAPISup_ zur Verfügung stellende Profilabschnitt wird vom MAPI-Spooler verwaltet, sodass daten im Zusammenhang mit diesem Benutzerkontext von Daten für andere Kontexte getrennt werden. 
  
Der Transportanbieter muss die **IUnknown::AddRef-Methode** für das Supportobjekt aufrufen und eine Kopie des Zeigers auf dieses Objekt als Teil des Anbieteranmeldeobjekts behalten. 
  
Der Profilanzeigename in  _lpszProfileName_ wird bereitgestellt, damit der Transportanbieter ihn in Fehlermeldungen oder Anmeldedialogfeldern verwenden kann. Wenn der Anbieter diesen Namen behält, muss er in den vom Anbieter zugewiesenen Speicher kopiert werden. 
  
Transportanbieter, die eng mit anderen Dienstanbietern gekoppelt sind, müssen bei der Anmeldung möglicherweise zusätzliche Arbeit tun, um die guten Anmeldeinformationen zu erstellen, die für Vorgänge zwischen Begleitanbietern erforderlich sind.
  
In der Regel werden Transportanbieter geöffnet, wenn sich der Benutzer zum ersten Mal bei einem Profil anmeldet. Da die erste Anmeldung bei einem Profil daher in der Regel vor der Anmeldung bei einem Beliebigen Nachrichtenspeicher erfolgt, ruft der MAPI-Spooler **transportLogon** in der Regel mit den in  _lpulFlags_ festgelegten LOGON_NO_INBOUND- und LOGON_NO_OUTBOUND-Flags auf. Wenn später die entsprechenden Nachrichtenspeicher in der Profilsitzung verfügbar sind, ruft der MAPI-Spooler **TransportNotify** auf, um eingehende und ausgehende Vorgänge für den Transportanbieter zu initiieren. 
  
Das Übergeben LOGON_NO_CONNECT in  _lpulFlags_ signalisiert den Offlinebetrieb des Transportanbieters. Dieses Flag gibt an, dass keine externen Verbindungen hergestellt werden sollen. Wenn der Transportanbieter keine Sitzung ohne externe Verbindung einrichten kann, sollte er einen Fehlerwert für die Anmeldung zurückgeben. 
  
Ein Transportanbieter sollte das LOGON_SP_IDLE in  _lpulFlags_ zur Initialisierungszeit festlegen, wenn es für die Verwendung von Zeit konzipiert ist, die das System ansonsten im Leerlauf verbringt. Diese Zeit wird häufig zum Verarbeiten automatischer Vorgänge verwendet, z. B. zum automatischen Herunterladen von Nachrichten, zum Herunterladen von Zeitnachrichten oder zum Senden von Zeitnachrichten. Wenn dieses Flag festgelegt ist, ruft der MAPI-Spooler **Idle** auf, wenn die Systemlaufzeit zum Initiieren solcher Vorgänge auftritt. Der #A0 aufruft **idle** nicht in festgelegten Intervallen. stattdessen wird sie nur während der echten Leerlaufzeit aufgerufen. Daher sollten Anbieter nicht davon ausgehen, wie häufig ihre **Idle-Methoden** aufgerufen werden. Anbieter, die Leerlaufzeitvorgänge unterstützen, sollten eine Konfigurationsbenutzeroberfläche dafür im Eigenschaftenblatt des Anbieters zur Verfügung stehen. 
  
Wenn die Anmeldung des Transportanbieters erfolgreich ist, sollte der Anbieter im  _lppXPLogon-Parameter_ einen Zeiger auf ein Anmeldeobjekt zurückgeben. Der MAPI-Spooler verwendet dieses Objekt für zusätzlichen Anbieterzugriff. Wenn **TransportLogon** ein Anmeldedialogfeld anzeigt und der Benutzer die  Anmeldung in der Regel abbricht, indem er im Dialogfeld auf die Schaltfläche Abbrechen klickt, sollte der Anbieter MAPI_E_USER_CANCEL. 
  
Bei den meisten von **TransportLogon** zurückgegebenen Fehlerwerten deaktiviert MAPI die Nachrichtendienste, zu denen der Anbieter gehört. MAPI wird für die restliche MAPI-Sitzung keine Anbieter aufrufen, die zu diesem Dienst gehören. Wenn **TransportLogon** hingegen den MAPI_E_FAILONEPROVIDER der Anmeldung zurückgibt, deaktiviert MAPI nicht den Nachrichtendienst, zu dem der Anbieter gehört. **TransportLogon** sollte MAPI_E_FAILONEPROVIDER, wenn ein Fehler auftritt, der keine Deaktivierung des Diensts für den Rest der Sitzung rechtfertigen würde. 
  
Wenn ein Anbieter MAPI_E_UNCONFIGURED der Anmeldung zurückgibt, wird die Nachrichtendiensteintragsfunktion des Anbieters von MAPI aufruft und dann die Anmeldung erneut wiederholen. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren. Wenn der Client eine Benutzeroberfläche für die Anmeldung zulassen hat, kann der Dienst sein Konfigurationseigenschaftsblatt präsentieren, damit der Benutzer Konfigurationsinformationen eingeben kann. 
  
Wenn der Anbieter findet, dass nicht alle erforderlichen Informationen im Profil enthalten sind, sollte er MAPI_E_UNCONFIGURED zurück, damit MAPI die Einstiegspunktfunktion des Anbieters aufruft. 
  
## <a name="see-also"></a>Siehe auch

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

