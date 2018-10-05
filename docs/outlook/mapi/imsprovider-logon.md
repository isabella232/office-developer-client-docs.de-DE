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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386565"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolle MAPI an eine Instanz der Anbieter eine Nachricht.
  
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
  
> [in] Ein Zeiger auf den aktuellen MAPI unterstützt Objekt für den Nachrichtenspeicher.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf eine Zeichenfolge mit dem Namen des Profils, das für die Anmeldung des Store verwendet wird. Diese Zeichenfolge kann in Dialogfeldern angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Es muss im Unicode-Format sein, wenn die Option MAPI_UNICODE im _UlFlags_ -Parameter festgelegt ist. 
    
 _cbEntryID_
  
> [in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher. Übergeben von **null** in _LpEntryID_ gibt an, dass ein Nachrichtenspeicher noch nicht ausgewählt wurde und Dialogfelder, mit denen den Benutzer die Auswahl ein Nachrichtenspeichers präsentiert werden können. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf ist zulässig, erfolgreich ausgeführt werden kann, auch wenn das zugrunde liegende Objekt nicht an die Implementierung der aufrufenden verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf für das Objekt ein Fehler ausgelöst.
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn der Parameter MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Dialogfeldern für die Anmeldung. Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Flag nicht festgelegt ist, kann der Nachricht Speicheranbieter fordert den Benutzer an den richtigen einen Namen oder das Kennwort, das zum Einfügen von eines Datenträgers oder andere Aktionen auszuführen, die Verbindung zu den Speicher erforderlich sind.
    
MDB_NO_MAIL 
  
> Der Nachrichtenspeicher sollte nicht für das Senden oder Empfangen von e-Mail verwendet werden. Das Flag signalisiert MAPI nicht für der MAPI-Warteschlange benachrichtigen, dass dieses Nachrichtenspeichers geöffnet wird. Wenn dieses Attribut festgelegt, und der Nachrichtenspeicher ist eng mit eines Transportdienstes gekoppelt, muss der Anbieter nicht die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode aufrufen. 
    
MDB_TEMPORARY 
  
> Protokolle für den Speicher, sodass Informationen aus dem Profilabschnitt programmgesteuert abgerufen werden kann verwenden, ohne Dialogfelder. Dieses Kennzeichen weist MAPI, dass der Speicher ist nicht für die Nachricht Store-Tabelle hinzugefügt werden und der Speicher permanent hergestellt werden kann. Wenn dieses Flag festgelegt ist, müssen Nachricht Anbieter nicht die [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) -Methode aufrufen. 
    
MDB_WRITE 
  
> Anfragen Lese-/Schreibberechtigung.
    
 _lpInterface_
  
> [in] Ein Zeiger auf der Benutzeroberfläche IID (Identifier) für den Nachrichtenspeicher anmelden. Übergeben von **null** gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ( [IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird. Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher (beispielsweise IID_IUnknown oder IID_IMAPIProp) festgelegt werden. 
    
 _lpcbSpoolSecurity_
  
> [out] Ein Zeiger auf die Variable, die in der Speicheranbieter die Größe in Bytes, der im Parameter _LppbSpoolSecurity_ Validierungsdaten zurückgibt. 
    
 _lppbSpoolSecurity_
  
> [out] Ein Zeiger auf den Zeiger auf das zurückgegebene Überprüfungsdaten. Diese Überprüfungsdaten werden bereitgestellt, sodass die [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) -Methode die MAPI-Warteschlange an den gleichen Speicher als den Anbieter für die Nachricht anmelden anmelden kann. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [MAPIERROR](mapierror.md) Struktur, falls vorhanden, die Angaben zu Version, Komponente und Kontext für einen Fehler enthält. Der Parameter _LppMAPIError_ kann auf **null** festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben. 
    
 _lppMSLogon_
  
> [out] Ein Zeiger auf den Zeiger auf die Nachricht speichern Objekt für die MAPI anmelden anmelden.
    
 _lppMDB_
  
> [out] Ein Zeiger auf den Zeiger auf die Nachricht speichern-Objekt für die MAPI-Warteschlange und Clientanwendungen anmelden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_FAILONEPROVIDER 
  
> Diesen Anbieter können sich nicht anmelden, aber dieser Fehler sollten Sie den Dienst nicht deaktivieren. 
    
MAPI_E_LOGON_FAILED 
  
> Eine Sitzung konnte nicht hergestellt werden.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht ausreichend Informationen für die Anmeldung für die Durchführung. Wenn dieser Wert zurückgegeben wird, ruft MAPI-Funktion die Nachricht Speicheranbieter Messagingdiensts Eintrag.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht zur Unterstützung der Codeseite für den Client konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht konfiguriert, um Gebietsschemainformationen des Clients zu unterstützen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachricht Speicheranbieter hat Fehlerinformationen verfügbar. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md). Wenn Sie die Fehlerinformationen vom Anbieter erhalten möchten, rufen Sie die [IMAPISession::GetLastError](imapisession-getlasterror.md) -Methode. 
    
## <a name="remarks"></a>Hinweise

MAPI-Aufrufen die **IMSProvider::Logon** -Methode dazu die Mehrzahl der Verarbeitung erforderlich sind, um Zugriff auf einen Nachrichtenspeicher zu erhalten. Nachricht Anbieter Überprüfen von Anmeldeinformationen erforderlich sind, um Zugriff auf einen bestimmten Speicher und ein Message Store-Objekt zurückzugeben, der _LppMDB_ -Parameter, der die MAPI-Warteschlange und Clientanwendungen anmelden können. 
  
Zusätzlich zu den zurückgegebenen Message Store-Objekts für Client- und MAPI-Warteschlange verwendet gibt den Anbieter auch ein Message Store Anmeldung-Objekt für die MAPI zum Steuern des geöffneten Speichers verwenden. Message Store Anmeldung-Objekts und Message Store-Objekts sollte eng innerhalb der Nachricht Informationsdienst verknüpft werden, sodass jede der anderen auswirken kann. Die Verwendung von das Store-Objekt und das Anmeldeobjekt sollten identisch sein. So, dass die Objekte fungieren, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht sollte eine 1: 1-Beziehung zwischen der Anmeldung-Objekt und das Store-Objekt sein. Zwei Objekte sollten auch zusammen und freigegebenen zusammen erstellt werden. 
  
Das MAPI-Support-Objekt von MAPI erstellt und an den Anbieter in der _LpMAPISup_ -Parameter übergebene bietet Zugriff auf Funktionen in MAPI, die der Anbieter erforderlich sind. Dazu gehören Funktionen, die zu speichern und Abrufen von Profilinformationen, Zugriff auf Adressbücher und so weiter. Der Mauszeiger _LpMAPISup_ kann für jeden Speicher unterschiedlich sein, das geöffnet wird. Während der Verarbeitung für einen Nachrichtenspeicher nach der Anmeldung aufruft, sollten Speicheranbieter die Variable _LpMAPISup_ verwenden, die speziell für diesen Speicher ist. Für jeden Anruf **Anmeldung** , die einen Nachrichtenspeicher öffnet und erfolgreich abgeschlossen wird, bei der Erstellung einer Nachricht Store Anmeldung-Objekt der Anbieter muss einen Zeiger auf das MAPI-Support-Objekt im Speicher Anmeldung Objekt speichern und muss die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode zum Hinzufügen eines Verweises für aufrufen das Objekt unterstützt. 
  
Der Parameter _UlUIParam_ sollte verwendet werden, wenn der Anbieter während des Anrufs **Anmeldung** Dialogfelder angezeigt. Dialogfelder sollte jedoch nicht angezeigt werden, wenn _UlFlags_ das MDB_NO_DIALOG-Flag enthält. Wenn eine Benutzeroberfläche aufgerufen werden muss, aber _UlFlags_ nicht zulassen oder einem anderen Grund eine Benutzeroberfläche angezeigt werden kann, sollte der Anbieter MAPI_E_LOGON_FAILED zurückgegeben. Wenn **Anmeldung** zeigt ein Dialogfeld an, und der Benutzer die Anmeldung abbricht, sollte in der Regel durch Klicken auf das Dialogfeld Schaltfläche **Abbrechen** des Anbieters MAPI_E_USER_CANCEL zurückgegeben werden. 
  
Der Parameter _LpEntryID_ kann entweder **null** sein oder zeigen Sie auf eine allein stehenden Store Eintrags-ID, die diese Meldung speichern zuvor erstellt haben. Wenn _LpEntryID_ auf einen Bezeichner allein stehenden Eintrag zeigt, kann die Eintrags-ID aus eine der verschiedenen Orten stammen: 
  
- Eine Eintrags-ID kann sein, die Speicheranbieter zuvor eingeschlossen und in den Profilabschnitt als Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) geschrieben haben.
    
- Eine Eintrags-ID kann sein, die der Anbieter zuvor eingeschlossen und an einen aufrufenden Client als Eigenschaft **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) zurückgegeben. 
    
- Es kann eine Eintrags-ID sein, die der Anbieter zuvor eingeschlossen und an einen aufrufenden Client als die **PR_ENTRYID** -Eigenschaft des Store-Objekt "Message" zurückgegeben. 
    
In einen dieser Fälle ist es möglich, dass die Eintrags-ID auf einem anderen Computer als die aktuell verwendeten erstellt wurde.
  
Wenn _LpEntryID_ nicht **null**ist, sollten sie alle Informationen zum Identifizieren und Auffinden des Nachrichtenspeichers benötigt enthalten. Diese Informationen kann Volume Netzwerknamen, Rufnummern, Benutzerkontonamen usw. enthalten. Wenn die Verbindung mit den Speicher mit den Daten in die Eintrags-ID festgelegt werden kann, sollte der Anbieter ein Dialogfeld angezeigt, die dem Benutzer ermöglicht, wählen Sie den Speicher geöffnet werden soll. Ein Dialogfeld wäre erforderlich, zum Beispiel ein Server umbenannt wurde, ein Kontonamen geändert wurde oder Teile des Netzwerks sind nicht verfügbar.
  
Wenn _LpEntryID_ **null**ist, hat der Nachrichtenspeicher verwenden Sie noch nicht ausgewählt. Der Anbieter kann weiterhin einen Speicher zugreifen, ohne dass ein Dialogfeld angezeigt, wenn weitere Methoden zum Angeben der Speichers unterstützt. Beispielsweise der Anbieter seine Initialisierungsdatei überprüfen kann, oder es kann Suchen nach zusätzlichen Eigenschaften, die an den oder die Nachricht des Dienstes Profilabschnitt an der Konfiguration vom abgelegt wurden.
  
Wenn ein Anbieter, dass alle erforderliche Informationen ist nicht im Profil feststellt, sollte MAPI_E_UNCONFIGURED zurückgegeben werden. MAPI ruft dann den Anbieter Nachricht Service Eintrag Point-Funktion zum Aktivieren des Benutzers einen Speicher auswählen, oder sogar zu erstellen und benötigt, um einen Kontonamen und ein Kennwort, als einzugeben. MAPI erstellt automatisch einen neuen Profilabschnitt für einen neuen Speicher. In diesem Profilabschnitt der neuen möglicherweise temporär oder dauerhaft, je nachdem, wie er hinzugefügt wurde. Wenn der Anbieter die **IMAPISupport::ModifyProfile** -Methode aufruft, der neuen Profilabschnitt dauerhaft entfernt wird, und der Speicher wird hinzugefügt, um die Liste der Informationsspeicher, die von der [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode zurückgegeben. 
  
Der _LpInterface_ -Parameter gibt die ID der Schnittstelle für die neu geöffnete Store-Objekt erforderlich. Übergeben von **null** in _LpInterface_ gibt an, dass die MAPI-Nachricht Store Schnittstelle **IMsgStore**, erforderlich ist. Übergeben das Objekt "Message" Store, IID_IMsgStore, gibt, dass **IMsgStore** erforderlich ist. Wenn IID_IUnknown _LpInterface_übergeben wird, sollte der Anbieter den Speicher öffnen Sie mithilfe der jeweilige Schnittstelle abgeleitet [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) ist am besten für den Anbieter (in diesem Fall ist dies in der Regel **IMsgStore**). Wenn IID_IUnknown übergeben wird, verwendet die aufrufende Implementierung die [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode, eine Schnittstelle auszuwählen, nachdem der Vorgang zum Öffnen von Store erfolgreich war. 
  
Der Anruf **IMSProvider::Logon** sollte über ausreichend Informationen, wie beispielsweise einen Pfad zu den Speicher und die Anmeldeinformationen für den Zugriff auf den Speicher, damit die MAPI-Warteschlange an den gleichen Speicher, die Speicheranbieter ausführt, ohne dass ein Dialogfeld anmelden können zurückgegeben werden. Die Parameter _LpcbSpoolSecurity_ und _LppbSpoolSecurity_ werden verwendet, um diese Informationen zurückzugeben. Der Anbieter weist den Speicher für diese Daten, indem Sie einen Zeiger auf einen Puffer in die [MSProviderInit](msproviderinit.md) -Funktion _LpfAllocateBuffer_ -Parameter übergeben; der Anbieter platziert die Größe dieses Puffers in _LpcbSpoolSecurity_. 
  
MAPI gibt dieser Puffer bei Bedarf frei. Wenn die MAPI-Warteschlange melden Sie sich an den Speicher von den Informationen im Profilabschnitt allein durchgeführt werden kann, kann der Anbieter in _LppbSpoolSecurity_ und 0 für die Informationen Größe in _LpcbSpoolSecurity_null zurück. Die MAPI-Warteschlange Anmeldung tritt im Rahmen von einem anderen Prozess als die Anmeldung Store; Da der Puffer, der die übergebene Informationen enthält, zwischen Prozessen kopiert Ruft ab, nicht im Arbeitsspeicher am selben Speicherort für den MAPI-Warteschlange Prozess wie bei der Speichervorgang Anbieter wird möglicherweise. Aus diesem Grund sollten kein Anbieter Adressen in dieser Puffer eingefügt. Weitere Informationen zu MAPI-Warteschlange Anmeldung finden Sie unter der [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) -Methode. 
  
Die meisten Anbieter verwenden die [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) -Methode des im Parameter _LpMAPISup_ zum Speichern und Abrufen von Benutzeranmeldeinformationen und Optionen übergebenen Support-Objekts. **"OpenProfileSection"** können einen Anbieter anmelden zum Speichern beliebiger Zusatzinformationen in einem Profilabschnitt, und ordnen Sie ihm eine bestimmte Ressource. Ein Anbieter anmelden kann beispielsweise den Benutzernamen und das Kennwort zugeordnet einer Ressource und Pfade oder andere Informationen, die für diese Ressource Zugriff auf Speichern. 
  
Eigenschaften mit Eigenschaftenbezeichner 0x6600 über 0x67FF sind sicheren Eigenschaften an den Anbieter zur eigenen Verwendung zum Speichern privater Daten im Profil Abschnitte zur Verfügung. Weitere Informationen zu den Verwendungsmöglichkeiten von Eigenschaften im Benutzerprofil Section-Objekten, finden Sie unter der [IProfSect: IMAPIProp](iprofsectimapiprop.md) Methode. 
  
Zusätzlich zu privaten Daten in Eigenschaften mit Bezeichnern 0x6600 über 0x67FF sollten Speicheranbieter Informationen für die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in einem Profilabschnitt bereitstellen. Sie sollten in **PR_DISPLAY_NAME** den Anzeigenamen des Anbieters selbst – eine Zeichenfolge zur Identifizierung (z. B. "Microsoft Personal Information Store"), die Benutzern angezeigt werden, damit sie dieses Nachrichtenspeichers von anderen unterscheiden können, sie möglicherweise Zugriff haben An. **PR_DISPLAY_NAME** enthält häufig Servernamen, den Namen des Benutzerkontos oder den Pfad. 
  
Einige im Abschnitt Benutzerprofileigenschaften sind in der Nachricht Store Tabelle angezeigt. andere Benutzer werden während des Setups, Installation und Konfiguration des MAPI-Subsystems angezeigt. Der Anbieter enthält in der Regel Informationen für diese sichtbaren Eigenschaften für einen neuen Profilabschnitt, der noch enthält keine gespeicherten Anmeldeinformationen und privaten Informationen, und wenn es findet, dass Eigenschaftsinformationen geändert hat. Weitere Informationen über Profil Abschnitte finden Sie unter [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Nach der erfolgreichen Anmeldung eines Benutzers und vor der Rückgabe MAPI, sollte der Anbieter das Array von Eigenschaften für die Statuszeile für die Ressource zu erstellen und die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aufzurufen. 
  
 **Anmeldung** -Anrufe, die Nachrichtenspeicher zu öffnen, die bereits für die aktuelle MAPI-Sitzung geöffnet sind überspringen Großteil der Verarbeitung weiter oben beschrieben. Bei diesen anrufen führen Sie nicht Status Zeilen erstellen, Message Store Anmeldung Objekte zurückgeben, aufrufen, **AddRef** für das MAPI-Support-Objekt oder Daten für die MAPI-Warteschlange Anmeldung zurück. Bei diesen anrufen S_OK zurück und eine Nachricht Store-Objekt mit der angeforderten Schnittstelle zurück. 
  
Um solcher Anrufe zu erkennen, sollte der Anbieter eine Liste in Message-Speicher-Anbieter-Objekts der Speicher für dieses Anbieterobjekt bereits geöffnet zu verwalten. Bei der Verarbeitung eines Anrufs **Anmeldung** sollte der Anbieter dieser Liste der open-Speicher zu überprüfen und bestimmen, ob der Speicher auf protokolliert werden bereits geöffnet ist. Wenn dies der Fall, Benutzeranmeldeinformationen müssen nicht überprüft werden soll, und die Anzeige eines Dialogfelds sollte vermieden werden, wenn möglich. Wenn Dialogfelder angezeigt werden müssen, sollte der Anbieter zurückgegebenen Informationen, um festzustellen, ob ein Speicher ein zweites Mal geöffnet wurde überprüfen. Darüber hinaus der Anbieter sollte prüfen, ob doppelte öffnen mithilfe von _LpEntryID_ am Anfang der **Anmeldung** Anruf verarbeitet. 
  
Verarbeitung für eine **Anmeldung** Aufruf, der geöffneten Shop greift auf Standard lautet wie folgt: 
  
1. Speicheranbieter ruft **AddRef** für das vorhandene Store-Objekt, wenn die neue Benutzeroberfläche angefordert wird die Schnittstelle für den vorhandenen Store identisch ist. Andernfalls wird die **QueryInterface** , um die neue Benutzeroberfläche zu erhalten. Wenn der Informationsspeicher die neue Benutzeroberfläche nicht unterstützt, sollte der Anbieter den Fehlerwert MAPI_E_INTERFACE_NOT_SUPPORTED zurückgegeben. 
    
2. Der Anbieter gibt einen Zeiger auf die erforderliche Schnittstelle des vorhandenen Store-Objekts in _LppMDB_.
    
3. Der Anbieter gibt in _LppMSLogon_ **null** zurück.
    
4. Der Anbieter sollte das Profil für den Anruf übergebenen Support-Objekt nicht geöffnet werden. Darüber hinaus sollten nicht registrieren ein eindeutigen Bezeichners für Anbieter, Registrieren einer Statuszeile oder MAPI-Warteschlange Anmeldung Daten zurückgeben.
    
5. Der Anbieter sollte keine **AddRef** für das Objekt Support aufrufen, da einen Zeiger auf das Objekt nicht erforderlich ist. 
    
Wenn möglich, Anbieter sollte die entsprechende Fehlermeldung zurückgegeben und Warnung Zeichenfolgen für die **Anmeldung** Aufrufe, da dies erheblich erleichtert die Last der Benutzer bei der Bestimmung, warum etwas nicht funktioniert. Wenn diese Zeichenfolgen zurückgeben möchten, legt ein Anbieter für die Mitglieder in der Struktur **MAPIERROR** fest. MAPI für sucht, verwendet und die Struktur **MAPIERROR** frei, wenn es von einem Anbieter zurückgegeben wird. 
  
Arbeitsspeicher für diese Struktur **MAPIERROR** sollte mit dem Gespräch **MSProviderInit** _LpfAllocateBuffer_ übergebene Puffer zugewiesen werden. Etwaige Fehler, die Zeichenfolgen in der zurückgegebenen Struktur enthalten im Unicode-Format werden soll, wenn der Parameter MAPI_UNICODE in die **Anmeldung** _UlFlags;_ andernfalls festgelegt ist, sollten sie in das ANSI-Zeichen festgelegt werden. 
  
Für die meisten zurückgegebenen Fehlerwerte von **Anmeldung**deaktiviert MAPI die Message-Dienste zu denen der fehlerhaften Anbieter gehört. MAPI rufen keine Anbieter, die zu dieser Dienste während der Lebensdauer der MAPI-Sitzung gehören. Im Gegensatz dazu bei der **Anmeldung** von dessen Anmeldung den Fehlerwert MAPI_E_FAILONEPROVIDER zurückgibt, wird MAPI nicht den Dienst deaktiviert zu dem der Anbieter gehört. **Anmeldung** sollte MAPI_E_FAILONEPROVIDER zurückgegeben, wenn ein Fehler auftritt, der nicht den gesamten Dienst für die Lebensdauer der Sitzung deaktivieren rechtfertigen ist. Beispielsweise könnte ein Anbieter dieser Fehler zurück, wenn nicht die Anzeige einer Benutzeroberfläche lässt und ein Kennwort erforderlich nicht verfügbar ist. 
  
Wenn ein Anbieter von dessen Anmeldung MAPI_E_UNCONFIGURED zurückgibt, wird MAPI Aufrufen des Anbieters Nachricht Service Eintrag-Funktion und wiederholen Sie die Anmeldung. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext aus, um dem Dienst selbst konfigurieren kann. Wenn der Client sich entschieden hat, um eine Benutzeroberfläche für die Anmeldung zu ermöglichen, kann der Dienst das Eigenschaftenblatt Konfiguration darstellen, damit der Benutzer Informationen eingeben kann.
  
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

