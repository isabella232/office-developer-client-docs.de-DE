---
title: Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: Das Feature Formulare zusammenführen des Microsoft InfoPath-Editors dient zum Kombinieren der Daten aus mehreren Formularen in einem einzigen Formular.
ms.openlocfilehash: 59a1f8a07252c9ae21e165c1377e69122a3953f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580580"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen

Das Feature **Formulare** zusammenführen des Microsoft InfoPath-Editors dient zum Kombinieren der Daten aus mehreren Formularen in einem einzigen Formular. Dieser Vorgang wird auch als Datenaggregation bezeichnet. Wenn das Zusammenführen von Formularen aktiviert ist, können Sie auf die Registerkarte **"Datei"** klicken, auf **&amp; "Senden speichern"** und dann auf **"Formulare zusammenführen"** unter **&amp; "Importlink"** klicken und dann auf die Schaltfläche **"Formulare zusammenführen"** klicken, um ein oder mehrere Formulare auszuwählen, die mit dem aktuell geöffneten Formular zusammengeführt werden sollen. Das formular, das derzeit geöffnet ist, ist das Zielformular, und die im Dialogfeld **Formulare zusammenführen** ausgewählten Formulare werden als Quellformulare bezeichnet.
  
Die Aggregation der Daten, die sich aus dem Zusammenführen von Formularen ergibt, kann alle Daten in den Quell- und Zielformularen oder nur einen Teil der Originaldaten einschließen. Nachstehend werden die Standardvorgänge beschrieben.
  
- Bei wiederholten Elementen werden die Daten an einer entsprechenden Position im Zieldokument eingefügt. Dies geschieht, wenn das **MaxOccurs**-Attribut des Zielelements größer als 1 ist. 
    
- Bei nicht wiederholten Elementen (das heißt bei Elementen, bei denen **MaxOccurs** gleich "1" ist), werden die Attribute der Quellelemente den vorhandenen Attributen des Zielelements hinzugefügt. 
    
## <a name="creating-a-custom-transform"></a>Erstellen einer benutzerdefinierten Transformation

Der Standardvorgang beim Zusammenführen von Formularen eignet sich gut für Formulare, die auf dem gleichen XML-Schema basieren. In manchen Fällen möchten Sie jedoch möglicherweise Formulare zusammenführen, die auf anderen Schemas basieren oder den Standardzusammenführungsvorgang für auf dem gleichen Schema basierende Formulare außer Kraft setzen. Für diese Szenarien können Sie eine XSL-Transformation (XSLT) erstellen, die Aggregationsanweisungen für den Zusammenführungsvorgang enthält. Die Transformation wird bei der Zusammenführung angewendet, um ein DOM-Dokument zu erstellen, das die zu importierenden Informationen enthält sowie Anmerkungen, in denen angegeben wird, wie diese Informationen in das Zieldokument integriert werden sollen. Diese Anmerkungen sind XML-Attribute im  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` Namespace.
  
Die XML-Attribute und die entsprechenden Werte dienen als Aggregationsanweisungen für die Zusammenführung der einzelnen Knoten mit dem XML-Zieldokument. Diese Attribute werden in den folgenden Abschnitten beschrieben.
  
### <a name="select"></a>select

Das **agg:select**-Attribut enthält einen absoluten XPath-Ausdruck, durch den das Zielelement identifiziert wird. 
  
### <a name="insert"></a>insert

Der Wert "insert" für das **agg:action-Attribut** weist InfoPath an, das Quellelement als untergeordnetes Element des Zielelements einzufügen, das mithilfe des **Attributs agg:select** angegeben wird. Die untergeordneten Elemente des Quellelements sind im Einfügevorgang enthalten. Mit dem **selectChild-Attribut** können Sie einen bestimmten Speicherort für den Vorgang "Knoten einfügen" auswählen. Das **Order-Attribut** wird verwendet, um anzugeben, ob die Quellelemente vor vorhandenen Zielelementen oder danach eingefügt werden. Der Standardwert, wenn das **Order-Attribut** nicht vorhanden ist, lautet "after". 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

Der Wert "replace" für das **Attribut agg:action** weist InfoPath an, jedes der Zielelemente zu ersetzen, auf die durch das **Select-Attribut** durch das Quellelement verwiesen wird. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

Wenn der Wert des **agg:action-Attributs** "mergeAttributes" lautet, werden die Attribute des Quellelements mit den Attributen der einzelnen Zielelemente zusammengeführt, auf die vom **Select-Attribut** verwiesen wird. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>Löschen

Wenn der Wert des **agg:action-Attributs** "delete" lautet, werden alle Zielelemente, auf die durch das **Select-Attribut** verwiesen wird, aus dem Zieldokument gelöscht. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

In Verbindung mit den im Namespace angegebenen Attributen  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` verwenden Sie den  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` Namespace, um ein XSL-Objekt zu kennzeichnen, das die Schnittstelle **IXMLDOMDocument** implementiert. Eines der nützlichsten Member dieser Schnittstelle ist die **get-documentElement**-Methode.
  
### <a name="get-documentelement"></a>get-documentElement

Die **target:get-documentElement**-Funktion ermöglicht den Zugriff auf das DOM (Document Object Model) des Zieldokuments. Damit kann die Funktionsweise des Zusammenführungsvorgangs basierend auf dem aktuellen Inhalt des Zieldokuments geändert werden.   
 
 
  
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
    
2. Leiten Sie das XML-Schema für jede Art von XML-Quelldokument für ein vorhandenes InfoPath-Formular ab. Dieser Schritt lässt sich ganz einfach durch Exportieren des XML-Schemas mit dem Befehl **"Quelldateien exportieren"** auf der Registerkarte **"Veröffentlichen"** in Backstage ausführen. Für XML-Dokumente, die nicht in InfoPath erstellt wurden, können Sie ein Tool wie Microsoft Visual Studio verwenden, um ein Schema aus dem XML-Beispieldokument zu erstellen, oder Sie können ein Beispielformular aus dem XML-Dokument in InfoPath erstellen und dann das Schema exportieren, das InfoPath von der Dokumentstruktur abgeleitet hat. 
    
3. Identifizieren Sie die Daten, die Sie aus den einzelnen XML-Quelldokumenttypen zusammenführen möchten. Dieser Schritt hängt fast vollständig von den Anforderungen der Quell- und Zielformulare ab. Bei manchen Formularen möchten Sie möglicherweise alle Daten aus dem Quellformular kopieren. Bei anderen benötigen Sie möglicherweise nur ein oder zwei Elemente aus dem dem Formular zugrunde liegenden XML-Dokument. Achten Sie beim Identifizieren der zusammenzuführenden Daten besonders auf die Quell- und Zieldokumente, um sicherzustellen, dass die Elemente zwischen den beiden Formularen logisch zugeordnet sind.
    
4. Erstellen Sie für jeden XML-Quelldokumenttyp eine XSL-Transformation. Dieser Schritt beansprucht beim Konfigurieren der Zusammenführung von Formularen die meiste Zeit. Der Zweck der XSL-Transformation besteht darin, das XML-Quelldokument in ein Format zu transformieren, das mit dem Zielformular zusammengeführt werden kann. Entscheiden Sie beim Entwerfen der Transformation, ob Sie die Zusammenführung aus XML-Speicherortpfaden oder die Zusammenführung aus InfoPath-Aggregationsanweisungen verwenden möchten.
    
    Visual Studio ist ein praktisches Tool zum Erstellen von XSL-Transformationen. Visual Studio bietet Eine Syntaxfarbe und eine Dokumentgliederung. Außerdem werden automatisch schließende Tags für die XSL-Elemente bereitgestellt, sodass Sie redundante Eingaben und schwer zu findende Rechtschreibfehler vermeiden können. Sie können XSL-Transformationen auch mit einem Text-Editor wie beispielsweise Editor erstellen.
    
    Beginnen Sie mit der Identitätstransformation, bei der es sich einfach um eine XSL-Transformation handelt, mit der die eingegebene XML-Datei ausgegeben wird:
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
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

    Fügen Sie dann überschreibende Vorlagenabschnitte für die Elemente hinzu, für die Sie eine spezielle Behandlung hinzufügen möchten. Diese Vorlage ändert beispielsweise ein  `<src:Task>` Element in ein Element und legt den Wert des  `<my:field1>` **Attributs agg:action** auf "replace" fest. 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Fügen Sie die XSL-Transformationsdateien und Schemadateien in der Formularvorlage hinzu. Nachdem Sie Schemas für jede Art von Quelldokument abgeleitet und eine XSL-Transformation erstellt haben, um jeden Dokumenttyp zu konvertieren, damit InfoPath seine Daten zusammenführen kann, fügen Sie sie dem Formular als Ressourcen hinzu. Klicken Sie auf der Registerkarte **"Daten"** auf **"Ressourcendateien",** und klicken Sie dann im Dialogfeld **"Ressourcendateien"** auf **"Hinzufügen",** navigieren Sie zu Ihrer Schema- oder XSL-Transformationsdatei, und klicken Sie dann auf **"OK".** Führen Sie dies für jede Schemadatei und XSL-Transformationsdatei aus, die Sie erstellt haben.
    
    Wenn die hinzugefügten Schemas das **TargetNamespace-Attribut** verwenden, müssen Sie der XSF-Datei des Formulars ein Eigenschaftselement hinzufügen, damit InfoPath den Namespace des Schemas kennt. Zum Zugreifen auf diese Datei klicken Sie auf die Registerkarte **Datei**, auf **Veröffentlichen** und dann auf **Quelldateien exportieren**. Wählen Sie einen Speicherort für die Dateien aus, und klicken Sie dann auf **OK**. Schließen Sie dann die InfoPath-Formularvorlage, die Sie entwerfen.
    
    Navigieren Sie zu dem Speicherort, den Sie für die extrahierten Dateien angegeben haben, und suchen Sie die Datei mit der Dateinamenerweiterung XSF. In der Regel heißt diese Datei "manifest.xsf". Öffnen Sie die Datei in Editor, suchen Sie das `<xsf:file>` Tag, das Ihrem Schema entspricht, und fügen Sie ein "Namespace"-Eigenschaftselement hinzu, um den **targetNamespace** anzugeben, wie im folgenden Beispiel gezeigt. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. Der letzte Schritt beim Vorbereiten des Formulars für die Unterstützung der benutzerdefinierten Zusammenführung besteht darin, das **importParameters**-Element in der dem Formular zugeordneten XSF-Datei zu aktualisieren. 

    Suchen Sie zuerst das  `<xsf:importParameters>` Tag in der XSF-Datei. Fügen Sie für jedes Schema/XSL-Transformationspaar, das Sie für Ihr Formular erstellt haben, dem Element **xsf:importParameters** ein **xsf:importSource-Element** hinzu: `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>` . 
    
    Das  Namensattribut des **xsf:importSource-Elements** enthält den Namen der Formularvorlage, der in einem XML-Quelldokument gefunden werden kann. Normalerweise lassen Sie dies leer. Das **schema**-Attribut enthält den Namen einer Schemadatei, die Sie der Formularvorlage im vorherigen Schritt hinzugefügt haben. Das **transform**-Attribut schließlich enthält den Namen der XSL-Transformation, die Sie zum Konvertieren von dem Schema entsprechenden Formularen verwenden möchten. 
    
    Sie können eine benutzerdefinierte Transformation entweder mit dem [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) oder allein verwenden. 
    
## <a name="creating-a-custom-merge-in-code"></a>Erstellen einer benutzerdefinierten Zusammenführung in Code

Die benutzerdefinierte Zusammenführung mit [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) Code wird mithilfe des Merge-Ereignishandlers mit dem entsprechenden **useScriptHandler-Attribut** des **importParameters-Elements** in der dem Formular zugeordneten XSF-Datei unterstützt. 

In verwaltetem Code können Sie das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) aktivieren, indem Sie das Kontrollkästchen **"Zusammenführen" mit benutzerdefiniertem Code** aktivieren und dann in der Kategorie **"Erweitert"** des Dialogfelds **"Formularoptionen",** das in backstage verfügbar ist, auf die Schaltfläche **"Bearbeiten"** klicken. 
  

