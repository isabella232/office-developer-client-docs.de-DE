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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01a8e3c479ab3ddd1be9386e033b993fda5835a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792931"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**Betrifft**: Outlook 
  
Richtet eine Sitzung, in der eine Clientanwendung eines Transportdienstes anmeldet. 
  
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

_LpMAPISup_: [in] Zeiger auf der Adressbuchhierarchie Support-Objekt für Rückruffunktionen in MAPI für diese Sitzung. Dieses Objekt bleibt gültig, bis der Adressbuchhierarchie freigegeben.
    
_UlUIParam_: [in] Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows diese Methode zeigt. Der _UlUIParam_ -Parameter kann nicht Null sein, beispielsweise wenn kennzeichnen der LOGON_SETUP im _LpulFlags_ -Parameter festgelegt ist. 
    
_LpszProfileName_: [in] Zeiger auf den Profilnamen des Benutzers. Der Parameter _LpszProfileName_ wird hauptsächlich verwendet, wenn ein Dialogfeld angezeigt werden muss. 
    
_LpulFlags_: [in, out] Bitmaske aus Flags, die steuert, wie die Sitzung eingerichtet wird. Die folgenden Kennzeichen können bei der Eingabe durch die MAPI-Warteschlange festgelegt werden:
    
  - LOGON_NO_CONNECT: Das Benutzerkonto ist für diesen Transportanbieter für andere Zwecke als Übertragung und Empfang von Nachrichten anmelden. Der Transportdienst sollten nicht versuchen, um alle Verbindungen mit anderen messaging-Systemen zu machen.
        
  - LOGON_NO_DIALOG: Kein Dialogfeld sollte angezeigt werden, auch wenn die aktuell gespeicherten Benutzeranmeldeinformationen ungültig oder für die Anmeldung nicht ausreichend sind.
        
  - LOGON_NO_INBOUND: Der Adressbuchhierarchie ist nicht erforderlich, für den Empfang von Nachrichten zu initialisieren und eingehende Nachrichten sollten nicht annehmen. Die MAPI-Warteschlange kann später verwenden die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode der Adressbuchhierarchie zum Aktivieren der Verarbeitung der eingehenden Nachricht signalisieren. 
        
  - LOGON_NO_OUTBOUND: Der Adressbuchhierarchie ist nicht erforderlich, initialisieren zum Senden von Nachrichten, die MAPI-Warteschlange eine nicht bereitstellen. Wenn eine Clientanwendung eine Verbindung zu einem remote-Anbieter während der Zusammensetzung des eine Nachricht erforderlich sind, damit es [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufgerufen werden kann, sollte der Adressbuchhierarchie die Verbindung herzustellen. **TransportNotify** können die MAPI-Warteschlange der Adressbuchhierarchie signalisieren, wenn ausgehende Vorgänge beginnen können. 
      
  - Parameter MAPI_UNICODE: Die übergebene Zeichenfolge für den Namen des Profils im Unicode-Format ist. Wenn die MAPI\_Unicode-Flag nicht festgelegt ist, die Zeichenfolge im ANSI-Format ist.
      
    Die folgenden Kennzeichen können bei der Ausgabe von der Adressbuchhierarchie festgelegt werden:
      
  - LOGON_SP_IDLE: Fordert an, dass die MAPI-Warteschlange leerlaufzeitverarbeitung häufig der Adressbuchhierarchie [IXPLogon::Idle](ixplogon-idle.md) -Methode aufrufen. 
      
  - LOGON_SP_POLL: Anforderungen, die die MAPI-Warteschlange aufrufen häufig die [IXPLogon::Poll](ixplogon-poll.md) -Methode auf das Objekt zurückgegebenen anmelden, um zu überprüfen auf neue Nachrichten. Wenn dieses Flag nicht festgelegt ist, überprüft die MAPI-Warteschlange nur für neue Nachrichten, wenn der Adressbuchhierarchie die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode verwendet, um der Warteschlange zu benachrichtigen, dass neue Nachrichten verarbeitet werden. Ein Transportdienstes wird effektiv nur senden, indem nicht dieses Flag festlegen und nicht die MAPI-Warteschlange Nachricht Eingang benachrichtigen. 
      
  - LOGON_SP_RESOLVE: Anforderungen, die in die Warteschlange MAPI aufgelöst vollständige Adressen nicht alle Nachrichtenadressen für Empfänger unterstützt von diesem Transportanbieter. Aus diesem Grund, dass der Adressbuchhierarchie für alle Empfänger einen Antwort Pfad erstellen kann.
      
  - Parameter MAPI_UNICODE: Die zurückgegebenen Zeichenfolgen in der Struktur [MAPIERROR](mapierror.md) werden, im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
_LppMAPIError_: [out] Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, sofern zutreffend, enthält Angaben zu Version, Komponente und Kontext für den Fehler. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben. 
    
_LppXPLogon_: [out] Zeiger auf den Zeiger auf das Objekt zurückgegebenen Transport Anbieter anmelden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK: Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.
    
MAPI_E_FAILONEPROVIDER: Dieser Anbieter können sich nicht anmelden, aber dieser Fehler sollten Sie den Dienst nicht deaktivieren. 
    
MAPI_E_UNCONFIGURED: Das Profil enthält nicht ausreichend Informationen für die Anmeldung ausgeführt werden. MAPI-Aufrufen des Anbieters Nachricht Service Entry Point-Funktion.
    
MAPI_E_UNKNOWN_CPID: Codepage dem Client kann nicht vom Anbieter unterstützt werden.
    
MAPI_E_UNKNOWN_LCID: Gebietsschemainformationen der Client kann nicht vom Anbieter unterstützt werden.
    
MAPI_E_USER_CANCEL: Der Benutzer den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld. 
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange die **IXPProvider::TransportLogon** -Methode aufgerufen, um eine Anmeldung für einen Benutzer einzurichten. 
  
Die meisten Transportanbieter verwenden Sie die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode mit der Support-Objekt, auf das durch den Parameter _LpMAPISup_ zum Speichern und Abrufen von Benutzeridentitätsinformationen Serveradressen und Anmeldeinformationen bereitgestellt. Mithilfe von **"OpenProfileSection"** kann beliebigen Informationen ein Transportdienstes und versenden eine Anmeldung für eine bestimmte Ressource zuordnen. Beispielsweise können ein Anbieter **"OpenProfileSection"** Sie speichern den Kontonamen und das Kennwort für eine bestimmte Sitzung und keine Servernamen oder andere erforderlichen Informationen, die für diese Sitzung zum Zugriff auf Ressourcen erforderlich sind. MAPI werden Informationen im Zusammenhang mit einer Ressource außerhalb von Access ausgeblendet. Profilabschnitt über _LpMAPISup_ zur Verfügung gestellt wird durch die MAPI-Warteschlange verwaltet, damit Daten im Zusammenhang mit diesen Benutzerkontext von Daten für andere Kontexte getrennt ist. 
  
Der Transportdienst muss rufen Sie die **IUnknown:: AddRef** -Methode für das Objekt unterstützt und behalten Sie eine Kopie des Zeigers auf dieses Objekt als Teil des Anbieters Anmeldung-Objekts. 
  
Der Anzeigenamen Profil in _LpszProfileName_ wird bereitgestellt, sodass der Adressbuchhierarchie in Fehlermeldungen oder Dialogfelder Anmeldung verwenden kann. Wenn der Anbieter dieser Name beibehält, muss er in vom Anbieter reserviert Speicher kopiert werden. 
  
Transportanbieter, die eng mit anderen Dienstanbietern gekoppelt sind möglicherweise zusätzliche Aufgaben bei der Anmeldung die guten für Vorgänge zwischen Anbietern Companion erforderlichen Anmeldeinformationen hergestellt werden.
  
In der Regel werden Transportanbieter geöffnet, wenn der Benutzer zuerst zu einem Profil anmeldet. Da die erste Anmeldung zu einem Profil daher im Allgemeinen vor der Anmeldung an alle Nachrichtenspeicher gelangt, ruft die MAPI-Warteschlange **TransportLogon** in der Regel mit der LOGON_NO_INBOUND und die LOGON_NO_OUTBOUND in _LpulFlags_festgelegten Flags. Später, wenn die entsprechende Meldung Speicher in der Sitzung Profil verfügbar sind, ruft die MAPI-Warteschlange **TransportNotify** zum ein- und ausgehenden Vorgänge für den Transportanbieter zu initiieren. 
  
Das LOGON_NO_CONNECT-Flag _LpulFlags_ Signale übergeben Offlinebetrieb von der Adressbuchhierarchie. Dieses Kennzeichen gibt an, dass keine externen Verbindungen hergestellt werden soll; Wenn der Adressbuchhierarchie eine Sitzung ohne eine externe Verbindung herstellen kann, muss er einen Fehlerwert für die Anmeldung zurückgeben. 
  
Ein Transportdienstes sollte das LOGON_SP_IDLE Flag in _LpulFlags_ bei der Initialisierung festgelegt, wenn es entwickelt wurde, zu verwenden, die das System andernfalls verbringt im Leerlauf. So lange wird häufig automatische Vorgänge wie automatische Nachricht herunterladen, ein Timeout aufgetreten Nachricht herunterladen, oder ein Timeout aufgetreten-Nachrichtenübermittlung behandeln. Wenn dieses Flag festgelegt ist, ruft die MAPI-Warteschlange **im Leerlauf** , wenn im Leerlauf Systemzeit tritt auf, um diese Vorgänge zu initiieren. Die MAPI-Warteschlange wird nicht **im Leerlauf** in festgelegten Intervallen aufgerufen. Stattdessen wird er nur während der Leerlaufzeit true aufgerufen. Anbieter sollte daher nicht funktionieren, auf alle Annahme darüber, wie häufig ihre Methoden **im Leerlauf** aufgerufen werden. Anbieter, die Leerlaufzeit Operationen unterstützen sollte eine Benutzeroberfläche für die Konfiguration dafür in ihren Anbieter-Eigenschaftenfenster bereitstellen. 
  
Wenn die Anmeldung des Transport erfolgreich ist, sollte der Anbieter im _LppXPLogon_ -Parameter einen Zeiger zurückzugeben auf ein Logon-Objekt. Die MAPI-Warteschlange wird dieses Objekt für den Anbieter für zusätzliche Zugriff verwenden. Wenn **TransportLogon** das Dialogfeld Anmeldung zeigt und der Benutzer Anmeldung in der Regel abbricht durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld sollte der Anbieter MAPI_E_USER_CANCEL zurückgegeben. 
  
Für die meisten Fehlerwerte von **TransportLogon**zurückgegeben deaktiviert MAPI die Message-Dienste zu denen der Anbieter gehört. MAPI rufen keine Anbieter, die zu diesem Dienst für den Rest der MAPI-Sitzung gehören. Im Gegensatz dazu gibt **TransportLogon** den Fehlerwert MAPI_E_FAILONEPROVIDER von dessen Anmeldung wird MAPI nicht den Dienst deaktiviert zu dem der Anbieter gehört. **TransportLogon** sollte MAPI_E_FAILONEPROVIDER zurückgegeben, wenn ein Fehler auftritt, der keine Garantie dafür ist das Deaktivieren des Dienstes für den Rest der Sitzung. 
  
Wenn ein Anbieter von dessen Anmeldung MAPI_E_UNCONFIGURED zurückgibt, wird MAPI Aufrufen des Anbieters Nachricht Service Eintrag-Funktion und wiederholen Sie die Anmeldung. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext aus, um dem Dienst selbst konfigurieren kann. Wenn der Client sich entschieden hat, um eine Benutzeroberfläche für die Anmeldung zu ermöglichen, kann der Dienst das Eigenschaftenblatt Konfiguration darstellen, damit der Benutzer Informationen eingeben kann. 
  
Wenn der Anbieter, dass alle erforderliche Informationen ist nicht im Profil feststellt, sollte MAPI_E_UNCONFIGURED zurückgegeben werden, damit MAPI des Anbieters Nachricht Service Entry Point-Funktion aufruft. 
  
## <a name="see-also"></a>Siehe auch

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

