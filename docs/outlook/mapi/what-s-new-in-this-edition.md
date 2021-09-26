---
title: Neuigkeiten in dieser Edition
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Last modified: February 09, 2020'
ms.openlocfilehash: a35e9ce774c0228014faa902e6768547a8b4fd92
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619463"
---
# <a name="whats-new-in-this-edition"></a>Neuigkeiten in dieser Edition

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Microsoft Outlook MAPI-Referenz wurde aktualisiert, um Dokumentationen für verschiedene neue Features einzuschließen. 
  
## <a name="new-content"></a>Neuer Inhalt

Für die folgenden Features wurde Inhalt hinzugefügt:
  
- Das Thema ["Erste Schritte mit der MAPI-Referenz für Outlook 2013"](getting-started-with-the-outlook-mapi-reference.md) wurde aktualisiert, um auf umfassende Informationen zu Programmiermodellen für Ihre Outlook und MAPI-Funktionen zu verweisen, mit denen Sie die APIs und Technologien ermitteln können, die für Ihre Anforderungen am besten geeignet sind. Links zum referenzierten technischen Artikel wurden auch in den folgenden Themen überarbeitet: 
    
  - [MAPI-Referenz für Outlook](outlook-mapi-reference.md)
    
  - [�bersicht �ber Outlook-MAPI-Referenz](outlook-mapi-reference-overview.md)
    
- **Message Store Provider Example**- The [Sample Wrapped PST Store Provider](message-store-provider-sample.md) code has now been revised to recognize and accommodate Outlook 2013. Weitere Informationen finden Sie unter "Zuvor überarbeiteter Inhalt" in diesem Thema. 
    
- Stream für **automatisches Vervollständigen**– Das [Spitznamencachethema,](nickname-cache.md) früher **Nk2-Dateiformat,** wurde aktualisiert, um Änderungen in Outlook 2013 und Outlook 2010 widerzuspiegeln. Die folgenden Themen wurden nun überarbeitet, um Informationen zu den NK2-Dateiformat-Entwicklerrichtlinien für Microsoft Outlook 2003/Microsoft Office Outlook 2007 und binäre Dateiparsing bereitzustellen. Weitere Informationen finden Sie unter "Zuvor überarbeiteter Inhalt" in diesem Thema.
    
  - [MAPI-Profile](mapi-profiles.md)
    
  - [Cache für Spitznamen](nickname-cache.md)
    
  - [Stream für automatisches Vervollständigen](autocomplete-stream.md)
    
- **Schnittstellen**– Das [IAddrBook::OpenEntry-Thema](iaddrbook-openentry.md) dokumentiert eine Methode zum Öffnen eines Adressbucheintrags und zum Zurückgeben eines Zeigers auf die Schnittstelle, die für den Zugriff darauf verwendet wird. Es enthielt zuvor ein Flag im  *ulFlags-Parameter,* **MAPI_GAL_ONLY**, das nur zum Öffnen der globalen Adressliste (GAL) verwendet werden konnte, und wurde überarbeitet, um seine Definition einzuschließen.
    
- **Eigenschaften**– Das Thema **PR_CONVERSATION_KEY** benannten Eigenschaft ([Kanonische PidTagConversationKey-Eigenschaft](pidtagconversationkey-canonical-property.md)) wurde hinzugefügt und bezieht sich auf **IPM. MessageManager-Nachrichten** nur in Outlook MAPI. Die folgenden Themen zu diesem Thema und die Dokumentation zum Transport-Neutral Kapselungsformat (Encapsulation Format, TNEF) wurden überarbeitet: 
    
  - [Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Zuordnen von TNEF-Attributen zu MAPI-Eigenschaften](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID und attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>MAPI-Initialisierungsmonitor  

- Es gibt Fälle, in denen eine Anwendung, die MAPI nutzt, wissen möchte, wann die Initialisierung abgeschlossen ist. Beispielsweise verfügen sie über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion auf die MAPI-Initialisierung möchte die Anwendung einige Aufgaben ausführen, aber nicht immer den MAPI-Stapel hochdrehen.  Der Initialisierungsmonitor stellt diese Funktionalität über eine Funktion (exportiert aus OLMAPI32.DLL) und einige einfache Schnittstellen bereit, die unten beschrieben werden. 

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor) 

- Dies ist ein Einstiegspunkt, der aus OLMAPI32.DLL der Aufrufer eine Schnittstelle abrufen kann, um den aktuellen Initialisierungsstatus abzurufen, einen Rückruf für den Abschluss der Initialisierung einzurichten oder den aktuellen Thread zu blockieren, bis er abgeschlossen ist.  Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur von Threads, die es abgerufen haben.  Im Gegensatz zu anderen Objekten, die von mapi verfügbar gemacht werden, ist dieses Objekt gültig, solange die DLL geladen ist, es kann in allen Initialisierungssitzungen wiederverwendet werden und vor oder nach dem Aufruf von MAPIInitialize genutzt werden. Gibt Erfolg oder Fehler über einen COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen Ausgabeparameter zu. 

### <a name="interface-imapiinitmonitor"></a>Schnittstelle: IMAPIInitMonitor 

**IFACEMETHODIMP_(BOOL) IsInitialized()**
- Gibt den aktuellen Status der MAPI-Initialisierung zurück. 

**IFACEMETHODIMP Wait(DWORD timeout)**
- Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgegeben wird, wenn die angegebene Anzahl von Millisekunden abgelaufen ist oder mapi initialisiert wurde.  INFINITE kann für eine unendliche Wartezeit verwendet werden. 

**IFACEMETHODIMP BeginWait(DWORD timeout, IMAPIWaitResult ppResult)**
- Starten Sie eine Wartezeit für die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden.   Dadurch wird eine IMAPIWaitResult-Schnittstelle zurückgegeben, bei der "End" aufgerufen werden sollte, um die Wartezeit zu beginnen.  Dadurch kann der Aufrufer steuern, welcher Thread während des Wartens blockiert wird. 

### <a name="interface-imapiwaitresult"></a>Schnittstelle IMAPIWaitResult
**Außerkraftsetzung von IFACEMETHODIMP End()**
- Wird aufgerufen, um die Blockierung abzuwarten, in dem Thread, in dem sie aufgerufen wird, muss nicht derselbe Thread sein, der "BeginWait" aufgerufen hat. 

    
## <a name="previously-revised-content"></a>Zuvor überarbeiteter Inhalt

Inhalte wurden in früheren Versionen der Outlook MAPI-Referenz für die folgenden Features hinzugefügt:
  
- Microsoft Outlook 2013 ermöglicht nicht herkömmliche Bereitstellungsszenarien, z. B. Nebeneinander und Klick-und-Los. Diese Szenarien können die Logik verkomplizieren, die zum Laden der richtigen MAPI-Bibliothek verwendet wird. MAPI-Entwickler haben jetzt die Möglichkeit, explizit mit MAPI-Funktionen zu verknüpfen, und können eine explizite Verknüpfung mit dem MAPI-Stub des Standardmäßigen MAPI-Clients (z. B. Msmapi32.dll von Outlook) auswählen, ohne die MAPI-Bibliothek und den Windows MAPI-Stub zu durchlaufen. Weitere Informationen zur expliziten Verknüpfung im Vergleich zur impliziten Verknüpfung finden Sie unter [Link zu MAPI-Funktionen.](how-to-link-to-mapi-functions.md) Die **MAPI-Stubbibliothek,** die auf der [CodePlex-Website](https://mapistublibrary.codeplex.com/) veröffentlicht wird, bietet einen Drop-In-Ersatz für Mapi32.lib, der das Erstellen von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt. 
    
- **Unterstützung für 64-Bit-Microsoft Outlook**– Referenzthemen zu entsprechenden API-Elementen wurden aktualisiert, um neuen Headerdateien zu entsprechen, die 64-Bit-Outlook unterstützen. Diese Headerdateien sind als Download unter [Outlook 2010 verfügbar: MAPI-Headerdateien.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1) Unter ["Überprüfen der Version von Outlook"](how-to-check-the-version-of-outlook.md) wurde ein neues Codebeispiel bereitgestellt, um zu überprüfen, ob die installierte Version von Outlook 64-Bit-Microsoft Outlook 2010 ist und für Outlook 2013 überarbeitet wurde. Wenn Ihre vorhandene 32-Bit-MAPI-Anwendung auf einem 64-Bit-Betriebssystem mit installiertem 64-Bit-Outlook ausgeführt wird, müssen Sie Ihre 32-Bit-Anwendung als 64-Bit-Anwendung neu erstellen. Weitere Informationen zur MAPI-Unterstützung für 64-Bit-Outlook finden Sie unter [Building MAPI Applications on 32-Bit and 64-Bit Platforms.](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)
    
- **Message Store Provider Example**- The [Sample Wrapped PST Store Provider](message-store-provider-sample.md) had previously been updated to support 64-bit architecture. Das Thema ["Initialisieren eines umschlossenen PST-Store Anbieters"](initializing-a-wrapped-pst-store-provider.md) im Beispiel wurde nun erweitert, um Informationen zum Thema "Umschlossene PST- und Unicode-Pfade" bereitzustellen. 
    
- Stream für **automatisches Vervollständigen**– Das [Spitznamencachethema,](nickname-cache.md) früher **Nk2-Dateiformat,** wurde aktualisiert, um Änderungen in Outlook 2013 und Outlook 2010 widerzuspiegeln. Informationen wie die AutoVervollständigen-Liste, bei der es sich um die Liste der Namen handelt, die in den Bearbeitungsfeldern **"An",** **"Cc"** und **"Bcc"** angezeigt werden, während ein Benutzer eine E-Mail erstellt, werden nun im Stream für automatisches [Vervollständigen](autocomplete-stream.md) einer Nachricht auf dem lokalen Computer gespeichert, anstatt sie in einer Datei wie in Outlook 2007 zu speichern. 
    
  - Interagieren mit dem Stream für automatisches Vervollständigen
    
  - Laden des Stream für automatisches Vervollständigen
    
  - Speichern des Stream für automatisches Vervollständigen
    
- **Unterstützung für schnelles Herunterfahren für MAPI-Clients**– MAPI-Clients können jetzt ein schnelles Herunterfahren initiieren und das MAPI-Subsystem geladene Anbieter benachrichtigen lassen, um Datenverluste durch das schnelle Herunterfahren zu minimieren. Für den Client und Anbieter wurden zusätzliche Schnittstellen hinzugefügt, um schnelles Herunterfahren zu unterstützen. Weitere Informationen zum schnellen Herunterfahren finden Sie unter ["Herunterfahren des Clients" in MAPI.](client-shutdown-in-mapi.md)
    
- **Datenstromstruktur für Felddefinitionen für ein Outlook Element**– Dokumentation für einen binären Datenstrom für die [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) wurde hinzugefügt. Diese Eigenschaft gibt Definitionen aller benutzerdefinierten Felder und Datenbindungseinstellungen für integrierte Felder eines Outlook Elements an. 
    
- **Persönliche Store Außerkraftsetzung**: Die folgenden Schnittstellen und die entsprechenden Methoden wurden hinzugefügt, um das Überschreiben der PST-Speicheranbieterrichtlinie (Personal Folders File, **PST)** zu unterstützen: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Verwenden mehrerer Exchange Konten**– Dokumentation für die [MAPI-Adressbuch-API](using-multiple-exchange-accounts.md) wurde hinzugefügt. Diese API wurde erweitert, um mehrere Exchange Konten in Microsoft Outlook 2010 zu unterstützen, und umfasst jetzt Microsoft Outlook 2013. Um Adressen ordnungsgem�� mit mehreren Exchange-Konten zu beheben, verwenden Sie die neuen Funktionen, die einen Konto Kontext ergreifen, damit Anrufe im Adressbuch das richtige Exchange-Konto suchen. 
    
- **MAPI-Dateiformate**– MAPI-Konfigurationsinformationen wurden erweitert, um zu erläutern, wie Sie Pfade in ["Registering Services and Service Providers in MapiSvc.inf"](registering-services-and-service-providers-in-mapisvc-inf.md)verwenden können.
    
- **Eigenschaften**– Die folgenden markierten Eigenschaften wurden zusätzlich zur Dokumentation für 38 andere markierte Eigenschaften und benannte Eigenschaften hinzugefügt, die zuvor hinzugefügt wurden:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI-Konstanten**: Die konsolidierten [MAPI-Konstanten](mapi-constants.md) wurden erweitert. In früheren Versionen wurden sie in einer Reihe von Themen verteilt, aber jetzt in einem einzigen Thema gesammelt, um ihnen die Suche und Verwendung zu erleichtern. Sie wurden auch erweitert, um eine umfassendere Abdeckung zu bieten, einschließlich der folgenden Abschnitte: 
    
  - Definitionen für Exchange Adressbuch- und Nachrichten-Store-Fehlercodes
    
  - Definitionen für Exchange Server Kontingente im Zwischenspeichermodus für Postfächer
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

