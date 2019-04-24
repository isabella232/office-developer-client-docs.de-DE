---
title: Informationen zur InfoPath-Unterstützung für XML-Technologien
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: Microsoft InfoPath ist ein Hybrid Tool, das das Beste aus einer herkömmlichen Dokumentbearbeitungsumgebung wie einer Textverarbeitung oder einer e-Mail-Anwendung mit den strengen Datenerfassungsfunktionen eines Formularpakets kombiniert. In diesem Artikel werden die Probleme beschrieben, mit denen InfoPath die Entwurfsprinzipien und XML-Industriestandards für die Lösung dieser Probleme behandeln und erläutern kann.
ms.openlocfilehash: 20831635fba8d76b9d6b45f42a5308ab7236db20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300336"
---
# <a name="about-infopath-support-for-xml-technologies"></a>Informationen zur InfoPath-Unterstützung für XML-Technologien

Microsoft InfoPath ist ein Hybrid Tool, das das Beste aus einer herkömmlichen Dokumentbearbeitungsumgebung wie einer Textverarbeitung oder einer e-Mail-Anwendung mit den strengen Datenerfassungsfunktionen eines Formularpakets kombiniert. In diesem Artikel werden die Probleme beschrieben, mit denen InfoPath die Entwurfsprinzipien und XML-Industriestandards für die Lösung dieser Probleme behandeln und erläutern kann.
  
## <a name="introduction"></a>Einführung

InfoPath ist ein hohes XML-Erstellungstool, mit dem normale Endbenutzer XML-Dokumente erstellen können, die zu einem benutzerdefinierten XML-Schema gehören. Wenn Benutzer ein XML-Dokument bearbeiten, werden die Änderungen am Dokument durch das XML-Schema gesteuert.
  
Die Benutzer interagieren mit dem XML-Dokument über eine umfangreiche formatierte Ansicht, die angezeigt wird, indem ein XSLT-Stylesheet auf das Dokument angewendet wird. Ein Blattknoten oder Attributwert aus dem XML-Dokument wird als Feld (beispielsweise als Textfeld oder Kontrollkästchen) angezeigt, während eine Knotenhierarchie als Gruppe von Feldern angezeigt wird.
  
InfoPath ermöglicht die validierte, strukturierte Bearbeitung von XML-Daten, indem die Bearbeitungsaktionen angezeigt werden, die für das aktuell ausgewählte Feld oder die Feldgruppe gültig sind. Mit dieser strukturierten Bearbeitung kann der Benutzer gültige XML-Elemente und-Attribute hinzufügen und entfernen, indem er mit Gruppen von Feldern arbeitet, die in dynamischen Ansichten angezeigt werden, ohne die Elemente und Attribute zu sehen.
  
InfoPath löst ein Problem im Bereich der Datenerfassung, das vor der Einführung von XML nicht gelöst werden konnte: durch das Hinzufügen von Formulargruppen, die das hierarchische Datenmodell von XML verwenden, wird die Flexibilität von Word Processor-Dokumenten erweitert. die strengen Validierungsfeatures einer Formularanwendung. Komplexe XSLT-Transformationen sind ein integraler Bestandteil dieser Lösung, die dynamische, benutzerfreundliche Ansichten der XML-Daten bereitstellt.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Einschränkungen herkömmlicher Formulare und Dokumente beim Sammeln von Daten

Beim Sammeln von Unternehmensdaten wünschen sich die Benutzer oft mehr Flexibilität, als statische Formulare bieten und gleichzeitig eine besser strukturierte Bearbeitung und Überprüfung als bei Textverarbeitungsdokumenten.
  
Herkömmliche Formulare sind statisch und in der Länge begrenzt. Diese Formulare enthalten eine feste Anzahl wiederholter Zeilen und können beim Ausfüllen des Formulars nicht erweitert werden. Herkömmliche Formulare sind schwierig zu verwenden, da nicht so umfangreiche Bearbeitungsfeatures vorhanden sind. Häufig müssen die Benutzer sämtliche Informationen in einem Durchgang eingeben.
  
Andererseits können die Benutzer bei herkömmlichen Dokumenten, die mit einer Textverarbeitung erstellt wurden, Inhalte frei hinzufügen und entfernen. Dabei haben die Benutzer jedoch wenig Anhaltspunkte für die Eingabe vollständiger, strukturierter und gültiger Informationen. Bei den im Dokument definierten Feldern werden die Datenwerte und Datentypen nur minimal oder gar nicht überprüft. Die Daten in den Feldern sind nicht so beschriftet, dass eine einfache Bezugnahme und automatische Wiederverwendung möglich ist. Die Daten liegen nicht strukturiert, sondern formfrei vor; die Informationen können nicht gruppiert werden, beispielsweise durch Anwendung des Etiketts Adresse auf eine Gruppe mit den Feldern Straße, Ort und Bundesland.
  
Daher wird eine flexible und doch strukturierte Bearbeitungsmöglichkeit benötigt. Da eine derartige Technologie vor der Einführung von XML jedoch nicht verfügbar war, mussten die Entwickler mit hohem Codieraufwand benutzerdefinierte Anwendungen erstellen. Benutzerdefinierte Anwendungen sind kostspielig, schwierig zu ändern und erfordern benutzerdefinierten Code für die Überprüfung. Benutzerdefinierte Anwendungen erfordern oft Endbenutzerschulungen, und es ist schwierig, die sich ergebenden Daten für andere Geschäftsprozesse wiederzuverwenden.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Ermöglichen der strukturierten Bearbeitung durch Anzeigen von XML-Daten als Feldgruppen

Ein wichtiges technisches Entwurfsproblem, das gelöst werden musste, war die Bereitstellung einer einfachen Benutzeroberfläche zum Hinzufügen oder Entfernen von XML-Elementen und -Attributen ohne Anzeigen der Elemente und Attribute. Gleichzeitig sollte die Gültigkeit der DOM-Struktur gemäß dem benutzerdefinierten XML-Schema aufrechterhalten werden. Die Benutzeroberfläche sollte eine natürliche Möglichkeit zum Bearbeiten der DOM-Struktur bieten (beispielsweise Einfügen optionaler Unterstrukturen, Ersetzen ausgewählter Unterstrukturen und Erweitern vorhandener Unterstrukturen).
  
Diese einfache Benutzeroberfläche wird bereitgestellt, indem eine DOM-Unterstruktur als Feldgruppe oder Bereich angezeigt wird. Eine Feldgruppe ist eine Gruppe von UI-Steuerelementen, beispielsweise Textfelder und Dropdownlisten, und dient als einfache Benutzeroberfläche, über die Benutzer hierarchische XML-Daten visualisieren und bearbeiten können. Eine Feldgruppe kann weitere Feldgruppen enthalten und optional oder wiederholt sein, genau wie eine DOM-Unterstruktur weitere Unterstrukturen enthalten und optional oder wiederholt sein kann. Der DOM-Struktur wird eine Unterstruktur hinzugefügt, wenn der Benutzer den Mauszeiger auf eine Feldgruppe setzt, auf das Dropdownmenü klickt, das in der Feldgruppe angezeigt wird, und dann den **Namen \<\>der Feldgruppe einfügen**auswählt.
  
InfoPath bietet diese strukturierte Bearbeitung von XML-Daten mithilfe des angegebenen XML-Schemas, um die Bearbeitung einzuschränken und zu lenken. Durch das Schema wird gesteuert, ob die Befehle **Einfügen** und **Entfernen** im Dropdownmenü für eine Feldgruppe angezeigt werden. Das Schema wird außerdem für die Überprüfung verwendet. Um die Bearbeitung eines XML-Dokuments zu ermöglichen, für das kein XML-Schema vorhanden ist, kann InfoPath ein Schema aus dem XML-Dokument generieren. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Ermöglichen benutzerfreundlicher Ansichten von XML-Daten mithilfe von XSLT-Transformationen

Eine weitere zu bewältigende technische Entwurfsherausforderung bestand darin, für den Inhalt der Ansichten auf der Benutzeroberfläche eine völlig von der Struktur der XML-Daten abweichende Organisation zu ermöglichen. Damit die Daten auf die für die Benutzer sinnvollste Weise angezeigt werden und die Benutzer die Daten leicht lesen und bearbeiten können, muss der Designer die Daten in einer anderen Reihenfolge als in der DOM-Datenstruktur anzeigen können, manche Daten in einer Ansicht auslassen können, angrenzende Datenstrukturknoten in separaten Ansichten neu organisieren können und Daten aus verschiedenen Teilen der Datenstruktur in einer einzigen Ansicht sammeln können.
  
Die Reihenfolge und Struktur des Inhalts der Ansichten muss daher unabhängig von der Reihenfolge und Struktur der DOM-Strukturknoten sein. Diese strukturelle Abhängigkeit von Darstellung und Daten erfordert eine komplexe, dynamische Bindung oder Zuordnung zwischen den gruppierten Feldern in den Ansichten und den Knoten in der DOM-Struktur.
  
Um diese komplexe Zuordnung zwischen Ansichten und Daten bereitzustellen, verwendet InfoPath XSL-Transformationen (XSLT) ausführlich. XSLT ist eine leistungsstarke Stylesheetsprache, die komplexe XSLT-Transformationen und umfassende Ansichten mit dynamischer, flexibler Darstellung der Inhalte unterstützt. Für jede Ansicht wird eine XSLT-Datei verwendet. Die Verwendung eines Stylesheets ist eine gebräuchliche und bewährte Entwurfsmethode in SGML- und XML-Erstellungstools, und XSLT ist der W3C-Standard für Stylesheets, die für derartige komplexe Transformationen verwendet werden.
  
Damit nicht jedes Mal, wenn ein Benutzer die Struktur einer Unterstruktur in DOM ändert, die gesamte XSLT-Transformation ausgeführt werden muss, wird mithilfe von Algorithmen ermittelt, welcher Teil der Ansicht aktualisiert werden muss. Dann wird nur der relevante Teil des XSLT-Stylesheets angewendet, und der betroffene Teil der Ansicht wird aktualisiert.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Verwendung von XML-Standards beim Bearbeiten eines Formulars

InfoPath basiert auf den XML-Standards, die Folgendes umfassen:
  
- Extensible Markup Language (XML) 1.0 Second Edition
    
- Namespaces in XML
    
- XML Path Language (XPath) 1.0
    
- XML Schema (XSD) 1.0 Part 1: Structures, and Part 2: Datatypes
    
- Extensible Stylesheet Language Transformations (XSLT) 1.0
    
- Extensible Hypertext Markup Language (XHTML) 1.0
    
- Cascading Style Sheets (CSS)
    
- Document Object Model (DOM) 1.0
    
- XML Digital Signatures (XML DSig)
    
- Simple Object Access Protocol (SOAP) 1.1
    
- Web Services Description Language (WSDL) 1.1
    
- Universal Description, Discovery, and Integration (UDDI) 1.0
    
InfoPath verwendet und generiert beispielsweise Standard-XML-, XSLT-und XSD-Dateien, die in verschiedenen Geschäftsprozessen wieder verwendet werden können. InfoPath verwendet MSXML, das SOAP-Toolkit und den .NET System. XML-Namespace zur Unterstützung dieser Standards und bietet umfassende integrierte Unterstützung für XML-Webdienste.
  
In Abbildung 1 wird das kontextbezogene Dropdownmenü für eine **customer**-Feldgruppe gezeigt, mit dessen Hilfe Benutzer eine weitere **customer**-Feldgruppe hinzufügen, diese **customer**-Feldgruppe entfernen, eine **item**-Zeile in die Tabelle der Einkaufsartikel in dieser Feldgruppe einfügen oder eine optionale **actions**-Feldgruppe innerhalb dieser Feldgruppe einfügen können. Der Link **Klicken Sie hier** stellt eine weitere Möglichkeit zum Einfügen der **actions**-Feldgruppe dar. In den einzelnen Einkaufsartikelzeilen wird ein kürzeres Dropdownmenü angezeigt. 
  
1. In InfoPath erstellt der Benutzer ein neues XML-Dokument auf der Grundlage einer InfoPath-Formularvorlage oder öffnet ein vorhandenes XML-Dokument, das auf einer Formularvorlage basiert. Bei einem XML-Dokument handelt es sich um eine XML-Datendatei, die einen Verweis auf die Formularvorlage enthält und in der XML-Namespaces verwendet werden können. 
    
    Eine Formularvorlage ist ein Satz von Dateien, durch die die strukturierte Bearbeitung von XML-Dokumenten ermöglicht wird, die einem bestimmten benutzerdefinierten XML-Schema entsprechen. Die Dateien, aus denen die Formularvorlage besteht, können als einzelne Dateien in einem normalen Ordner oder als Dateien in einem CAB-Dateiordner gepackt sein. In beiden Fällen handelt es sich um standardmäßige XML-Dateien und optionale Hilfsdateien, beispielsweise Assemblys für verwalteten Code.
    
2. Wenn das XML-Dokument mit der XML-Signatur digital signiert ist, bestätigt InfoPath, dass die XML-Datei konsistent ist, bevor Sie geöffnet wird.
    
3. InfoPath erstellt eine DOM-Datenstruktur des XML-Dokuments im Arbeitsspeicher.
    
4. XSLT-Transformationen werden auf die DOM-Struktur angewendet, und dabei werden Ansichten erzeugt, in denen dem Benutzer eine entsprechende Darstellung des Dokuments angezeigt wird. Elemente am Anfang des XML-Dokuments können am unteren Ende der Ansicht und außerdem in einer anderen Ansicht in einer anderen Anordnung angezeigt werden. Die Ansichten bestehen aus Benutzeroberflächencontainern wie beispielsweise Bereichen, die Text und Steuerelemente enthalten (beispielsweise Textfelder, Felder für Rich-Text, Datumsauswahlfelder und Dropdownlisten. Container können auch weitere Container enthalten.
    
5. Bei der XSLT-Transformation wird XHTML als Ausgabe erzeugt, und dann wird ein CSS verwendet, um die Darstellung der XHTML-Ausgabe zu steuern.
    
6. Wenn das XML-Schema das Hinzufügen von Knoten zu einem Knoten der Datenstruktur zulässt, weist das dem Knoten zugeordnete Feld oder die Feldgruppe ein Dropdownmenü auf, mit dem der Benutzerfeld Gruppen hinzufügen oder entfernen kann. Der Benutzer bearbeitet das Dokument, indem eine wiederholte oder optionale Feldgruppe hinzugefügt wird, ein Wert eingegeben wird, eine Option ausgewählt oder Rich-Text eingegeben wird. Wenn ein XML-Schemaknoten mit dem Schema für XHTML verknüpft ist, stellt InfoPath eine Benutzeroberfläche zum Erstellen von Rich-Text dar. Wenn der Benutzer Rich-Text eingibt, wird der XHTML-Inhalt als Unterstruktur im DOM erstellt.
    
7. Die Gültigkeit der DOM-Struktur wird immer aufrechterhalten. Wenn Benutzer das XML-Dokument bearbeiten, werden die Bearbeitungen anhand des zugeordneten XML-Schemas überprüft. Die versuchten Änderungen an der DOM-Struktur und den Blattknotenwerten werden anhand des XML-Schemas überprüft, um sicherzustellen, dass die Datentypen und Werte gültig sind. Wenn die versuchten Änderungen nicht gültig sind, wird ein Überprüfungsdialogfeld geöffnet, und die Änderungen werden nicht auf die DOM-Struktur angewendet. Wenn die Änderungen gültig sind, wird die DOM-Struktur aktualisiert.
    
8. Der geänderte Teil der Ansicht wird aktualisiert, indem nur die erforderlichen Teile des XSLT-Stylesheets auf die DOM-Struktur angewendet werden.
    
9. Die Benutzer können das XML-Dokument speichern oder mithilfe von einfachem HTTP oder SOAP senden. Die Benutzer können das Dokument nur senden, wenn dieses gemäß dem XML-Schema gültig ist.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a>Verwendung von XML-Standards beim Entwerfen eines Formulars

Sie können ein Formular entwerfen, indem Sie mit einem vorhandenen XML-Schema beginnen, indem Sie eine Verbindung mit einem XML-Webdienst oder einer XML-Datenbank herstellen und dessen bzw. deren XML-Schema abrufen oder indem Sie automatisch ein Schema aus einem neuen Formular oder aus einer XML-Datendatei generieren. Diese Szenarien werden in den folgenden Verfahren beschrieben. In Abbildung 3 wird die einfache Benutzeroberfläche zum Entwerfen einer Formularvorlage gezeigt.
  
1. Erstellen Sie im InfoPath Designer ein neues Formular, indem Sie die Formularvorlage **XML oder Schema** und anschließend als Datenquelle eine vorhandene XML-Schemadatei auswählen. Das XML-Schema wird in den Aufgabenbereich geladen und als Struktursteuerelement angezeigt. 
    
2. Verwenden Sie die Entwurfslayouttools, um die UI-Steuerelemente wie beispielsweise Zeilen und das Hintergrunddesign in einer oder mehreren Ansichten anzuordnen. Daraufhin werden einige der XSLT-Elemente generiert. Die XSLT-Ansichten und das XML-Schema werden automatisch der Formularvorlage zugeordnet.
    
3. Ordnen Sie die XML-Schemaelemente mithilfe von Drag & Drop den Benutzeroberflächen-Steuerelementen in den Ansichten zu. InfoPath unterstützt Sie bei der Auswahl der geeigneten Steuerelemente für die XML-Schemaelemente basierend auf der Art der Schemaelemente. Wenn beispielsweise der XML-Datentyp Date lautet, schlägt InfoPath ein Datumsauswahl-Steuerelement vor. Basierend auf Auswahlmöglichkeiten im XML-Schema kann InfoPath Gruppen von optionalen oder wiederholten Feldern einfügen. Durch Zuordnen der XML-Schemaelemente zu den Benutzeroberflächen-Steuerelementen wird die XSLT-Struktur generiert.
    
4. Speichern Sie die Formularvorlage. Sie können die Dateien, aus denen die Formularvorlage besteht, als einzelne Dateien in einem normalen Ordner oder als Dateien in einem CAB-Dateiordner speichern. In beiden Fällen handelt es sich um standardmäßige XML-Dateien. Die Formularvorlage kann jetzt von Benutzern verwendet werden.
    
Eine Formularvorlage enthält alle semantischen Informationen, die erforderlich sind, um eine strukturierte Bearbeitung zu ermöglichen, wenn ein Formular in InfoPath geöffnet wird. Eine Formularvorlage enthält eine Manifestdatei, die XSLT-Dateien, durch die die Ansichten definiert werden, die Informationen, die zum Überprüfen der Daten benötigt werden, und einen optionalen Ressourcenbezeichner für einen XML-Webdienst.
  
Die Manifest- oder Formulardefinitionsdatei ist der allgemeine Knoten- und Einstiegspunkt für alle Dateien, die von der Formularvorlage benötigt werden. Das Manifest enthält Verweise auf andere Dateien in der Formularvorlage sowie die Informationen, die zum Überprüfen der Daten und zum Ermöglichen der strukturierten Bearbeitung benötigt werden. Die XML-Schemaüberprüfungsinformationen werden für die sich ergebende Benutzeroberfläche angepasst und der Manifestdatei hinzugefügt. Wenn das Schema beispielsweise das Einfügen mehrerer optionaler Elemente in einer bestimmten Unterstruktur zulässt, können Sie die Benutzeroberfläche so entwerfen, dass mehrere optionale Elemente hinzugefügt werden, wenn Benutzer einen einzigen Vorgang auf der Benutzeroberfläche ausführen. Diese Anpassung ist wichtig, um gewöhnlichen Benutzern größtmöglichen Komfort zu bieten. 
  
Außerdem können Sie ein Formular entwerfen, indem Sie einen vorhandenen XML-Webdienst verwenden, um das XML-Schema bereitzustellen. Gehen Sie dazu folgendermaßen vor:
  
1. Verwenden Sie UDDI, um relevante Webdienste zu suchen.
    
2. Wählen Sie den zu verwendenden Webdienst aus. InfoPath liest die WSDL-Datei, die dem Webdienst zugeordnet ist, und identifiziert das zu verwendende XML-Schema.
    
3. Öffnen Sie das XML-Schema, um dieses zu laden.
    
4. Ordnen Sie die UI-Steuerelemente an, und ordnen Sie XML-Schemaelemente und -Attribute zu.
    
5. Definieren Sie, wie das XML-Dokument an den Webdienst gesendet werden soll, von dem SOAP verwendet wird.
    
Wenn Sie ein Formular von Grund auf entwerfen und das XML-Schema automatisch generieren möchten, gehen Sie folgendermaßen vor:
  
1. Klicken Sie auf der Registerkarte **Datei** entweder auf die Formularvorlage **Leeres Formular** oder **Leeres Formular (InfoPath Filler)**, und klicken Sie dann auf **Formular entwerfen**.
    
2. Klicken Sie auf der Registerkarte **Start** rechts unten in der Gruppe **Steuerelemente** auf den Pfeil, um den Aufgabenbereich **Steuerelemente** anzuzeigen. Vergewissern Sie sich anschließend, dass das Kontrollkästchen **Datenquelle automatisch erstellen** aktiviert ist. (Standardmäßig ist dieses Kontrollkästchen aktiviert.) 
    
3. Ordnen Sie die UI-Steuerelemente an. Während Sie das Layout erstellen, erstellt InfoPath automatisch das XML-Schema und ordnet die Elemente und Attribute den Benutzeroberflächen-Steuerelementen zu.
    
So entwerfen Sie ein Formular, indem Sie mit einer wohlgeformten XML-Datendatei beginnen
  
1. Klicken Sie auf der Registerkarte **Datei** auf die Formularvorlage **XML oder Schema**, und klicken Sie dann auf **Formular entwerfen**.
    
2. Wählen Sie im Datenquellen-Assistent die XML-Datei aus, die Sie als Datenquelle wünschen. Anschließend wird ein auf der XML-Datendatei basierendes XML-Schema automatisch erstellt.
    
3. Ordnen Sie die UI-Steuerelemente wie weiter oben in diesem Abschnitt beschrieben an.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Entworfen als idealer Client für Webdienste

Webdienste werden inzwischen branchenweit unterstützt. Viele Back-End- und Middle-Tier-Systeme können für die Kommunikation über Webdienststandards wie beispielsweise SOAP, UDDI und WSDL konfiguriert werden. Zu diesen webdienstfähigen Systemen gehören Datenbanken, Workflowsysteme, ERP-Systeme (Enterprise Resource Planning), CRM-Systeme (Customer Relationship Management) und andere Systeme. InfoPath bietet jetzt eine ideale Benutzeroberfläche zum Anzeigen und Bearbeiten der XML-Daten, die über Webdienste gesendet werden. In Abbildung 4 wird die integrierte Unterstützung für XML-Webdienste gezeigt.
  
InfoPath passt gut zu dem Modell mit losen gekoppelten Webdiensten, in dem Daten zwischen Computern als vollständige XML-Dokumente gesendet werden. Dieses grobkörnige Kommunikationsmodell passt gut zum asynchronen Charakter des Webs. Als hochwertiges Authoring Tool für XML-Dokumente unterstützt InfoPath die SOAP-Codierung "Document/Literal" anstelle der SOAP-Codierung (Remote Procedure Call, RPC). InfoPath ist ein idealer Client für Webdienste, da es das in einer SOAP-Nachricht angegebene XML-Schema nativ lesen und dann eine Benutzeroberfläche basierend auf dem Schema erstellen kann, die es Benutzern ermöglicht, XML-Dokumente, die vom entsprechenden Web generiert oder empfangen werden, einfach anzuzeigen und zu bearbeiten. Service. InfoPath bietet außerdem Unterstützung für ADO.NET-Datasets, die Änderungsnachverfolgung enthalten.
  
## <a name="terminology"></a>Terminologie

|||
|:-----|:-----|
|**Feldgruppe:** <br/> |Ein Bereich, ein wiederholter Bereich, ein optionaler Bereich oder eine wiederholte Tabelle. Bereiche und wiederholte Tabellen sind Steuerelemente in einem Formular, die weitere Steuerelemente enthalten und nach Bedarf wiederholt werden. Benutzer können beim Ausfüllen des Formulars mehrere Bereiche oder Zeilen einfügen.  <br/> |
|**DOM-Struktur:** <br/> |Die Struktur der Datenquelle des Formulars. Insbesondere die Auflistung von Feldern und Gruppen, die die Daten für ein InfoPath-Formular definieren und speichern.  <br/> |
   
## <a name="conclusion"></a>Schlussbemerkung

InfoPath verwendet Open XML-Standards, um Benutzern eine flexible und dennoch strukturierte XML-Bearbeitung für die Datenerfassung bereitzustellen. Um eine einfache Benutzeroberfläche zum Visualisieren und Bearbeiten hierarchischer XML-Daten bereitzustellen, werden der DOM-Struktur geschachtelte Feldgruppen mit UI-Steuerelementen zugeordnet. Mithilfe von XSLT-Transformationen kann der Inhalt der Ansichten der Benutzeroberfläche abweichend von der Struktur der XML-Daten organisiert werden.
  
InfoPath bietet mehr Flexibilität als statische Formulare mit strukturierter Bearbeitung und Überprüfung als Textverarbeitungsdokumente. Dadurch ergibt sich ein hybrides Tool, das die Vorteile der herkömmlichen Dokumentbearbeitung mit den umfassenden Datenerfassungsfunktionen eines Formularpakets vereint und mit dem gewöhnliche Benutzer gültige XML-Dokumente erstellen können, die zu einem benutzerdefinierten XML-Schema gehören. Dank der integrierten Unterstützung für Webdienste können einfach Ansichten zum Bearbeiten von XML-Dokumenten erstellt werden, die einem Webdienstschema entsprechen.
  

