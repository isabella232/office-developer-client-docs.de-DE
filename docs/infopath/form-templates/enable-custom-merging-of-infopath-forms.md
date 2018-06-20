---
title: Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: Das Feature Formulare zusammenführen von Microsoft InfoPath-Editor ist darauf ausgelegt, um die Daten aus mehreren Formularen in ein einziges Formular zu kombinieren.
ms.openlocfilehash: e0e6bfc074829f262d7eef3cf7bf6a86c3b2253b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790728"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen

Das Feature **Formulare zusammenführen** von Microsoft InfoPath-Editor ist darauf ausgelegt, um die Daten aus mehreren Formularen in ein einziges Formular zu kombinieren. Dies ist auch bekannt als Datenaggregation. Zusammenführen von Formularen aktiviert ist, können Sie klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Speichern &amp; senden**, klicken Sie auf **Das Zusammenführen von Formularen** unter **Import &amp; Link**, und klicken Sie dann auf die Schaltfläche **Formulare zusammenführen** eines oder mehrere Formulare zum Zusammenführen auswählen die zurzeit geöffnete Formular. Das Formular, das zurzeit geöffnet ist ist das Ziel und die Formulare im Dialogfeld **Formulare zusammenführen** ausgewählt werden als die Quellformulare bezeichnet.
  
Die Aggregation der Daten, die sich aus dem Zusammenführen von Formularen ergibt, kann alle Daten in den Quell- und Zielformularen oder nur einen Teil der Originaldaten einschließen. Nachstehend werden die Standardvorgänge beschrieben.
  
- Für sich wiederholende Elemente werden Daten an einer passenden Stelle im Zieldokument eingefügt. Dies geschieht, wenn das **MaxOccurs** -Attribut des Zielelements größer als 1 ist. 
    
- Bei nicht wiederholten Elementen (d. h., für Elemente, bei denen **MaxOccurs** "1"), werden die Attribute der Quellelemente den vorhandenen Attributen des Zielelements hinzugefügt. 
    
## <a name="creating-a-custom-transform"></a>Erstellen einer benutzerdefinierten Transformation

Der Standardvorgang beim Zusammenführen von Formularen eignet sich gut für Formulare, die auf das gleiche XML-Schema basieren. In einigen Fällen jedoch sollten Sie Formulare, die auf verschiedenen Schemas basieren zusammengeführt oder durch Überschreiben der standardmäßigen Zusammenführungsvorgang für Formulare, die auf das gleiche Schema basieren. Für diese Szenarien können Sie eine XSL-Transformation (XSLT), erstellen, die Aggregation von Anweisungen für den Zusammenführungsvorgang enthält. Die Transformation Merge Zeitpunkt zum Erstellen eines DOM-Dokuments mit den Informationen, die zusammen mit Anmerkungen angeben, wie diese Informationen in das Zieldokument integrieren importiert werden. Diese Anmerkungen sind XML-Attribute im Namespace `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.
  
Die XML-Attribute und die entsprechenden Werte dienen als Aggregationsanweisungen für die Zusammenführung der einzelnen Knoten mit dem XML-Zieldokument. Diese Attribute werden in den folgenden Abschnitten beschrieben.
  
### <a name="select"></a>select

Das **agg: Select** -Attribut enthält einen absoluten XPath-Ausdruck, der das Zielelement identifiziert wird. 
  
### <a name="insert"></a>insert

Der Wert "Einfügen" für das **agg: Action** -Attribut weist InfoPath Quellelements als untergeordnetes Element des Zielelements einfügen, die mit dem **agg: Select** -Attribut angegeben ist. Die untergeordneten Elemente des Quellelements sind in der Einfügevorgang enthalten. Das Attribut **SelectChild** können Sie eine bestimmte Position für den Knoteneinfügevorgang auswählen. Das **Reihenfolge** -Attribut wird verwendet, um anzugeben, ob die Quellelemente vor einer vorhandenen eingefügt werden Ziel Elemente oder nachdem. Der Standardwert ist das **Reihenfolge** -Attribut nicht vorhanden ist, ist "nach". 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

Der Wert "ersetzen" für das **agg: Action** -Attribut weist InfoPath aller Zielelemente durch das Attribut **Wählen** mit Quellelements ersetzen. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

Wenn der Wert des **agg: Action** -Attributs "MergeAttributes" ist, werden die Attribute des Quellelements mit den Attributen aller Zielelemente, auf die durch das Attribut **auswählen** zusammengeführt. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>Löschen

Wenn der Wert des **agg: Action** -Attributs ist "löschen", aller Zielelemente, auf die durch das Attribut **auswählen** werden gelöscht aus dem Zieldokument. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

In Verbindung mit den Attributen angegeben, der `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` -Namespace, verwenden Sie die `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` Namespace zu versehen sind, wird ein XSL-Objekt, das die **IXMLDOMDocument**-Schnittstelle implementiert. Eine der nützlichsten Elemente dieser Schnittstelle ist die Methode **Get-DocumentElement**.
  
### <a name="get-documentelement"></a>get-documentElement

Die **Ziel: Get-DocumentElement** Funktion ermöglicht den Zugriff auf das Dokumentobjektmodell des Zieldokuments. Sie können zum Ändern der Funktionsweise der Zusammenführungsvorgang basierend auf den aktuellen Inhalt des Zieldokuments verwendet werden. 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>Schritte zum Erstellen einer benutzerdefinierten Zusammenführung

1. Wählen Sie die Typen der XML-Quelldokumente aus, aus denen Sie Daten zusammenführen möchten. Sammeln Sie repräsentative Beispiele für die einzelnen Quelldokumenttypen.
    
2. Leiten Sie das XML-Schema für jede Art von XML-Quelldokument für ein vorhandenes InfoPath-Formular. Dieser Schritt erfolgt auf einfache Weise durch Exportieren von XML-Schema mit dem Befehl **Quelldateien exportieren** auf der Registerkarte **Veröffentlichen** die Backstage-Ansicht. Für XML-Dokumente, die nicht in InfoPath erstellt wurden, können einem Tool wie Microsoft Visual Studio zum Erstellen eines Schemas aus dem Beispiel-XML-Dokument oder Sie können das Erstellen eines Beispielformulars aus dem XML-Dokument in InfoPath und exportieren Sie das Schema, das InfoPath von t abgeleitet ist. er Dokumentstruktur. 
    
3. Identifizieren Sie die Daten, die Sie über jede Art von XML-Quelldokument zusammenführen möchten. Dieser Schritt ist nahezu vollständig die Anforderungen der Quelle und des Ziels Formulare abhängig. Für manche Formulare können Sie alle Daten aus dem Quellformular kopieren möchten. Für andere Benutzer sollten Sie nur ein oder zwei Elemente aus dem Formular zugrunde liegenden XML-Dokument. Beim Festlegen, welche Daten, die Sie zusammenführen möchten, achten Sie zusätzliche auf sowohl die Quell-als auch Dokumente, um sicherzustellen, dass die Elemente logisch zwischen den beiden Formularen zugeordnet.
    
4. Erstellen Sie eine XSL-Transformation für jede Art von XML-Quelldokument. Wenn das Zusammenführen von Formularen konfigurieren, wird dieser Schritt die meiste Zeit dauern. Der Zweck der XSL-Transformation ist das Quell-XML-Dokument in ein Format umgewandelt, die mit dem Zielformular zusammengeführt werden können. Beim Entwerfen Ihrer Transform entscheiden Sie, ob Sie Zusammenführen von XML-Speicherortpfade oder Zusammenführen von InfoPath Aggregation Anweisungen verwenden möchten.
    
    Visual Studio ist ein praktisches Tool zum Erstellen von XSL-Transformationen. Visual Studio bietet Syntax Codefarben und ein Dokument Gliederung an. Es bietet auch automatisch schließenden Tags für XSL-Elemente, die Abnahme redundante Eingaben und schwer zu suchenden Rechtschreibfehler helfen können. Sie können auch die XSL-Transformationen mit einem Text-Editor wie Editor erstellen.
    
    Beginnen Sie mit der Identitätstransformation, bei dem es sich einfach eine XSL-Transformation handelt, die die gleiche XML-Datei ausgibt, die eingegeben wird:
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="http://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="http://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    Fügen Sie überschreibende Bereiche der Dokumentvorlage für die Elemente, denen Sie besondere Behandlung für den hinzufügen möchten. Diese Vorlage beispielsweise ändert ein `<src:Task>` Element in einer `<my:field1>` -Element, und legt der Wert des **agg: Action** -Attribut, um "ersetzen". 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Fügen Sie die XSL-Transformationsdateien und Schemadateien in der Formularvorlage ein. Nach-Schemas für jede Art von Quelldokument abgeleitet und erstellt eine XSL-Transformation zum Konvertieren jedes Dokumenttyps, damit die Daten von InfoPath zusammengeführt werden kann, fügen sie auf dem Formular als Ressourcen hinzu. Klicken Sie auf der Registerkarte **Daten** auf **Ressourcendateien** und klicken Sie dann auf **Hinzufügen** , klicken Sie im Dialogfeld **Ressourcendateien** , wechseln Sie zu Ihrem Schema oder XSL-Transformation-Datei, und klicken Sie dann auf **OK**. Führen Sie diese Option, um für jede Schemadatei und XSL-Transformation-Datei, die Sie erstellt haben.
    
    Wenn die Schemas, die Sie hinzufügen das **TargetNamespace** -Attribut verwenden, müssen Sie ein Property-Element für das Formular XSF-Datei hinzufügen, sodass InfoPath den Namespace des Schemas kennt. Zugriff auf diese Datei, klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Veröffentlichen**, und klicken Sie dann auf **Quelldateien exportieren**. Wählen Sie einen Speicherort für die Dateien, und klicken Sie dann auf **OK**. Schließen Sie dann die InfoPath-Formularvorlage, die Sie entwerfen.
    
    Navigieren Sie zum Speicherort, den Sie für die extrahierten Dateien angegeben, und suchen Sie die Datei, die Erweiterung XSF-Datei hat. Normalerweise wird diese Datei manifest.xsf bezeichnet. Beim Suchen der Datei in Editor öffnen der `<xsf:file>` -Tag, das Ihrem Schema entspricht, und fügen eine "Namespace" Property-Element zum **TargetNamespace** angeben, wie im folgenden Beispiel dargestellt. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. Vorbereiten des Formulars zur Unterstützung von benutzerdefinierten Zusammenführung der letzte Schritt besteht darin, **ImportParameters** -Element in der XSF-Datei, die dem Formular zugeordneten aktualisieren. 

    Suchen Sie zunächst die `<xsf:importParameters>` Tag in der XSF-Datei. Für jedes Schema-XSL-Transformationspaar Sie für Ihr Formular erstellt haben, fügen Sie **-Element ein** **importSource** -Element: `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`. 
    
    **Name** -Attributs **der-Element** enthält die Namen der Formularvorlage, die in einem XML-Quelldokument gefunden werden kann. In der Regel können Sie dies leer lassen. Das **Schema** -Attribut enthält den Namen einer Schemadatei, die Sie die Formularvorlage im vorherigen Schritt hinzugefügt haben. Schließlich enthält das **transform** -Attribut den Namen der XSL-Transformation, die Sie zum Konvertieren von Formularen, die entsprechen dem Schema verwenden möchten. 
    
    Sie können entweder mit dem [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis oder auf einem eigenen eine benutzerdefinierte Transformation verwenden. 
    
## <a name="creating-a-custom-merge-in-code"></a>Erstellen einer benutzerdefinierten Zusammenführung in Code

Benutzerdefinierte Zusammenführung mit Code wird mithilfe des ereignishandlers [Zusammenführen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) mit seinem entsprechenden **UseScriptHandler** -Attribut des **ImportParameters** -Elements in der XSF-Datei, die dem Formular zugeordneten unterstützt. 

In verwaltetem Code können Sie das [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis aktivieren, indem das Kontrollkästchen **Mithilfe benutzerdefiniertem Code Zusammenführen**, und dann auf die Schaltfläche **Bearbeiten** in der Kategorie **Erweitert** im Dialogfeld **Formularoptionen** aus der Backstage-Ansicht zur Verfügung. 
  

