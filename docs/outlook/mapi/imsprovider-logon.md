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
  
Protokolliert MAPI für eine Instanz eines Nachrichtenspeicher Anbieters.
  
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
  
> in Ein Zeiger auf das aktuelle MAPI-Unterstützungsobjekt für den Nachrichtenspeicher.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. 
    
 _lpszProfileName_
  
> in Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die Speicheranbieter Anmeldung verwendet wird. Diese Zeichenfolge kann in Dialogfeldern angezeigt werden, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Sie muss im Unicode-Format vorliegen, wenn das MAPI_UNICODE-Flag im _ulFlags_ -Parameter festgelegt ist. 
    
 _cbEntryID_
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher. Durch das Übergeben von **null** in _lpEntryID_ wird angegeben, dass noch kein Nachrichtenspeicher ausgewählt wurde und dass Dialogfelder angezeigt werden können, in denen der Benutzer einen Nachrichtenspeicher auswählen kann. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Ausführung der Anmeldung steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann bei einem nachfolgenden Aufruf des Objekts ein Fehler ausgelöst werden.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Anmelde Dialogfeldern. Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Flag nicht festgelegt ist, kann der Nachrichtenspeicher Anbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren, einen Datenträger einzufügen oder andere Aktionen auszuführen, die erforderlich sind, um eine Verbindung mit dem Speicher herzustellen.
    
MDB_NO_MAIL 
  
> Der Nachrichtenspeicher sollte nicht zum Senden oder empfangen von e-Mails verwendet werden. Das Flag signalisiert, dass MAPI den MAPI-Spooler nicht benachrichtigt, dass dieser Nachrichtenspeicher geöffnet wird. Wenn dieses Flag festgelegt ist und der Nachrichtenspeicher eng mit einem Transportanbieter gekoppelt ist, muss der Anbieter die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode nicht aufrufen. 
    
MDB_TEMPORARY 
  
> Protokolliert den Speicher, sodass Informationen programmgesteuert aus dem Abschnitt profile abgerufen werden können, ohne dass Dialogfelder verwendet werden. Dieses Flag weist MAPI darauf hin, dass der Informationsspeicher nicht der Nachrichtenspeichertabelle hinzugefügt werden soll und dass der Speicher nicht dauerhaft festgelegt werden kann. Wenn dieses Flag festgelegt ist, müssen die Nachrichtenspeicher Anbieter die [IMAPISupport:: ModifyProfile](imapisupport-modifyprofile.md) -Methode nicht aufrufen. 
    
MDB_WRITE 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) für den Nachrichtenspeicher, an dem sich die Anmeldung anmeldet. Übergeben von **null** gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ( [IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird. Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher festgelegt werden (beispielsweise IID_IUnknown oder IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> Out Ein Zeiger auf die Variable, in der der Informationsspeicher Anbieter die Größe (in Bytes) der Validierungsdaten im _lppbSpoolSecurity_ -Parameter zurückgibt. 
    
 _lppbSpoolSecurity_
  
> Out Ein Zeiger auf den Zeiger auf die zurückgegebenen Validierungsdaten. Diese Validierungsdaten werden bereitgestellt, damit die [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) -Methode den MAPI-Spooler in demselben Speicher wie der Nachrichtenspeicher Anbieter protokollieren kann. 
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR](mapierror.md) -Struktur, die Versions-, Komponenten-und Kontextinformationen für einen Fehler enthält. Der _lppMAPIError_ -Parameter kann auf **null** festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll. 
    
 _lppMSLogon_
  
> Out Ein Zeiger auf den Zeiger auf das Nachrichtenspeicher-Anmeldeobjekt für die Anmeldung bei MAPI.
    
 _lppMDB_
  
> Out Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt für die MAPI-Spooler und Clientanwendungen, die sich bei anmelden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_FAILONEPROVIDER 
  
> Dieser Anbieter kann sich nicht anmelden, aber dieser Fehler sollte den Dienst nicht deaktivieren. 
    
MAPI_E_LOGON_FAILED 
  
> Es konnte keine Anmeldesitzung hergestellt werden.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. Wenn dieser Wert zurückgegeben wird, ruft MAPI die Nachrichtendienst-Einstiegspunktfunktion des Nachrichtenspeicher Anbieters auf.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachrichtenspeicher Anbieter hat Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md). Rufen Sie die [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) -Methode auf, um die Fehlerinformationen vom Anbieter abzurufen. 
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die **IMSProvider:: LOGON** -Methode auf, um die Mehrzahl der erforderlichen Verarbeitungsschritte für den Zugriff auf einen Nachrichtenspeicher auszuführen. Nachrichtenspeicher Anbieter überprüfen alle für den Zugriff auf einen bestimmten Speicher erforderlichen Benutzeranmeldeinformationen und geben ein Nachrichtenspeicherobjekt im _lppMDB_ -Parameter zurück, an dem sich die MAPI-Warteschlange und die Clientanwendungen anmelden können. 
  
Zusätzlich zum zurückgegebenen Nachrichtenspeicherobjekt für die Verwendung von Client-und MAPI-Spoolern gibt der Anbieter auch ein Nachrichtenspeicher-Anmeldeobjekt für MAPI zurück, das beim Steuern des geöffneten Speichers verwendet werden soll. Das Nachrichtenspeicher-Anmeldeobjekt und das Nachrichtenspeicherobjekt sollten eng innerhalb des Nachrichtenspeicher Anbieters miteinander verknüpft sein, damit sich jeder auf die andere auswirken kann. Die Verwendung des Store-Objekts und des LOGON-Objekts sollte identisch sein; Es sollte eine 1:1-Entsprechung zwischen dem Logon-Objekt und dem Store-Objekt vorhanden sein, sodass die Objekte so handeln, als ob es sich um ein Objekt handelt, das zwei Schnittstellen verfügbar macht. Die beiden Objekte sollten auch zusammen erstellt und freigegeben werden. 
  
Das MAPI-Unterstützungsobjekt, erstellt von MAPI und im _lpMAPISup_ -Parameter an den Anbieter übergeben, ermöglicht den Zugriff auf Funktionen in MAPI, die vom Anbieter benötigt werden. Hierzu gehört auch die Funktion zum Speichern und Abrufen von Profilinformationen, Zugriffs Adressbüchern usw. Der _lpMAPISup_ -Zeiger kann für jeden geöffneten Speicher unterschiedlich sein. Während der Verarbeitung von Aufrufen für einen Nachrichtenspeicher nach der Anmeldung sollte der Informationsspeicher Anbieter die _lpMAPISup_ -Variable verwenden, die für diesen Speicher spezifisch ist. Bei einem **Anmelde** Anruf, bei dem ein Nachrichtenspeicher geöffnet und ein Nachrichtenspeicher-Anmeldeobjekt erstellt werden kann, muss der Anbieter einen Zeiger auf das MAPI-Unterstützungsobjekt im Store-Anmeldeobjekt speichern und die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode aufrufen, um einen Verweis auf das Support Objekt. 
  
Der Parameter _ulUIParam_ sollte verwendet werden, wenn der Anbieter während des **Anmelde** Aufrufs Dialogfelder anzeigt. Dialogfelder sollten jedoch nicht angezeigt werden, wenn _ulFlags_ das MDB_NO_DIALOG-Flag enthält. Wenn eine Benutzeroberfläche aufgerufen werden muss, aber _ulFlags_ dies nicht zulässt, oder wenn aus irgendeinem anderen Grund eine Benutzeroberfläche nicht angezeigt werden kann, sollte der Anbieter MAPI_E_LOGON_FAILED zurückgeben. Wenn bei der **Anmeldung** ein Dialogfeld angezeigt wird und der Benutzer die Anmeldung abbricht, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** des Dialogfelds, sollte der Anbieter MAPI_E_USER_CANCEL zurückgeben. 
  
Der _lpEntryID_ -Parameter kann entweder **null** sein oder auf eine nicht eingeschlossene Speicher Eintrags-ID verweisen, die dieser Nachrichtenspeicher zuvor erstellt hat. Wenn _lpEntryID_ auf eine nicht umbrochene Eintrags-ID zeigt, kann diese Eintrags-ID von einer von mehreren Stellen stammen: 
  
- Dabei kann es sich um eine Eintrags-ID handeln, die der Store-Anbieter zuvor verpackt und in den profile-Abschnitt als **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft geschrieben hat.
    
- Es kann sich um eine Eintrags-ID handeln, die der Anbieter zuvor umschlossen und an einen aufrufenden Client als **PR_STORE_ENTRYID** ([pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))-Eigenschaft zurückgegeben hat. 
    
- Es kann sich um eine Eintrags-ID handeln, die der Anbieter zuvor umschlossen und an einen aufrufenden Client als **PR_ENTRYID** -Eigenschaft eines Nachrichtenspeicher Objekts zurückgegeben hat. 
    
In einem dieser Fälle ist es möglich, dass die Eintrags-ID auf einem anderen Computer erstellt wurde als der, der derzeit verwendet wird.
  
Wenn _lpEntryID_ nicht **null**ist, sollte es alle erforderlichen Informationen enthalten, um den Nachrichtenspeicher zu identifizieren und zu suchen. Diese Informationen können Netzwerknamen, Telefonnummern, Benutzerkontonamen usw. aufweisen. Wenn die Verbindung mit dem Speicher nicht mithilfe der Daten in der Eintrags-ID hergestellt werden kann, sollte der Informationsspeicher Anbieter ein Dialogfeld anzeigen, in dem der Benutzer den zu öffnenden Speicher auswählen können. Möglicherweise ist ein Dialogfeld erforderlich, beispielsweise, wenn ein Server umbenannt wurde, ein Kontoname geändert oder Teile des Netzwerks nicht verfügbar sind.
  
Wenn _lpEntryID_ ist ****, wurde der zu verwendende Nachrichtenspeicher noch nicht ausgewählt. Der Anbieter kann weiterhin auf einen Speicher zugreifen, ohne ein Dialogfeld anzuzeigen, wenn weitere Methoden zum Angeben des Speichers unterstützt werden. Beispielsweise kann der Anbieter seine Initialisierungsdatei überprüfen oder nach zusätzlichen Eigenschaften suchen, die im Profil Abschnitt des Nachrichtendiensts unter Konfiguration gespeichert wurden.
  
Wenn ein Anbieter feststellt, dass alle erforderlichen Informationen nicht im Profil sind, sollte MAPI_E_UNCONFIGURED zurückgegeben werden. MAPI ruft dann die Nachrichtendienst-Einstiegspunktfunktion des Anbieters auf, um dem Benutzer zu ermöglichen, einen Speicher auszuwählen oder sogar einen zu erstellen, und bei Bedarf einen Kontonamen und ein Kennwort einzugeben. MAPI erstellt automatisch einen neuen Profil Abschnitt für einen neuen Speicher; Dieser neue Profil Abschnitt kann temporär oder permanent sein, je nachdem, wie er hinzugefügt wurde. Wenn der Informationsspeicher Anbieter die **IMAPISupport:: ModifyProfile** -Methode aufruft, wird der neue Profil Abschnitt permanent, und der Speicher wird der Liste der Nachrichtenspeicher hinzugefügt, die von der [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode zurückgegeben werden. 
  
Der Parameter _lpInterface_ gibt die IID der Schnittstelle an, die für das neu geöffnete Store-Objekt erforderlich ist. Durch das Übergeben von **null** in _lpInterface_ wird festgelegt, dass die MAPI-Nachrichtenspeicher Schnittstelle **IMsgStore**erforderlich ist. Das Übergeben des Nachrichtenspeicher Objekts, IID_IMsgStore, gibt auch an, dass **IMsgStore** erforderlich ist. Wenn IID_IUnknown in _lpInterface_übergeben wird, sollte der Anbieter den Speicher mithilfe der von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) abgeleiteten Schnittstelle für den Anbieter öffnen (Dies ist in der Regel **IMsgStore**). Wenn IID_IUnknown übergeben wird, verwendet die aufrufende Implementierung die [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode, um eine Schnittstelle auszuwählen, nachdem der Store Open-Vorgang erfolgreich abgeschlossen wurde. 
  
Der **IMSProvider:: LOGON** -Aufruf sollte genügend Informationen zurückgeben, beispielsweise einen Pfad zum Speicher und die Anmeldeinformationen für den Zugriff auf den Speicher, damit sich der MAPI-Spooler an demselben Speicher anmelden kann, den der Informationsspeicher Anbieter ausführt, ohne ein Dialogfeld zu präsentieren. Die Parameter _lpcbSpoolSecurity_ und _lppbSpoolSecurity_ werden verwendet, um diese Informationen zurückzugeben. Der Anbieter ordnet den Speicher für diese Daten an, indem er einen Zeiger auf einen Puffer im _lpfAllocateBuffer_ -Parameter der [MSProviderInit](msproviderinit.md) -Funktion übergibt. der Anbieter platziert die Größe dieses Puffers in _lpcbSpoolSecurity_. 
  
MAPI gibt diesen Puffer bei Bedarf frei. Wenn die Anmeldung des MAPI-Spoolers an den Speicher allein aus den Informationen im Profil Abschnitt erfolgen kann, kann der Anbieter in _lppbSpoolSecurity_ und 0 für die Größe der Informationen in _lpcbSpoolSecurity_NULL zurückgeben. Die MAPI-Spooler-Anmeldung tritt als Teil eines anderen Prozesses als die Speicher Anmeldung auf. Da der Puffer, der die übergebenen Informationen enthält, zwischen Prozessen kopiert wird, befindet er sich möglicherweise nicht am selben Speicherort für den MAPI-Spooler-Prozess wie für den Speicheranbieter Prozess. Daher sollte ein Anbieter keine Adressen in diesen Puffer setzen. Weitere Informationen zur MAPI-Spooler-Anmeldung finden Sie unter der [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) -Methode. 
  
Die meisten Speicheranbieter verwenden die [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) -Methode des Support-Objekts, das im _lpMAPISup_ -Parameter zum Speichern und Abrufen von Benutzeranmeldeinformationen und-Optionen übergeben wird. **OpenProfileSection** ermöglicht einem Speicheranbieter das Speichern zusätzlicher beliebiger Informationen in einem Profil Abschnitt und das Zuordnen zu einer bestimmten Ressource. Ein Speicheranbieter kann beispielsweise den Namen und das Kennwort eines Benutzers speichern, die einer Ressource zugeordnet sind, sowie alle Pfade oder andere Informationen, die für den Zugriff auf diese Ressource benötigt werden. 
  
Eigenschaften mit Eigenschafts Bezeichnern 0x6600 bis 0x67FF sind sichere Eigenschaften, die dem Anbieter zur eigenen Verwendung zum Speichern privater Daten in Profil Abschnitten zur Verfügung stehen. Weitere Informationen zu den Verwendungsmöglichkeiten von Eigenschaften in Profil Abschnitts Objekten finden Sie unter der [IProfSect: IMAPIProp](iprofsectimapiprop.md) -Methode. 
  
Zusätzlich zu privaten Daten in Eigenschaften mit Bezeichnern 0x6600 bis 0x67FF sollte der Informationsspeicher Anbieter Informationen für die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft im Profil Abschnitt bereitstellen. Sie sollte den Anzeigenamen des Anbieters selbst **PR_DISPLAY_NAME** – eine identifizierende Zeichenfolge (beispielsweise "Microsoft Personal Information Store"), die für die Benutzer angezeigt wird, damit Sie diesen Nachrichtenspeicher von anderen Benutzern unterscheiden können, auf die Sie möglicherweise Zugriff haben. An. **PR_DISPLAY_NAME** enthält häufig einen Servernamen, einen Benutzerkontonamen oder einen Pfad. 
  
Einige Profil Abschnittseigenschaften sind in der Nachrichtenspeichertabelle sichtbar. andere sind während der Installation und Konfiguration des MAPI-Subsystems sichtbar. Der Anbieter bietet in der Regel Informationen zu diesen sichtbaren Eigenschaften für einen neuen Profil Abschnitt, der noch keine gespeicherten Anmeldeinformationen oder privaten Informationen enthält, und wenn er feststellt, dass sich Eigenschaftsinformationen geändert haben. Weitere Informationen zu Profil Abschnitten finden Sie unter [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md).
  
Nach der erfolgreichen Anmeldung eines Benutzers und vor der Wiederherstellung an MAPI sollte der Anbieter das Array von Eigenschaften für die Statuszeile für die Ressource erstellen und die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aufrufen. 
  
 **Anmelde** Anrufe, die bereits für die aktuelle MAPI-Sitzung geöffnete Nachrichtenspeicher öffnen, überspringen einen Großteil der zuvor beschriebenen Verarbeitung. Mit diesen Aufrufen werden keine Statuszeilen erstellt, Anmeldeobjekte für den Nachrichtenspeicher zurückgegeben, **AddRef** für das MAPI-Support Objekt aufgerufen oder Daten für die MAPI-Spooler-Anmeldung zurückgegeben. Diese Aufrufe geben S_OK zurück und geben ein Nachrichtenspeicherobjekt mit der angeforderten Schnittstelle zurück. 
  
Um solche Aufrufe zu identifizieren, sollte der Anbieter eine Liste im Nachrichtenspeicher-Anbieterobjekt von Speichern verwalten, die bereits für dieses Anbieterobjekt geöffnet sind. Bei der Verarbeitung eines **Anmelde** Anrufs sollte der Anbieter diese Liste der geöffneten Speicher überprüfen und ermitteln, ob der zu angemeldete Speicher bereits geöffnet ist. Wenn dies der Fall ist, müssen die Benutzeranmeldeinformationen nicht überprüft werden, und die Anzeige eines Dialogfelds sollte möglichst vermieden werden. Wenn Dialogfelder angezeigt werden müssen, sollte der Anbieter zurückgegebene Informationen überprüfen, um festzustellen, ob ein Speicher ein zweites Mal geöffnet wurde. Darüber hinaus sollte der Anbieter mithilfe von _lpEntryID_ zu Beginn der Verarbeitung von **Anmelde** anrufen nach doppelten Öffnungen suchen. 
  
Standard Verarbeitung für einen **Anmelde** Anruf, der auf einen geöffneten Speicher zugreift, lautet wie folgt: 
  
1. Der Informationsspeicher Anbieter ruft **AddRef** für das vorhandene Store-Objekt auf, wenn die angeforderte neue Schnittstelle mit der Schnittstelle für den vorhandenen Speicher identisch ist. Andernfalls wird **QueryInterface** aufgerufen, um die neue Schnittstelle abzurufen. Wenn der Informationsspeicher die neue Schnittstelle nicht unterstützt, sollte der Anbieter den Fehlerwert MAPI_E_INTERFACE_NOT_SUPPORTED zurückgeben. 
    
2. Der Anbieter gibt einen Zeiger auf die erforderliche Schnittstelle des vorhandenen Store-Objekts in _lppMDB_zurück.
    
3. Der Anbieter gibt in _lppMSLogon_ **null** zurück.
    
4. Der Anbieter sollte das Profil für das im Aufruf übergebene Support Objekt nicht öffnen. Darüber hinaus sollte er keinen Anbieter eindeutigen Bezeichner registrieren, eine Statuszeile registrieren oder MAPI-Spooler-Anmeldedaten zurückgeben.
    
5. Der Anbieter sollte nicht **AddRef** für das Support-Objekt aufrufen, da es keinen Zeiger auf das Objekt erfordert. 
    
Wenn möglich, sollten Anbieter entsprechende Fehler-und Warn Zeichenfolgen für **Anmelde** Aufrufe zurückgeben, da dadurch die Benutzerbelastung erheblich erleichtert wird, wenn Sie ermitteln, warum etwas nicht funktioniert hat. Um diese Zeichenfolgen zurückzugeben, legt ein Anbieter die Member in der **MAPIERROR** -Struktur fest. MAPI sucht, verwendet und veröffentlicht die **MAPIERROR** -Struktur, wenn Sie von einem Anbieter zurückgegeben wird. 
  
Der Speicher für diese **MAPIERROR** -Struktur sollte mithilfe des Puffers zugewiesen werden, der in _LpfAllocateBuffer_ für den **MSProviderInit** -Aufruf übergeben wird. Alle in der zurückgegebenen Struktur enthaltenen Fehlerzeichenfolgen sollten im Unicode-Format vorliegen, wenn MAPI_UNICODE in der **Anmelde** _ulFlags_ festgelegt ist; andernfalls sollten Sie sich im ANSI-Zeichensatz befinden. 
  
Bei den meisten Fehlerwerten, die von der **Anmeldung**zurückgegeben werden, deaktiviert MAPI die Nachrichtendienste, zu denen der fehlerhafte Anbieter gehört. MAPI Ruft für die Lebensdauer der MAPI-Sitzung keine Anbieter auf, die zu diesen Diensten gehören. Wenn der MAPI_E_FAILONEPROVIDER- **** Fehlerwert von der Anmeldung zurückgegeben wird, deaktiviert MAPI hingegen den Nachrichtendienst, zu dem der Anbieter gehört. Bei der **Anmeldung** sollte MAPI_E_FAILONEPROVIDER zurückgegeben werden, wenn ein Fehler auftritt, der die Deaktivierung des gesamten Diensts für die Dauer der Sitzung nicht zulässt. Beispielsweise kann ein Anbieter diesen Fehler zurückgeben, wenn er die Anzeige einer Benutzeroberfläche nicht zulässt und ein erforderliches Kennwort nicht verfügbar ist. 
  
Wenn ein Anbieter MAPI_E_UNCONFIGURED von seiner Anmeldung zurückgibt, ruft MAPI die Nachrichtendienst-Eintrags Funktion des Anbieters auf und wiederholt die Anmeldung. MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext, um dem Dienst die Möglichkeit zu geben, sich selbst zu konfigurieren. Wenn der Client eine Benutzeroberfläche für die Anmeldung zulässt, kann der Dienst sein Konfigurationseigenschaften Blatt anzeigen, damit der Benutzerkonfigurationsinformationen eingeben kann.
  
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

