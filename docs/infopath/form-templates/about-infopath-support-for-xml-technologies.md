---
title: Informationen zur InfoPath-Unterstützung für XML-Technologien
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: Microsoft InfoPath ist ein hybrides Tool, das das beste eines bearbeiten wünschen, wie ein Textverarbeitung oder e-Mail-Anwendung, mit den strengen Datenerfassung Funktionen eines herkömmlichen Dokuments kombiniert. Dieser Artikel beschreibt die Probleme, die InfoPath ausgelegt und erläutert die Entwurfsprinzipien und XML-Industriestandards verwendet, um diese Probleme zu lösen.
ms.openlocfilehash: 5d7b0bd0de045bdb9ada6946b7142993cd80df0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790731"
---
# <a name="about-infopath-support-for-xml-technologies"></a>Informationen zur InfoPath-Unterstützung für XML-Technologien

Microsoft InfoPath ist ein hybrides Tool, das das beste eines bearbeiten wünschen, wie ein Textverarbeitung oder e-Mail-Anwendung, mit den strengen Datenerfassung Funktionen eines herkömmlichen Dokuments kombiniert. Dieser Artikel beschreibt die Probleme, die InfoPath ausgelegt und erläutert die Entwurfsprinzipien und XML-Industriestandards verwendet, um diese Probleme zu lösen.
  
## <a name="introduction"></a>Einführung

InfoPath ist eine allgemeine authoring XML-Tool, mit das normalen Endbenutzer zum Erstellen von XML-Dokumenten, die zu einer benutzerdefinierten XML-Schema gehören kann. Wenn der Benutzer ein XML-Dokument bearbeitet wird, werden Änderungen an das Dokument durch das XML-Schema gesteuert.
  
Die Benutzer interagieren mit dem XML-Dokument über eine umfangreiche formatierte Ansicht, die angezeigt wird, indem ein XSLT-Stylesheet auf das Dokument angewendet wird. Ein Blattknoten oder Attributwert aus dem XML-Dokument wird als Feld (beispielsweise als Textfeld oder Kontrollkästchen) angezeigt, während eine Knotenhierarchie als Gruppe von Feldern angezeigt wird.
  
InfoPath ermöglicht validiertes, strukturiertes Bearbeiten von XML-Daten durch Anzeigen der Bearbeitungsaktionen, die für das Feld oder das derzeit ausgewählte Feldgruppe gültig sind. Diese strukturierte Bearbeitung ermöglicht dem Benutzer hinzufügen und Entfernen von gültigen XML-Elementen und Attributen durch die Arbeit mit Gruppen von Feldern, die in dynamischen Ansichten, ohne dass die Elemente und Attribute angezeigt.
  
InfoPath löst ein Problem im Bereich der Sammeln von Daten, die vor der Einführung des XML nicht gelöst werden konnte: durch Bereitstellen von Formularen, die wachsen können durch Hinzufügen von Gruppen von Feldern, die das hierarchische Datenmodell-XML-Daten verwenden, fügt InfoPath die Flexibilität der Textverarbeitungsdokumente zu die strengen Validierungsfeatures Forms-Anwendung. Komplexe XSLT-Transformationen sind ein integraler Bestandteil dieser Lösung, die dynamische, leicht zu bedienende Ansichten von XML-Daten bereitstellt.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Einschränkungen herkömmlicher Formulare und Dokumente beim Sammeln von Daten

Beim Sammeln von Unternehmensdaten wünschen sich die Benutzer oft mehr Flexibilität, als statische Formulare bieten und gleichzeitig eine besser strukturierte Bearbeitung und Überprüfung als bei Textverarbeitungsdokumenten.
  
Herkömmliche Formulare sind statisch und in der Länge begrenzt. Diese Formulare enthalten eine feste Anzahl wiederholter Zeilen und können beim Ausfüllen des Formulars nicht erweitert werden. Herkömmliche Formulare sind schwierig zu verwenden, da nicht so umfangreiche Bearbeitungsfeatures vorhanden sind. Häufig müssen die Benutzer sämtliche Informationen in einem Durchgang eingeben.
  
Andererseits können die Benutzer bei herkömmlichen Dokumenten, die mit einer Textverarbeitung erstellt wurden, Inhalte frei hinzufügen und entfernen. Dabei haben die Benutzer jedoch wenig Anhaltspunkte für die Eingabe vollständiger, strukturierter und gültiger Informationen. Bei den im Dokument definierten Feldern werden die Datenwerte und Datentypen nur minimal oder gar nicht überprüft. Die Daten in den Feldern sind nicht so beschriftet, dass eine einfache Bezugnahme und automatische Wiederverwendung möglich ist. Die Daten liegen nicht strukturiert, sondern formfrei vor; die Informationen können nicht gruppiert werden, beispielsweise durch Anwendung des Etiketts Adresse auf eine Gruppe mit den Feldern Straße, Ort und Bundesland.
  
Daher wird eine flexible und doch strukturierte Bearbeitungsmöglichkeit benötigt. Da eine derartige Technologie vor der Einführung von XML jedoch nicht verfügbar war, mussten die Entwickler mit hohem Codieraufwand benutzerdefinierte Anwendungen erstellen. Benutzerdefinierte Anwendungen sind kostspielig, schwierig zu ändern und erfordern benutzerdefinierten Code für die Überprüfung. Benutzerdefinierte Anwendungen erfordern oft Endbenutzerschulungen, und es ist schwierig, die sich ergebenden Daten für andere Geschäftsprozesse wiederzuverwenden.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Ermöglichen der strukturierten Bearbeitung durch Anzeigen von XML-Daten als Feldgruppen

Ein wichtiges technisches Entwurfsproblem, das gelöst werden musste, war die Bereitstellung einer einfachen Benutzeroberfläche zum Hinzufügen oder Entfernen von XML-Elementen und -Attributen ohne Anzeigen der Elemente und Attribute. Gleichzeitig sollte die Gültigkeit der DOM-Struktur gemäß dem benutzerdefinierten XML-Schema aufrechterhalten werden. Die Benutzeroberfläche sollte eine natürliche Möglichkeit zum Bearbeiten der DOM-Struktur bieten (beispielsweise Einfügen optionaler Unterstrukturen, Ersetzen ausgewählter Unterstrukturen und Erweitern vorhandener Unterstrukturen).
  
Um diese einfache Benutzeroberfläche bereitzustellen, wird eine DOM-Unterstruktur als Feldgruppe oder Abschnitt angezeigt. Eine Feldgruppe ist eine Gruppe von UI-Steuerelemente, wie Textfelder und Dropdownlisten, und dient als eine einfache Benutzeroberfläche, mit die den Benutzer zum Visualisieren und hierarchische XML-Daten bearbeiten kann. Eine Feldgruppe kann kann andere Feldgruppen enthalten und optional oder wiederholten, wie eine DOM-Unterstruktur weitere Unterstrukturen enthalten kann und optional oder wiederholt werden kann. Wird der DOM-Struktur eine Unterstruktur hinzugefügt, wenn der Benutzer den Mauszeiger über einer Feldgruppe positioniert, klickt auf das Dropdown-Menü, das angezeigt wird, auf die Feldgruppe und wählt dann **Einfügen \<Feldgruppenname\>**.
  
InfoPath bietet diese strukturierte Bearbeitung von XML-Daten mithilfe des angegebenen XML-Schemas zum Einschränken und Anleiten bearbeiten. Das Schema steuert, ob die Befehle **Einfügen** und **Entfernen von** auf das Dropdownmenü für eine Feldgruppe angezeigt werden. Das Schema wird auch für die Validierung verwendet. Zum Aktivieren der Bearbeitung eines XML-Dokuments für die kein XML-Schema vorhanden ist, kann InfoPath aus dem XML-Dokument ein Schema generieren. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Ermöglichen benutzerfreundlicher Ansichten von XML-Daten mithilfe von XSLT-Transformationen

Eine weitere zu bewältigende technische Entwurfsherausforderung bestand darin, für den Inhalt der Ansichten auf der Benutzeroberfläche eine völlig von der Struktur der XML-Daten abweichende Organisation zu ermöglichen. Damit die Daten auf die für die Benutzer sinnvollste Weise angezeigt werden und die Benutzer die Daten leicht lesen und bearbeiten können, muss der Designer die Daten in einer anderen Reihenfolge als in der DOM-Datenstruktur anzeigen können, manche Daten in einer Ansicht auslassen können, angrenzende Datenstrukturknoten in separaten Ansichten neu organisieren können und Daten aus verschiedenen Teilen der Datenstruktur in einer einzigen Ansicht sammeln können.
  
Die Reihenfolge und Struktur des Inhalts der Ansichten muss daher unabhängig von der Reihenfolge und Struktur der DOM-Strukturknoten sein. Diese strukturelle Abhängigkeit von Darstellung und Daten erfordert eine komplexe, dynamische Bindung oder Zuordnung zwischen den gruppierten Feldern in den Ansichten und den Knoten in der DOM-Struktur.
  
Um diese komplexe Zuordnung zwischen Ansichten und Daten zu ermöglichen, wird InfoPath umfassend XSL-Transformation (XSLT) verwendet. XSLT ist eine Sprache leistungsstarke Formatvorlage, die komplexe XSLT-Transformationen und rich-Ansichten mit flexiblen Präsentation von Inhalt unterstützt. Für jede Ansicht wird eine XSLT-Datei verwendet. Mithilfe einer Formatvorlage Blatt ist eine gängige und etablierten Ansatz SGML-und XML-Erstellungstools, und XSLT ist der W3C-Standard für Stylesheets, die für diese Art der komplexen Transformation verwendet werden.
  
Damit nicht jedes Mal, wenn ein Benutzer die Struktur einer Unterstruktur in DOM ändert, die gesamte XSLT-Transformation ausgeführt werden muss, wird mithilfe von Algorithmen ermittelt, welcher Teil der Ansicht aktualisiert werden muss. Dann wird nur der relevante Teil des XSLT-Stylesheets angewendet, und der betroffene Teil der Ansicht wird aktualisiert.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Verwendung von XML-Standards beim Bearbeiten eines Formulars

InfoPath ist von Grund auf den folgenden XML-Standards aufgebaut:
  
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
    
Beispielsweise InfoPath verwendet und generiert standard XML und XSLT-XSD-Dateien, die wiederverwendet werden können in verschiedenen Geschäftsprozessen. InfoPath verwendet MSXML, das SOAP Toolkit und den .NET System.XML-Namespace zur Unterstützung dieser Standards und bietet vollständig integrierte Unterstützung für XML-Webdienste.
  
Abbildung 1 zeigt die kontextbezogene Dropdownmenü für eine Feldgruppe **Kunden** , wodurch den Benutzer eine andere **Kunden** Feldgruppe hinzufügen, Entfernen dieser **Kunden** Feldgruppe, Einfügezeile ein **Element** in der Tabelle der Kauf von Elementen in Diese Feldgruppe oder Einfügen einer Feldgruppe optional **Aktionen** in dieser Gruppe dar. Der Link **Klicken Sie hier,** bietet eine andere Möglichkeit, fügen Sie die Gruppe **Aktionen** dar. Ein kürzerer Dropdownmenü wird auf jeder Zeile angezeigt. 
  
1. In InfoPath der Benutzer ein neues XML-Dokument basierend auf einer InfoPath-Formularvorlage erstellt oder öffnet ein vorhandenes XML-Dokument, das auf einer Formularvorlage basiert. Das XML-Dokument ist eine XML-Datendatei, die einen Verweis auf die Formularvorlage enthält und XML-Namespaces verwenden kann. 
    
    Eine Formularvorlage ist ein Satz von Dateien, durch die die strukturierte Bearbeitung von XML-Dokumenten ermöglicht wird, die einem bestimmten benutzerdefinierten XML-Schema entsprechen. Die Dateien, aus denen die Formularvorlage besteht, können als einzelne Dateien in einem normalen Ordner oder als Dateien in einem CAB-Dateiordner gepackt sein. In beiden Fällen handelt es sich um standardmäßige XML-Dateien und optionale Hilfsdateien, beispielsweise Assemblys für verwalteten Code.
    
2. Wenn das XML-Dokument mithilfe von XML-Signatur digital signiert ist, wird von InfoPath bestätigt, dass die XML-Datei vor dem Öffnen konsistent ist.
    
3. InfoPath erstellt, der das XML-Dokument im Arbeitsspeicher eine DOM-Datenstruktur.
    
4. XSLT-Transformationen werden auf die DOM-Struktur angewendet, und dabei werden Ansichten erzeugt, in denen dem Benutzer eine entsprechende Darstellung des Dokuments angezeigt wird. Elemente am Anfang des XML-Dokuments können am unteren Ende der Ansicht und außerdem in einer anderen Ansicht in einer anderen Anordnung angezeigt werden. Die Ansichten bestehen aus Benutzeroberflächencontainern wie beispielsweise Bereichen, die Text und Steuerelemente enthalten (beispielsweise Textfelder, Felder für Rich-Text, Datumsauswahlfelder und Dropdownlisten. Container können auch weitere Container enthalten.
    
5. Bei der XSLT-Transformation wird XHTML als Ausgabe erzeugt, und dann wird ein CSS verwendet, um die Darstellung der XHTML-Ausgabe zu steuern.
    
6. Wenn das XML-Schema ermöglicht das Hinzufügen von Knoten zu einem Knoten der Datenstruktur, hat das Feld oder Gruppe dar, das die Knoten zugeordnet ist, ein Dropdown-Menü, in dem den Benutzer zum Hinzufügen oder Entfernen von Feldgruppen. Der Benutzer bearbeitet das Dokument durch eine wiederholte oder optionale Feldgruppe hinzufügen, wenn ein Wert eingegeben, Auswählen einer Option oder rich-Text eingegeben. Wenn ein XML-Schema-Knoten das Schema für XHTML zugeordnet ist, zeigt InfoPath eine Benutzeroberfläche zum Erstellen von rich-Text. Wenn der Benutzer rich-Text eingibt, wird XHTML-Inhalt als eine Unterstruktur im DOM erstellt.
    
7. Die Gültigkeit der DOM-Struktur wird immer aufrechterhalten. Wenn Benutzer das XML-Dokument bearbeiten, werden die Bearbeitungen anhand des zugeordneten XML-Schemas überprüft. Die versuchten Änderungen an der DOM-Struktur und den Blattknotenwerten werden anhand des XML-Schemas überprüft, um sicherzustellen, dass die Datentypen und Werte gültig sind. Wenn die versuchten Änderungen nicht gültig sind, wird ein Überprüfungsdialogfeld geöffnet, und die Änderungen werden nicht auf die DOM-Struktur angewendet. Wenn die Änderungen gültig sind, wird die DOM-Struktur aktualisiert.
    
8. Der geänderte Teil der Ansicht wird aktualisiert, indem nur die erforderlichen Teile des XSLT-Stylesheets auf die DOM-Struktur angewendet werden.
    
9. Die Benutzer können das XML-Dokument speichern oder mithilfe von einfachem HTTP oder SOAP senden. Die Benutzer können das Dokument nur senden, wenn dieses gemäß dem XML-Schema gültig ist.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a> Verwendung von XML-Standards beim Entwerfen eines Formulars

Sie können ein Formular entwerfen, indem Sie mit einem vorhandenen XML-Schema beginnen, indem Sie eine Verbindung mit einem XML-Webdienst oder einer XML-Datenbank herstellen und dessen bzw. deren XML-Schema abrufen oder indem Sie automatisch ein Schema aus einem neuen Formular oder aus einer XML-Datendatei generieren. Diese Szenarien werden in den folgenden Verfahren beschrieben. In Abbildung 3 wird die einfache Benutzeroberfläche zum Entwerfen einer Formularvorlage gezeigt.
  
1. Erstellen Sie ein neues Formular im InfoPath-Designer, indem Sie die Formularvorlage **XML oder Schema** auswählen, und wählen Sie dann eine vorhandene XML-Schema-Datei als Datenquelle aus. Das XML-Schema wird in den Aufgabenbereich geladen und als ein Strukturansicht-Steuerelement angezeigt wird. 
    
2. Verwenden Sie die Entwurfslayouttools, um die UI-Steuerelemente wie beispielsweise Zeilen und das Hintergrunddesign in einer oder mehreren Ansichten anzuordnen. Daraufhin werden einige der XSLT-Elemente generiert. Die XSLT-Ansichten und das XML-Schema werden automatisch der Formularvorlage zugeordnet.
    
3. Ordnen Sie die UI-Steuerelemente in den Ansichten der XML-Schemaelemente mithilfe von Drag-and-Drop. InfoPath schützt Sie geeignete Steuerelemente für die XML-Schemaelemente basierend auf der Art der Schemaelemente auswählen. Wenn der XML-Datentyp Datum angegeben wird, schlägt InfoPath beispielsweise ein Datumsauswahl-Steuerelement. Abhängig von Auswahl im XML-Schema, kann InfoPath Gruppen von Optionaler oder wiederholter Felder einfügen. Zuordnen der XML-Schemaelemente zu UI-Steuerelemente, generiert die XSLT-Struktur.
    
4. Speichern Sie die Formularvorlage. Sie können die Dateien, aus denen die Formularvorlage besteht, als einzelne Dateien in einem normalen Ordner oder als Dateien in einem CAB-Dateiordner speichern. In beiden Fällen handelt es sich um standardmäßige XML-Dateien. Die Formularvorlage kann jetzt von Benutzern verwendet werden.
    
Eine Formularvorlage enthält alle semantische Informationen, die zum Bereitstellen der strukturierten Bearbeitung, wenn ein Formular in InfoPath geöffnet ist erforderlich ist. Eine Formularvorlage enthält eine Manifestdatei, die XSLT-Dateien, die Ansichten zu definieren, die Informationen, die benötigt werden, um Daten und eine optionale Ressourcenbezeichner für ein XML-Webdienst zu überprüfen.
  
Das Manifest oder Formulardefinitionsdatei, ist der allgemeine Hub- and -Eintrag für alle Dateien, die von der Formularvorlage erforderlich sind. Das Manifest enthält Verweise auf die anderen Dateien in der Formularvorlage, und enthält Informationen, die zum Überprüfen von Daten und Bereitstellen der strukturierten Bearbeitung erforderlich ist. Die XML-Überprüfung Schemainformationen ist für die resultierende Benutzeroberfläche angepasst und der manifest-Datei hinzugefügt. Beispielsweise lässt das Schema Einfügen von mehreren optionalen Elemente in eine bestimmte Unterstruktur können Sie die Benutzeroberfläche entwerfen, sodass mehrere optionale Elemente hinzugefügt werden, wenn der Benutzer eine einzelne UI-Operation ausführt. Diese Anpassung ist wichtig, beim Bereitstellen von großer Benutzerzufriedenheit für normale Benutzer. 
  
Außerdem können Sie ein Formular entwerfen, indem Sie einen vorhandenen XML-Webdienst verwenden, um das XML-Schema bereitzustellen. Gehen Sie dazu folgendermaßen vor:
  
1. Verwenden Sie UDDI, um relevante Webdienste zu suchen.
    
2. Wählen Sie den Webdienst verwenden. InfoPath liest die WSDL-Datei des Webdiensts zugeordnet und identifiziert das XML-Schema verwendet werden.
    
3. Öffnen Sie das XML-Schema, um dieses zu laden.
    
4. Ordnen Sie die UI-Steuerelemente an, und ordnen Sie XML-Schemaelemente und -Attribute zu.
    
5. Definieren Sie, wie das XML-Dokument an den Webdienst gesendet werden soll, von dem SOAP verwendet wird.
    
Wenn Sie ein Formular von Grund auf entwerfen und das XML-Schema automatisch generieren möchten, gehen Sie folgendermaßen vor:
  
1. Klicken Sie auf der Registerkarte **Datei** wählen Sie entweder die **Leeres Formular** oder **Leeres Formular (InfoPath Filler)** einer Formularvorlage, und klicken Sie dann auf **Formular entwerfen**.
    
2. Klicken Sie auf der Registerkarte **Start** auf den Pfeil in der unteren rechten Ecke der Gruppe der **Steuerelemente** im Aufgabenbereich **Steuerelemente** anzeigen, und stellen Sie sicher, dass das Kontrollkästchen **Datenquelle automatisch erstellen** ausgewählt ist. (Standardmäßig ist dieses Kontrollkästchen aktiviert.) 
    
3. Entwerfen Sie die UI-Steuerelemente. Wie Sie diese Steuerelemente anordnen, InfoPath automatisch das XML-Schema erstellt und ordnet die Elemente und Attribute hinzu die UI-Steuerelemente.
    
So entwerfen Sie ein Formular, indem Sie mit einer wohlgeformten XML-Datendatei beginnen
  
1. Klicken Sie auf der Registerkarte **Datei** wählen Sie die Formularvorlage **XML oder Schema** , und klicken Sie dann auf **Formular entwerfen**.
    
2. Wählen Sie im **Datenquellen-Assistent**der XML-Datei, die Sie als Datenquelle verwenden möchten. Ein XML-Schema wird automatisch erstellt, basierend auf der XML-Datendatei.
    
3. Ordnen Sie die UI-Steuerelemente wie weiter oben in diesem Abschnitt beschrieben an.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Entworfen als idealer Client für Webdienste

Umfassende Unterstützung für Webdienste verfügbar gewinnt. Viele Back-End und Middle-Tier-Systeme können konfiguriert werden, für die Kommunikation mithilfe von Web Services-Standards wie SOAP, UDDI und WSDL-Datei. Diese Web Services aktivierten Systeme umfassen Datenbanken, Workflow-Systeme, Enterprise Resource planning (ERP), Customer Relationship Management (CRM) und anderen Systemen. InfoPath bietet nun eine ideale Benutzeroberfläche zum Anzeigen und bearbeiten die XML-Daten, die über die Webdienste gesendet wird. Abbildung 4 zeigt die integrierte Unterstützung für XML-Webdienste.
  
InfoPath passt gut zu dem lose verbundenen Modell von Webdiensten, in denen Daten zwischen Computern als vollständige XML-Dokumente gesendet werden. In diesem Kommunikationsmodell passt gut zur asynchronen Natur des Webs. Als allgemeine authoring Tool für XML-Dokumente unterstützt InfoPath der Dokument-Literal SOAP-Codierung anstelle von (Remote Procedure Call, RPC) SOAP-Codierung. InfoPath ist ein idealer Client für Webdienste, da es eine systemeigene lesen kann das XML-Schema in einer SOAP-Nachricht angegeben und erstellen Sie eine Benutzeroberfläche basierend auf dem Schema, wodurch Benutzer auf einfache Weise anzeigen und Bearbeiten von XML-Dokumenten, die generiert oder durch die entsprechende Web empfangen werden Dienst. InfoPath bietet auch Unterstützung für ADO.NET-Datasets, die das Nachverfolgen von Änderung enthält.
  
## <a name="terminology"></a>Terminologie

|||
|:-----|:-----|
|**Feldgruppe:** <br/> |Ein Bereich, ein wiederholter Bereich, ein optionaler Bereich oder eine wiederholte Tabelle. Bereiche und wiederholte Tabellen sind Steuerelemente in einem Formular, die weitere Steuerelemente enthalten und nach Bedarf wiederholt werden. Benutzer können beim Ausfüllen des Formulars mehrere Bereiche oder Zeilen einfügen.  <br/> |
|**DOM-Struktur:** <br/> |Die Struktur der Datenquelle des Formulars. In bestimmten, die die Auflistung der Felder und Gruppen, die definieren, und speichern Sie die Daten für ein InfoPath-Formular.  <br/> |
   
## <a name="conclusion"></a>Schlussbemerkung

InfoPath verwendet open XML-Standards, um Benutzern mit flexible, aber strukturierte Bearbeitung XML zur Datenerfassung bereitzustellen. Um eine einfache Benutzeroberfläche zum Visualisieren und Bearbeiten von hierarchischen XML-Daten zu ermöglichen, werden die DOM-Struktur verschachtelte Feldgruppen, die UI-Steuerelemente enthält zugeordnet. XSLT-Transformationen können der Inhalt der UI-Ansichten anders als die Struktur der XML-Daten organisiert werden.
  
InfoPath bietet mehr Flexibilität als statische Formulare mit strukturierte Bearbeitung und Überprüfung als Textverarbeitungsdokumente. Das Ergebnis ist ein hybrides Tool, das das beste eines herkömmlichen Dokuments bearbeiten Oberfläche mit den Funktionen strengen Datenerfassung eines Pakets Formulare, wodurch normalen Benutzer gültige XML-Dokumente zu erstellen, die zu einer benutzerdefinierten XML-Schema gehören kombiniert. Integrierte Unterstützung für Webdienste kann auf einfache Weise Definieren von Ansichten für die Bearbeitung von XML-Dokumenten, die mit einem Web Services-Schema entsprechen.
  

