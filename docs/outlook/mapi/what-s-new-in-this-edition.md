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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329547"
---
# <a name="whats-new-in-this-edition"></a>Neuigkeiten in dieser Edition

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Microsoft Outlook 2013 MAPI-Referenz wurde aktualisiert und enthält Dokumentationen für verschiedene neue Features. 
  
## <a name="new-content"></a>Neuer Inhalt

Inhalte wurden für die folgenden Features hinzugefügt:
  
- Das Thema [Erste Schritte mit der MAPI-Referenz für outlook 2013](getting-started-with-the-outlook-mapi-reference.md) wurde aktualisiert und verweist auf umfassende Informationen zu Programmiermodellen für Ihre Outlook-und MAPI-Funktionalität, die Ihnen helfen, die am häufigsten verwendeten APIs und Technologien zu identifizieren. passend für Ihre Anforderungen. Links zu dem referenzierten technischen Artikel wurden auch in den folgenden Themen überarbeitet: 
    
  - [MAPI-Referenz für Outlook](outlook-mapi-reference.md)
    
  - [�bersicht �ber Outlook-MAPI-Referenz](outlook-mapi-reference-overview.md)
    
- **Beispiel für den Nachrichtenspeicher Anbieter**– der Beispielcode für den eingebundenen [PST-Speicheranbieter](message-store-provider-sample.md) wurde nun überarbeitet, um Outlook 2013 zu erkennen und aufzunehmen. Weitere Informationen finden Sie unter zuvor überarbeitete Inhalte in diesem Thema. 
    
- **Auto**vervollständigen-Stream – das Thema [Nickname-Cache](nickname-cache.md) , früher **Nk2-Datei Format**, wurde aktualisiert, um änderungen in Outlook 2013 sowie Outlook 2010 widerzuspiegeln. Die folgenden Themen wurden jetzt überarbeitet, um Informationen zu den Richtlinien für das NK2-Dateiformat für Microsoft Outlook 2003/Microsoft Office Outlook 2007 und zur Binärdatei Analyse bereitzustellen. Weitere Informationen finden Sie unter zuvor überarbeitete Inhalte in diesem Thema.
    
  - [MAPI-Profile](mapi-profiles.md)
    
  - [Cache für Spitznamen](nickname-cache.md)
    
  - [AutoVervollständigen-Stream](autocomplete-stream.md)
    
- **Interfaces**– das [IAddrBook:: OpenEntry](iaddrbook-openentry.md) -Thema dokumentiert eine Methode zum Öffnen eines Adressbucheintrags und zum Zurückgeben eines Zeigers auf die Schnittstelle, die für den Zugriff verwendet wird. Es enthielt zuvor eine Kennzeichnung im *ulFlags* -Parameter **MAPI_GAL_ONLY**, die verwendet werden konnte, um die globale Adressliste (GAL) zu öffnen, und wurde geändert, um Ihre Definition einzuschließen.
    
- **Eigenschaften**– das Thema **PR_CONVERSATION_KEY** Named Property ([pidtagconversationkey (Canonical Property](pidtagconversationkey-canonical-property.md)) wurde hinzugefügt und bezieht sich auf **IPM. MessageManager** -Nachrichten nur in Outlook MAPI. Die folgenden Themen im Zusammenhang mit diesem und der TNEF-Stream-Dokumentation (Transport-Neutral Encapsulation Format) wurden überarbeitet: 
    
  - [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Zuordnen von TNEF-Attributen zu MAPI-Eigenschaften](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID und attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Zuvor überarbeitete Inhalte

In früheren Versionen der Outlook-MAPI-Referenz wurden Inhalte für die folgenden Features hinzugefügt:
  
- Microsoft Outlook 2013 ermöglicht nicht-herkömmliche Bereitstellungsszenarien wie Side-by-Side und Click-to-Run. Diese Szenarien können die Logik, die zum Laden der richtigen MAPI-Bibliothek verwendet wird, erschweren. MAPI-Entwickler haben jetzt die Möglichkeit, explizit mit MAPI-Funktionen zu verknüpfen, und können explizit eine Verknüpfung mit dem MAPI-Stub des Standard-MAPI-Clients (beispielsweise msmapi32. dll von Outlook) herstellen, ohne die MAPI-Bibliothek und den Windows MAPI-Stub zu durchlaufen. Weitere Informationen zur expliziten Verknüpfung im Vergleich zur impliziten Verknüpfung finden Sie unter [Link zu MAPI Functions](how-to-link-to-mapi-functions.md). Die **MAPI-Stub-Bibliothek**, die auf der [codeplex](https://mapistublibrary.codeplex.com/) -Website veröffentlicht wurde, bietet einen Ersatz für Mapi32. lib, der das Erstellen von 32-Bit-und 64-Bit-MAPI-Anwendungen unterstützt. 
    
- **Unterstützung für 64-Bit Microsoft Outlook**– Referenzthemen zu ANWENDBARen API-Elementen wurden aktualisiert und entsprechen neuen Headerdateien, die 64-Bit Outlook unterstützen. Diese Headerdateien stehen als Download unter [Outlook 2010: MAPI-Headerdateien](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1)zur Verfügung. Ein neues Codebeispiel wurde in [Überprüfen Sie die Version von Outlook](how-to-check-the-version-of-outlook.md) bereitgestellt, um zu zeigen, wie Sie überprüfen, ob die installierte Version von Outlook 64-Bit Microsoft Outlook 2010 ist und für Outlook 2013 überarbeitet wurde. Wenn Ihre vorhandene 32-Bit-MAPI-Anwendung auf einem 64-Bit-Betriebssystem mit 64-Bit Outlook installiert werden soll, müssen Sie Ihre 32-Bit-Anwendung als eine 64-Bit-Anwendung neu erstellen. Weitere Informationen zur MAPI-Unterstützung für 64-Bit-Outlook finden Sie unter [Erstellen von MAPI-Anwendungen auf 32-Bit-und 64-Bit-Plattformen](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Beispiel für Nachrichtenspeicher Anbieter**– der beispielhafte [PST-Speicheranbieter](message-store-provider-sample.md) wurde zuvor zur Unterstützung der 64-Bit-Architektur aktualisiert. Das Beispiel das [Initialisieren eines EingebundenEN PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md) wurde erweitert, um Informationen zu den "umbrochenen PST-und Unicode-Pfaden" bereitzustellen. 
    
- **Auto**vervollständigen-Stream – das Thema [Nickname-Cache](nickname-cache.md) , früher **Nk2-Datei Format**, wurde aktualisiert, um änderungen in Outlook 2013 sowie Outlook 2010 widerzuspiegeln. Informationen wie die AutoVervollständigen-Liste, bei der es sich um die Liste der Namen handelt, die in den Bearbeitungsfeldern **an**, **CC**und **Bcc** angezeigt werden, während ein Benutzer eine e-Mail verfaßt, wird nun im AutoVervollständigen- [Stream](autocomplete-stream.md) einer Nachricht auf dem lokalen Computer gespeichert. anstatt Sie in einer Datei wie in Outlook 2007 zu speichern. 
    
  - Interagieren mit dem Stream "AutoVervollständigen"
    
  - Laden des AutoVervollständigen-Streams
    
  - Speichern des AutoVervollständigen-Streams
    
- **Unterstützung für schnelles Herunterfahren für MAPI-Clients**– MAPI-Clients können nun ein schnelles Herunterfahren initiieren und das MAPI-Subsystem hat geladene Anbieter benachrichtigt, um Datenverluste beim schnellen Herunterfahren zu minimieren. Für den Client und den Anbieter wurden zusätzliche Schnittstellen hinzugefügt, um das schnelle Herunterfahren zu unterstützen. Weitere Informationen zum schnellen Herunterfahren finden Sie unter [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md).
    
- **Streamstruktur für Felddefinitionen für ein Outlook-Element**– Dokumentation für einen binären Stream für die [pidlidpropertydefinitionstream (](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft wurde hinzugefügt. Diese Eigenschaft gibt Definitionen aller benutzerdefinierten Felder und Datenbindungseinstellungen für integrierte Felder eines Outlook-Elements an. 
    
- **Außerkraftsetzung für persönliche Speicher**– die folgenden Schnittstellen und ihre entsprechenden Methoden wurden hinzugefügt, um die Überschreibung der **PSTDisableGrow** -Richtlinie für persönliche Ordner-Dateien (PST) zu unterstützen: 
    
    [IPSTOVERRIDEREQ:: IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1:: IUnknown](ipstoverride1iunknown.md)
    
- **Verwenden mehrerer Exchange-Konten**– Dokumentation für die [MAPI-Adressbuch-API](using-multiple-exchange-accounts.md) wurde hinzugefügt. Diese API wurde zur Unterstützung mehrerer Exchange-Konten in Microsoft Outlook 2010 erweitert und umfasst jetzt Microsoft Outlook 2013. Um Adressen ordnungsgem�� mit mehreren Exchange-Konten zu beheben, verwenden Sie die neuen Funktionen, die einen Konto Kontext ergreifen, damit Anrufe im Adressbuch das richtige Exchange-Konto suchen. 
    
- **MAPI-Dateiformate**– MAPI-Konfigurationsinformationen wurden erweitert, um zu erläutern, wie Sie Pfade beim [Registrieren von Diensten und Dienstanbietern in MapiSvc. inf](registering-services-and-service-providers-in-mapisvc-inf.md)verwenden können.
    
- **Properties**– die folgenden gekennzeichneten Eigenschaften wurden zusätzlich zur dokumentation zu 38 anderen markierten Eigenschaften und benannten Eigenschaften hinzugefügt, die zuvor hinzugefügt wurden:
    
  - [Pidtagaddressbookchoosedirectoryautomatically (](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [Pidtagassociatedsharingprovider (](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [Pidtagroamingbinary (](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [Pidtagstoreentryidemsmdbv1 (](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **MAPI-Konstanten**– die konsolidierten [MAPI-Konstanten](mapi-constants.md) wurden erweitert. In früheren Versionen wurden Sie in einer Reihe von Themen verteilt, aber jetzt in einem einzigen Thema gesammelt, um Sie einfacher zu finden und zu verwenden. Sie wurden auch erweitert, um eine umfassendere Abdeckung einschließlich der folgenden Abschnitte bereitzustellen: 
    
  - Definitionen für Exchange-Adressbuch-und Nachrichtenspeicher-Fehler Codes
    
  - Definitionen für Exchange Server-Postfachcache-Kontingente
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

