---
title: Arbeiten mit XML-Schemas in InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Eine Formularvorlage, die Sie mit Microsoft InfoPath erstellen verwendet ein XML-Schema (XSD) strukturelle ausführen und die datenüberprüfung auf den XML-Code, die Eingabe des bearbeitet haben, und die Ausgabe von einem InfoPath-Formular. Jede Formularvorlage in InfoPath-Formular-Designer erstellten enthält mindestens eine XSD-Schemadatei (XSD), die für die Validierung zur Laufzeit verwendet wird.
ms.openlocfilehash: 6b19399e4f31f6270fa6f360a8428c725050ce16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568273"
---
# <a name="working-with-xml-schemas-in-infopath"></a>Arbeiten mit XML-Schemas in InfoPath

Eine Formularvorlage, die Sie mit Microsoft InfoPath erstellen verwendet ein XML-Schema (XSD) strukturelle ausführen und die datenüberprüfung auf den XML-Code, die Eingabe des bearbeitet haben, und die Ausgabe von einem InfoPath-Formular. Jede Formularvorlage in InfoPath-Formular-Designer erstellten enthält mindestens eine XSD-Schemadatei (XSD), die für die Validierung zur Laufzeit verwendet wird.
  
> [!NOTE]
> Die in diesem Thema enthaltene Informationen gilt für Formularvorlagen für die Verwendung in der InfoPath-Editor. Browserkompatible Formularvorlagen weisen strengere XSD-Schemas. Weitere Informationen finden Sie in der Dokumentation zu XML-Schemas in browserkompatiblen Formularvorlagen verfügbar auf MSDN. 
  
## <a name="using-externally-authored-xml-schemas"></a>Verwenden extern verfasster XML-Schemas

Befolgen Sie diese Schritte, um eine XSD-Schemadatei zu laden, die außerhalb von InfoPath verfasst wurde.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Erstellen einer Formularvorlage auf Grundlage eines externen Schemas

1. Klicken Sie in der Backstage-Ansicht auf **neu**, klicken Sie unter **Erweiterte Formularvorlagen**auf **XML oder Schema** , und klicken Sie dann auf **Dieses Formular entwerfen**.
    
2. Geben Sie im **Datenquellen-Assistent** die XSD-Schemadatei an, die Sie verwenden möchten und klicken Sie dann auf **Weiter**, um die restlichen Seiten im Assistenten zu vervollständigen. 
    
## <a name="unsupported-xsd-constructs"></a>Nicht unterstützte XSD-Konstrukte

In folgenden abschnitten werden die XSD-Konstrukte behandelt, die InfoPath zur Laufzeit nicht verarbeiten kann. Vermeiden Sie diese Konstrukte beim Erstellen einer Formularvorlage im InfoPath-Formulardesigner.
  
## <a name="entity-and-entities-types"></a>Die Typen ENTITY und ENTITIES

Bei den Typen **ENTITY** und **ENTITIES** ist für die Validierung eine Dokumenttypdefinition erforderlich, die InfoPath nicht unterstützt. Mit InfoPath können Sie keine Formularvorlage mit solch einem Schema entwerfen, es zeigt dann eine Fehlermeldung an, in der Ihnen empfohlen wird, den **ENTITY**-Typ in **NCName**  zu ändern, aus dem **ENTITY** abgeleitet wird. 
  
> [!NOTE]
>  Wenn Sie eine InfoPath-Formularvorlage außerhalb des Entwurfsmodus verfassen und sie ein XSD verwendet, das die Typen **ENTITY** und **ENTITIES** enthält, funktioniert die Formularvorlage möglicherweise zur Laufzeit, wenn die Template.xml-Datei die erforderliche DTD fü diese Typen enthält. 
  
## <a name="required-xsdany-element"></a>Erforderliche xsd:beliebiges Element

Ein Vorkommen eines **xsd:any**-Platzhalterelements, also ein Vorkommen eines **xsd:any**-Elements mit einem **minOccurs**-Attributwert größer Null ("beliebige erforderlich“) verhindert, dass InfoPath deterministisch eine gültige Instanz für dieses Schemafragment erstellt. InfoPath muss in der Lage sein, beim Generieren eines Formulars eine gültige Instanz zu erstellen, die dieses Schemafragment verwendet. Als Teil der Ausführung des **Datenquellenassistenten** müssen Sie bei Schemas mit erforderlichen **xsd:any**-Elementen auswähle, welches Schemaelement Sie statt des erforderlichen **xsd:any**-Elements verwenden möchten. 
  
## <a name="elements-with-an-abstract-complex-type"></a>Elemente mit einem abstrakten komplexen Typ

InfoPath-Entwurfsmodus unterstützt Entwerfen einer Formularvorlage für Schemas, die abstrakte komplexe Typen verwendet werden. Beispielsweise, wenn ein Element mit dem Namen `shippingAddress` hat einen abstrakten komplexen Typ mit dem Namen `address` , bei dem abgeleiteten Objekte `USAddress` und `CanadianAddress`, InfoPath behandelt jede Instanz von `shippingAddress` als Wahl zwischen `shippingAddress` mit Typ `USAddress` und `shippingAddress` mit `CanadianAddress` . In diesem Beispiel wird die bereitgestellten Schemas keine Typen enthalten, die von-Adresse abgeleitet fordert InfoPath ein zusätzliches Schema an, das diese Anforderung erfüllt. 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>XSD-Konstrukte mit reduzierter Funktionialität

In den folgenden Abschnitten werden XSD-Konstrukte beschrieben, die beim Verwenden zur Erstellung einer Formularvorlage im InfoPath-Formulardesigner reduzierte Funktionalität besitzen.
  
## <a name="substitution-groups"></a>Ersatzgruppen

Alle Elemente der Ersatzgruppen werden im Aufgabenbereich **Felder** angezeigt. InfoPath stellt die Ersatzmöglichkeiten als Auswahl aller Ersatzgruppen bereit (einschließlich des definierenden Elements, wenn es nicht abstrakt ist). Wenn für ein abstraktes Element keine Ersatzgruppen vorhanden sind, fordert Sie InfoPath dazu auf, ein Schema anzugeben, das mindestens ein Element enthält, bei dem es sich um eine Ersatzgruppe handelt. 
  
## <a name="unbounded-choice-elements"></a>Nicht gebundene Auswahlelemente

Das folgende Schemafragment zeigt ein nicht gebundenes Auswahlelement:
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

InfoPath zeigt sich wiederholende Auswahlelemente als wiederholte Auswahlen im Aufgabenbereich **Felder** an. Es gibt ein **Wiederholte Auswahlgruppe**-Steuerelement, das Sie zum Darstellen der heterogenen Liste verwenden können, die vom wiederholten Auswahlelement in der XSD definiert wird. 
  
## <a name="repeating-sequence"></a>Wiederholte Sequenz

Folgendes Schemafragment zeigt eine wiederholte Sequenz:
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

Solange die wiederholte Sequenz ein erforderliches Element enthält, lädt InfoPath die XSD ohne sie anzupassen. Sie können die Steuerelemente für wiederholte Abschnitte an die wiederholte Sequenz binden
  
## <a name="choice-of-model-groups"></a>Modellgruppenauswahl

Folgendes Schemafragement zeigt das Auswahlelement, das mehrere Modellgruppen enthält:
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

Der InfoPath-Entwurfsmodus unterstützt diese XSD-Konstrukte, ohne dass eine Anpassung durch den Formulardesigner erforderlich ist. Obwohl InfoPath die Bedeutung des Schemas nicht anpasst, vereinfacht es das Auswahlkonstrukt oben in einer equivalenten reduzierten einzelnen Auswahl im Aufgabenbereich **Felder**. 
  
## <a name="optional-sibling-with-same-qualified-name"></a>Optionales gleichgeordnetes Element mit dem gleichen qualifizierten Namen

Das folgende Schemafragment zeigt einen optionalen gleichgeordneten Knoten mit demselben qualifizierten Namen (`QName`):
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

**XPath**-Ausdrücke für diese Knoten können komplex sein, da jede potenzielle XML-Instanz im InfoPath-Formulardesigner berücksichtigt werden muss. InfoPath macht keine Teile des Schemas verfügbar, bei denen beim Erstellen der korrekten **XPath**-Bindungen Schwierigkeiten auftreten können. Es werden Warnungen zu den Teilen des Schemas angezeigt, die ignoriert werden. 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>XSD-Konstrukte in InfoPath mit besonderer Bedeutung

In den folgenden Abschnitten werden XSD-Konstrukte beschrieben, die beim Erstellen einer Formularvorlage im Entwurfsmodus eine besondere Bedeutung haben. In diesen Abschnitten wird beschrieben, wie Sie die Konstrukte in Ihrem Schema verwenden können, um bestimmte Verhaltensweisen zu aktivieren.
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>Hinzufügen neuer Elementfelder und Gruppen mit dem Aufgabenbereich "Felder"

Sie können Ihr Schema so erstellen, dass Sie den Aufgabenbereich **Felder** zum Hinzufügen neuer Elementfelder und Gruppen zu einem Element zur Entwurfszeit verwenden können. Deklarieren Sie dazu ein Element in Ihrem Schema mit einem optionalen, nicht gebundenen **xsd:any**-Element, das das Namespace-Attribut mit dem **##any**-Platzhalter angibt. Im Entwurfsmodus können Sie anschließend den Aufgabenbereich **Felder** verwenden, um dem Element neue Elementfelder und Gruppen hinzuzufügen. Sie können beispielsweise folgendem Element neue Inhalte hinzufügen: 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>Hinzufügen neuer Attributfelder mit dem Aufgabenbereich "Felder"

Ähnlich wie bei dem Elementfall können Sie ein Attribut mit einem **anyAttribute**-Element deklarieren, bei dem das Namespace-Attribut als **##any**-Platzhalter angegeben ist. Zur Entwurfszeit können Sie den Aufgabenbereich **Felder** verwenden, um dem Schemaattribut neue Inhalte hinzuzufügen. 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>Speichern von XML-Signaturen in der Datenquelle

Um Benutzern zum digitalen Signieren ein Formulars zur Laufzeit zu ermöglichen, muss das Schema der Datenquelle deklarieren Sie ein Element mit dem Namen Signatur zum Speichern von XML-Signaturen (digitale Signatur) Informationen, die erstellt wird, wenn ein Benutzer das Formular signiert. Stellen Sie diese Deklaration mit der **Xsd: alle** Element mit dem Namespaceattribut als XML-Signaturen Namespace mit einem Platzhalterzeichen wie folgt angegeben: "http://www.w3c.org/2000/09/xmldsig#" 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a>Binden eines Felds an ein Rich-Text-Steuerelement

 **Rich-Text-Feld**-Steuerelemente in InfoPath generieren generische XHTML; deshalb muss Ihr Schema angeben, dass eine beliebige Anzahl von Texten und XHTML-Knoten im XML der Formularinstanz gültig ist. Sie können diese Spezifikation mit folgendem XSD-Konstrukt erreichen: 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="http://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> InfoPath ändert niemals die Inhalte der Schemadatei (.xsd), folgert daraus jedoch zu Entwurfszwecken möglicherweise logisch eine Teilmenge. Die Schemadatei bleibt in der Formularvorlage zur Entwurfs- und Laufzeit immer unverändert. 
  
## <a name="debugging-common-xsd-errors"></a>Debuggen häufiger XSD-Fehler

Wenn Sie extern verfasste XSD-Dateien zum Erstellen von Formularvorlagen im InfoPath-Formulardesigner laden, erhalten Sie möglicherweise eine von zwei Fehlermeldungstypen: MSXML-Fehlermeldungen oder InfoPath-Fehlermeldungen. MSXML-Fehlermeldungen werden im Bereich **Details** eines Dialogfelds einer InfoPath-Fehlermeldung angezeigt, sie beginnen immer mit einem Verweis zu dem Namen oder Pfad der Schemadatei, die den Fehler auslöst. Einige gültige XSD-Schemakonstrukte werden von InfoPath nicht unterstützt; diese werden im Abschnitt "Nicht unterstützte XSD-Konstrukte" behandeltn. In den folgenden Abschnitten werden einige häufige Fehler beschrieben, durch die beim Laden von Schemas in InfoPath ein Fehler erzeugt wird. 
  
## <a name="the-xsd-namespace-declaration"></a>Die XSD-Namespace-Deklaration

Ähnlich wie bei allen W3C-Standards, haben XML-Schemas (XSD) ein langwieriges Überprüfungsverfahren durchlaufen, bevor Sie als Empfehlung genannte wurden. Es gab viele Arbeitsentwürfe und folglich wurden viele XSD-Dateien basierend auf diesen entwickelten Standards geschrieben. Während des Verfahrens hat Microsoft eine proprietäre Schemasprache mit der Bezeichnung XML-Data Reduced (XDR) entwickelt, die bei MSXML 3.0 enthalten ist. Ab Version MSXML 4.0 unterstützen die Microsoft XML Core Services das gesamte Empfehlungsspektrum an XSD. Viele Programme zum Erstellen von Schemas warteten nicht darauf, dass das gesamte Empfehlungsspektrum für XSD ausgesprochen wurde. Ältere Versionen dieser Programme erzeugen möglicherweise veraltete XSD-Dateien, das die MSXML 5.0-Infrastruktur nicht unterstützt, von der InfoPath abhängt.
  
Um sicherzustellen, dass eine XSD-Datei die volle XSD-Empfehlung unterstützt, sollte in die folgenden XML-Namespacedeklaration enthalten die \<Schema\> Tag:
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

Ähnlich wie bei allen XML-Namespacedeklarationen kann das, XML-Präfix (in diesem Fall 'xsd') jede gültige Präfixzeichenfolge sein. Einige Ihnen in der Praxis begegnende Präfixe sind 'xsd', 'xs' und '' (kein Präfix). MSXML meldet in der Regel einen Fehler, dass der Stamm nicht korrekt definiert wird, wenn diese Namespace-Deklaration fehlt.
  
## <a name="importing-and-including-schemas"></a>Importieren und Aufnehmen von Schemas

XSD-Schemas können erweitert werden und können andere Schemas importieren sowie aufnehmen. Allgemein kann man sagen, Sie sollten ein Schema importieren, wenn das im **targetNamespace**-Attribut angegebene Schema vom aktuellen Schema abweicht. Sie sollten es aufnehmen, wenn das im **targetNamespace**-Attribut angegebene Schema dem aktuellen Schema entspricht. 
  
Die Semantik zum Importieren und Aufnehmen von Schemas lautet wie folgt:
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

Wenn das **schemaLocation**-Attribut fehlt (wie es bei einigen Konvertern vorkommt), löst MSXML einen Fehler aus, da es die Datei nicht finden kann. Wenn Sie diesen Fehler erhalten, stellen Sie außerdem sicher, dass die Ressource oder der Speicherort, der im schemaLocation-Attribut angegeben ist, für Benutzer der Formularvorlage zugänglich ist. Offenbar treten Fehler auf, wenn das **schemaLocation**-Attribut auf einen Server oder ein Verzeichnis verweist, der ausgefallen oder nicht vorhanden ist oder wenn Benutzer darauf keine Zugriffsberechtigungen besitzen. Untersuchen Sie außerdem alle importierten und aufgenommenen Schemas, um sicherzustellen, dass sie gültig sind. 
  
> [!NOTE]
> Von Problemen mit dem **schemaLocation**-Attribut verursachte Probleme sind nur ein Problem, wenn InfoPath zunächst die Schemas importiert; also wenn Sie zunächst ein Formular auf Grundlage eines vorhandenen Schemas entwerfen. Anschließend arbeitet InfoPath mit zwischengespeicherten Versionen der Schemadateien, die in der Formularvorlage gespeichert sind. 
  
Beim Import eines Schemas ist ein Namespace-Attribut zulässig, wenn das Schema kein **targetNamespace**-Attribut angibt. Allgemein lässt sich sagen, dass der Namespace beim Import mit dem im Schema angegebenen **targetNamespace** übereinstimmen muss, das Sie importieren. 
  
## <a name="nondeterministic-schemas"></a>Nicht deterministische Schemas

Die MSXML 5.0-Infrastruktur, von der InfoPath abhängt, kann zuverlässig Fehler erkennen und auslösen, um Sie zu nicht deterministischen Schemas zu benachrichtigen, die sich daraus ergebende Fehlermeldung stellt jedoch keine Zeilenanzahl bereit, um Ihnen mitzuteilen, welcher Teil des Schemas einen Fehler auslöst. In diesem Abschnitt wird besprochen, warum es bei XSD-Schemadateien wichtig ist, dass sie deterministisch sind und welche Bedeutung es hat, wenn sie nicht deterministisch sind. Außerdem werden einige zu vermeidende Fehler aufgezeigt.
  
XSD-Schemas dienen der Validierung der XML-Datenstruktur und der Typensemantik. Zur Realisierung dieser Aufgabe muss das Validierungssystem (in diesem Fall MSXML 5.0) den XSD-Deklarationen XML-Knoten zuordnen. Ohne diese Zuordnung kann das Validierungssystem diese Aufgabe nicht erfüllen. Wenn eine Zuordnung garantiert werden kann, ist das Schema deterministisch. Wenn es eine einzelne XML-Instanz gibt, durch die diese Zuordnung unmöglich wird, ist das Schema nicht deterministisch.
  
Folgendes Beispielschema ist nicht deterministisch:
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

Um aufzuzeigen, warum dieses XSD-Segment nicht deterministisch ist, nehmen Sie an, Sie hätten folgendes XML-Fragment, das Sie mit diesem Schema validieren möchten:
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

In diesem XML-Fragment, es ist nicht klar, ob die * \<Dateipfad\> * Element des ersten Teils der auswahldeklaration des Knotens erforderlich oder optional diejenige des zweiten Teils der auswahldeklaration ist. Diese Unterscheidung ist aus den folgenden Gründen wichtig: 
  
1. Wenn das XML-Fragment mit dem ersten Teil der Auswahldeklaration validiert wird, ist die XML mit dem Schema gültig.
    
2. Wenn das XML-Fragment anhand des zweiten Teils der auswahldeklaration überprüft wird, ist das Schema nicht gültig, da der erforderliche \<URI\> -Knoten fehlt. 
    
Einige XSD-Validierungssysteme validieren mit diesem Schema, da es einen gültigen Pfad gibt. MSXML ist strenger und löst einen Fehler aus, in dem angegeben ist,dass das Schema nicht deterministisch ist.
  
Darauf folgenden einige Beispiele von nicht deterministischen Schemas. Das erste behandelt optionale Elemente. Diese Fälle treten oft bei XDR-zu-XSD-Konvertern auf, da Unterschiede in den Standard-Kardinalitäten in den beiden Schemasprachen vorliegen. Der erste zu berücksichtigende Fall sind optional deklarierte Elemente mit **xsd:choice**- und **xsd:sequence**-Elementen. Optionale in einem **xsd:sequence**-Element deklarierte Elemente können in der Regel ordnungsgemäß deklariert werden, so lange Sie Elemente mit dem gleichen Namen nicht mehrmals besitzen, und nur optionale Elemente dazwischen. Beispiel: 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

Um zu verstehen, warum dieses Schemasegment nicht deterministisch ist, wird davon ausgegangen, dass Sie das folgende ungültige XML-Fragment besitzen:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

Dieses Fragment betrachten, Sie können sehen, warum es ungültig ist: Es gibt zwei `<aNode>` Elemente vor dem `<anotherNode>` Element, während nur eines zulässig ist. 
  
Gehen wir nun davon aus, Sie müssen folgende XML-Instanz validieren:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

Die Herausforderung besteht darin, zu bestimmen, ob diese Instanz gültig ist. Haben Sie zwei `<aNode>` Elemente, in dem nur eines zulässig ist, oder verfügen Sie über, ein `<aNode>` -Element, in dem es zulässig ist, und eine andere Position zulässig? Das Schema ist nicht deterministisch, da es nicht möglich ist, kennen. 
  
Optionale in einem **xsd:choice**-Element deklarierte Elementen sind in der Regel problematisch. Im folgenden vereinfachten Beispiel gibt es keine Möglichkeit zu ermitteln, ob die Auswahl einmal mit dem nicht vorhandenen optionalen Element auftrat, oder es nie auftrat. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

Die letzten Verfahren ist die Verwendung einer **Xsd: alle** -Element ohne eine Namespace-Definition, wie in `<xsd:any namespace="##other"/>` , nach einem **xsd: Sequence** -Element. Dieses Konstrukt ist besonders störend, wenn es sich um ein optionales Element folgt. Wenn Sie im vorherige Beispiel Laufe und ändern nur den letzten Knoten, der ein **Xsd: alle** -Element können Sie sehen, dass alle vorherigen Argumente zu Nondeterminism weiterhin anwenden, die wie folgt: 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a>Ungültige Aufzählungswerte

XSD-Schemas führen in der Regel keine Typenvalidierung durch, bis Sie ein tatsächliches Instanzdokument validieren. Eine Ausnahme davon ist es, wenn Sie eine Aufzählung in Ihrem Schema haben. In diesem Fall validiert das Schema die Aufzählungswerte mit den Aufzählungstypen, um sicherzustellen, dass sie die korrekten Knotenwerte sind. Im Folgenden zwei Beispiele:
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Dieses Schema ist ungültig, da "elf Uhr" kein gültiger Wert für ein Element des Typs **xsd:time** ist.
  
Im Folgenden ein komplexeres Beispiel:
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Um zu verstehen, warum dieses Beispiel ungültig ist, müssen Sie verstehen, wie der Typ **xsd:NMTOKEN** definiert ist. Die W3C-Datentypenspezifikation definiert den **NMTOKEN**-Typ wie folgt: "Ein NMTOKEN (Namenstoken) ist eine beliebige Mischung von Namenszeichen." 
  
Wenn Sie den Fall weiter untersuchen, werden Sie herausfinden, dass '&' kein gültiges Namenszeichen ist und deshalb kann "M&Ms" nicht als **NMTOKEN**-Typ validiert werden. 
  
## <a name="empty-sequence-or-choice-elements"></a>Leere Sequenz oder Auswahlelemente

MSXML löst in manchen Fällen Fehler zu Schemadeklarationen aus, die leere  **xsd:choice**- oder **xsd:sequence**-Elemente enthalten, siehe folgendes Beispiel. 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

Entfernen des leeren `<xsd:choice />` Tag sollte dieses Problem zu beheben. 
  
## <a name="regular-expressions"></a>Reguläre Ausdrücke

MSXML 5.0 möglich Problemen mit der Überprüfung der regulären Ausdrucksmuster beim Laden. Reguläre Ausdrücke können kompliziert sein, und Sie vorsichtig, wenn Sie solche verwenden. Alle XSD-Parser scheint flexible regulären Ausdruck Sprachen haben; d. h., implementieren sie die offizielle XSD-regulären Sprache plus Elemente aus anderen Sprachen für reguläre Ausdrücke. Wenn InfoPath-Formular-Designer Probleme Analysieren eines regulären Ausdrucks aufweist, klicken Sie dann InfoPath generiert Beispieldaten möglicherweise ungültig oder überhaupt nicht generiert werden können. Dies ist zur Entwurfszeit zulässig, da InfoPath nur Beispieldaten für die Formatierung verwendet. Jedoch, wenn Sie einen regulären Ausdruck, den MSXML nicht unterstützt verwenden, kann nicht klicken Sie dann InfoPath überprüfen einen Wert dafür, wenn ein Benutzer ein Formular ausfüllt. [XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)wird beschrieben, was in regulären Ausdrücken XSD-unterstützt wird. Weitere Informationen zu regulären XSD-Ausdrücken und Unicode-Ebene 1 reguläre Ausdrücke finden Sie unter [Reguläre Ausdrücke Unicode](http://www.unicode.org/reports/tr18/) . 
  
## <a name="targetnamespace-attribute-issues"></a>targetNamespace-Attribut-Probleme

XSD ist insofern, dass standardmäßig das **TargetNamespace** -Attribut auf nur Deklarationen der obersten Ebene, verweist zwar Sie festlegen können, `attributeFormDefault=qualified` und `elementFormDefault=qualified` dieses Standardverhalten außer Kraft gesetzt. Als Beispiel wird davon ausgegangen Sie, dass Sie die folgenden XSD verfügen. 
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

Ihr XML-Instanzdokument ähnelt folgendem Beispiel.
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

Lokale Definitionen erfordern keinen Zielnamespace, da die Qualifizierung standardmäßig deaktiviert ist. Wenn Sie jedoch Ihre lokale Definition in global ändern, muss der Verweis mit dem Namespace-Präfix qualifiziert werden. Das folgende Schema ist beispielsweise ungültig.
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

Mit diesem Schema ist ungültig, da im Namespace "global" ist "http://ns". Das einfache Ref = "global" wird nicht erkannt, da kein Standardnamespace ist "http://ns". Um dieses Problem zu beheben, müssen Sie ein Präfix für den Zielnamespace hinzufügen und verwenden, die für alle globalen Verweise und-Typ verwendet. Das korrigierte Schema sieht folgendermaßen aus.
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
    xmlns:ns="http://ns" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

Wenn bei Ihrem Schema das **targetNamespace**-Attribut angegeben ist, vergewissern Sie sich, dass alle globalen Verweise mit dem korrekten Namespace-Präfix qualifiziert werden. 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>XML-Verarbeitungsanweisungscodierung (Unicode vs. ANSII)

XML unterstützt nur Unicode-Zeichensätze. Deshalb gehen Ihnen möglicherweise Informationen verloren, wenn Sie Dateien speichern, die ANSII-Zeichen verwenden. Das Speichern von Dateien als UTF-16 ist möglicherweise jedoch unverhältnismäßig für Ihre Zwecke. Um die Implementierungskosten eines XML-Readers zu verringern, muss der XML-Autor angeben, welche Codierung er in der XML-Verarbeitungsanweisung auf oberster Ebene verwenden möchte. Dabei nehmen Sie möglicherweise von folgende Verarbeitungsanweisung Notiz.
  
```XML
xml version="1.0" encoding="UTF-8"
```

Dieses Verarbeitsungsanweisungstag gibt die an, dass die Codierung der Datei UTF-8 lautet. Sie müssen sich vergewissern, dass die Dateicodierung der Codierung entspricht, die im Verarbeitungsanweisungstag angegeben ist. Sie können die Codierung ermitteln, indem Sie sich die Bytes der Datei und das Unicode-Byte der Reihenfolgemarken ansehen. Es geht jedoch auch noch einfacher. Wenn Sie Probleme mit dem Öffnen eines XSD-Schemas haben, geben Sie die Codierung als "UTF-8" an, öffnen Sie es in einem Text-Editor (z. B. Notepad) und speichern Sie die Datei dann mit der UTF-8-Codierung ab (Notepad stellt im Dialogfeld**Speichern unter**  die Dropdownliste **Codierung** bereit). Wenn Sie dennoch Probleme mit dem Öffnen der Datei haben, handelt es sich nicht um ein Codierungsproblem. 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>maxOccurs-Attribut im xsd:all-Element

Aufgrund der Art und Weise wie nicht deterministisch in der XML-Schemaempfehlung definiert ist, lautet der einzige gültige Wert für das **maxOccurs**-Attribut eines **xsd:element**-Elements in einem **xsd:all**-Element 1. Der folgende Wert ist beispielsweise gültig. 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

Dieses Beispiel ist jedoch ungültig.
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

In diesem Beispiel ist ungültig, da das Validierung System bestimmen, ob zwei kann nicht Vorkommen des `<x/>` Zuordnung der einzelnen Deklaration oder die Deklaration und einem anderen ungültige Definition. Entlang der gleichen Linien kann Ihnen nicht zwei Elemente mit demselben Namen in einer `<xsd:all>` Tag. 
  
In diesem Beispiel ist auch interessant, weil es Ihnen ermöglicht, eine beliebige Anzahl von `<x/>` und `<docs/>` Knoten innerhalb eines enthaltenden Elements in beliebiger Reihenfolge. Obwohl dieses Konstrukt ungültig ist, kann ein umgangen werden. Mit dem **xsd: choice** -Element, erzielen Sie dasselbe Ergebnis wie im folgenden Beispiel gezeigt. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Bearbeiten oder Erstellen eines XSD für InfoPath

Die beiden Beispiel in den folgenden beiden Abschnitten zeigen auf, wie ein Schema bearbeitet oder erstellt werden kann, um in InfoPath bestimmte Ergebnisse zu erzeugen.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Zulassen von Einfügevorgängen benutzerdefinierter Elemente im Aufgabenbereich "Felder"

Damit benutzerdefinierte Elemente unter einem übergeordneten Element im Aufgabenbereich **Felder** angezeigt werden können, müssen Sie das Einfügen eines **Xsd: alle** Element unterhalb des übergeordneten Elements. Um benutzerdefinierte Elemente in eingefügt werden können `<your_node_name>` , die XSD-Deklaration sollte etwa folgendermaßen aussehen. 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

Wenn Sie auch benutzerdefinierte Attribute zulassen möchten, müssen Sie hinzufügen `<xsd:anyAttribute namespace="##any | ##other"/>` Sie der Elementdeklaration. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Zulassen des Bindens von Rich-Text-Elementen in den Entwurfs- und Bearbeitungsmodi in InfoPath

Wenn Sie möchten, deklarieren ein Element, das an ein **Feld für Rich-Text** -Steuerelement gebunden werden können, es sollte folgende Form auf, einschließlich der **Xsd: alle** Element, das ein Namespace-Attribut auf festgelegt hat "http://www.w3.org/1999/xhtml" wie im folgenden Beispiel dargestellt. 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a>Schlussbemerkung

Durch die Nutzung der InfoPath-Unterstützung zum Entwerden von XML-Formularlösungen, die auf extern verfassten XML Schemadateien (.xsd) basieren, können Sie eine Formularvorlage erstellen, die mit einem Schema gemäß Industriestandard oder einem benutzerdefinierten Schema funktioniert, das von Ihrem Unternehmen erstellt wurde. Mithilfe der Informationen in diesem artikel können Sie benutzerdefinierte XSD-Schemadateien erstellen, die mit InfoPath kompatibel sind und Sie können häufige Probleme behandeln, die beim Laden extern verfasster XS-Dateien in der InfoPath-Entwurfsumgebung auftreten können.
  
## <a name="see-also"></a>Siehe auch

- [W3C-XML-Schema](http://www.w3.org/XML/Schema)
- [Einführung in W3C XML-Schema](http://www.w3.org/TR/xmlschema-0/)
- [W3C XML-Schemareferenz Strukturen](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [W3C XML-Schemareferenz für Datentypen](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [XML-Schema-Lernprogramm](https://www.w3schools.com/xml/schema_intro.asp)
- [XML Developer Center](http://msdn.microsoft.com/en-us/xml/default.aspx)

