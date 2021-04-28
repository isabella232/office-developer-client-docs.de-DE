---
title: Neues in dieser Edition
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Letzte Änderung: 09. Februar 2020'
ms.openlocfilehash: 3a3d38d83311b63686a2379c3321194e538ff840
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061328"
---
# <a name="whats-new-in-this-edition"></a>Neues in dieser Edition

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Microsoft Outlook MAPI Reference wurde aktualisiert, um Dokumentation für verschiedene neue Features zu enthalten. 
  
## <a name="new-content"></a>Neue Inhalte

Für die folgenden Features wurden Inhalte hinzugefügt:
  
- Das Thema Erste Schritte mit der [Outlook 2013-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md) wurde aktualisiert, um auf umfassende Informationen zu Programmiermodellen für Ihre Outlook- und MAPI-Funktionen zu verweisen, damit Sie die APIs und Technologien identifizieren können, die für Ihre Anforderungen am besten geeignet sind. Links zu dem referenzierten technischen Artikel wurden auch in den folgenden Themen überarbeitet: 
    
  - [MAPI-Referenz für Outlook](outlook-mapi-reference.md)
    
  - [�bersicht �ber Outlook-MAPI-Referenz](outlook-mapi-reference-overview.md)
    
- **Beispiel Store** Anbieter für Nachrichten – Der Code des Store-Anbieters [Store](message-store-provider-sample.md) Beispiel wurde überarbeitet, um 2013 zu erkennen und Outlook zu können. Weitere Informationen finden Sie unter Previously Revised Content in this topic. 
    
- **Autocomplete Stream** [](nickname-cache.md) – Das Thema Spitzname-Cache, früher **das Nk2-Dateiformat,** wurde aktualisiert, um Änderungen in Outlook 2013 und Outlook 2010 widerzuspiegeln. Die folgenden Themen wurden nun überarbeitet, um Informationen zu den Entwicklerrichtlinien für das .nk2-Dateiformat für Microsoft Outlook 2003/Microsoft Office Outlook 2007 und die Binärdatei parsing zu erhalten. Weitere Informationen finden Sie unter Previously Revised Content in this topic.
    
  - [MAPI-Profile](mapi-profiles.md)
    
  - [Cache für Spitznamen](nickname-cache.md)
    
  - [Autocomplete Stream](autocomplete-stream.md)
    
- **Schnittstellen**– Das [Thema IAddrBook::OpenEntry](iaddrbook-openentry.md) dokumentiert eine Methode zum Öffnen eines Adressbucheintrags und zurückgeben eines Zeigers auf die Schnittstelle, die für den Zugriff darauf verwendet wird. Er enthielt zuvor ein Flag im  *ulFlags-Parameter* **MAPI_GAL_ONLY**, das nur zum Öffnen der globalen Adressliste (GAL) verwendet werden konnte, und wurde überarbeitet, um seine Definition zu enthalten.
    
- **Properties**– Das **PR_CONVERSATION_KEY** benannte Eigenschaft ([PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md)) wurde hinzugefügt und bezieht sich auf **IPM. MessageManager-Nachrichten** in Outlook MAPI. Die folgenden Themen zu diesem Thema und die Transport-Neutral Encapsulation Format (TNEF)-Streamdokumentation wurden überarbeitet: 
    
  - [Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Zuordnung von TNEF-Attributen zu MAPI-Eigenschaften](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID und attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>MAPI-Initialisierungsmonitor  

- Es gibt Zeiten, in denen eine Anwendung, die MAPI verwendet, wissen möchte, wann die Initialisierung abgeschlossen ist. Sie verfügt beispielsweise über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion darauf, dass MAPI initialisiert wird, möchte die Anwendung einige Aufgaben ausführen, möchte aber nicht immer den MAPI-Stapel spinn.  Der Initialisierungsmonitor stellt diese Funktionalität über eine Funktion (exportiert aus OLMAPI32.DLL) und einige einfache Schnittstellen bereit, die unten beschrieben werden. 

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor) 

- Dies ist ein Einstiegspunkt, der aus OLMAPI32.DLL dadurch kann der Aufrufer eine Schnittstelle abrufen, um den aktuellen Initialisierungsstatus abzurufen, einen Rückruf für den Initialisierungsabschluss einrichten oder den aktuellen Thread blockieren, bis er abgeschlossen ist.  Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur vom Thread, der es abgerufen hat.  Im Gegensatz zu anderen Objekten, die von MAPI verfügbar gemacht werden, ist dieses Objekt auch gültig, solange die DLL geladen wird, sie kann in initialisierungssitzungen erneut verwendet werden und vor oder nach dem Aufrufen von MAPIInitialize verwendet werden. Gibt Erfolg oder Fehler über ein COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen out-Parameter zu. 

### <a name="interface-imapiinitmonitor"></a>Schnittstelle: IMAPIInitMonitor 

**IFACEMETHODIMP_(BOOL) IsInitialized()**
- Gibt den aktuellen Status der MAPI-Initialisierung zurück. 

**IFACEMETHODIMP Wait(DWORD timeout)**
- Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde.  INFINITE kann für unendliche Wartezeiten verwendet werden. 

**IFACEMETHODIMP BeginWait(DWORD timeout, IMAPIWaitResult ppResult)**
- Starten Sie eine Wartezeit auf die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden bis zum Verstreichen.   Dadurch wird eine IMAPIWaitResult-Schnittstelle zurück, die "End" aufgerufen haben sollte, um mit dem Warten zu beginnen.  Dadurch kann der Aufrufer steuern, welcher Thread während der Wartezeit blockiert wird. 

### <a name="interface-imapiwaitresult"></a>Schnittstelle IMAPIWaitResult
**AUßERKRAFTSETZUNG von IFACEMETHODIMP End()**
- Wird aufgerufen, um das Blockieren des Threads zu initiieren, in dem er aufgerufen wird, muss es sich nicht um denselben Thread wie "BeginWait" handelt. 

    
## <a name="previously-revised-content"></a>Zuvor überarbeitete Inhalte

Inhalt wurde in früheren Versionen der Outlook mapI Reference für die folgenden Features hinzugefügt:
  
- Microsoft Outlook 2013 ermöglicht nicht herkömmliche Bereitstellungsszenarien, z. B. nebeneinander und Klick-und-Aus. Diese Szenarien können die Logik zum Laden der richtigen MAPI-Bibliothek erschweren. MAPI-Entwickler haben jetzt die Möglichkeit, explizit mit MAPI-Funktionen zu verknüpfen, und können eine explizite Verknüpfung mit dem MAPI-Stub des standardmäßigen MAPI-Clients (z. B. Msmapi32.dll von Outlook) ohne die MAPI-Bibliothek und den Windows-MAPI-Stub verwenden. Weitere Informationen zur expliziten Verknüpfung im Vergleich zu impliziten Verknüpfungen finden Sie [unter Link to MAPI Functions](how-to-link-to-mapi-functions.md). Die auf der [CodePlex-Website](https://mapistublibrary.codeplex.com/) veröffentlichte **MAPI-Stubbibliothek** bietet einen Drop-In-Ersatz für Mapi32.lib, der das Erstellen von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt. 
    
- **Unterstützung für 64-Bit-Microsoft Outlook**– Referenzthemen für anwendbare API-Elemente wurden aktualisiert, um neuen Headerdateien zu entsprechen, die 64-Bit-Outlook. Diese Headerdateien stehen als Download unter [Outlook 2010 zur Verfügung: MAPI-Headerdateien](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Ein neues Codebeispiel wurde unter Überprüfen der Version von [Outlook](how-to-check-the-version-of-outlook.md) bereitgestellt, um zu überprüfen, ob die installierte Version von Outlook 64-Bit-Microsoft Outlook 2010 ist und für Outlook 2013 überarbeitet wurde. Wenn Ihre vorhandene 32-Bit-MAPI-Anwendung unter einem 64-Bit-Betriebssystem ausgeführt wird, auf dem 64-Bit-Outlook installiert ist, müssen Sie Ihre 32-Bit-Anwendung als 64-Bit-Anwendung neu erstellen. Weitere Informationen zur MAPI-Unterstützung für 64-Bit-Outlook finden Sie unter [Building MAPI Applications on 32-Bit and 64-Bit Platforms](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Beispiel Store** Anbieter für Nachrichten – Der Beispielanbieter für umschlossene [PST Store](message-store-provider-sample.md) wurde zuvor aktualisiert, um die 64-Bit-Architektur zu unterstützen. Das Thema [Initializing a Wrapped PST Store Provider des](initializing-a-wrapped-pst-store-provider.md) Beispiels wurde nun erweitert, um Informationen zu den "Umschlossenen PST- und Unicode-Pfaden" zur Verfügung zu stellen. 
    
- **Autocomplete Stream** [](nickname-cache.md) – Das Thema Nickname cache, vormalig **Nk2 File Format,** wurde aktualisiert, um Änderungen in Outlook 2013 und Outlook 2010 widerzuspiegeln. Informationen wie die Liste der automatischen Vervollständigungen, bei der es sich um die Liste der Namen handelt, die in [](autocomplete-stream.md) den Bearbeitungsfeldern **An,** **Cc** und **Bcc** angezeigt werden, während ein Benutzer eine E-Mail erstellt, werden jetzt im Automatischen Vervollständigungsstream einer Nachricht auf dem lokalen Computer gespeichert, anstatt sie in einer Datei wie in Outlook 2007 zu speichern. 
    
  - Interagieren mit dem AutoComplete Stream
    
  - Laden des Automatischen Vervollständigungsstreams
    
  - Speichern des Automatischen Vervollständigungsstreams
    
- Unterstützung für schnelles Herunterfahren für **MAPI-Clients**– MAPI-Clients können jetzt ein schnelles Herunterfahren initiieren und das MAPI-Subsystem die geladenen Anbieter benachrichtigen lassen, um datenverluste durch schnelles Herunterfahren zu minimieren. Für den Client und den Anbieter wurden zusätzliche Schnittstellen hinzugefügt, um schnelles Herunterfahren zu unterstützen. Weitere Informationen zum schnellen Herunterfahren finden Sie unter [Client Shutdown in MAPI](client-shutdown-in-mapi.md).
    
- **Streamstruktur für Felddefinitionen für ein Outlook -Dokumentation** für einen binären Datenstrom für die [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) wurde hinzugefügt. Diese Eigenschaft gibt Definitionen aller benutzerdefinierten Felder und Datenbindungseinstellungen für integrierte Felder eines Outlook an. 
    
- **Persönliche Store Außerkraftsetzung**– Die folgenden Schnittstellen und die entsprechenden Methoden wurden hinzugefügt, um das Außerkraftsetzen der **PstDisableGrow-Richtlinie (Personal** Folders File, PST)-Speicheranbieter zu unterstützen: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Using Multiple Exchange Accounts**– Documentation for the [MAPI Address Book API](using-multiple-exchange-accounts.md) was added. Diese API wurde erweitert, um mehrere Exchange in Microsoft Outlook 2010 zu unterstützen und enthält jetzt Microsoft Outlook 2013. Um Adressen ordnungsgem�� mit mehreren Exchange-Konten zu beheben, verwenden Sie die neuen Funktionen, die einen Konto Kontext ergreifen, damit Anrufe im Adressbuch das richtige Exchange-Konto suchen. 
    
- **MAPI-Dateiformate**– MapI-Konfigurationsinformationen wurden erweitert, um zu erläutern, wie Sie Pfade unter Registrieren von Diensten und [Dienstanbietern in MapiSvc.inf verwenden können.](registering-services-and-service-providers-in-mapisvc-inf.md)
    
- **Eigenschaften**– Die folgenden markierten Eigenschaften wurden zusätzlich zur Dokumentation für 38 weitere markierte und benannte Eigenschaften hinzugefügt, die zuvor hinzugefügt wurden:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI-Konstanten**– Die konsolidierten [MAPI-Konstanten](mapi-constants.md) wurden erweitert. In früheren Versionen wurden sie in einer Reihe von Themen verteilt, aber jetzt in einem einzigen Thema gesammelt, um sie leichter zu entdecken und zu verwenden. Sie wurden auch erweitert, um eine umfassendere Abdeckung zu bieten, einschließlich der folgenden Abschnitte: 
    
  - Definitionen Exchange Adressbuch- und Store-Fehlercodes
    
  - Definitionen für Exchange Server postfachcached Mode Quotas
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

