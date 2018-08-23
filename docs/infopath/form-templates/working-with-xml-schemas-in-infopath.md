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
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="3fc49-104">Arbeiten mit XML-Schemas in InfoPath</span><span class="sxs-lookup"><span data-stu-id="3fc49-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="3fc49-105">Eine Formularvorlage, die Sie mit Microsoft InfoPath erstellen verwendet ein XML-Schema (XSD) strukturelle ausführen und die datenüberprüfung auf den XML-Code, die Eingabe des bearbeitet haben, und die Ausgabe von einem InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="3fc49-105">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form.</span></span> <span data-ttu-id="3fc49-106">Jede Formularvorlage in InfoPath-Formular-Designer erstellten enthält mindestens eine XSD-Schemadatei (XSD), die für die Validierung zur Laufzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3fc49-106">Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3fc49-107">Die in diesem Thema enthaltene Informationen gilt für Formularvorlagen für die Verwendung in der InfoPath-Editor.</span><span class="sxs-lookup"><span data-stu-id="3fc49-107">The information contained in this topic applies to form templates designed for use in the InfoPath editor.</span></span> <span data-ttu-id="3fc49-108">Browserkompatible Formularvorlagen weisen strengere XSD-Schemas.</span><span class="sxs-lookup"><span data-stu-id="3fc49-108">Browser-compatible form templates have stricter XSD Schema requirements.</span></span> <span data-ttu-id="3fc49-109">Weitere Informationen finden Sie in der Dokumentation zu XML-Schemas in browserkompatiblen Formularvorlagen verfügbar auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="3fc49-109">For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="3fc49-110">Verwenden extern verfasster XML-Schemas</span><span class="sxs-lookup"><span data-stu-id="3fc49-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="3fc49-111">Befolgen Sie diese Schritte, um eine XSD-Schemadatei zu laden, die außerhalb von InfoPath verfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="3fc49-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="3fc49-112">Erstellen einer Formularvorlage auf Grundlage eines externen Schemas</span><span class="sxs-lookup"><span data-stu-id="3fc49-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="3fc49-113">Klicken Sie in der Backstage-Ansicht auf **neu**, klicken Sie unter **Erweiterte Formularvorlagen**auf **XML oder Schema** , und klicken Sie dann auf **Dieses Formular entwerfen**.</span><span class="sxs-lookup"><span data-stu-id="3fc49-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="3fc49-114">Geben Sie im **Datenquellen-Assistent** die XSD-Schemadatei an, die Sie verwenden möchten und klicken Sie dann auf **Weiter**, um die restlichen Seiten im Assistenten zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="3fc49-115">Nicht unterstützte XSD-Konstrukte</span><span class="sxs-lookup"><span data-stu-id="3fc49-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="3fc49-p104">In folgenden abschnitten werden die XSD-Konstrukte behandelt, die InfoPath zur Laufzeit nicht verarbeiten kann. Vermeiden Sie diese Konstrukte beim Erstellen einer Formularvorlage im InfoPath-Formulardesigner.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p104">The following sections describe XSD constructs that InfoPath cannot handle at run time. Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="3fc49-118">Die Typen ENTITY und ENTITIES</span><span class="sxs-lookup"><span data-stu-id="3fc49-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="3fc49-p105">Bei den Typen **ENTITY** und **ENTITIES** ist für die Validierung eine Dokumenttypdefinition erforderlich, die InfoPath nicht unterstützt. Mit InfoPath können Sie keine Formularvorlage mit solch einem Schema entwerfen, es zeigt dann eine Fehlermeldung an, in der Ihnen empfohlen wird, den **ENTITY**-Typ in **NCName**  zu ändern, aus dem **ENTITY** abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p105">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support. InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="3fc49-121">Wenn Sie eine InfoPath-Formularvorlage außerhalb des Entwurfsmodus verfassen und sie ein XSD verwendet, das die Typen **ENTITY** und **ENTITIES** enthält, funktioniert die Formularvorlage möglicherweise zur Laufzeit, wenn die Template.xml-Datei die erforderliche DTD fü diese Typen enthält.</span><span class="sxs-lookup"><span data-stu-id="3fc49-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="3fc49-122">Erforderliche xsd:beliebiges Element</span><span class="sxs-lookup"><span data-stu-id="3fc49-122">Required xsd:any Element</span></span>

<span data-ttu-id="3fc49-p106">Ein Vorkommen eines **xsd:any**-Platzhalterelements, also ein Vorkommen eines **xsd:any**-Elements mit einem **minOccurs**-Attributwert größer Null ("beliebige erforderlich“) verhindert, dass InfoPath deterministisch eine gültige Instanz für dieses Schemafragment erstellt. InfoPath muss in der Lage sein, beim Generieren eines Formulars eine gültige Instanz zu erstellen, die dieses Schemafragment verwendet. Als Teil der Ausführung des **Datenquellenassistenten** müssen Sie bei Schemas mit erforderlichen **xsd:any**-Elementen auswähle, welches Schemaelement Sie statt des erforderlichen **xsd:any**-Elements verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p106">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment. InfoPath must be able to create a valid instance when generating a form that uses this schema fragment. As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="3fc49-126">Elemente mit einem abstrakten komplexen Typ</span><span class="sxs-lookup"><span data-stu-id="3fc49-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="3fc49-127">InfoPath-Entwurfsmodus unterstützt Entwerfen einer Formularvorlage für Schemas, die abstrakte komplexe Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-127">InfoPath design mode supports designing a form template against schemas that use abstract complex types.</span></span> <span data-ttu-id="3fc49-128">Beispielsweise, wenn ein Element mit dem Namen `shippingAddress` hat einen abstrakten komplexen Typ mit dem Namen `address` , bei dem abgeleiteten Objekte `USAddress` und `CanadianAddress`, InfoPath behandelt jede Instanz von `shippingAddress` als Wahl zwischen `shippingAddress` mit Typ `USAddress` und `shippingAddress` mit `CanadianAddress` .</span><span class="sxs-lookup"><span data-stu-id="3fc49-128">For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` .</span></span> <span data-ttu-id="3fc49-129">In diesem Beispiel wird die bereitgestellten Schemas keine Typen enthalten, die von-Adresse abgeleitet fordert InfoPath ein zusätzliches Schema an, das diese Anforderung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-129">In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="3fc49-130">XSD-Konstrukte mit reduzierter Funktionialität</span><span class="sxs-lookup"><span data-stu-id="3fc49-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="3fc49-131">In den folgenden Abschnitten werden XSD-Konstrukte beschrieben, die beim Verwenden zur Erstellung einer Formularvorlage im InfoPath-Formulardesigner reduzierte Funktionalität besitzen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="3fc49-132">Ersatzgruppen</span><span class="sxs-lookup"><span data-stu-id="3fc49-132">Substitution Groups</span></span>

<span data-ttu-id="3fc49-p108">Alle Elemente der Ersatzgruppen werden im Aufgabenbereich **Felder** angezeigt. InfoPath stellt die Ersatzmöglichkeiten als Auswahl aller Ersatzgruppen bereit (einschließlich des definierenden Elements, wenn es nicht abstrakt ist). Wenn für ein abstraktes Element keine Ersatzgruppen vorhanden sind, fordert Sie InfoPath dazu auf, ein Schema anzugeben, das mindestens ein Element enthält, bei dem es sich um eine Ersatzgruppe handelt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p108">All members of the substitution group appear in the **Fields** task pane. InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract). If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="3fc49-136">Nicht gebundene Auswahlelemente</span><span class="sxs-lookup"><span data-stu-id="3fc49-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="3fc49-137">Das folgende Schemafragment zeigt ein nicht gebundenes Auswahlelement:</span><span class="sxs-lookup"><span data-stu-id="3fc49-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="3fc49-p109">InfoPath zeigt sich wiederholende Auswahlelemente als wiederholte Auswahlen im Aufgabenbereich **Felder** an. Es gibt ein **Wiederholte Auswahlgruppe**-Steuerelement, das Sie zum Darstellen der heterogenen Liste verwenden können, die vom wiederholten Auswahlelement in der XSD definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p109">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane. There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="3fc49-140">Wiederholte Sequenz</span><span class="sxs-lookup"><span data-stu-id="3fc49-140">Repeating Sequence</span></span>

<span data-ttu-id="3fc49-141">Folgendes Schemafragment zeigt eine wiederholte Sequenz:</span><span class="sxs-lookup"><span data-stu-id="3fc49-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="3fc49-142">Solange die wiederholte Sequenz ein erforderliches Element enthält, lädt InfoPath die XSD ohne sie anzupassen. Sie können die Steuerelemente für wiederholte Abschnitte an die wiederholte Sequenz binden</span><span class="sxs-lookup"><span data-stu-id="3fc49-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="3fc49-143">Modellgruppenauswahl</span><span class="sxs-lookup"><span data-stu-id="3fc49-143">Choice of Model Groups</span></span>

<span data-ttu-id="3fc49-144">Folgendes Schemafragement zeigt das Auswahlelement, das mehrere Modellgruppen enthält:</span><span class="sxs-lookup"><span data-stu-id="3fc49-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="3fc49-p110">Der InfoPath-Entwurfsmodus unterstützt diese XSD-Konstrukte, ohne dass eine Anpassung durch den Formulardesigner erforderlich ist. Obwohl InfoPath die Bedeutung des Schemas nicht anpasst, vereinfacht es das Auswahlkonstrukt oben in einer equivalenten reduzierten einzelnen Auswahl im Aufgabenbereich **Felder**.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p110">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer. While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="3fc49-147">Optionales gleichgeordnetes Element mit dem gleichen qualifizierten Namen</span><span class="sxs-lookup"><span data-stu-id="3fc49-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="3fc49-148">Das folgende Schemafragment zeigt einen optionalen gleichgeordneten Knoten mit demselben qualifizierten Namen (`QName`):</span><span class="sxs-lookup"><span data-stu-id="3fc49-148">The following schema fragment shows an optional sibling with same qualified name (`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="3fc49-p111">**XPath**-Ausdrücke für diese Knoten können komplex sein, da jede potenzielle XML-Instanz im InfoPath-Formulardesigner berücksichtigt werden muss. InfoPath macht keine Teile des Schemas verfügbar, bei denen beim Erstellen der korrekten **XPath**-Bindungen Schwierigkeiten auftreten können. Es werden Warnungen zu den Teilen des Schemas angezeigt, die ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p111">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer. InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings. Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="3fc49-152">XSD-Konstrukte in InfoPath mit besonderer Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3fc49-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="3fc49-p112">In den folgenden Abschnitten werden XSD-Konstrukte beschrieben, die beim Erstellen einer Formularvorlage im Entwurfsmodus eine besondere Bedeutung haben. In diesen Abschnitten wird beschrieben, wie Sie die Konstrukte in Ihrem Schema verwenden können, um bestimmte Verhaltensweisen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p112">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode. These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="3fc49-155">Hinzufügen neuer Elementfelder und Gruppen mit dem Aufgabenbereich "Felder"</span><span class="sxs-lookup"><span data-stu-id="3fc49-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="3fc49-p113">Sie können Ihr Schema so erstellen, dass Sie den Aufgabenbereich **Felder** zum Hinzufügen neuer Elementfelder und Gruppen zu einem Element zur Entwurfszeit verwenden können. Deklarieren Sie dazu ein Element in Ihrem Schema mit einem optionalen, nicht gebundenen **xsd:any**-Element, das das Namespace-Attribut mit dem **##any**-Platzhalter angibt. Im Entwurfsmodus können Sie anschließend den Aufgabenbereich **Felder** verwenden, um dem Element neue Elementfelder und Gruppen hinzuzufügen. Sie können beispielsweise folgendem Element neue Inhalte hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="3fc49-p113">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time. To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard. Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element. For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="3fc49-160">Hinzufügen neuer Attributfelder mit dem Aufgabenbereich "Felder"</span><span class="sxs-lookup"><span data-stu-id="3fc49-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="3fc49-p114">Ähnlich wie bei dem Elementfall können Sie ein Attribut mit einem **anyAttribute**-Element deklarieren, bei dem das Namespace-Attribut als **##any**-Platzhalter angegeben ist. Zur Entwurfszeit können Sie den Aufgabenbereich **Felder** verwenden, um dem Schemaattribut neue Inhalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p114">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard. At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="3fc49-163">Speichern von XML-Signaturen in der Datenquelle</span><span class="sxs-lookup"><span data-stu-id="3fc49-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="3fc49-164">Um Benutzern zum digitalen Signieren ein Formulars zur Laufzeit zu ermöglichen, muss das Schema der Datenquelle deklarieren Sie ein Element mit dem Namen Signatur zum Speichern von XML-Signaturen (digitale Signatur) Informationen, die erstellt wird, wenn ein Benutzer das Formular signiert.</span><span class="sxs-lookup"><span data-stu-id="3fc49-164">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form.</span></span> <span data-ttu-id="3fc49-165">Stellen Sie diese Deklaration mit der **Xsd: alle** Element mit dem Namespaceattribut als XML-Signaturen Namespace mit einem Platzhalterzeichen wie folgt angegeben: "http://www.w3c.org/2000/09/xmldsig#"</span><span class="sxs-lookup"><span data-stu-id="3fc49-165">You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "http://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
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

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="3fc49-166">Binden eines Felds an ein Rich-Text-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3fc49-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="3fc49-p116">**Rich-Text-Feld**-Steuerelemente in InfoPath generieren generische XHTML; deshalb muss Ihr Schema angeben, dass eine beliebige Anzahl von Texten und XHTML-Knoten im XML der Formularinstanz gültig ist. Sie können diese Spezifikation mit folgendem XSD-Konstrukt erreichen:</span><span class="sxs-lookup"><span data-stu-id="3fc49-p116">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance. You can achieve this specification with the following XSD construct:</span></span> 
  
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
> <span data-ttu-id="3fc49-p117">InfoPath ändert niemals die Inhalte der Schemadatei (.xsd), folgert daraus jedoch zu Entwurfszwecken möglicherweise logisch eine Teilmenge. Die Schemadatei bleibt in der Formularvorlage zur Entwurfs- und Laufzeit immer unverändert.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p117">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes. The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="3fc49-171">Debuggen häufiger XSD-Fehler</span><span class="sxs-lookup"><span data-stu-id="3fc49-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="3fc49-p118">Wenn Sie extern verfasste XSD-Dateien zum Erstellen von Formularvorlagen im InfoPath-Formulardesigner laden, erhalten Sie möglicherweise eine von zwei Fehlermeldungstypen: MSXML-Fehlermeldungen oder InfoPath-Fehlermeldungen. MSXML-Fehlermeldungen werden im Bereich **Details** eines Dialogfelds einer InfoPath-Fehlermeldung angezeigt, sie beginnen immer mit einem Verweis zu dem Namen oder Pfad der Schemadatei, die den Fehler auslöst. Einige gültige XSD-Schemakonstrukte werden von InfoPath nicht unterstützt; diese werden im Abschnitt "Nicht unterstützte XSD-Konstrukte" behandeltn. In den folgenden Abschnitten werden einige häufige Fehler beschrieben, durch die beim Laden von Schemas in InfoPath ein Fehler erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p118">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages. MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error. Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section. The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="3fc49-176">Die XSD-Namespace-Deklaration</span><span class="sxs-lookup"><span data-stu-id="3fc49-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="3fc49-p119">Ähnlich wie bei allen W3C-Standards, haben XML-Schemas (XSD) ein langwieriges Überprüfungsverfahren durchlaufen, bevor Sie als Empfehlung genannte wurden. Es gab viele Arbeitsentwürfe und folglich wurden viele XSD-Dateien basierend auf diesen entwickelten Standards geschrieben. Während des Verfahrens hat Microsoft eine proprietäre Schemasprache mit der Bezeichnung XML-Data Reduced (XDR) entwickelt, die bei MSXML 3.0 enthalten ist. Ab Version MSXML 4.0 unterstützen die Microsoft XML Core Services das gesamte Empfehlungsspektrum an XSD. Viele Programme zum Erstellen von Schemas warteten nicht darauf, dass das gesamte Empfehlungsspektrum für XSD ausgesprochen wurde. Ältere Versionen dieser Programme erzeugen möglicherweise veraltete XSD-Dateien, das die MSXML 5.0-Infrastruktur nicht unterstützt, von der InfoPath abhängt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p119">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation. There were many working drafts, and consequently, many XSD files were written based on these evolving standards. During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0. Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD. Many programs for creating schemas did not wait for XSD to become a full recommendation. Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="3fc49-183">Um sicherzustellen, dass eine XSD-Datei die volle XSD-Empfehlung unterstützt, sollte in die folgenden XML-Namespacedeklaration enthalten die \<Schema\> Tag:</span><span class="sxs-lookup"><span data-stu-id="3fc49-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="3fc49-p120">Ähnlich wie bei allen XML-Namespacedeklarationen kann das, XML-Präfix (in diesem Fall 'xsd') jede gültige Präfixzeichenfolge sein. Einige Ihnen in der Praxis begegnende Präfixe sind 'xsd', 'xs' und '' (kein Präfix). MSXML meldet in der Regel einen Fehler, dass der Stamm nicht korrekt definiert wird, wenn diese Namespace-Deklaration fehlt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p120">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string. Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix). MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="3fc49-187">Importieren und Aufnehmen von Schemas</span><span class="sxs-lookup"><span data-stu-id="3fc49-187">Importing and Including Schemas</span></span>

<span data-ttu-id="3fc49-p121">XSD-Schemas können erweitert werden und können andere Schemas importieren sowie aufnehmen. Allgemein kann man sagen, Sie sollten ein Schema importieren, wenn das im **targetNamespace**-Attribut angegebene Schema vom aktuellen Schema abweicht. Sie sollten es aufnehmen, wenn das im **targetNamespace**-Attribut angegebene Schema dem aktuellen Schema entspricht.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p121">XSD schemas are extensible and can import and include other schemas. Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema. You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="3fc49-191">Die Semantik zum Importieren und Aufnehmen von Schemas lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3fc49-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="3fc49-p122">Wenn das **schemaLocation**-Attribut fehlt (wie es bei einigen Konvertern vorkommt), löst MSXML einen Fehler aus, da es die Datei nicht finden kann. Wenn Sie diesen Fehler erhalten, stellen Sie außerdem sicher, dass die Ressource oder der Speicherort, der im schemaLocation-Attribut angegeben ist, für Benutzer der Formularvorlage zugänglich ist. Offenbar treten Fehler auf, wenn das **schemaLocation**-Attribut auf einen Server oder ein Verzeichnis verweist, der ausgefallen oder nicht vorhanden ist oder wenn Benutzer darauf keine Zugriffsberechtigungen besitzen. Untersuchen Sie außerdem alle importierten und aufgenommenen Schemas, um sicherzustellen, dass sie gültig sind.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p122">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file. If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template. Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions. Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3fc49-p123">Von Problemen mit dem **schemaLocation**-Attribut verursachte Probleme sind nur ein Problem, wenn InfoPath zunächst die Schemas importiert; also wenn Sie zunächst ein Formular auf Grundlage eines vorhandenen Schemas entwerfen. Anschließend arbeitet InfoPath mit zwischengespeicherten Versionen der Schemadateien, die in der Formularvorlage gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p123">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema. After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="3fc49-p124">Beim Import eines Schemas ist ein Namespace-Attribut zulässig, wenn das Schema kein **targetNamespace**-Attribut angibt. Allgemein lässt sich sagen, dass der Namespace beim Import mit dem im Schema angegebenen **targetNamespace** übereinstimmen muss, das Sie importieren.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p124">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute. In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="3fc49-200">Nicht deterministische Schemas</span><span class="sxs-lookup"><span data-stu-id="3fc49-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="3fc49-p125">Die MSXML 5.0-Infrastruktur, von der InfoPath abhängt, kann zuverlässig Fehler erkennen und auslösen, um Sie zu nicht deterministischen Schemas zu benachrichtigen, die sich daraus ergebende Fehlermeldung stellt jedoch keine Zeilenanzahl bereit, um Ihnen mitzuteilen, welcher Teil des Schemas einen Fehler auslöst. In diesem Abschnitt wird besprochen, warum es bei XSD-Schemadateien wichtig ist, dass sie deterministisch sind und welche Bedeutung es hat, wenn sie nicht deterministisch sind. Außerdem werden einige zu vermeidende Fehler aufgezeigt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p125">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error. This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic. It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="3fc49-p126">XSD-Schemas dienen der Validierung der XML-Datenstruktur und der Typensemantik. Zur Realisierung dieser Aufgabe muss das Validierungssystem (in diesem Fall MSXML 5.0) den XSD-Deklarationen XML-Knoten zuordnen. Ohne diese Zuordnung kann das Validierungssystem diese Aufgabe nicht erfüllen. Wenn eine Zuordnung garantiert werden kann, ist das Schema deterministisch. Wenn es eine einzelne XML-Instanz gibt, durch die diese Zuordnung unmöglich wird, ist das Schema nicht deterministisch.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p126">XSD schemas exist for the purpose of validating XML data structure and type semantics. To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations. Without this mapping, the validating system cannot accomplish its task. If a mapping can be guaranteed, then the schema is deterministic. If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="3fc49-209">Folgendes Beispielschema ist nicht deterministisch:</span><span class="sxs-lookup"><span data-stu-id="3fc49-209">The following example schema is nondeterministic:</span></span>
  
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

<span data-ttu-id="3fc49-210">Um aufzuzeigen, warum dieses XSD-Segment nicht deterministisch ist, nehmen Sie an, Sie hätten folgendes XML-Fragment, das Sie mit diesem Schema validieren möchten:</span><span class="sxs-lookup"><span data-stu-id="3fc49-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="3fc49-211">In diesem XML-Fragment, es ist nicht klar, ob die * \<Dateipfad\> * Element des ersten Teils der auswahldeklaration des Knotens erforderlich oder optional diejenige des zweiten Teils der auswahldeklaration ist.</span><span class="sxs-lookup"><span data-stu-id="3fc49-211">In this XML fragment, it is not clear whether the  *\<file_path\>*  element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration.</span></span> <span data-ttu-id="3fc49-212">Diese Unterscheidung ist aus den folgenden Gründen wichtig:</span><span class="sxs-lookup"><span data-stu-id="3fc49-212">This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="3fc49-213">Wenn das XML-Fragment mit dem ersten Teil der Auswahldeklaration validiert wird, ist die XML mit dem Schema gültig.</span><span class="sxs-lookup"><span data-stu-id="3fc49-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="3fc49-214">Wenn das XML-Fragment anhand des zweiten Teils der auswahldeklaration überprüft wird, ist das Schema nicht gültig, da der erforderliche \<URI\> -Knoten fehlt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="3fc49-p128">Einige XSD-Validierungssysteme validieren mit diesem Schema, da es einen gültigen Pfad gibt. MSXML ist strenger und löst einen Fehler aus, in dem angegeben ist,dass das Schema nicht deterministisch ist.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p128">Some XSD validation systems err toward validating against this schema because there is a valid path. MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="3fc49-p129">Darauf folgenden einige Beispiele von nicht deterministischen Schemas. Das erste behandelt optionale Elemente. Diese Fälle treten oft bei XDR-zu-XSD-Konvertern auf, da Unterschiede in den Standard-Kardinalitäten in den beiden Schemasprachen vorliegen. Der erste zu berücksichtigende Fall sind optional deklarierte Elemente mit **xsd:choice**- und **xsd:sequence**-Elementen. Optionale in einem **xsd:sequence**-Element deklarierte Elemente können in der Regel ordnungsgemäß deklariert werden, so lange Sie Elemente mit dem gleichen Namen nicht mehrmals besitzen, und nur optionale Elemente dazwischen. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3fc49-p129">What follows are a few more examples of nondeterministic schemas. The first deals with optional elements. These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages. The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements. Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between. For example:</span></span> 
  
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

<span data-ttu-id="3fc49-223">Um zu verstehen, warum dieses Schemasegment nicht deterministisch ist, wird davon ausgegangen, dass Sie das folgende ungültige XML-Fragment besitzen:</span><span class="sxs-lookup"><span data-stu-id="3fc49-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="3fc49-224">Dieses Fragment betrachten, Sie können sehen, warum es ungültig ist: Es gibt zwei `<aNode>` Elemente vor dem `<anotherNode>` Element, während nur eines zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3fc49-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="3fc49-225">Gehen wir nun davon aus, Sie müssen folgende XML-Instanz validieren:</span><span class="sxs-lookup"><span data-stu-id="3fc49-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="3fc49-226">Die Herausforderung besteht darin, zu bestimmen, ob diese Instanz gültig ist.</span><span class="sxs-lookup"><span data-stu-id="3fc49-226">The challenge is to determine whether this instance is valid.</span></span> <span data-ttu-id="3fc49-227">Haben Sie zwei `<aNode>` Elemente, in dem nur eines zulässig ist, oder verfügen Sie über, ein `<aNode>` -Element, in dem es zulässig ist, und eine andere Position zulässig?</span><span class="sxs-lookup"><span data-stu-id="3fc49-227">Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed?</span></span> <span data-ttu-id="3fc49-228">Das Schema ist nicht deterministisch, da es nicht möglich ist, kennen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-228">The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="3fc49-p131">Optionale in einem **xsd:choice**-Element deklarierte Elementen sind in der Regel problematisch. Im folgenden vereinfachten Beispiel gibt es keine Möglichkeit zu ermitteln, ob die Auswahl einmal mit dem nicht vorhandenen optionalen Element auftrat, oder es nie auftrat.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p131">Similarly, optional elements declared in an **xsd:choice** element are usually problematic. In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="3fc49-231">Die letzten Verfahren ist die Verwendung einer **Xsd: alle** -Element ohne eine Namespace-Definition, wie in `<xsd:any namespace="##other"/>` , nach einem **xsd: Sequence** -Element.</span><span class="sxs-lookup"><span data-stu-id="3fc49-231">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element.</span></span> <span data-ttu-id="3fc49-232">Dieses Konstrukt ist besonders störend, wenn es sich um ein optionales Element folgt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-232">This construct is especially troublesome when it follows an optional element.</span></span> <span data-ttu-id="3fc49-233">Wenn Sie im vorherige Beispiel Laufe und ändern nur den letzten Knoten, der ein **Xsd: alle** -Element können Sie sehen, dass alle vorherigen Argumente zu Nondeterminism weiterhin anwenden, die wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3fc49-233">If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
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

## <a name="illegal-enumeration-values"></a><span data-ttu-id="3fc49-234">Ungültige Aufzählungswerte</span><span class="sxs-lookup"><span data-stu-id="3fc49-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="3fc49-p133">XSD-Schemas führen in der Regel keine Typenvalidierung durch, bis Sie ein tatsächliches Instanzdokument validieren. Eine Ausnahme davon ist es, wenn Sie eine Aufzählung in Ihrem Schema haben. In diesem Fall validiert das Schema die Aufzählungswerte mit den Aufzählungstypen, um sicherzustellen, dass sie die korrekten Knotenwerte sind. Im Folgenden zwei Beispiele:</span><span class="sxs-lookup"><span data-stu-id="3fc49-p133">XSD schemas typically do not perform any type validation until you validate an actual instance document. An exception to this is when you have an enumeration in your schema. In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values. Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="3fc49-239">Dieses Schema ist ungültig, da "elf Uhr" kein gültiger Wert für ein Element des Typs **xsd:time** ist.</span><span class="sxs-lookup"><span data-stu-id="3fc49-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="3fc49-240">Im Folgenden ein komplexeres Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3fc49-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="3fc49-p134">Um zu verstehen, warum dieses Beispiel ungültig ist, müssen Sie verstehen, wie der Typ **xsd:NMTOKEN** definiert ist. Die W3C-Datentypenspezifikation definiert den **NMTOKEN**-Typ wie folgt: "Ein NMTOKEN (Namenstoken) ist eine beliebige Mischung von Namenszeichen."</span><span class="sxs-lookup"><span data-stu-id="3fc49-p134">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined. The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="3fc49-243">Wenn Sie den Fall weiter untersuchen, werden Sie herausfinden, dass '&' kein gültiges Namenszeichen ist und deshalb kann "M&Ms" nicht als **NMTOKEN**-Typ validiert werden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-243">If you investigate further, you find that '&' is not a valid name character, and therefore "M&Ms" does not validate as an **NMTOKEN** type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="3fc49-244">Leere Sequenz oder Auswahlelemente</span><span class="sxs-lookup"><span data-stu-id="3fc49-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="3fc49-245">MSXML löst in manchen Fällen Fehler zu Schemadeklarationen aus, die leere  **xsd:choice**- oder **xsd:sequence**-Elemente enthalten, siehe folgendes Beispiel.</span><span class="sxs-lookup"><span data-stu-id="3fc49-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="3fc49-246">Entfernen des leeren `<xsd:choice />` Tag sollte dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3fc49-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="3fc49-247">Reguläre Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="3fc49-247">Regular Expressions</span></span>

<span data-ttu-id="3fc49-248">MSXML 5.0 möglich Problemen mit der Überprüfung der regulären Ausdrucksmuster beim Laden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-248">MSXML 5.0 can have problems validating regular expression patterns on load.</span></span> <span data-ttu-id="3fc49-249">Reguläre Ausdrücke können kompliziert sein, und Sie vorsichtig, wenn Sie solche verwenden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-249">Regular expressions can be complicated, and you should be careful when you are using them.</span></span> <span data-ttu-id="3fc49-250">Alle XSD-Parser scheint flexible regulären Ausdruck Sprachen haben; d. h., implementieren sie die offizielle XSD-regulären Sprache plus Elemente aus anderen Sprachen für reguläre Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="3fc49-250">Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages.</span></span> <span data-ttu-id="3fc49-251">Wenn InfoPath-Formular-Designer Probleme Analysieren eines regulären Ausdrucks aufweist, klicken Sie dann InfoPath generiert Beispieldaten möglicherweise ungültig oder überhaupt nicht generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="3fc49-251">If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all.</span></span> <span data-ttu-id="3fc49-252">Dies ist zur Entwurfszeit zulässig, da InfoPath nur Beispieldaten für die Formatierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3fc49-252">This is acceptable at design time, because InfoPath uses only sample data for formatting.</span></span> <span data-ttu-id="3fc49-253">Jedoch, wenn Sie einen regulären Ausdruck, den MSXML nicht unterstützt verwenden, kann nicht klicken Sie dann InfoPath überprüfen einen Wert dafür, wenn ein Benutzer ein Formular ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-253">However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form.</span></span> <span data-ttu-id="3fc49-254">[XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)wird beschrieben, was in regulären Ausdrücken XSD-unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3fc49-254">[XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions.</span></span> <span data-ttu-id="3fc49-255">Weitere Informationen zu regulären XSD-Ausdrücken und Unicode-Ebene 1 reguläre Ausdrücke finden Sie unter [Reguläre Ausdrücke Unicode](http://www.unicode.org/reports/tr18/) .</span><span class="sxs-lookup"><span data-stu-id="3fc49-255">For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](http://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="3fc49-256">targetNamespace-Attribut-Probleme</span><span class="sxs-lookup"><span data-stu-id="3fc49-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="3fc49-257">XSD ist insofern, dass standardmäßig das **TargetNamespace** -Attribut auf nur Deklarationen der obersten Ebene, verweist zwar Sie festlegen können, `attributeFormDefault=qualified` und `elementFormDefault=qualified` dieses Standardverhalten außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-257">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior.</span></span> <span data-ttu-id="3fc49-258">Als Beispiel wird davon ausgegangen Sie, dass Sie die folgenden XSD verfügen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-258">As an example, assume that you have the following XSD.</span></span> 
  
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

<span data-ttu-id="3fc49-259">Ihr XML-Instanzdokument ähnelt folgendem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="3fc49-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="3fc49-p137">Lokale Definitionen erfordern keinen Zielnamespace, da die Qualifizierung standardmäßig deaktiviert ist. Wenn Sie jedoch Ihre lokale Definition in global ändern, muss der Verweis mit dem Namespace-Präfix qualifiziert werden. Das folgende Schema ist beispielsweise ungültig.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p137">Local definitions do not require the target namespace because qualification is turned off by default. However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix. For example, the following schema is invalid.</span></span>
  
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

<span data-ttu-id="3fc49-263">Mit diesem Schema ist ungültig, da im Namespace "global" ist "http://ns".</span><span class="sxs-lookup"><span data-stu-id="3fc49-263">This schema is invalid because "global" is in the namespace "http://ns".</span></span> <span data-ttu-id="3fc49-264">Das einfache Ref = "global" wird nicht erkannt, da kein Standardnamespace ist "http://ns".</span><span class="sxs-lookup"><span data-stu-id="3fc49-264">The simple ref="global" is not recognized because the default namespace is not "http://ns".</span></span> <span data-ttu-id="3fc49-265">Um dieses Problem zu beheben, müssen Sie ein Präfix für den Zielnamespace hinzufügen und verwenden, die für alle globalen Verweise und-Typ verwendet.</span><span class="sxs-lookup"><span data-stu-id="3fc49-265">To fix this, you must add a prefix for the target namespace and use that for all global references and type uses.</span></span> <span data-ttu-id="3fc49-266">Das korrigierte Schema sieht folgendermaßen aus.</span><span class="sxs-lookup"><span data-stu-id="3fc49-266">The corrected schema looks like the following.</span></span>
  
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

<span data-ttu-id="3fc49-267">Wenn bei Ihrem Schema das **targetNamespace**-Attribut angegeben ist, vergewissern Sie sich, dass alle globalen Verweise mit dem korrekten Namespace-Präfix qualifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="3fc49-268">XML-Verarbeitungsanweisungscodierung (Unicode vs. ANSII)</span><span class="sxs-lookup"><span data-stu-id="3fc49-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="3fc49-p139">XML unterstützt nur Unicode-Zeichensätze. Deshalb gehen Ihnen möglicherweise Informationen verloren, wenn Sie Dateien speichern, die ANSII-Zeichen verwenden. Das Speichern von Dateien als UTF-16 ist möglicherweise jedoch unverhältnismäßig für Ihre Zwecke. Um die Implementierungskosten eines XML-Readers zu verringern, muss der XML-Autor angeben, welche Codierung er in der XML-Verarbeitungsanweisung auf oberster Ebene verwenden möchte. Dabei nehmen Sie möglicherweise von folgende Verarbeitungsanweisung Notiz.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p139">XML supports only Unicode character sets. Therefore, you may lose information if you save files that use ANSII characters. However, saving files as UTF-16 may be excessive for your particular use. To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction. You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="3fc49-p140">Dieses Verarbeitsungsanweisungstag gibt die an, dass die Codierung der Datei UTF-8 lautet. Sie müssen sich vergewissern, dass die Dateicodierung der Codierung entspricht, die im Verarbeitungsanweisungstag angegeben ist. Sie können die Codierung ermitteln, indem Sie sich die Bytes der Datei und das Unicode-Byte der Reihenfolgemarken ansehen. Es geht jedoch auch noch einfacher. Wenn Sie Probleme mit dem Öffnen eines XSD-Schemas haben, geben Sie die Codierung als "UTF-8" an, öffnen Sie es in einem Text-Editor (z. B. Notepad) und speichern Sie die Datei dann mit der UTF-8-Codierung ab (Notepad stellt im Dialogfeld**Speichern unter**  die Dropdownliste **Codierung** bereit). Wenn Sie dennoch Probleme mit dem Öffnen der Datei haben, handelt es sich nicht um ein Codierungsproblem.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p140">This processing instruction tag specifies that the encoding of the file is UTF-8. You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag. You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks. But there is an easier way. If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box). If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="3fc49-280">maxOccurs-Attribut im xsd:all-Element</span><span class="sxs-lookup"><span data-stu-id="3fc49-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="3fc49-p141">Aufgrund der Art und Weise wie nicht deterministisch in der XML-Schemaempfehlung definiert ist, lautet der einzige gültige Wert für das **maxOccurs**-Attribut eines **xsd:element**-Elements in einem **xsd:all**-Element 1. Der folgende Wert ist beispielsweise gültig.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p141">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1. For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="3fc49-283">Dieses Beispiel ist jedoch ungültig.</span><span class="sxs-lookup"><span data-stu-id="3fc49-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="3fc49-284">In diesem Beispiel ist ungültig, da das Validierung System bestimmen, ob zwei kann nicht Vorkommen des `<x/>` Zuordnung der einzelnen Deklaration oder die Deklaration und einem anderen ungültige Definition.</span><span class="sxs-lookup"><span data-stu-id="3fc49-284">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition.</span></span> <span data-ttu-id="3fc49-285">Entlang der gleichen Linien kann Ihnen nicht zwei Elemente mit demselben Namen in einer `<xsd:all>` Tag.</span><span class="sxs-lookup"><span data-stu-id="3fc49-285">Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="3fc49-286">In diesem Beispiel ist auch interessant, weil es Ihnen ermöglicht, eine beliebige Anzahl von `<x/>` und `<docs/>` Knoten innerhalb eines enthaltenden Elements in beliebiger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3fc49-286">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order.</span></span> <span data-ttu-id="3fc49-287">Obwohl dieses Konstrukt ungültig ist, kann ein umgangen werden.</span><span class="sxs-lookup"><span data-stu-id="3fc49-287">Although this construct is invalid, there is a workaround.</span></span> <span data-ttu-id="3fc49-288">Mit dem **xsd: choice** -Element, erzielen Sie dasselbe Ergebnis wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-288">By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="3fc49-289">Bearbeiten oder Erstellen eines XSD für InfoPath</span><span class="sxs-lookup"><span data-stu-id="3fc49-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="3fc49-290">Die beiden Beispiel in den folgenden beiden Abschnitten zeigen auf, wie ein Schema bearbeitet oder erstellt werden kann, um in InfoPath bestimmte Ergebnisse zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="3fc49-291">Zulassen von Einfügevorgängen benutzerdefinierter Elemente im Aufgabenbereich "Felder"</span><span class="sxs-lookup"><span data-stu-id="3fc49-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="3fc49-292">Damit benutzerdefinierte Elemente unter einem übergeordneten Element im Aufgabenbereich **Felder** angezeigt werden können, müssen Sie das Einfügen eines **Xsd: alle** Element unterhalb des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="3fc49-292">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element.</span></span> <span data-ttu-id="3fc49-293">Um benutzerdefinierte Elemente in eingefügt werden können `<your_node_name>` , die XSD-Deklaration sollte etwa folgendermaßen aussehen.</span><span class="sxs-lookup"><span data-stu-id="3fc49-293">To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
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

<span data-ttu-id="3fc49-294">Wenn Sie auch benutzerdefinierte Attribute zulassen möchten, müssen Sie hinzufügen `<xsd:anyAttribute namespace="##any | ##other"/>` Sie der Elementdeklaration.</span><span class="sxs-lookup"><span data-stu-id="3fc49-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="3fc49-295">Zulassen des Bindens von Rich-Text-Elementen in den Entwurfs- und Bearbeitungsmodi in InfoPath</span><span class="sxs-lookup"><span data-stu-id="3fc49-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="3fc49-296">Wenn Sie möchten, deklarieren ein Element, das an ein **Feld für Rich-Text** -Steuerelement gebunden werden können, es sollte folgende Form auf, einschließlich der **Xsd: alle** Element, das ein Namespace-Attribut auf festgelegt hat "http://www.w3.org/1999/xhtml" wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3fc49-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "http://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
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

## <a name="conclusion"></a><span data-ttu-id="3fc49-297">Schlussbemerkung</span><span class="sxs-lookup"><span data-stu-id="3fc49-297">Conclusion</span></span>

<span data-ttu-id="3fc49-p145">Durch die Nutzung der InfoPath-Unterstützung zum Entwerden von XML-Formularlösungen, die auf extern verfassten XML Schemadateien (.xsd) basieren, können Sie eine Formularvorlage erstellen, die mit einem Schema gemäß Industriestandard oder einem benutzerdefinierten Schema funktioniert, das von Ihrem Unternehmen erstellt wurde. Mithilfe der Informationen in diesem artikel können Sie benutzerdefinierte XSD-Schemadateien erstellen, die mit InfoPath kompatibel sind und Sie können häufige Probleme behandeln, die beim Laden extern verfasster XS-Dateien in der InfoPath-Entwurfsumgebung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="3fc49-p145">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization. By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3fc49-300">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fc49-300">See also</span></span>

- [<span data-ttu-id="3fc49-301">W3C-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="3fc49-301">W3C XML Schema</span></span>](http://www.w3.org/XML/Schema)
- [<span data-ttu-id="3fc49-302">Einführung in W3C XML-Schema</span><span class="sxs-lookup"><span data-stu-id="3fc49-302">W3C XML Schema Primer</span></span>](http://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="3fc49-303">W3C XML-Schemareferenz Strukturen</span><span class="sxs-lookup"><span data-stu-id="3fc49-303">W3C XML Schema Structures Reference</span></span>](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [<span data-ttu-id="3fc49-304">W3C XML-Schemareferenz für Datentypen</span><span class="sxs-lookup"><span data-stu-id="3fc49-304">W3C XML Schema Datatypes Reference</span></span>](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [<span data-ttu-id="3fc49-305">XML-Schema-Lernprogramm</span><span class="sxs-lookup"><span data-stu-id="3fc49-305">XML Schema Tutorial</span></span>](https://www.w3schools.com/xml/schema_intro.asp)
- [<span data-ttu-id="3fc49-306">XML Developer Center</span><span class="sxs-lookup"><span data-stu-id="3fc49-306">XML Developer Center</span></span>](http://msdn.microsoft.com/en-us/xml/default.aspx)

