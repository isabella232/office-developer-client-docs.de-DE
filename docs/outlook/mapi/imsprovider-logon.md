---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1cc5d841e28275ad4ccdcaa6f7a41ff1f7bd4b4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620660"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert die MAPI bei einer Instanz eines Nachrichtenspeicheranbieters.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die Anmeldung beim Store-Anbieter verwendet wird. Diese Zeichenfolge kann in Dialogfeldern angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Es muss im Unicode-Format vorliegen, wenn das MAPI_UNICODE-Flag im  _ulFlags-Parameter_ festgelegt ist. 
    
 _cbEntryID_
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _parameter lpEntryID_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner für den Nachrichtenspeicher. Das Übergeben von **NULL** in  _lpEntryID_ gibt an, dass noch kein Nachrichtenspeicher ausgewählt wurde und dass Dialogfelder, in denen der Benutzer einen Nachrichtenspeicher auswählen kann, angezeigt werden können. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung durchgeführt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf des Objekts einen Fehler auslösen.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Anmeldedialogfeldern. Wenn dieses Kennzeichen festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren, einen Datenträger einzufügen oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Speicher erforderlich sind.
    
MDB_NO_MAIL 
  
> Der Nachrichtenspeicher sollte nicht zum Senden oder Empfangen von E-Mails verwendet werden. Das Flag signalisiert der MAPI, den MAPI-Spooler nicht zu benachrichtigen, dass dieser Nachrichtenspeicher geöffnet wird. Wenn dieses Flag festgelegt ist und der Nachrichtenspeicher eng mit einem Transportanbieter gekoppelt ist, muss der Anbieter die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) nicht aufrufen. 
    
MDB_TEMPORARY 
  
> Protokolliert den Speicher, sodass Informationen programmgesteuert aus dem Profilabschnitt ohne Verwendung von Dialogfeldern abgerufen werden können. Dieses Kennzeichen weist die MAPI an, dass der Informationsspeicher nicht der Nachrichtenspeichertabelle hinzugefügt werden soll und dass der Speicher nicht dauerhaft sein kann. Wenn dieses Kennzeichen festgelegt ist, müssen Nachrichtenspeicheranbieter die [IMAPISupport::ModifyProfile-Methode](imapisupport-modifyprofile.md) nicht aufrufen. 
    
MDB_WRITE 
  
> Fordert Lese-/Schreibberechtigung an.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), bei dem sich der Nachrichtenspeicher anmelden soll. Das Übergeben von **NULL** gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ( [IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher festgelegt werden (z. B. IID_IUnknown oder IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Ein Zeiger auf die Variable, in der der Speicheranbieter die Größe der Validierungsdaten im  _Parameter "lppbSpoolSecurity"_ in Bytes zurückgibt. 
    
 _lppbSpoolSecurity_
  
> [out] Ein Zeiger auf den Zeiger auf die zurückgegebenen Überprüfungsdaten. Diese Überprüfungsdaten werden bereitgestellt, damit die [IMSProvider::SpoolerLogon-Methode](imsprovider-spoolerlogon.md) den MAPI-Spooler im selben Speicher wie der Nachrichtenspeicheranbieter protokollieren kann. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR-Struktur(](mapierror.md) falls vorhanden), die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält. Der  _Parameter lppMAPIError_ kann auf **NULL** festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
 _lppMSLogon_
  
> [out] Ein Zeiger auf den Zeiger auf das Anmeldeobjekt des Nachrichtenspeichers, bei dem sich MAPI anmelden soll.
    
 _lppMDB_
  
> [out] Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt für die MAPI-Spooler- und Clientanwendungen, bei denen sie sich anmelden möchten.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_FAILONEPROVIDER 
  
> Dieser Anbieter kann sich nicht anmelden, aber dieser Fehler sollte den Dienst nicht deaktivieren. 
    
MAPI_E_LOGON_FAILED 
  
> Eine Anmeldesitzung konnte nicht eingerichtet werden.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. Wenn dieser Wert zurückgegeben wird, ruft MAPI die Nachrichtendienst-Einstiegspunktfunktion des Nachrichtenspeicheranbieters auf.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codepage des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachrichtenspeicheranbieter verfügt über Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md) Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter abzurufen. 
    
## <a name="remarks"></a>Bemerkungen

MAPI ruft die **IMSProvider::Logon-Methode** auf, um den Großteil der Verarbeitung durchzuführen, die erforderlich ist, um Zugriff auf einen Nachrichtenspeicher zu erhalten. Nachrichtenspeicheranbieter überprüfen alle Benutzeranmeldeinformationen, die für den Zugriff auf einen bestimmten Speicher erforderlich sind, und geben ein Nachrichtenspeicherobjekt im  _lppMDB-Parameter_ zurück, bei dem sich der MAPI-Spooler und die Clientanwendungen anmelden können. 
  
Zusätzlich zum zurückgegebenen Nachrichtenspeicherobjekt für die Verwendung von Client- und MAPI-Spoolern gibt der Anbieter auch ein Anmeldeobjekt für den Nachrichtenspeicher zurück, das die MAPI zum Steuern des geöffneten Speichers verwendet. Das Anmeldeobjekt des Nachrichtenspeichers und das Nachrichtenspeicherobjekt sollten innerhalb des Nachrichtenspeicheranbieters eng verknüpft sein, damit sich jede auf den anderen auswirken kann. Die Verwendung des Speicherobjekts und des Anmeldeobjekts sollte identisch sein. Es sollte eine 1:1-Entsprechung zwischen dem Anmeldeobjekt und dem Speicherobjekt bestehen, sodass die Objekte so agieren, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht. Die beiden Objekte sollten auch zusammen erstellt und gemeinsam freigegeben werden. 
  
Das MAPI-Unterstützungsobjekt, das von der MAPI erstellt und im  _lpMAPISup-Parameter_ an den Anbieter übergeben wird, bietet Zugriff auf Funktionen in der MAPI, die der Anbieter benötigt. Dazu gehören Funktionen, die Profilinformationen speichern und abrufen, auf Adressbücher zugreifen usw. Der  _lpMAPISup-Zeiger_ kann für jeden geöffneten Speicher unterschiedlich sein. Bei der Verarbeitung von Aufrufen für einen Nachrichtenspeicher nach der Anmeldung sollte der Speicheranbieter die  _variable lpMAPISup_ verwenden, die für diesen Speicher spezifisch ist. Für jeden **Anmeldeaufruf,** der einen Nachrichtenspeicher öffnet und erfolgreich ein Anmeldeobjekt für den Nachrichtenspeicher erstellt, muss der Anbieter einen Zeiger auf das MAPI-Unterstützungsobjekt im Store-Anmeldeobjekt speichern und die [IUnknown::AddRef-Methode aufrufen,](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) um einen Verweis für das Supportobjekt hinzuzufügen. 
  
Der  _ulUIParam-Parameter_ sollte verwendet werden, wenn der Anbieter während des **Anmeldeaufrufs** Dialogfelder darstellt. Dialogfelder sollten jedoch nicht angezeigt werden, wenn  _ulFlags_ das flag MDB_NO_DIALOG enthält. Wenn eine Benutzeroberfläche aufgerufen werden muss,  _ulFlags_ dies jedoch nicht zulässt, oder wenn aus einem anderen Grund keine Benutzeroberfläche angezeigt werden kann, sollte der Anbieter MAPI_E_LOGON_FAILED zurückgeben. Wenn **bei der Anmeldung** ein Dialogfeld angezeigt wird und der Benutzer die Anmeldung abbricht, in der Regel durch Klicken auf die Schaltfläche **"Abbrechen"** des Dialogfelds, sollte der Anbieter MAPI_E_USER_CANCEL zurückgeben. 
  
Der  _lpEntryID-Parameter_ kann entweder **NULL** sein oder auf einen nicht gepackten Speichereintragsbezeichner zeigen, den dieser Nachrichtenspeicher zuvor erstellt hat. Wenn  _lpEntryID_ auf einen nicht gepackten Eintragsbezeichner zeigt, kann dieser Eintragsbezeichner von einer von mehreren Stellen stammen: 
  
- Es kann ein Eintragsbezeichner sein, den der Speicheranbieter zuvor umschlossen und als **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft in den Profilabschnitt geschrieben hat.
    
- Dies kann ein Eintragsbezeichner sein, den der Anbieter zuvor umschlossen und als **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) -Eigenschaft an einen aufrufenden Client zurückgegeben hat. 
    
- Es kann sich um einen Eintragsbezeichner handeln, den der Anbieter zuvor umschlossen und als **PR_ENTRYID** Eigenschaft eines Nachrichtenspeicherobjekts an einen aufrufenden Client zurückgegeben hat. 
    
In jedem dieser Fälle ist es möglich, dass der Eintragsbezeichner auf einem anderen Computer als dem aktuell verwendeten erstellt wurde.
  
Wenn  _lpEntryID_ nicht **NULL** ist, sollte es alle Informationen enthalten, die zum Identifizieren und Suchen des Nachrichtenspeichers erforderlich sind. Diese Informationen können Netzwerkvolumenamen, Telefonnummern, Benutzerkontonamen usw. enthalten. Wenn die Verbindung mit dem Speicher nicht mithilfe der Daten im Eintragsbezeichner hergestellt werden kann, sollte der Speicheranbieter ein Dialogfeld anzeigen, in dem der Benutzer den zu öffnenden Speicher auswählen kann. Möglicherweise ist ein Dialogfeld erforderlich, z. B. wenn ein Server umbenannt wurde, ein Kontoname geändert wurde oder Teile des Netzwerks nicht verfügbar sind.
  
Wenn  _lpEntryID_ **null** ist, wurde der zu verwendende Nachrichtenspeicher noch nicht ausgewählt. Der Anbieter kann weiterhin auf einen Speicher zugreifen, ohne ein Dialogfeld anzuzeigen, wenn weitere Methoden zum Angeben des Speichers unterstützt werden. Beispielsweise kann der Anbieter seine Initialisierungsdatei überprüfen oder nach zusätzlichen Eigenschaften suchen, die bei der Konfiguration im Profilabschnitt des Nachrichtendiensts platziert wurden.
  
Wenn ein Anbieter feststellt, dass sich nicht alle erforderlichen Informationen im Profil befinden, sollte er MAPI_E_UNCONFIGURED zurückgeben. MapI ruft dann die Nachrichtendienst-Einstiegspunktfunktion des Anbieters auf, damit der Benutzer einen Speicher auswählen oder sogar einen erstellen kann, und bei Bedarf einen Kontonamen und ein Kennwort einzugeben. MAPI erstellt automatisch einen neuen Profilabschnitt für einen neuen Speicher. Dieser neue Profilabschnitt kann temporär oder dauerhaft sein, je nachdem, wie er hinzugefügt wurde. Wenn der Speicheranbieter die **IMAPISupport::ModifyProfile-Methode** aufruft, wird der neue Profilabschnitt dauerhaft, und der Speicher wird der Liste der Nachrichtenspeicher hinzugefügt, die von der [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) zurückgegeben werden. 
  
Der  _Parameter lpInterface_ gibt den IID der Schnittstelle an, die für das neu geöffnete Speicherobjekt erforderlich ist. Das Übergeben von **NULL** in  _lpInterface_ gibt an, dass die MAPI-Nachrichtenspeicherschnittstelle **IMsgStore** erforderlich ist. Das Übergeben des Nachrichtenspeicherobjekts IID_IMsgStore gibt außerdem an, dass **IMsgStore** erforderlich ist. Wenn IID_IUnknown in _lpInterface_ übergeben wird, sollte der Anbieter den Speicher öffnen, indem er die von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) abgeleitete Schnittstelle verwendet, die für den Anbieter am besten geeignet ist (auch hierbei handelt es sich in der Regel **um IMsgStore).** Wenn IID_IUnknown übergeben wird, verwendet die aufrufende Implementierung die [IUnknown::QueryInterface-Methode,](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) um eine Schnittstelle auszuwählen, nachdem der Vorgang zum Öffnen des Speichers erfolgreich war. 
  
Der **IMSProvider::Logon-Aufruf** sollte ausreichende Informationen zurückgeben, z. B. einen Pfad zum Speicher und Anmeldeinformationen für den Zugriff auf den Speicher, damit sich der MAPI-Spooler beim gleichen Speicher anmeldet, den der Speicheranbieter ohne Darstellen eines Dialogfelds ausführt. Die Parameter  _lpcbSpoolSecurity_ und  _lppbSpoolSecurity_ werden verwendet, um diese Informationen zurückzugeben. Der Anbieter weist den Speicher für diese Daten zu, indem er einen Zeiger an einen Puffer im _lpfAllocateBuffer-Parameter_ der [MSProviderInit-Funktion](msproviderinit.md) übergibt. Der Anbieter platziert die Größe dieses Puffers in _lpcbSpoolSecurity_. 
  
MapI gibt diesen Puffer bei Bedarf frei. Wenn die Anmeldung des MAPI-Spoolers beim Speicher allein anhand der Informationen im Profilabschnitt erfolgen kann, kann der Anbieter null in  _lppbSpoolSecurity_ und 0 für die Größe der Informationen in  _lpcbSpoolSecurity_ zurückgeben. Die MAPI-Spooleranmeldung erfolgt als Teil eines anderen Prozesses als die Store-Anmeldung. da der Puffer, der die übergebenen Informationen enthält, zwischen Prozessen kopiert wird, befindet er sich möglicherweise nicht im Arbeitsspeicher am selben Speicherort für den MAPI-Spoolerprozess wie für den Speicheranbieterprozess. Daher sollte ein Anbieter keine Adressen in diesen Puffer einfügen. Weitere Informationen zur MAPI-Spooleranmeldung finden Sie unter der [IMSProvider::SpoolerLogon-Methode.](imsprovider-spoolerlogon.md) 
  
Die meisten Speicheranbieter verwenden die [IMAPISession::OpenProfileSection-Methode](imapisession-openprofilesection.md) des Supportobjekts, das im  _lpMAPISup-Parameter_ zum Speichern und Abrufen von Benutzeranmeldeinformationen und -optionen übergeben wird. **OpenProfileSection** ermöglicht es einem Speicheranbieter, zusätzliche zufällige Informationen in einem Profilabschnitt zu speichern und einer bestimmten Ressource zuzuordnen. Beispielsweise kann ein Speicheranbieter den Namen und das Kennwort des Benutzerkontos speichern, das einer Ressource zugeordnet ist, sowie alle Pfade oder andere Informationen, die für den Zugriff auf diese Ressource erforderlich sind. 
  
Eigenschaften mit Eigenschaftsbezeichnern 0x6600 über 0x67FF sind sichere Eigenschaften, die dem Anbieter zur eigenen Verwendung zum Speichern privater Daten in Profilabschnitten zur Verfügung stehen. Weitere Informationen zur Verwendung von Eigenschaften in Profilabschnittsobjekten finden Sie unter der [IProfSect : IMAPIProp-Methode.](iprofsectimapiprop.md) 
  
Zusätzlich zu privaten Daten in Eigenschaften mit Bezeichnern, die über 0x67FF 0x6600, sollte der Speicheranbieter Informationen für die **Eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in seinem Profilabschnitt bereitstellen. Sie sollte **PR_DISPLAY_NAME** den Anzeigenamen des Anbieters selbst einfügen – eine identifizierende Zeichenfolge (z. B. "Microsoft Personal Information Store"), die Benutzern angezeigt wird, damit sie diesen Nachrichtenspeicher von anderen unterscheiden können, auf die sie möglicherweise Zugriff haben. **PR_DISPLAY_NAME** enthält in der Regel einen Servernamen, einen Benutzerkontonamen oder pfad. 
  
Einige Profilabschnittseigenschaften sind in der Nachrichtenspeichertabelle sichtbar. andere sind während der Einrichtung, Installation und Konfiguration des MAPI-Subsystems sichtbar. Der Anbieter stellt in der Regel Informationen zu diesen sichtbaren Eigenschaften sowohl für einen neuen Profilabschnitt bereit, der noch keine gespeicherten Anmeldeinformationen oder privaten Informationen enthält, als auch für den Zeitpunkt, zu dem festgestellt wird, dass sich eigenschafteninformationen geändert haben. Weitere Informationen zu Profilabschnitten finden Sie unter [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Nach der erfolgreichen Protokollierung eines Benutzers und vor der Rückkehr zur MAPI sollte der Speicheranbieter das Array von Eigenschaften für die Statuszeile für die Ressource erstellen und die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aufrufen. 
  
 **Anmeldeaufrufe,** die Nachrichtenspeicher öffnen, die bereits für die aktuelle MAPI-Sitzung geöffnet sind, überspringen einen Großteil der zuvor beschriebenen Verarbeitung. Diese Aufrufe erstellen keine Statuszeilen, geben keine Anmeldeobjekte für den Nachrichtenspeicher zurück, rufen **AddRef** für das MAPI-Unterstützungsobjekt auf oder geben Daten für die MAPI-Spooleranmeldung zurück. Diese Aufrufe geben S_OK zurück und geben ein Nachrichtenspeicherobjekt mit der angeforderten Schnittstelle zurück. 
  
Um solche Aufrufe zu erkennen, sollte der Anbieter eine Liste im Nachrichtenspeicheranbieterobjekt der Speicher verwalten, die bereits für dieses Anbieterobjekt geöffnet sind. Bei der Verarbeitung eines **Anmeldeaufrufs** sollte der Anbieter diese Liste der geöffneten Speicher überprüfen und ermitteln, ob der speicher, bei dem angemeldet werden soll, bereits geöffnet ist. Wenn dies der Fall ist, müssen die Benutzeranmeldeinformationen nicht überprüft werden, und die Anzeige eines Dialogfelds sollte nach Möglichkeit vermieden werden. Wenn Dialogfelder angezeigt werden müssen, sollte der Anbieter die zurückgegebenen Informationen überprüfen, um festzustellen, ob ein Speicher ein zweites Mal geöffnet wurde. Darüber hinaus sollte der Anbieter zu Beginn der Verarbeitung von **Anmeldeaufrufen** mithilfe von _lpEntryID_ auf doppelte Öffnungen prüfen. 
  
Die Standardverarbeitung für einen **Anmeldeaufruf,** der auf einen geöffneten Speicher zugreift, lautet wie folgt: 
  
1. Der Store-Anbieter ruft **AddRef** für das vorhandene Speicherobjekt auf, wenn die angeforderte neue Schnittstelle mit der Schnittstelle für den vorhandenen Speicher identisch ist. Andernfalls wird **QueryInterface** aufgerufen, um die neue Schnittstelle abzurufen. Wenn der Speicher die neue Schnittstelle nicht unterstützt, sollte der Anbieter den Fehlerwert MAPI_E_INTERFACE_NOT_SUPPORTED zurückgeben. 
    
2. Der Anbieter gibt einen Zeiger auf die erforderliche Schnittstelle des vorhandenen Speicherobjekts in  _lppMDB_ zurück.
    
3. Der Anbieter gibt **null** in  _lppMSLogon_ zurück.
    
4. Der Anbieter sollte das Profil für das support-Objekt, das im Aufruf übergeben wurde, nicht öffnen. Darüber hinaus sollte kein eindeutiger Anbieterbezeichner registriert, keine Statuszeile registriert oder MAPI-Spooler-Anmeldedaten zurückgegeben werden.
    
5. Der Anbieter sollte **AddRef** für das Supportobjekt nicht aufrufen, da kein Zeiger auf das Objekt erforderlich ist. 
    
Anbieter sollten nach Möglichkeit geeignete Fehler- und Warnzeichenfolgen für **Anmeldeaufrufe** zurückgeben, da dies die Benutzer erheblich erleichtert, um zu bestimmen, warum etwas nicht funktioniert hat. Um diese Zeichenfolgen zurückzugeben, legt ein Anbieter die Elemente in der **MAPIERROR-Struktur** fest. Die MAPI sucht, verwendet und gibt die **MAPIERROR-Struktur** frei, wenn sie von einem Anbieter zurückgegeben wird. 
  
Der Speicher für diese **MAPIERROR-Struktur** sollte mithilfe des Puffers zugewiesen werden, der im Aufruf **von "MSProviderInit"** in _"lpfAllocateBuffer"_ übergeben wurde. Alle Fehlerzeichenfolgen, die in der zurückgegebenen Struktur enthalten sind, sollten im Unicode-Format vorliegen, wenn MAPI_UNICODE in den  _Anmelde-ulFlags_ festgelegt ist. Andernfalls sollten sie sich im ANSI-Zeichensatz befinden. 
  
Bei den meisten von **der Anmeldung** zurückgegebenen Fehlerwerten deaktiviert MAPI die Nachrichtendienste, zu denen der fehlerhafte Anbieter gehört. Die MAPI ruft während der MAPI-Sitzung keine Anbieter auf, die zu diesen Diensten gehören. Wenn die **Anmeldung** dagegen den MAPI_E_FAILONEPROVIDER Fehlerwert aus der Anmeldung zurückgibt, deaktiviert MAPI nicht den Nachrichtendienst, zu dem der Anbieter gehört. **Die Anmeldung** sollte MAPI_E_FAILONEPROVIDER zurückgeben, wenn ein Fehler auftritt, der nicht die Deaktivierung des gesamten Diensts für die Dauer der Sitzung erfordert. Beispielsweise kann ein Anbieter diesen Fehler zurückgeben, wenn er die Anzeige einer Benutzeroberfläche nicht zulässt und ein erforderliches Kennwort nicht verfügbar ist. 
  
Wenn ein Anbieter MAPI_E_UNCONFIGURED aus seiner Anmeldung zurückgibt, ruft MAPI die Nachrichtendienst-Eintragsfunktion des Anbieters auf und versucht dann erneut, die Anmeldung auszuführen. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren. Wenn der Client eine Benutzeroberfläche für die Anmeldung zugelassen hat, kann der Dienst sein Konfigurationseigenschaftenblatt anzeigen, damit der Benutzer Konfigurationsinformationen eingeben kann.
  
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

