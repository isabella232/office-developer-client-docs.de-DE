---
title: Neuigkeiten in dieser Edition
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392886"
---
# <a name="whats-new-in-this-edition"></a>Neuigkeiten in dieser Edition

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2013 MAPI-Referenz wurde aktualisiert, um die Dokumentation für verschiedene neue Features enthalten. 
  
## <a name="new-content"></a>Neue Inhalte

Inhalt wurde für die folgenden Features hinzugefügt:
  
- Das Thema [Erste Schritte mit Outlook 2013 MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md) wurde aktualisiert, um umfassende Informationen zu Ihrer Outlook- und MAPI-Funktionen, mit denen Sie den APIs und Technologien, die meisten sind, Programmiermodellen verweisen für Ihre Zwecke geeignet. Links zu technischen Artikel verwiesen wird, wurde auch in den folgenden Themen überarbeitet: 
    
  - [MAPI-Referenz für Outlook](outlook-mapi-reference.md)
    
  - [Übersicht über die Outlook-MAPI-Referenz](outlook-mapi-reference-overview.md)
    
- **Nachricht Store Provider Example**– der Code [Sample umfließendem PST Store Provider](message-store-provider-sample.md) wurde erkannt und Outlook 2013 aufzunehmen jetzt überarbeitet. Weitere Informationen finden Sie unter zuvor überarbeitet Inhalt in diesem Thema. 
    
- **AutoVervollständigen Stream**– das Thema [Nickname-Cache](nickname-cache.md) , früher das **Dateiformat Nk2**, um Änderungen in Outlook 2013 sowie Outlook 2010 aktualisiert wurde. In den folgenden Themen haben jetzt überarbeitet, um Informationen über die NK2 File Format Developer Richtlinien für Microsoft Outlook 2003 und Microsoft Office Outlook 2007 und Analysieren Binärdatei bereitstellen. Weitere Informationen finden Sie unter zuvor überarbeitet Inhalt in diesem Thema.
    
  - [MAPI-Profile](mapi-profiles.md)
    
  - [Cache für Spitznamen](nickname-cache.md)
    
  - [Stream für automatisches Vervollständigen](autocomplete-stream.md)
    
- **Schnittstellen**-das [IAddrBook::OpenEntry](iaddrbook-openentry.md) Thema beschreibt eine Methode zum Öffnen eines Adresseintrags Adressbuch und Zurückgeben von einen Zeiger auf die Schnittstelle verwendet, um darauf zugreifen. Sie enthalten zuvor ein Flag in den *UlFlags* -Parameter **MAPI_GAL_ONLY**, die zum Öffnen der globalen Adressliste (GAL), nur verwendet werden können und wurde überarbeitet, um dessen Definition enthalten.
    
- **Eigenschaften**– die **PR_CONVERSATION_KEY** mit dem Namen Thema-Eigenschaft ([PidTagConversationKey kanonische-Eigenschaft](pidtagconversationkey-canonical-property.md)) hinzugefügt wurde und bezieht sich auf **IPM. Nachrichten-Managers** nur im Outlook-MAPI-Nachrichten. In den folgenden Themen im Zusammenhang mit es und der Transport-Neutral Encapsulation Format (TNEF) Stream Dokumentation wurde überarbeitet: 
    
  - [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Zuordnung von TNEF-Attributen zu MAPI-Eigenschaften](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID und attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Zuvor überarbeiteten Inhalten

Inhalt wurde in früheren Versionen von Outlook-MAPI-Referenz für die folgenden Features hinzugefügt:
  
- Microsoft Outlook 2013 ermöglicht nicht traditionellen Bereitstellungsszenarien wie Side-by-Side und Klick-und-los. Diese Szenarien können die Logik verwendet, um die richtige MAPI-Bibliothek laden erschweren. MAPI-Entwickler die Möglichkeit, verknüpfen explizit mit MAPI-Funktionen, und alle explizit mit den MAPI-Stub der Standard-MAPI-Client (z. B. von Msmapi32.dll von Outlook) verknüpfen auswählen können, ohne Umweg über die MAPI-Bibliothek und den Windows-MAPI-Stub. Weitere Informationen zu explizite Verknüpfung beim Vergleich implizite Verknüpfung finden Sie unter [Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md). Die **MAPI-Stub-Bibliothek**auf der [CodePlex](https://mapistublibrary.codeplex.com/) -Website veröffentlicht bietet Technik Ersatz für Mapi32.lib, die Erstellung von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt. 
    
- **Unterstützung für 64-Bit-Microsoft Outlook**– Referenzthemen für zutreffend API-Elemente wurden aktualisiert, um die neuen Headerdateien entsprechen, die 64-Bit-Outlook unterstützen. Diese Headerdateien stehen als Download an [Outlook 2010: MAPI-Headerdateien](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Ein neues Codebeispiel wurde in wird gezeigt, wie Sie überprüfen, ob die installierte Version von Outlook 64-Bit-Microsoft Outlook 2010 ist und für Outlook 2013 überarbeitet wurde [Überprüfen der Version von Outlook](how-to-check-the-version-of-outlook.md) bereitgestellt. Wenn Ihre vorhandene 32-Bit-MAPI-Anwendung auf einem 64-Bit-Betriebssystem mit 64-Bit-Outlook installiert ausgeführt werden soll, müssen Sie die 32-Bit-Anwendung als 64-Bit-Anwendung neu erstellen. Weitere Informationen zu MAPI-Unterstützung für 64-Bit-Outlook finden Sie unter [Erstellen von MAPI-Anwendungen auf 32-Bit- und 64-Bit-Plattformen](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Nachricht Store Provider Example**– der [Umbrochen PST Store Beispielanbieter](message-store-provider-sample.md) zuvor zur Unterstützung der 64-Bit-Architektur aktualisiert wurde. Im Beispiel [einem umfließendem PST-Anbieter initialisieren](initializing-a-wrapped-pst-store-provider.md) Thema wurde jetzt erweitert, um Informationen über die "Wrapped PST und Unicode-Pfade." 
    
- **AutoVervollständigen Stream**– das Thema [Nickname-Cache](nickname-cache.md) , früher das **Dateiformat Nk2**, wurde aktualisiert, um die Änderungen in Outlook 2013 sowie Outlook 2010 aktualisiert. Informationen wie die AutoVervollständigen-Liste, die die Liste der Namen, die in der **an**, **Cc**und **Bcc** Bearbeitungsfelder angezeigt wird, während ein Benutzer eine e-Mail-Nachricht erstellt wird, ist nun an den [Stream AutoVervollständigen](autocomplete-stream.md) einer Nachricht auf dem lokalen Computer gespeichert. statt in eine Datei wie in Outlook 2007 speichern. 
    
  - Interaktion mit dem AutoVervollständigen-Stream
    
  - Laden den AutoVervollständigen-Stream
    
  - Speichern den AutoVervollständigen-Stream
    
- **Schnelles Herunterfahren Unterstützung für MAPI-Clients**– MAPI-Clients können jetzt ein Schnelles Herunterfahren initiieren und MAPI-Subsystems zu minimieren Verlust von Daten über das schnelle Herunterfahren geladenen Anbieter zu benachrichtigen. Zusätzliche Schnittstellen wurden für die Client- und Anbieter zur Unterstützung von schnellen Herunterfahren hinzugefügt. Weitere Informationen zu Schnelles Herunterfahren finden Sie unter [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md).
    
- **Stream-Struktur für Felddefinitionen für ein Outlook-Element**– Dokumentation für einen binären Datenstrom für die [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft wurde hinzugefügt. Diese Eigenschaft gibt die Definitionen aller benutzerdefinierten Felder und Datenbindung Einstellungen für integrierte Felder eines Outlook-Elements an. 
    
- **Persönliche speichern außer Kraft setzen**– die folgenden Schnittstellen und ihre entsprechenden Methoden zur Unterstützung von Überschreiben der Persönliche Ordner-Datei (PST) Store Anbieter **PSTDisableGrow** Richtlinie hinzugefügt wurden: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Verwenden mehrerer Exchange-Konten**– Dokumentation für die [MAPI-Address Book-API](using-multiple-exchange-accounts.md) wurde hinzugefügt. Diese API wurde verbessert, um die Unterstützung mehrerer Exchange-Konten in Microsoft Outlook 2010 und umfasst jetzt Microsoft Outlook 2013. Um Adressen ordnungsgem�� mit mehreren Exchange-Konten zu beheben, verwenden Sie die neuen Funktionen, die einen Konto Kontext ergreifen, damit Anrufe im Adressbuch das richtige Exchange-Konto suchen. 
    
- **MAPI-Dateiformaten**– MAPI-Konfigurationsinformationen wurde erweitert, um zu erläutern, wie Sie Pfade in [Registrieren von Diensten und Dienstanbieter MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md)verwenden können.
    
- **Eigenschaften**, die folgenden markierten Eigenschaften wurden zusammen mit der Dokumentation für 38 andere Eigenschaften markiert und Eigenschaften, die zuvor hinzugefügten Namen hinzugefügt:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI-Konstanten**– die konsolidierte [MAPI-Konstanten](mapi-constants.md) erweitert wurden. In früheren Versionen klicken sie in einer Reihe von Themen verteilt wurden, jedoch werden nun in einem einzigen Thema, damit sie einfacher zu erkennen und verwenden erfasst. Sie haben auch erweitert, um mehr ausführlich behandelt, einschließlich in den folgenden Abschnitten bereitzustellen: 
    
  - Definitionen für Exchange-Adressbuch und Nachrichtenspeicher-Fehlercodes
    
  - Definitionen für Exchange Server-Postfach-Cache-Modus von Kontingenten
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

