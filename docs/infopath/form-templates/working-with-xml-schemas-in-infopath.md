---
title: Arbeiten mit XML-Schemas in InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Eine Formularvorlage, die Sie mit Microsoft InfoPath erstellen, verwendet ein XML-Schema (XSD), um eine Struktur- und Datenüberprüfung für die XML durchzuführen, die von einem InfoPath-Formular eingegeben, bearbeitet und ausgegeben wird. Jede im InfoPath-Formulardesigner erstellte Formularvorlage enthält mindestens eine XSD-Schemadatei (.xsd), die zur Laufzeigt für die Validierung verwendet wird.
ms.openlocfilehash: 25828c3ec21d22a9952452d5a82fe1a3b4bab54c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303164"
---
# <a name="working-with-xml-schemas-in-infopath"></a>Arbeiten mit XML-Schemas in InfoPath

Eine Formularvorlage, die Sie mit Microsoft InfoPath erstellen, verwendet ein XML-Schema (XSD), um eine Struktur- und Datenüberprüfung für die XML durchzuführen, die von einem InfoPath-Formular eingegeben, bearbeitet und ausgegeben wird. Jede im InfoPath-Formulardesigner erstellte Formularvorlage enthält mindestens eine XSD-Schemadatei (.xsd), die zur Laufzeigt für die Validierung verwendet wird.
  
> [!NOTE]
> Die in diesem Thema enthaltenen Informationen gelten für Formularvorlagen, die für die Verwendung im InfoPath-Editor entwickelt wurden. Browserkompatible Formularvorlagen haben strengere XSD-Schemaanforderungen. Weitere Informationen fniden Sie in der Dokumentation zu XML-Schemas in browserkompatiblen Formularvorlagen, die im MSDN verfügbar sind. 
  
## <a name="using-externally-authored-xml-schemas"></a>Verwenden extern verfasster XML-Schemas

Befolgen Sie diese Schritte, um eine XSD-Schemadatei zu laden, die außerhalb von InfoPath verfasst wurde.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Erstellen einer Formularvorlage auf Grundlage eines externen Schemas

1. Klicken Sie in der Backstage auf **Neu,** klicken Sie unter **Erweiterte Formularvorlagen** auf XML oder **Schema,** und klicken Sie dann **auf Dieses Formular entwerfen.**
    
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

Der InfoPath-Entwurfsmodus unterstützt das Entwerfen einer Formularvorlatge mit Schemas, die abstrakte komplexe Typen verwenden. Wenn ein Element mit dem Namen beispielsweise einen abstrakten komplexen Typ mit dem Namen hat, der zwei Ableitungen enthält, und  `shippingAddress`  `address` behandelt  `USAddress`  `CanadianAddress` InfoPath  `shippingAddress`  `shippingAddress`  `USAddress`  `shippingAddress` jede  `CanadianAddress` Instanz von als Auswahl zwischen typ und mit typ . Wenn die in diesem Beispiel bereitgestellten Schemas keine Typen enthalten, die von einer Adresse abgeleitet wurden, fordert InfoPath ein zusätzliches Schema an, das diese Anforderung erfüllt. 
  
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

Das folgende Schemafragment zeigt ein optionales gleichgeordnetes Schema mit demselben qualifizierten Namen ( `QName` ):
  
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

Damit Benutzer ein Formular zur Laufzeit digital signieren können, muss das Schema der Datenquelle ein Element mit der Bezeichnung "Signatur" zum Speichern von XML-Signaturinformationen (digitale Signatur) deklarieren, das beim Signieren des Formulars durch einen Benutzer signiert wird. Sie erstellen diese Deklaration, indem Sie das **xsd:any-Element** mit dem Namespaceattribut verwenden, das als XML Signatures-Namespace mit einem Platzhalterzeichen angegeben ist, wie folgt: https://www.w3c.org/2000/09/xmldsig# " " 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3c.org/2000/09/xmldsig#"  
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
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="https://www.w3.org/1999/xhtml" processContents="lax"/> 
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
  
Um sicherzustellen, dass eine XSD-Datei die vollständige XSD-Empfehlung unterstützt, sollte sie die folgende XML-Namespacedeklaration im \< Schematag \> enthalten:
  
```XML
xmlns:xsd="https://www.w3.org/2001/XMLSchema"
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

In diesem XML-Fragment ist nicht klar, ob das *\< \> file_path-Element* der erforderliche Knoten aus dem ersten Teil der Auswahldeklaration oder der optionale aus dem zweiten Teil der Auswahldeklaration ist. Diese Unterscheidung ist aus folgenden Gründen relevant: 
  
1. Wenn das XML-Fragment mit dem ersten Teil der Auswahldeklaration validiert wird, ist die XML mit dem Schema gültig.
    
2. Wenn das XML-Fragment für den zweiten Teil der Auswahldeklaration überprüft wird, ist das Schema ungültig, da der erforderliche \< URI-Knoten \> fehlt. 
    
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

Wenn Sie sich dieses Fragment anschauen, sehen Sie, warum es ungültig ist: Es gibt zwei Elemente vor dem Element, wenn nur  `<aNode>`  `<anotherNode>` eines zulässig ist. 
  
Gehen wir nun davon aus, Sie müssen folgende XML-Instanz validieren:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

Die Herausforderung besteht darin, zu ermitteln, ob diese Instanz gültig ist. Verfügen Sie über zwei Elemente, bei denen nur eines zulässig ist, oder haben Sie ein Element, in dem es zulässig ist, und ein weiteres Element, in dem  `<aNode>`  `<aNode>` es zulässig ist? Das Schema ist nicht deterministisch, da es keine Möglichkeit gibt, es mit Sicherheit zu sagen. 
  
Optionale in einem **xsd:choice**-Element deklarierte Elementen sind in der Regel problematisch. Im folgenden vereinfachten Beispiel gibt es keine Möglichkeit zu ermitteln, ob die Auswahl einmal mit dem nicht vorhandenen optionalen Element auftrat, oder es nie auftrat. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

Die letzte fragwürdige Vorgehensweise ist die Verwendung eines **xsd:any-Elements** ohne Namespacedefinition, wie in , nach einem `<xsd:any namespace="##other"/>` **xsd:sequence-Element.** Dieses Konstrukt ist besonders fehleranfällit, wenn es auf ein optionales Element folgt. Wenn Sie das vorherige Beispiel erneut aufrufen, uund nur den letzen Knoten eines **xsd:any**-Elements ändern, werden Sie sehen, dass alle vorherigen Argumente zu den nicht deterministischen Eigenschaften weiterhin gelten, siehe Folgendes: 
  
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

Das Entfernen des leeren  `<xsd:choice />` Tags sollte dieses Problem beheben. 
  
## <a name="regular-expressions"></a>Reguläre Ausdrücke

MSXML 5.0 kann Probleme beim Überprüfen regulärer Ausdrucksmuster beim Laden haben. Reguläre Ausdrücke können kompliziert sein, und Sie sollten vorsichtig sein, wenn Sie sie verwenden. Jeder XSD-Parser scheint flexible Sprachen für reguläre Ausdrücke zu haben. Das heißt, sie implementieren die offizielle XSD-reguläre Ausdruckssprache sowie Elemente aus anderen regulären Ausdruckssprachen. Wenn der InfoPath-Formulardesigner Probleme beim Analyse eines regulären Ausdrucks hat, sind die von InfoPath generierten Beispieldaten möglicherweise ungültig oder werden gar nicht generiert. Dies ist zur Entwurfszeit akzeptabel, da InfoPath nur Beispieldaten für die Formatierung verwendet. Wenn Sie jedoch einen regulären Ausdruck verwenden, der von MSXML nicht unterstützt wird, kann InfoPath keinen Wert dafür überprüfen, wenn ein Benutzer ein Formular ausfüllt. [Xml Schema Part 0: Primer Second Edition](https://www.w3.org/TR/xmlschema-0/)beschreibt, was in regulären XSD-Ausdrücken unterstützt wird. Weitere Informationen zu regulären XSD-Ausdrücken und regulären Unicode-Ausdrücke auf Ebene 1 finden Sie unter [Unicode Regular Expressions](https://www.unicode.org/reports/tr18/) . 
  
## <a name="targetnamespace-attribute-issues"></a>targetNamespace-Attribut-Probleme

XSD ist interessant, da sich das **targetNamespace-Attribut** standardmäßig nur auf die Deklarationen auf oberster Ebene bezieht, obwohl Sie dieses Standardverhalten festlegen und  `attributeFormDefault=qualified`  `elementFormDefault=qualified` überschreiben können. Gehen Sie als Beispiel von folgender XSD aus. 
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema" targetNamespace="https://ns" > 
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
<ns:root xmlns:ns="https://ns"> 
    <local/> 
</ns:root> 

```

Lokale Definitionen erfordern keinen Zielnamespace, da die Qualifizierung standardmäßig deaktiviert ist. Wenn Sie jedoch Ihre lokale Definition in global ändern, muss der Verweis mit dem Namespace-Präfix qualifiziert werden. Das folgende Schema ist beispielsweise ungültig.
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema" targetNamespace="https://ns" > 
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

Dieses Schema ist ungültig, da sich "global" im Namespace " " https://ns " befindet. Der einfache ref="global" wird nicht erkannt, da der Standardnamespace nicht " https://ns " ist. Um dieses Problem zu lösen, müssen Sie ein Präfix für den Zielnamespace hinzufügen und es für alle globalen Verweise und Typen verwenden. Das korrigierte Schema sieht folgendermaßen aus.
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
    xmlns:ns="https://ns" targetNamespace="https://ns" > 
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

Dieses Verarbeitsungsanweisungstag gibt die an, dass die Codierung der Datei UTF-8 lautet. Sie müssen sich vergewissern, dass die Dateicodierung der Codierung entspricht, die im Verarbeitungsanweisungstag angegeben ist. Sie können die Codierung ermitteln, indem Sie sich die Bytes der Datei und das Unicode-Byte der Reihenfolgemarken ansehen. Es geht jedoch auch noch einfacher. Wenn Sie Probleme mit dem Öffnen eines XSD-Schemas haben, geben Sie die Codierung als "UTF-8" an, öffnen Sie es in einem Text-Editor (z. B. Notepad) und speichern Sie die Datei dann mit der UTF-8-Codierung ab (Notepad stellt im Dialogfeld **Speichern unter**  die Dropdownliste **Codierung** bereit). Wenn Sie dennoch Probleme mit dem Öffnen der Datei haben, handelt es sich nicht um ein Codierungsproblem. 
  
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

Dieses Beispiel ist ungültig, da das Überprüfungssystem nicht ermitteln kann, ob zwei Vorkommen von Zuordnungen zur einzelnen Deklaration oder zur Deklaration und zu einer anderen  `<x/>` ungültigen Definition auftreten. In einem Tag können nicht zwei Elemente mit demselben Namen enthalten  `<xsd:all>` sein. 
  
Dieses Beispiel ist auch deshalb interessant, weil es ihnen ermöglicht, eine beliebige Anzahl von und Knoten in einem enthaltenden Element  `<x/>`  `<docs/>` in beliebiger Reihenfolge zu haben. Obwohl dieses Konstrukt ungültig ist, gibt es eine Problemumgehung. Indem Sie das **xsd:choice**-Element verwenden, können Sie das gleiche Ergebnis erzielen, wie in folgendem Beispiel dargestellt. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Bearbeiten oder Erstellen eines XSD für InfoPath

Die beiden Beispiel in den folgenden beiden Abschnitten zeigen auf, wie ein Schema bearbeitet oder erstellt werden kann, um in InfoPath bestimmte Ergebnisse zu erzeugen.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Zulassen von Einfügevorgängen benutzerdefinierter Elemente im Aufgabenbereich "Felder"

Damit benutzerdefinierte Elemente unter einem übergeordneten Elemente im Aufgabenbereich **Felder** angezeigt werden, müssen Sie unter dem übergeordneten Element ein **xsd:any**-Element einfügen. Damit benutzerdefinierte Elemente innerhalb eingefügt werden  `<your_node_name>` können, sollte die XSD-Deklaration wie folgt aussehen. 
  
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

Wenn Sie auch benutzerdefinierte Attribute zulassen möchten, müssen Sie der  `<xsd:anyAttribute namespace="##any | ##other"/>` Elementdeklaration hinzufügen. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Zulassen des Bindens von Rich-Text-Elementen in den Entwurfs- und Bearbeitungsmodi in InfoPath

Wenn Sie ein Element deklarieren möchten, das an ein **Rich-Text-Box-Steuerelement** gebunden werden kann, sollte es das folgende Formular haben, das das **xsd:any-Element** enthält, für das ein Namespaceattribut auf " festgelegt ist, wie im folgenden Beispiel https://www.w3.org/1999/xhtml gezeigt. 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a>Zusammenfassung

Durch die Nutzung der InfoPath-Unterstützung zum Entwerden von XML-Formularlösungen, die auf extern verfassten XML Schemadateien (.xsd) basieren, können Sie eine Formularvorlage erstellen, die mit einem Schema gemäß Industriestandard oder einem benutzerdefinierten Schema funktioniert, das von Ihrem Unternehmen erstellt wurde. Mithilfe der Informationen in diesem artikel können Sie benutzerdefinierte XSD-Schemadateien erstellen, die mit InfoPath kompatibel sind und Sie können häufige Probleme behandeln, die beim Laden extern verfasster XS-Dateien in der InfoPath-Entwurfsumgebung auftreten können.
  
## <a name="see-also"></a>Siehe auch

- [W3C-XML-Schema](https://www.w3.org/XML/Schema)
- [W3C XML Schema Primer](https://www.w3.org/TR/xmlschema-0/)
- [Referenz zu W3C-XML-Schemastrukturen](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [Referenz zu W3C-XML-Schemadatentypen](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [XML-Schema-Lernprogramm](https://www.w3schools.com/xml/schema_intro.asp)
- [XML Developer Center](https://msdn.microsoft.com/xml/default.aspx)

