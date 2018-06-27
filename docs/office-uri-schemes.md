---
title: Office-URI-Schemas
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 834c4d2c2f47c6cc3f35423a7dfe3c13caf3d209
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790900"
---
# <a name="office-uri-schemes"></a>Office-URI-Schemas

## <a name="11-abstract"></a>1.1 EXPOSEE

Dieses Dokument definiert das Format von Uniform Resource Identifiers (URIs) für Office-Produktivitätsanwendungen. Das Schema wird in Microsoft Office 2010 Service Pack 2 und höher unterstützt, z. B. in den Microsoft Office 2013-Produkten für Windows und den Microsoft SharePoint 2013-Produkten. Es wird auch in Office für iPhone, Office für iPad und Office für Mac 2011 unterstützt.
  
## <a name="12-introduction"></a>1.2 EINFÜHRUNG

Dank dieser URI-Schemas können Office-Produktivitätsanwendungen mit verschiedenen Befehlen aufgerufen werden. Jede Anwendung erhält ein anders benanntes Schema, aber in allen Schemas gelten dieselben Regeln für den Aufbaus des URI (URI-Schema).
  
## <a name="13-uri-schema"></a>1.3 URI-SCHEMA

### <a name="full-schema"></a>Vollständiges Schema

< *Schemaname*  >:<  *Befehlsname*  >„|"<  *Befehlsargumentdeskriptor*  >„|"<  *Befehlsargument*  > 
  
Ein der Definition in diesem Dokument entsprechender URI kann ein oder mehrere Befehlsargumente aufweisen, die die Elemente < *Befehlsargumentdeskriptor*  > und <  *Befehlsargument*  > enthalten und durch den senkrechten Strich („|") getrennt sind. Wenn mehrere Befehlsargumente in einem URI enthalten sind, muss jedes Befehlsargument durch einen senkrechten Strich („|") vom nächsten Befehlsargument getrennt sein. 
  
Diese Schemas enthalten keine Autoritätskomponente, wie in RFC 3986, Abschnitt 3.2 definiert. Der Aufruf der in diesem Dokument angegebenen Befehle erfolgt im Kontext des Systems, das den Befehl aufruft. Wenn z. B. der URI „ms-excel:ofv|u|http://contoso/Q4/budget.xls" von einem Personalcomputer unter Microsoft Windows mit Microsoft Office 2013 aufgerufen wird, wird als Ergebnis erwartet, dass die lokale Installation von Microsoft Excel gestartet wird und Argumente zum Öffnen der Datei unter  *http://contoso/Q4/budget.xls*  im schreibgeschützten Modus an sie übergeben werden. Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können. 
  
Die Schemasyntax enthält Folgendes:
  
1. < *Schemaname*  >: Dies bezieht sich auf den Anwendungstyp, der aufgerufen werden soll. Beispielsweise ist der Schemaname „ms-word:" von Microsoft Word registriert. 
    
2. Trennzeichen „:"
    
3. < *Befehlsname*  >: Dies beschreibt die Aktionen, die die Anwendung ausführen soll. Beispielsweise Öffnen eines Dokuments zur Anzeige. Die Liste der Befehlsnamen wird in Abschnitt 1.5 beschrieben. 
    
4. Trennzeichen „|" (senkrechter Strich)
    
5. < *Befehlsargumentdeskriptor*  >: Dieses Element enthält weitere Informationen zur Bedeutung des Befehlsarguments. 
    
6. Trennzeichen „|" (senkrechter Strich)
    
7. < *Befehlsargument*  >: Die Argumente variieren je nach Befehl. Ein allgemeines Argument ist der URI eines Dokuments, in der Regel nach dem HTTP- oder HTTPS-Schema. Beachten Sie, dass in <  *Befehlsargument*  >-Segmenten die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen sind und daher ohne Escapezeichen verwendet werden. 
    
### <a name="abbreviated-schema"></a>Verkürztes Schema

Eine Kurzform des Office-URI-Schemas ermöglicht eine kompaktere Anforderung, um eine angegebene Office-Anwendung zu starten und die Ressource unter einem angegebenen URI zu öffnen. Diese Kurzform umfasst den < *Befehlsnamen*  > „ofv" und den <  *Befehlsargumentdeskriptor*  > „u". In diesem Schema sind keine weiteren Befehle oder Argumente zulässig. 
  
< *Schemaname*  >:<  *Befehlsargument*  > 
  
1. < *Schemaname*  >: Der Anwendungstyp, der aufgerufen werden soll. Zum Beispiel „ms-word:" für Microsoft Word. 
    
2. < *Befehlsargument*  >: Der URI für die Ressource, die die Anwendung öffnen soll. Derzeit werden nur URIs auf Grundlage des HTTP- oder HTTPS-Schemas unterstützt. 
    
## <a name="14-scheme-names-and-office-application-registrations"></a>1.4 SCHEMANAMEN UND OFFICE-ANWENDUNGSREGISTRIERUNGEN

Im Folgenden finden Sie die Liste der in Microsoft Office-Anwendungen implementierten Schemanamen. Bei der Installation von Microsoft Office wird jeder Schemaname in Windows registriert, damit er vom Office-Produkt desselben Namens verarbeitet werden kann. Beachten Sie, dass „ms-spd" eine Abkürzung für SharePoint Designer ist.
  
> - *ms-word:* 
    
> - *ms-powerpoint:* 
    
> - *ms-excel:* 
    
> - *ms-visio:* 
    
> - *ms-access:* 
    
> - *ms-project:* 
    
> - *ms-publisher:* 
    
> - *ms-spd:* 
    
> - *ms-infopath:* 
    
## <a name="15-commands-and-required-command-arguments"></a>1.5 BEFEHLE UND ERFORDERLICHE BEFEHLSARGUMENTE

### <a name="view-document"></a>Dokument anzeigen

Der folgende Befehl bewirkt das Öffnen des vom URI referenzierten Dokuments in der Anwendung im schreibgeschützten Modus oder im Anzeigemodus.
  
> Befehlsname: ofv
    
> Befehlsargumentdeskriptor: u
    
> Befehlsargument: ein URI zum Dokument auf Basis des HTTP- oder HTTPS-Schemas
    
> Beispiel:  *ms-excel:ofv|u|http://contoso/Q4/budget.xls* 
    
### <a name="edit-document"></a>Dokument bearbeiten

Der folgende Befehl bewirkt das Öffnen des vom URI referenzierten Dokuments in der Anwendung im Bearbeitungsmodus.
  
> Befehlsname: ofe
    
> Befehlsargumentdeskriptor: u
    
> Befehlsargument: ein URI zum Dokument auf Basis des HTTP- oder HTTPS-Schemas
    
> Beispiel:  *ms-powerpoint:ofe|u|http://www.fourthcoffee.com/AllHandsDeck.ppt* 
    
### <a name="new-document-from-template"></a>Neues Dokument aus Vorlage

Der folgende Befehl bewirkt das Erstellen und Öffnen eines neuen Dokuments in der Anwendung, basierend auf der unter dem angegebenen URI gespeicherten Vorlage. Die Vorlagendatei wird dabei nicht geändert. In einem zusätzlichen Befehlsargument kann der Standardpfad angegeben werden, der beim ersten Speichern der Datei als Speicherort angeboten wird. Der Benutzer kann einen anderen Speicherort auswählen.
  
> Befehlsname: nft
    
> Befehlsargumentdeskriptor 1: u
    
> Befehlsargument: ein URI zur Vorlage auf Basis des HTTP- oder HTTPS-Schemas
    
> Optionaler Befehlsargumentdeskriptor 2: s
    
> Optionales Befehlsargument 2: ein URI zur Angabe des Standardspeicherordners
    
> Beispiel:  *ms-word:nft|u|http://cohowinery/templates/elegance.pot|s|http://cohowinery/presentations* 
    
Hinweis: Wenn der optionale Standardspeicherort angegeben wird, muss er auf denselben Hostnamen verweisen wie die Vorlage.
  
Außerdem wird die Funktion „Neues Dokument aus Vorlage" von den Anwendungen SharePoint Designer und InfoPath (die das Schema „ms-spd:" bzw. „ms-infopath:" implementieren) nicht unterstützt.
  
## <a name="16-backwards-compatibility"></a>1.6 ABWÄRTSKOMPATIBILITÄT

Bei der Analyse eines URI zum Extrahieren der entsprechenden Befehlsargumente für einen bestimmten Befehl verwendet der Office-URI-Handler nur die Befehlsargumente, die den erwarteten Befehlsargumentdeskriptor aufweisen. Wenn weitere Paare von Argumenten und Argumentdeskriptoren vorhanden sind, die unerwartete Argumentdeskriptoren haben, werden sie aus dem URI entfernt. Dieser Mechanismus ermöglicht es, in zukünftigen Versionen des Schemas zusätzliche Befehlsargumente hinzuzufügen, ohne die Abwärtskompatibilität mit älteren Implementierungen dieses Schemas zu gefährden.
  
## <a name="17-implementation-restrictions-on-command-arguments"></a>1.7 IMPLEMENTIERUNGSEINSCHRÄNKUNGEN FÜR BEFEHLSARGUMENTE

Die folgenden Einschränkungen gelten für Befehlsargumente in der aktuellen Implementierung in Office 2013.
  
### <a name="length-limitations-on-uri-command-arguments"></a>Längenbeschränkungen für URI-Befehlsargumente

Die maximale Länge für URI-Befehlsargumente beträgt 256 Zeichen für alle Apps mit Ausnahme von Excel; hier beträgt der Grenzwert 216. Längere Pfade werden möglicherweise von einzelnen Apps unterstützt. Es wird empfohlen, dies vor der Bereitstellung von Lösungen zu testen, die längere Pfade verwenden.
  
### <a name="allowed-characters-in-uri-command-arguments"></a>Zulässige Zeichen in URI-Befehlsargumenten

Zulässige URIs müssen den in RFC 3987 - Internationalized Resource Identifiers (IRIs) - vorgeschlagenen Standards entsprechen. In RFC 3986 als reserviert aufgeführte Zeichen dürfen nicht mit Prozentzeichen codiert werden. Dateinamen dürfen die folgenden Zeichen nicht enthalten: \ / : ? \< \> | " oder \*.  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a>ANHANG A - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-WORD-SCHEMA
<a name="bk_addresources"> </a>

### <a name="a-3-uri-scheme-syntax"></a>A-3. URI-Schemasyntax

> Word-Schema = „ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
> template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
> save-location = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
### <a name="a-4-uri-scheme-semantics"></a>A-4. URI-Schemasemantik

Das Schema „ms-word" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Textverarbeitungsdokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Textverarbeitungsanwendung anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Textverarbeitungsanwendung anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Textverarbeitungsanwendung anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a>A-5. Anwendungen/Protokolle, die das URI-Schema „ms-word" verwenden

Das URI-Schema „ms-word" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Word 2013 oder Microsoft Word 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-word-URIs als Links zu Textverarbeitungsdokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="a-6-interoperability-considerations"></a>A-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="a-7-security-considerations"></a>A-7. Überlegungen zur Sicherheit

 Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-word-URIs bewirkt das Klicken auf einen Link zu einem ms-word-URI den Start der registrierten Textverarbeitungsanwendung. Dabei werden an die Textverarbeitungsanwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Textverarbeitungsanwendungen, die zur Verarbeitung von ms-word-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können. 
  
### <a name="a-8-references"></a>A-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a>ANHANG B - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-POWERPOINT-SCHEMA
<a name="bk_addresources"> </a>

### <a name="b-3-uri-scheme-syntax"></a>B-3. URI-Schemasyntax

- PowerPoint-Schema = „ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
- open-for-edit-cmd = „ofe|u|" document-uri
    
- open-for-view-cmd = „ofv|u|" document-uri
    
- new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
- document-uri = URI-Speicherort des zu öffnenden Dokuments
    
- template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
- save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
- \*save-location ist ein optionaler Parameter
    
### <a name="b-4-uri-scheme-semantics"></a>B-4. URI-Schemasemantik

Das Schema „ms-powerpoint" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Präsentationsdokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Präsentationsanwendung anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Präsentationsanwendung anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Präsentationsanwendung anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a>B-5. Anwendungen/Protokolle, die das URI-Schema „ms-powerpoint" verwenden

Das URI-Schema „ms-powerpoint" wird von Microsoft Office 2013 zum Aufrufen von Microsoft PowerPoint 2013 oder Microsoft PowerPoint 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-powerpoint-URIs als Links zu Präsentationsdokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="b-6-interoperability-considerations"></a>B-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="b-7-security-considerations"></a>B-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-powerpoint-URIs bewirkt das Klicken auf einen Link zu einem ms-powerpoint-URI den Start der registrierten Präsentationsanwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-powerpoint-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="b-8-references"></a>B-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a>ANHANG C - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-EXCEL-SCHEMA
<a name="bk_addresources"> </a>

### <a name="c-3-uri-scheme-syntax"></a>C-3. URI-Schemasyntax

> Excel-Schema = „ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
> template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
> save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
> \*save-location ist ein optionaler Parameter
    
### <a name="c-4-uri-scheme-semantics"></a>C-4. URI-Schemasemantik

Das Schema „ms-excel" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Tabellenblatts. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Tabellenkalkulationsanwendung anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Tabellenkalkulationsanwendung anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Tabellenkalkulationsanwendung anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a>C-5. Anwendungen/Protokolle, die das URI-Schema „ms-excel" verwenden

Das URI-Schema „ms-excel" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Excel 2013 oder Microsoft Excel 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-excel-URIs als Links zu Tabellenblättern in SharePoint-Dokumentbibliotheken.
  
### <a name="c-6-interoperability-considerations"></a>C-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="c-7-security-considerations"></a>C-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-excel-URIs bewirkt das Klicken auf einen Link zu einem ms-excel-URI den Start der registrierten Tabellenkalkulationsanwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-excel-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="c-8-references"></a>C-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a>ANHANG D - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-VISIO-SCHEMA
<a name="bk_addresources"> </a>

### <a name="d-3-uri-scheme-syntax"></a>D-3. URI-Schemasyntax

> Visio-Schema = „ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
> template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
> save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
> \*save-location ist ein optionaler Parameter
    
### <a name="d-4-uri-scheme-semantics"></a>D-4. URI-Schemasemantik

Das Schema „ms-visio" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Visio-Dokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Visio anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der Visio anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der Visio anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a>D-5. Anwendungen/Protokolle, die das URI-Schema „ms-visio" verwenden

Das URI-Schema „ms-visio" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Visio 2013 oder Microsoft Visio 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-visio-URIs als Links zu Visio-Dokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="d-6-interoperability-considerations"></a>D-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="d-7-security-considerations"></a>D-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-visio-URIs bewirkt das Klicken auf einen Link zu einem ms-visio-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-visio-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="d-8-references"></a>D-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a>ANHANG E - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-ACCESS-SCHEMA
<a name="bk_addresources"> </a>

### <a name="e-3-uri-scheme-syntax"></a>E-3. URI-Schemasyntax

> Access-Schema = „ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
> template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
> save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
> \*save-location ist ein optionaler Parameter
    
### <a name="e-4-uri-scheme-semantics"></a>E-4. URI-Schemasemantik

Das Schema „ms-access" definiert eine URI-Syntax zum Öffnen oder Erstellen einer Datenbank. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit der referenzierten Datenbankdatei geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Datenbankanwendung anweist, die Datenbank am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Datenbankanwendung anweist, die Datenbank am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Datenbankanwendung anweist, eine neue Datenbank basierend auf der Vorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a>E-5. Anwendungen/Protokolle, die das URI-Schema „ms-access" verwenden

Das URI-Schema „ms-access" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Access 2013 oder Microsoft Access 2010 mit Service Pack 2 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-access-URIs als Links zu Access-Datenbanken in SharePoint-Dokumentbibliotheken.
  
### <a name="e-6-interoperability-considerations"></a>E-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können. In \<Befehlsargument\>-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.
  
### <a name="e-7-security-considerations"></a>E-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-access-URIs bewirkt das Klicken auf einen Link zu einem ms-access-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen einer Datenbank am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-access-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Datenbanken von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="e-8-references"></a>E-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a>ANHANG F - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-PROJECT-SCHEMA
<a name="bk_addresources"> </a>

### <a name="f-3-uri-scheme-syntax"></a>F-3. URI-Schemasyntax

> Project-Schema = „ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
> template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
> save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
> \*save-location ist ein optionaler Parameter
    
### <a name="f-4-uri-scheme-semantics"></a>F-4. URI-Schemasemantik

Das Schema „ms-project" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Project-Dokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Project anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der Project anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der Project anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a>F-5. Anwendungen/Protokolle, die das URI-Schema „ms-project" verwenden

Das URI-Schema „ms-project" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Project 2013 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-project-URIs als Links zu Project-Dokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="f-6-interoperability-considerations"></a>F-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="f-7-security-considerations"></a>F-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-project-URIs bewirkt das Klicken auf einen Link zu einem ms-project-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-project-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="f-8-references"></a>F-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a>ANHANG G - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-PUBLISHER-SCHEMA
<a name="bk_addresources"> </a>

### <a name="g-3-uri-scheme"></a>G-3. URI-Schema

> Syntax Publisher-Schema = „ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
> template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert
    
> save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll
    
> \*save-location ist ein optionaler Parameter
    
### <a name="g-4-uri-scheme-semantics"></a>G-4. URI-Schemasemantik

Das Schema „ms-publisher" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Publisher-Dokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Publisher anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der Publisher anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der Publisher anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a>G-5. Anwendungen/Protokolle, die das URI-Schema „ms-publisher" verwenden

Das URI-Schema „ms-publisher" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Publisher 2013 oder Microsoft Publisher 2010 mit Service Pack 2 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-publisher-URIs als Links zu Publisher-Dokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="g-6-interoperability-considerations"></a>G-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können. In \<Befehlsargument\>-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.
  
### <a name="g-7-security-considerations"></a>G-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-publisher-URIs bewirkt das Klicken auf einen Link zu einem ms-publisher-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-publisher-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="g-9-references"></a>G-9. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a>ANHANG H - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-SPD-SCHEMA
<a name="bk_addresources"> </a>

### <a name="h-3-uri-scheme-syntax"></a>H-3. URI-Schemasyntax

> SharePoint Designer-Schema = „ms-spd:" open-for-edit-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
### <a name="h-4-uri-scheme-semantics"></a>H-4. URI-Schemasemantik

Das Schema „ms-spd" definiert eine URI-Syntax zum Öffnen eines Microsoft SharePoint Designer-Dokuments. Das Schema definiert zwei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der SharePoint Designer anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, und (2) open-for-view-cmd (ofv), der SharePoint Designer anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen.
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a>H-5. Anwendungen/Protokolle, die das URI-Schema „ms-spd" verwenden

Das URI-Schema „ms-spd" wird von Microsoft Office 2013 zum Aufrufen von Microsoft SharePoint Designer 2013 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-spd-URIs als Links zu SharePoint Designer-Dokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="h-6-interoperability-considerations"></a>H-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="h-7-security-considerations"></a>H-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-spd-URIs bewirkt das Klicken auf einen Link zu einem ms-spd-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-spd-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="h-8-references"></a>H-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a>ANHANG I - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-INFOPATH-SCHEMA
<a name="bk_addresources"> </a>

###   <a name="i-3-uri-scheme-syntax"></a>I-3. URI-Schemasyntax

> Infopath-Schema = „ms-infopath:" open-for-edit-cmd | open-for-view-cmd
    
> open-for-edit-cmd = „ofe|u|" document-uri
    
> open-for-view-cmd = „ofv|u|" document-uri
    
> document-uri = URI-Speicherort des zu öffnenden Dokuments
    
### <a name="i-4-uri-scheme-semantics"></a>I-4. URI-Schemasemantik

Das Schema „ms-infopath" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Infopath-Dokuments. Das Schema definiert zwei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Infopath anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, und (2) open-for-view-cmd (ofv), der Infopath anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen.
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a>I-5. Anwendungen/Protokolle, die das URI-Schema „ms-infopath" verwenden

Das URI-Schema „ms-infopath" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Infopath 2013 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-infopath-URIs als Links zu Infopath-Dokumenten in SharePoint-Dokumentbibliotheken.
  
### <a name="i-6-interoperability-considerations"></a>I-6. Überlegungen zur Interoperabilität

Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.
  
In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet. 
  
### <a name="i-7-security-considerations"></a>I-7. Überlegungen zur Sicherheit

Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-infopath-URIs bewirkt das Klicken auf einen Link zu einem ms-infopath-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-infopath-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.
  
### <a name="i-8-references"></a>I-8. Referenzen

RFC 3987 - International Resource Identifiers (IRIs)  
  

