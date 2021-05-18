---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9c7f62c69c7a06f7ca0e4bfddcf789cddc536ea6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309667"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert MAPI an einer Instanz eines Nachrichtenspeicheranbieters.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG FAR * lpcbSpoolSecurity,
  LPBYTE FAR * lppbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parameter

 _lpMAPISup_
  
> [in] Ein Zeiger auf das aktuelle MAPI-Unterstützungsobjekt für den Nachrichtenspeicher.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die Anmeldung des Speicheranbieters verwendet wird. Diese Zeichenfolge kann in Dialogfelder angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Sie muss im Unicode-Format vorliegen, wenn MAPI_UNICODE im  _ulFlags-Parameter festgelegt_ ist. 
    
 _cbEntryID_
  
> [in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher. Das Übergeben von **Null** in  _lpEntryID_ gibt an, dass ein Nachrichtenspeicher noch nicht ausgewählt wurde und dass Dialogfelder angezeigt werden können, in denen der Benutzer einen Nachrichtenspeicher auswählen kann. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich sein, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf des Objekts einen Fehler zur Folge haben.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format angezeigt.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Anmeldedialogfeldern. Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer zur Korrektur eines Namens oder Kennworts, zum Einfügen eines Datenträgers oder zum Ausführen anderer Aktionen aufgefordert, die zum Herstellen einer Verbindung mit dem Speicher erforderlich sind.
    
MDB_NO_MAIL 
  
> Der Nachrichtenspeicher sollte nicht zum Senden oder Empfangen von E-Mails verwendet werden. Das Flag signalisiert MAPI, den MAPI-Spooler nicht darüber zu informieren, dass dieser Nachrichtenspeicher geöffnet wird. Wenn dieses Flag festgelegt ist und der Nachrichtenspeicher eng mit einem Transportanbieter gekoppelt ist, muss der Anbieter die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) nicht aufrufen. 
    
MDB_TEMPORARY 
  
> Protokolliert den Speicher, damit Informationen programmgesteuert aus dem Profilabschnitt ohne Verwendung von Dialogfelder abgerufen werden können. Mit diesem Flag wird MAPI angewiesen, dass der Speicher nicht der Nachrichtenspeichertabelle hinzugefügt werden soll und dass der Speicher nicht dauerhaft gemacht werden kann. Wenn dieses Flag festgelegt ist, müssen Nachrichtenspeicheranbieter nicht die [IMAPISupport::ModifyProfile-Methode](imapisupport-modifyprofile.md) aufrufen. 
    
MDB_WRITE 
  
> Fordert Lese-/Schreibberechtigungen an.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), bei der sich der Nachrichtenspeicher anmelden soll. Wenn **Null** übergeben wird, wird die MAPI-Schnittstelle für den Nachrichtenspeicher ( [IMsgStore](imsgstoreimapiprop.md)) zurückgegeben. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine geeignete Schnittstelle für den Nachrichtenspeicher festgelegt werden (z. B. IID_IUnknown oder IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Ein Zeiger auf die Variable, in der der Speicheranbieter die Größe der Überprüfungsdaten im  _lppbSpoolSecurity-Parameter_ in Bytes zurückgibt. 
    
 _lppbSpoolSecurity_
  
> [out] Ein Zeiger auf den Zeiger auf die zurückgegebenen Überprüfungsdaten. Diese Überprüfungsdaten werden bereitgestellt, damit die [IMSProvider::SpoolerLogon-Methode](imsprovider-spoolerlogon.md) den MAPI-Spooler im selben Speicher wie der Nachrichtenspeicheranbieter protokollieren kann. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR-Struktur,](mapierror.md) die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf **null festgelegt** werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
 _lppMSLogon_
  
> [out] Ein Zeiger auf den Zeiger auf das Anmeldeobjekt des Nachrichtenspeichers, bei dem sich MAPI anmelden soll.
    
 _lppMDB_
  
> [out] Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt, an dem sich der MAPI-Spooler und die Clientanwendungen anmelden können.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_FAILONEPROVIDER 
  
> Dieser Anbieter kann sich nicht anmelden, aber dieser Fehler sollte den Dienst nicht deaktivieren. 
    
MAPI_E_LOGON_FAILED 
  
> Eine Anmeldesitzung konnte nicht eingerichtet werden.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. Wenn dieser Wert zurückgegeben wird, ruft MAPI die Message-Service-Einstiegspunktfunktion des Nachrichtenspeicheranbieters auf.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Locale-Informationen des Clients konfiguriert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf ist erfolgreich, der Nachrichtenspeicheranbieter verfügt jedoch über Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md). Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter zu erhalten. 
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **IMSProvider::Logon-Methode** auf, um den Großteil der Verarbeitung zu verarbeiten, die erforderlich ist, um Zugriff auf einen Nachrichtenspeicher zu erhalten. Nachrichtenspeicheranbieter überprüfen alle Benutzeranmeldeinformationen, die für den Zugriff auf einen bestimmten Speicher erforderlich sind, und geben ein Nachrichtenspeicherobjekt im  _lppMDB-Parameter_ zurück, an dem sich der MAPI-Spooler und die Clientanwendungen anmelden können. 
  
Zusätzlich zum zurückgegebenen Nachrichtenspeicherobjekt für client- und MAPI-Spooler gibt der Anbieter auch ein Anmeldeobjekt für den Nachrichtenspeicher für MAPI zurück, das beim Steuern des geöffneten Speichers verwendet werden soll. Das Anmeldeobjekt des Nachrichtenspeichers und das Nachrichtenspeicherobjekt sollten innerhalb des Nachrichtenspeicheranbieters eng verknüpft sein, damit sich beides auf das andere auswirken kann. Die Verwendung des Store-Objekts und des Anmeldeobjekts sollte identisch sein. Es sollte eine 1:1-Entsprechung zwischen dem Anmeldeobjekt und dem Storeobjekt sein, damit die Objekte so tun, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht. Die beiden Objekte sollten auch gemeinsam erstellt und gemeinsam frei werden. 
  
Das MAPI-Supportobjekt, das von MAPI erstellt und an den Anbieter im  _lpMAPISup-Parameter_ übergeben wurde, bietet Zugriff auf Funktionen in MAPI, die der Anbieter benötigt. Dazu gehören Funktionen zum Speichern und Abrufen von Profilinformationen, zum Zugreifen auf Adressbücher und so weiter. Der  _lpMAPISup-Zeiger_ kann für jeden geöffneten Speicher unterschiedlich sein. Bei der Verarbeitung von Aufrufen für einen Nachrichtenspeicher nach der Anmeldung sollte der Speicheranbieter die  _lpMAPISup-Variable_ verwenden, die für diesen Speicher spezifisch ist. Für jeden **Anmeldeaufruf,** der einen Nachrichtenspeicher öffnet und erfolgreich ein Anmeldeobjekt für den Nachrichtenspeicher erstellt, muss der Anbieter einen Zeiger auf das MAPI-Unterstützungsobjekt im Anmeldeobjekt des Speichers speichern und die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um einen Verweis für das Supportobjekt hinzuzufügen. 
  
Der  _ulUIParam-Parameter_ sollte verwendet werden, wenn der Anbieter während des Anmeldeaufrufs **Dialogfelder** präsentiert. Dialogfelder sollten jedoch nicht angezeigt werden, wenn  _ulFlags_ das MDB_NO_DIALOG enthält. Wenn eine Benutzeroberfläche aufgerufen werden muss,  _ulFlags_ dies jedoch nicht zu lässt, oder wenn aus einem anderen Grund keine Benutzeroberfläche angezeigt werden kann, sollte der Anbieter MAPI_E_LOGON_FAILED. Wenn **die Anmeldung ein** Dialogfeld anzeigt und der Benutzer die Anmeldung abbricht,  sollte der Anbieter in der Regel durch Klicken auf die Schaltfläche Abbrechen des Dialogfelds MAPI_E_USER_CANCEL. 
  
Der _lpEntryID-Parameter_  kann null sein oder auf einen unverpackten Speichereintragsbezeichner verweisen, den dieser Nachrichtenspeicher zuvor erstellt hat. Wenn  _lpEntryID_ auf einen nicht ausgepackten Eintragsbezeichner verweist, kann dieser Eintragsbezeichner von einer von mehreren Stellen stammen: 
  
- Dies kann eine Eintrags-ID sein, die der Speicheranbieter zuvor als PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) **in** den Profilabschnitt geschrieben hat.
    
- Es kann sich um eine Eintrags-ID, die der Anbieter zuvor umschlossen und an einen aufrufenden Client als **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) -Eigenschaft zurückgegeben. 
    
- Dies kann eine Eintrags-ID sein, die der Anbieter zuvor als PR_ENTRYID eines Nachrichtenspeicherobjekts **umschlossen** und an einen aufrufenden Client zurückgegeben hat. 
    
In jedem dieser Fälle ist es möglich, dass die Eintrags-ID auf einem anderen Computer als dem derzeit verwendeten erstellt wurde.
  
Wenn  _lpEntryID_ nicht **null** ist, sollte sie alle Informationen enthalten, die zum Identifizieren und Suchen des Nachrichtenspeichers erforderlich sind. Diese Informationen können Netzwerkvolumenamen, Telefonnummern, Benutzernamen und so weiter enthalten. Wenn die Verbindung mit dem Speicher nicht mithilfe der Daten in der Eintrags-ID hergestellt werden kann, sollte der Speicheranbieter ein Dialogfeld anzeigen, in dem der Benutzer den zu öffnende Speicher auswählen kann. Ein Dialogfeld kann z. B. erforderlich sein, wenn ein Server umbenannt wurde, ein Kontoname geändert wurde oder Teile des Netzwerks nicht verfügbar sind.
  
Wenn  _lpEntryID_ **null ist,** wurde der zu verwendende Nachrichtenspeicher noch nicht ausgewählt. Der Anbieter kann weiterhin auf einen Speicher zugreifen, ohne ein Dialogfeld anzuzeigen, wenn er weitere Methoden zum Angeben des Speichers unterstützt. Beispielsweise kann der Anbieter seine Initialisierungsdatei überprüfen oder bei der Konfiguration nach zusätzlichen Eigenschaften suchen, die im Profilabschnitt des Nachrichtendiensts oder des Nachrichtendiensts platziert wurden.
  
Wenn ein Anbieter findet, dass alle erforderlichen Informationen nicht im Profil enthalten sind, sollte er MAPI_E_UNCONFIGURED. MAPI wird dann die Einstiegspunktfunktion des Anbieters aufrufen, um dem Benutzer die Auswahl eines Speichers oder sogar das Erstellen eines Speichers zu ermöglichen und bei Bedarf einen Kontonamen und ein Kennwort einzugeben. MAPI erstellt automatisch einen neuen Profilabschnitt für einen neuen Speicher. Dieser neue Profilabschnitt kann temporär oder dauerhaft sein, je nachdem, wie er hinzugefügt wurde. Wenn der Speicheranbieter die **IMAPISupport::ModifyProfile-Methode** aufruft, wird der neue Profilabschnitt dauerhaft, und der Speicher wird der Liste der Nachrichtenspeicher hinzugefügt, die von der [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) zurückgegeben werden. 
  
Der  _lpInterface-Parameter_ gibt die IID der Schnittstelle an, die für das neu geöffnete Store-Objekt erforderlich ist. Das **Übergeben von null** in  _lpInterface_ gibt an, dass die SCHNITTSTELLE des MAPI-Nachrichtenspeichers, **IMsgStore**, erforderlich ist. Das Übergeben des Nachrichtenspeicherobjekts, IID_IMsgStore, gibt außerdem an, dass **IMsgStore** erforderlich ist. Wenn IID_IUnknown in  _lpInterface_ übergeben wird, sollte der Anbieter den Speicher öffnen, indem er die von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) abgeleitete Schnittstelle verwendet, die für den Anbieter am besten ist (auch hier ist dies in der Regel **IMsgStore**). Wenn IID_IUnknown übergeben wird, verwendet die aufrufende Implementierung die [IUnknown::QueryInterface-Methode,](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) um eine Schnittstelle auszuwählen, nachdem der Speicher geöffnete Vorgang erfolgreich war. 
  
Der **IMSProvider::Logon-Aufruf** sollte ausreichende Informationen zurückgeben, z. B. einen Pfad zum Speicher und Anmeldeinformationen für den Zugriff auf den Speicher, damit sich der MAPI-Spooler bei demselben Speicher anmelden kann, den der Speicheranbieter ohne Einzeigedialogfeld macht. Die  _Parameter lpcbSpoolSecurity_ und  _lppbSpoolSecurity_ werden zum Zurückgeben dieser Informationen verwendet. Der Anbieter weist den Arbeitsspeicher für diese Daten zu, indem er einen Zeiger an einen Puffer im _lpfAllocateBuffer-Parameter_ der [MSProviderInit-Funktion](msproviderinit.md) übertünft. Der Anbieter platziert die Größe dieses Puffers in _lpcbSpoolSecurity_. 
  
MapI gibt diesen Puffer frei, wenn dies der Richtige ist. Wenn die Anmeldung des MAPI-Spoolers beim Speicher allein aus den Informationen im Profilabschnitt durchgeführt werden kann, kann der Anbieter null in _lppbSpoolSecurity_ und 0 für die Größe der Informationen in _lpcbSpoolSecurity zurückgeben._ Die #A0 erfolgt als Teil eines anderen Prozesses als die Storeanmeldung. Da der Puffer, der die übergebenen Informationen enthält, zwischen Prozessen kopiert wird, befindet er sich möglicherweise nicht im Arbeitsspeicher am gleichen Speicherort für den MAPI-Spoolerprozess wie für den Speicheranbieterprozess. Daher sollte ein Anbieter keine Adressen in diesen Puffer setzen. Weitere Informationen zur Anmeldung von MAPI-Spoolern finden Sie unter [DER IMSProvider::SpoolerLogon-Methode.](imsprovider-spoolerlogon.md) 
  
Die meisten Speicheranbieter verwenden die [IMAPISession::OpenProfileSection-Methode](imapisession-openprofilesection.md) des im  _lpMAPISup-Parameter_ übergebenen Supportobjekts zum Speichern und Abrufen von Benutzeranmeldeinformationen und -optionen. **Mit OpenProfileSection** kann ein Speicheranbieter zusätzliche beliebige Informationen in einem Profilabschnitt speichern und einer bestimmten Ressource zuordnen. Ein Speicheranbieter kann beispielsweise den Benutzernamen und das Kennwort speichern, die einer Ressource zugeordnet sind, sowie alle Pfade oder sonstigen Informationen, die für den Zugriff auf diese Ressource erforderlich sind. 
  
Eigenschaften mit Eigenschaftenbezeichnern 0x6600 bis 0x67FF sind sichere Eigenschaften, die dem Anbieter zur eigenen Verwendung zum Speichern privater Daten in Profilabschnitten zur Verfügung stehen. Weitere Informationen zur Verwendung von Eigenschaften in Profilabschnittsobjekten finden Sie unter [der IProfSect : IMAPIProp-Methode.](iprofsectimapiprop.md) 
  
Zusätzlich zu privaten Daten in Eigenschaften mit Bezeichnern 0x6600 bis 0x67FF sollte der Speicheranbieter Informationen für die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft im Profilabschnitt bereitstellen. Sie sollte  PR_DISPLAY_NAME den Anzeigenamen des Anbieters selbst eingeben – eine identifizierende Zeichenfolge (z. B. "Microsoft Personal Information Store"), die Benutzern angezeigt wird, damit sie diesen Nachrichtenspeicher von anderen unterscheiden können, auf die sie möglicherweise Zugriff haben. **PR_DISPLAY_NAME** enthält in der Regel einen Servernamen, einen Benutzernamen oder einen Pfad. 
  
Einige Profilabschnittseigenschaften sind in der Nachrichtenspeichertabelle sichtbar. Andere sind während der Einrichtung, Installation und Konfiguration des MAPI-Subsystems sichtbar. Der Anbieter stellt in der Regel Informationen zu diesen sichtbaren Eigenschaften sowohl für einen neuen Profilabschnitt zur Verfügung, der noch keine gespeicherten Anmeldeinformationen oder privaten Informationen enthält, als auch, wenn er findet, dass Eigenschafteninformationen geändert wurden. Weitere Informationen zu Profilabschnitten finden Sie unter [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Nach der erfolgreichen Protokollierung für einen Benutzer und vor der Rückkehr zu MAPI sollte der Speicheranbieter das Array der Eigenschaften für die Statuszeile für die Ressource erstellen und die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aufrufen. 
  
 **Anmeldeaufrufe,** die Nachrichtenspeicher öffnen, die bereits für die aktuelle MAPI-Sitzung geöffnet sind, überspringen einen großen Teil der zuvor beschriebenen Verarbeitung. Diese Aufrufe erstellen keine Statuszeilen, geben Anmeldeobjekte des Nachrichtenspeichers zurück, rufen **AddRef** für das MAPI-Unterstützungsobjekt auf oder geben Daten für die ANMELDUNG des MAPI-Spoolers zurück. Diese Aufrufe geben S_OK zurück und geben ein Nachrichtenspeicherobjekt mit der angeforderten Schnittstelle zurück. 
  
Um solche Aufrufe zu erkennen, sollte der Anbieter eine Liste im Objekt des Nachrichtenspeicheranbieters von Speichern verwalten, die bereits für dieses Anbieterobjekt geöffnet sind. Bei der Verarbeitung **eines Anmeldeaufrufs** sollte der Anbieter diese Liste der geöffneten Speicher überprüfen und ermitteln, ob der zu verwendende Speicher bereits geöffnet ist. Wenn ja, müssen die Benutzeranmeldeinformationen nicht überprüft werden, und die Anzeige eines Dialogfelds sollte möglichst vermieden werden. Wenn Dialogfelder angezeigt werden müssen, sollte der Anbieter die zurückgegebenen Informationen überprüfen, um festzustellen, ob ein Speicher ein zweites Mal geöffnet wurde. Darüber hinaus sollte der Anbieter zu Beginn der Anrufverarbeitung mit  _lpEntryID_ auf doppelte **Öffnungen** überprüfen. 
  
Die Standardverarbeitung für **einen Anmeldeaufruf,** der auf einen geöffneten Speicher zutritt, lautet wie folgt: 
  
1. Der Speicheranbieter ruft **AddRef für** das vorhandene Speicherobjekt auf, wenn die angeforderte neue Schnittstelle mit der Schnittstelle für den vorhandenen Speicher identisch ist. Andernfalls ruft sie **QueryInterface auf,** um die neue Schnittstelle zu erhalten. Wenn der Speicher die neue Schnittstelle nicht unterstützt, sollte der Anbieter den Fehlerwert MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Der Anbieter gibt einen Zeiger auf die erforderliche Schnittstelle des vorhandenen Speicherobjekts in _lppMDB zurück._
    
3. Der Anbieter gibt **null** in _lppMSLogon zurück._
    
4. Der Anbieter sollte das Profil für das im Aufruf übergebene Supportobjekt nicht öffnen. Darüber hinaus sollte kein eindeutiger Bezeichner des Anbieters registriert, keine Statuszeile registriert oder MAPI-Spooler-Anmeldedaten zurückgeben.
    
5. Der Anbieter sollte **AddRef** nicht für das Supportobjekt aufrufen, da kein Zeiger auf das Objekt erforderlich ist. 
    
Wann immer möglich, sollten Anbieter geeignete  Fehler- und Warnungszeichenfolgen für Anmeldeanrufe zurückgeben, da dies die Benutzer erheblich erleichtert, wenn sie ermitteln, warum etwas nicht funktioniert hat. Zum Zurückgeben dieser Zeichenfolgen legt ein Anbieter die Member in der **MAPIERROR-Struktur** fest. MAPI sucht, verwendet und gibt die **MAPIERROR-Struktur** frei, wenn sie von einem Anbieter zurückgegeben wird. 
  
Der Arbeitsspeicher für diese **MAPIERROR-Struktur** sollte mithilfe des Puffers zugewiesen werden, der in  _lpfAllocateBuffer_ für den **MSProviderInit-Aufruf übergeben** wurde. **Fehlerzeichenfolgen,** die in der zurückgegebenen Struktur enthalten sind, sollten im #A0 vorliegen, wenn MAPI_UNICODE in den _Anmelde-ulFlags_ festgelegt ist. Andernfalls sollten sie im #A1 enthalten sein. 
  
Bei den meisten von der **Anmeldung** zurückgegebenen Fehlerwerten deaktiviert MAPI die Nachrichtendienste, zu denen der fehlerhafte Anbieter gehört. MAPI wird für die Lebensdauer der MAPI-Sitzung keine Anbieter aufrufen, die zu diesen Diensten gehören. Im Gegensatz  dazu deaktiviert MAPI nicht den Nachrichtendienst, zu dem der Anbieter gehört, wenn MAPI_E_FAILONEPROVIDER der Anmeldung den Fehlerwert MAPI_E_FAILONEPROVIDER zurückgibt. **Die Anmeldung** sollte MAPI_E_FAILONEPROVIDER, wenn ein Fehler auftritt, der keine Deaktivierung des gesamten Diensts während der Gesamten Sitzung garantiert. Beispielsweise kann ein Anbieter diesen Fehler zurückgeben, wenn er die Anzeige einer Benutzeroberfläche nicht zu lässt und ein erforderliches Kennwort nicht verfügbar ist. 
  
Wenn ein Anbieter MAPI_E_UNCONFIGURED der Anmeldung zurückgibt, wird die Nachrichtendiensteintragsfunktion des Anbieters von MAPI aufruft und dann die Anmeldung erneut wiederholen. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren. Wenn der Client eine Benutzeroberfläche für die Anmeldung zulassen hat, kann der Dienst sein Konfigurationseigenschaftsblatt präsentieren, damit der Benutzer Konfigurationsinformationen eingeben kann.
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md)
  
[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
  
[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MSProviderInit](msproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

