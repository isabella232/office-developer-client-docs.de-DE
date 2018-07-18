---
title: Inhaltssteuerelemente in Word
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- Inhaltssteuerelemente [Word], Inhaltssteuerelemente [Word], Neuigkeiten
localization_priority: Normal
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Erfahren Sie, wie Microsoft Word 2013-Inhaltssteuerelemente einen größeren Bereich von Szenarien für strukturierte Dokumente.
ms.openlocfilehash: 1b0b88da4bc3347ac6748ab57b99d45edd57558d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798515"
---
# <a name="content-controls-in-word"></a>Inhaltssteuerelemente in Word

Erfahren Sie, wie Microsoft Word 2013-Inhaltssteuerelemente einen größeren Bereich von Szenarien für strukturierte Dokumente.

Dieses Thema enthält Informationen zu Änderungen an Inhaltssteuerelemente in Microsoft Word 2013 und die Dokument-Szenarien, die diese Änderungen zu ermöglichen.
  
### <a name="structured-documents"></a>Strukturierte Dokumente
<a name="WordCC_StructuredDocs"> </a>

Strukturierte Dokumente sind Dokumente, die steuern, an welchen Stellen welche Art von Inhalten in einem Dokument angezeigt und ob Inhalte bearbeitet werden können.
  
Es folgen einige häufige Szenarien für strukturierte Inhalte in Microsoft Word:
  
- Eine Anwaltskanzlei muss Dokumente erstellen, die juristische Fachsprache enthalten, die nicht vom Benutzer geändert werden sollte.
    
- Ein Unternehmen muss ein Deckblatt für ein Angebot erstellen, in dem nur der Titel, der Autor und das Datum vom Benutzer eingegeben werden.
    
- Ein Unternehmen muss Rechnungen erstellen, in denen die Kundendaten in vordefinierten Bereichen der Rechnung enthalten sind.
    
### <a name="using-content-controls-to-structure-a-document"></a>Verwenden von Inhaltssteuerelementen zum Strukturieren eines Dokuments
<a name="WordCC_StructuredDocs"> </a>

Inhaltssteuerelemente sind Microsoft Word-Entitäten, die als Container für bestimmte Inhalte in einem Dokument verwendet. Einzelne Inhaltssteuerelemente können Inhalt wie Daten, Listen oder Absätze mit formatierten Text enthalten. Inhaltssteuerelemente helfen Ihnen erstellen umfassender, strukturierte Blöcke mit Inhalt und für die Verwendung in Vorlagen, die definierte Blöcke in Ihre Dokumente, Erstellen von strukturierten Dokumenten einfügen vorgesehen sind.
  
Inhaltssteuerelemente sind ideal für das Erstellen strukturierter Dokumente geeignet, da sie Sie dabei unterstützen, die Position von Inhalten festzulegen, die Art von Inhalten anzugeben (z. B. ein Datum, ein Bild oder Text), die Bearbeitung einzuschränken oder zu ermöglichen und Inhalten eine semantische Bedeutung hinzuzufügen.
  
### <a name="content-controls-in-word-2010"></a>Inhaltssteuerelemente in Word 2010
<a name="WordCC_StructuredDocs"> </a>

Die folgenden Inhaltssteuerelemente sind in Word 2010 verfügbar:
  
- Rich-Text
    
- Nur-Text
    
- Bild
    
- Bausteinkatalog
    
- Kombinationsfeld
    
- Dropdownliste
    
- Datum
    
- Kontrollkästchen
    
- Gruppe
    
Word 2010 mit Inhaltssteuerelementen können verschiedene potenzielle strukturiertes dokumentlösungen, aber in Word 2013 Inhaltssteuerelemente einen größeren Wertebereich Szenarien aktivieren.
  
## <a name="content-control-improvements-in-word-2013"></a>Inhaltssteuerelement Verbesserungen in Word 2013
<a name="WordCC_WhatsNew"> </a>

In Word 2013, Inhaltssteuerelemente bieten drei wichtige Verbesserungen: Visualisierung, Unterstützung für die XML-Zuordnung für Rich-Text-Inhaltssteuerelemente und ein neues Inhaltssteuerelement sich wiederholende Inhalte verbessert.
  
### <a name="improved-visualization"></a>Verbesserte Visualisierung

Word 2013 ermöglicht ein einzelnes Inhaltssteuerelement in einer von drei möglichen Zuständen angezeigt werden:
  
- Umgebendes Feld
    
- Start/Ende-Tags
    
- Keine
    
> [!NOTE]
> Wenn nicht anders angegeben, gilt für die Darstellung der Visualisierung von Inhaltssteuerelementen in diesem Abschnitt, dass das Dokument nicht im **Entwurfsmodus** angezeigt wird. Sie legen den Anzeigemodus für ein Inhaltssteuerelement über das Dropdownlisten-Steuerelement **Anzeigen als** im Dialogfeld **Eigenschaften von Inhaltssteuerelementen** fest. 
  
**Abbildung 1: Das Dialogfeld „Eigenschaften von Inhaltssteuerelementen“**

![Im Dialogfeld Eigenschaften von Inhaltssteuerelement] (media/DK2_WordCC_Fig01.jpg "Im Dialogfeld Eigenschaften von Inhaltssteuerelement")
  
Sie können auch den Anzeigemodus für ein Inhaltssteuerelement mit dem Word 2013-Objektmodell (weiter unten in der [neuen Word 2013 Inhaltssteuerelement Objektmodellelemente](#WordCC_NewOM)) festlegen.
  
### <a name="bounding-box"></a>Umgebendes Feld
<a name="WordCC_DefaultRendering"> </a>

Das standardmäßige Rendering für Inhaltssteuerelementen in Word 2013 ist das Erscheinungsbild von Inhaltssteuerelementen beibehalten, wenn sie in Word 2007 und Word 2010 angezeigt werden. d. h., als umgebenden Feld. Wenn ein Inhaltssteuerelement festgelegt ist, als **Umgebenden Feld**, die Anzeige ändert sich je nach den folgenden Benutzerinteraktion anzeigen:
  
- Wenn das Inhaltssteuerelement nicht im Fokus steht, findet keine Visualisierung statt.
    
- Wenn Sie den Mauszeiger über das Inhaltssteuerelement bewegen, wird es als schattiertes Rechteck angezeigt.
    
**Abbildung 2: Inhaltssteuerelement, wenn der Mauszeiger darüber bewegt wird**

![Inhaltssteuerelement auf Maus über] (media/DK2_WordCC_Fig02.jpg "Inhaltssteuerelement auf Maus über")
  
- Wenn das Inhaltssteuerelement im Fokus steht (wenn der Benutzer das Inhaltssteuerelement auswählt), wird das Steuerelement als „umgebendes Feld“ angezeigt (mit einer Linie um den Inhalt und angezeigtem Titel, wenn ein Titel festgelegt wurde).
    
**Abbildung 3: Inhaltssteuerelement mit Fokus**

![Inhaltssteuerelement mit Fokus] (media/DK2_WordCC_Fig03.jpg "Inhaltssteuerelement mit Fokus")
  
### <a name="startend-tags"></a>Start/Ende-Tags
<a name="WordCC_StartEndTags"> </a>

Wenn die Anzeige des Inhaltssteuerelements als **Start/Ende-Tag** festgelegt ist, werden die Tags unabhängig von der Benutzerinteraktion angezeigt, und der Titel wird nicht angezeigt. Wenn Sie den Mauszeiger darüber bewegen, werden jedoch Schaltflächen, z. B. die Schaltfläche **Dropdownliste** angezeigt. 
  
**Abbildung 4: Anzeige von Inhaltssteuerelementen als Start/Ende-Tags**

![Inhaltssteuerelement eingerichtet wird, um anzuzeigen, wie starten und Beenden von tags] (media/DK2_WordCC_Fig04.jpg "Inhaltssteuerelement eingerichtet wird, um anzuzeigen, wie starten und Beenden von tags")
  
### <a name="none"></a>Keine
<a name="WordCC_Invisible"> </a>

Wenn die Anzeige des Inhaltssteuerelements auf **Keine** festgelegt ist, wird das Inhaltssteuerelement nicht angezeigt.
  
### <a name="content-control-colorization"></a>Farbgebung für Inhaltssteuerelemente
<a name="WordCC_CCColorization"> </a>

Neben der Aktivierung einer anderen Art der Anzeige für ein Inhaltssteuerelement, hilft Word 2013 hinaus Ihnen die Farbe für ein Inhaltssteuerelement festgelegt. Legen Sie die Farbe eines Inhaltssteuerelements mithilfe der Schaltfläche **Farbe** im Dialogfeld **Eigenschaften von Inhaltssteuerelementen** . 
  
Sie können auch die Farbe eines Inhaltssteuerelements festlegen, indem Sie mit dem Word 2013-Objektmodell (weiter unten in der [neuen Word 2013 Inhaltssteuerelement Objektmodellelemente](#WordCC_NewOM)).
  
**Abbildung 5: Das Dialogfeld „Eigenschaften von Inhaltssteuerelementen“**

![Im Dialogfeld Eigenschaften von Inhaltssteuerelement] (media/DK2_WordCC_Fig05.jpg "Im Dialogfeld Eigenschaften von Inhaltssteuerelement")
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a>Unterstützung für die XML-Zuordnung für Rich-Text-Inhaltssteuerelemente
<a name="WordCC_XMLMapping"> </a>

Word 2013 können Sie die Inhalte von rich-Text-Inhaltssteuerelemente sowie Dokument Baustein-Inhaltssteuerelemente XML-Datenspeicher zuordnen. Zu diesem Zweck legen Sie die *XML-Zuordnung* für das Inhaltssteuerelement. Sie können diese Eigenschaft festlegen, mithilfe der vorhandenen **XMLMapping.SetMapping** -Methode im Objektmodell. Innerhalb der benutzerdefinierten XML-Komponente wird der benutzerdefinierten XML-Code als flat Open XML-Markup in einer Zeichenfolge konvertiert (mithilfe der standard-XML-Codierung), also, gespeichert als Textknoten in benutzerdefinierten XML-Komponente kann gespeichert werden. Die Zuordnung wird jedoch weiterhin die Einschränkung verfügen, die es nur erfolgreich zum Knoten oder Attribute Blätter zuordnen kann. 
  
> [!NOTE]
> Rich-Text-Inhaltssteuerelemente können keine anderen Rich-Text-Inhaltssteuerelemente enthalten. Wenn eins in einem anderen vorhanden ist (z. B. aufgrund von Dateiformatänderungen, Kopieren und Einfügen usw.), wird das Steuerelement getrennt, bis es nicht mehr in einem zugeordneten Rich-Text-Steuerelement enthalten ist. 
  
Weitere Informationen zum Einrichten der XML-Zuordnung finden Sie im Abschnitt  [Neue Word 2013-Inhaltssteuerelement-Objektmodellelemente](#WordCC_NewOM) weiter unten in diesem Thema. 
  
### <a name="supporting-repeating-content"></a>Unterstützung für wiederholte Inhalte
<a name="WordCC_SupportingRepeating"> </a>

Zusätzlich zur Visualisierung Verbesserungen und Unterstützung für XML-Zuordnung für rich-Text-Inhaltssteuerelemente fügt Word 2013 auch ein neues Inhaltssteuerelement, das Sie wiederholen die Inhalte ermöglicht. Das wiederholten Abschnitt Inhaltssteuerelement wird den Inhalt enthaltenen, einschließlich anderer Inhaltssteuerelemente wiederholt.
  
Sie fügen das Steuerelement für wiederkehrende Abschnittsinhalte um ganze Absätze oder Tabellenzeilen ein. Nachdem das Steuerelement einen Abschnitt umgibt, können Sie Kopien des Abschnitts über oder unter dem enthaltenen Abschnitt einfügen.
  
**Abbildung 6: Kontextmenü des Steuerelements für wiederkehrende Inhaltsabschnitte**

![Wiederholt Kontext] (media/DK2_WordCC_Fig06.jpg "Wiederholt Kontext")
  
Sie können den eingefügten Abschnitt mithilfe der entweder das Steuerelement auf das Ende des Inhaltssteuerelements (angezeigt als Schaltfläche mit einem Pluszeichen (![Pluszeichen (+)](media/DK2_WordCC_Fig06A.jpg "Pluszeichen (+)"))) oder indem Sie auf einen Befehl im Kontextmenü wiederholen, wie in Abbildung 6 dargestellt. Der wiederholte Inhalt wird einem separaten Abschnitt des Steuerelements können Sie einen Titel über das Dialogfeld **Eigenschaften von Inhaltssteuerelementen** zuweisen. 
  
**Abbildung 7: Zuweisen eines Abschnittstitels im Dialogfeld „Eigenschaften von Inhaltssteuerelementen“**

![Im Dialogfeld Eigenschaften von Inhaltssteuerelement] (media/DK2_WordCC_Fig07.jpg "Im Dialogfeld Eigenschaften von Inhaltssteuerelement")
  
Nachdem Sie dem Abschnitt einen Titel gegeben haben, können Benutzer den Abschnitt nach Namen hinzufügen oder löschen, wenn Sie die Option **Benutzern das Hinzufügen und Entfernen von Abschnitten erlauben** im Dialogfeld **Eigenschaften von Inhaltssteuerelementen** auswählen. 
  
**Abbildung 8: Verwenden des Kontextmenüs des Steuerelements für wiederkehrende Abschnittsinhalte zum Löschen eines Abschnitts**

![Wiederholt Kontext] (media/DK2_WordCC_Fig08.jpg "Wiederholt Kontext")
  
Wenn ein wiederkehrender Abschnitt andere Inhaltssteuerelemente umgibt, werden die eingeschlossenen Inhaltssteuerelemente in jedem neuen Element wiederholt. Allerdings werden bei solchen Inhaltssteuerelementen die Inhalte auf Platzhaltertext zurückgesetzt. Es gibt zwei Ausnahmen, bei denen untergeordnete Steuerelementinhalte beibehalten werden: 
  
- Wenn ein untergeordnetes Steuerelement ein Steuerelement für wiederkehrende Abschnitte ist.
    
- Wenn ein untergeordnetes Steuerelement per XML einem Knoten außerhalb des Steuerelements für wiederkehrende Abschnittsinhalte zugeordnet ist.
    
**Abbildung 9: Steuerelement für wiederkehrende Abschnittsinhalte mit untergeordneten Steuerelementen vor Wiederholung**

![Wiederholen Sie die wiederholungsabschnitts vor] (media/DK2_WordCC_Fig09.jpg "Wiederholen Sie die wiederholungsabschnitts vor")
  
**Abbildung 10: Steuerelement für wiederkehrende Abschnittsinhalte mit untergeordneten Steuerelementen nach Wiederholung**

![Wiederholen Sie die wiederholungsabschnitts nach] (media/DK2_WordCC_Fig10.jpg "Wiederholen Sie die wiederholungsabschnitts nach")
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a>Steuerelemente für wiederkehrende Abschnittsinhalte rund um per XML zugeordnete Steuerelemente
<a name="WordCC_RepeatingSectionCCs"> </a>

Für XML-Zuordnungen, die in einem wiederholten Abschnitt enthalten sind, ordnet Word 2013 diese wie folgt aus.
  
Wenn die Zuordnung nicht mit einem Element in der Gruppe als Teil der Kette übergeordneten Knoten schneidet, die Bindung "absolute Bindung" und zeigt den gleichen Inhalt in alle Elemente in einem wiederholten Abschnitt.
  
Wenn die Zuordnung eines Elements in der Gruppe als Teil der Kette übergeordneten Knoten schneidet, wird die Bindung einer Bindung"relative", und wird wie folgt zugeordnet:
  
- Die absolute Bindung für den Knoten wird bestimmt (dabei werden alle Abfrageausdrücke vereinfacht) – dies sollte bei der anfänglichen Zuordnung stattfinden.
    
- Die Achse der Bindung, die sich mit dem festgelegten Knoten überschneidet, wird entfernt.
    
- Der restliche Teil des XPath-Ausdrucks wird relativ zum XPath des wiederholten Abschnittsinhaltselements ausgewertet.
    
Beispielsweise könnten die folgenden Zuordnungen auftreten:
  
- Der wiederholte Abschnitt wird \root\next\path zugeordnet.
    
- Das Steuerelement im Beispielelement wird \root\next\path[2]\baz zugeordnet.
    
- Word ordnet \root\next\path[2] einem Element im Knotensatz zu.
    
Die Bindung wird daher als .\baz ausgewertet, wobei die Basis der Knoten des wiederholten Inhaltselements ist.
  
Die folgenden Vorschläge für das Arbeiten mit Steuerelementen für wiederkehrende Inhalte können dazu beitragen, Datenverluste und Frustration zu vermeiden.
  
### <a name="working-with-repeating-section-content-controls-that-are-mapped-to-xml-data"></a>Arbeiten mit Steuerelementen für wiederkehrende Abschnittsinhalte, die XML-Daten zugeordnet sind
<a name="WordCC_RepeatingSectionCCs"> </a>

Beim Einfügen einer wiederholten Abschnitt Inhaltssteuerelement, das XML-Daten zugeordnet ist, jedes Mal, wenn die Benutzer das Dokument erneut öffnet, werden die Elemente in einem wiederholten Abschnitt, anhand der Informationen im Datenspeicher von Word neu erstellt. Auch wenn Sie das Dokument zu speichern, sind alle Änderungen, die der Benutzer in der Elemente in einem wiederholten Abschnitt im Dokument vornimmt, die auch in dem Datenspeicher zugeordnet werden nicht verloren.
  
Um dies zu verhindern, sollten Sie das Steuerelement für wiederkehrende Abschnittsinhalte sperren und für den Benutzer nur das Bearbeiten in nicht gesperrten untergeordneten Inhaltssteuerelementen erlauben, die ebenfalls dem XML-Code zugeordnet sind.
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a>Binden eines Steuerelements für wiederkehrende Abschnittsinhalte zu einer Tabelle
<a name="WordCC_RepeatingSectionCCs"> </a>

Wenn ein wiederholten Abschnitt Inhaltssteuerelement an eine Tabelle gebunden werden soll, legen Sie die Tabelle, und *Klicken Sie dann* das Einfügen wiederholter Abschnitt Inhaltssteuerelement und nicht umgekehrt. (Andernfalls wird nicht Sie nur die Tabelle auswählen können). 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a>Schachtelung von Steuerelementen für wiederkehrende Abschnittsinhalte innerhalb einer Tabelle
<a name="WordCC_RepeatingSectionCCs"> </a>

Das Schachteln von Steuerelementen für wiederkehrende Abschnittsinhalte innerhalb einer Tabelle (wenn sich beispielsweise das Ende des übergeordneten und des untergeordneten Steuerelements für wiederkehrende Abschnittsinhalte in derselben Zelle befindet) bewirkt, dass der äußere wiederholte Abschnitt gelöscht wird, wenn dem inneren Abschnitt ein Element hinzugefügt oder ein Element daraus entfernt wird.
  
Sie können dies verhindern, indem Sie eine Absatzmarkierung zwischen dem Ende eines Steuerelements für wiederkehrende Abschnittsinhalte und dem nächsten hinzufügen. Zum Ausblenden der Absatzmarkierung deaktivieren Sie auf der Registerkarte **Start** des Menübands die Option **Ein-/Ausblenden**. 
  
### <a name="open-xml-file-format-schema-additions"></a>Erweiterungen für das Open XML-Dateiformatschema
<a name="WordCC"> </a>

Die folgenden Elemente wurden zum Open XML-WordprocessingML-Dateiformatschema hinzugefügt.
  
**Tabelle 1: Neue Elemente im Open XML-WordprocessingML-Dateiformatschema für Inhaltssteuerelemente**

|**Element**|**Beschreibung**|
|:-----|:-----|
|\<w:Appearance\>  <br/> |\<W:Appearance\> ist ein untergeordnetes Element des \<W:sdtPr\>.  <br/> Die folgenden Werte sind für das val-Attribut gültig:  <br/> \<W:Appearance Val = BoundingBox|-Tags hinzugefügtes Markup|ausgeblendet.  <br/> Der Standardwert ist boundingBox.  <br/> |
|\<w:Color\>  <br/> |\<W:Color\> ist ein untergeordnetes Element des \<W:sdtPr\>.  <br/> Das Inhaltsmodell stimmt mit dem vorhandenen komplexen CT_Color-Typ überein. Der Standardwert ist die in Word 2010 verwendete Farbe.  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a>Neue Word 2013 Inhaltssteuerelement Elemente des Objektmodells
<a name="WordCC_NewOM"> </a>

Mit dem neuen Verbesserungen und Ergänzungen von Inhaltssteuerelementen in Word 2013 wurde das Objektmodell für Word aktualisiert, um die programmgesteuerte Bearbeitung der neuen Features zu ermöglichen. Darüber hinaus haben auch die zugrunde liegenden Open XML-Dateiformat für Textverarbeitungsdokumenten geändert wurde.
  
In den folgenden Abschnitten finden Sie weitere Informationen zu den speziellen Objektmodelländerungen im Zusammenhang mit der jeweiligen Inhaltssteuerelementverbesserung.
  
### <a name="visualization-enhancements"></a>Verbesserungen der Visualisierung
<a name="WordCC_VisEnhancements"> </a>

Mehrere objektmodellergänzungen sind für Inhaltssteuerelement Visualisierung Verbesserungen in Word 2013 enthalten. In der folgenden Tabelle werden neue Elemente des **ContentControl** -Objekts für Visualisierung aufgelistet. 
  
**Tabelle 2: Neue ContentControl-Objektelemente**

|**Member**|**Beschreibung**|
|:-----|:-----|
|. **Darstellung** als **WdContentControlAppearance** <br/> |Ruft die Visualisierung des Inhaltssteuerelements ab oder legt sie fest.  <br/> |
|. **Farbe** als **WdColor** <br/> |Ruft die Farbe des Inhaltssteuerelements ab oder legt sie fest.  <br/> |
   
In der folgenden Tabelle sind Konstanten in der neuen **WdContentControlAppearance**-Enumeration aufgeführt. 
  
**Tabelle 3: Neue WdContentControlAppearance-Enumerationskonstanten**

|**Konstante**|**Beschreibung**|
|:-----|:-----|
|**wdContentControlBoundingBox** <br/> |Stellt ein Inhaltssteuerelement dar, das als schattiertes Rechteck/umgebendes Feld angezeigt wird (mit optionalem Titel).  <br/> |
|**wdContentControlTags** <br/> |Stellt ein Inhaltssteuerelement dar, das als Start/Ende-Markierung angezeigt wird.  <br/> |
|**wdContentControlHidden** <br/> |Stellt ein Inhaltssteuerelement dar, das nicht angezeigt wird.  <br/> |
   
### <a name="code-sample"></a>Codebeispiel
<a name="WordCC_VisEnhancements"> </a>

Das folgende Codebeispiel zeigt, wie Rich-Text-Inhaltssteuerelemente erstellt werden und die Visualisierung programmgesteuert festgelegt wird.
  
```vb
Sub testVisualization()
   Dim objcc As ContentControl
   Dim objRange As Range
   
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Default Bounding Box"
   ' Set visualization to the default.
   objcc.Appearance = wdContentControlBoundingBox
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(2).Range
   ' Create a rich text content control around the second paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Non Bounding"
   ' Set visualization to invisible.
   objcc.Appearance = wdContentControlHidden
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(3).Range
   ' Create a rich text content control around the third paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Tags Only with Pink color"
   ' Set visualization to Start/End tags with pink color.
   objcc.Appearance = wdContentControlTags
   objcc.Color = wdColorPink
End Sub
```

### <a name="xml-mapping"></a>XML-Zuordnung
<a name="WordCC_XMLMappingOM"> </a>

Keine Ergänzungen wurden dem Objektmodell von Word 2013 vorgenommen, rich-Text-Zuordnung, die XML-Knoten im Datenspeicher Dokument einzeln zu autorisieren. Verwenden Sie stattdessen das vorhandene Objektmodell, um ein rich-Text-Inhaltssteuerelement einem XML-Knoten im Datenspeicher Dokument zuzuordnen. Darüber hinaus wurden keine Änderungen an der zugrunde liegenden Open XML-Datei Format WordprocessingML-Schema als Teil der neu enthalten rich-Text-Inhaltssteuerelement Unterstützung speziell für XML-Zuordnung vorgenommen.
  
#### <a name="code-sample"></a>Codebeispiel

Das folgende Codebeispiel zeigt, wie ein Rich-Text-Inhaltssteuerelement programmgesteuert einem XML-Knoten zugeordnet wird.
  
```vb
Sub testRichBinding()
   Dim objRange As Range
   Dim objcc As ContentControl
   Dim objCustomPart As CustomXMLPart
   Dim blnMap As Boolean
   
   ' Add a custom XML part to the data store.
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   ' Load XML fragment into the custom XML part.
   objCustomPart.LoadXML ("<x>Rich Text Databinding</x>")
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   ' Bind the XML node to the rich text content control.
   blnMap = objcc.XMLMapping.SetMapping("/x")
   ' Return whether mapping worked.
   MsgBox objcc.XMLMapping.IsMapped
End Sub
```

### <a name="repeating-section-content-controls-represented-in-the-object-model"></a>Im Objektmodell dargestellte Steuerelemente für wiederkehrende Abschnittsinhalte
<a name="WordCC_RepeatingSection"> </a>

Das Steuerelement für wiederkehrende Abschnittsinhalte steht im Objektmodell zur Verfügung, indem Sie die folgenden Ergänzungen für das **ContentControl**-Objekt und die neuen **RepeatingSectionItem**- und **RepeatingSectionItemColl**-Objekte verwenden. In Tabelle 4 sind die wichtigsten neuen Elemente des **ContentControl**-Objekts für Steuerelemete für wiederkehrende Abschnittsinhalte aufgeführt. 
  
**Tabelle 4: ContentControl-Objektelemente**

|**Member**|**Beschreibung**|
|:-----|:-----|
|**AllowInsertDeleteSection** als **Boolean** <br/> |Ruft ab oder legt fest, ob Benutzer können Abschnitte hinzufügen oder aus dem Inhaltssteuerelement entfernen mithilfe der Benutzeroberfläche. Wenn diese Eigenschaft für ein Inhaltssteuerelement, die nicht vom Typ wiederholter Abschnitt ist aufgerufen wird, wird der Aufruf fehlschlägt, wobei die folgende Fehlermeldung angezeigt: "Diese Eigenschaft kann nur verwendet werden mit wiederholter Abschnitt Inhaltssteuerelemente."  <br/> |
|**RepeatingSectionItemTitle** als **String** <br/> |Dient zum Abrufen oder Festlegen des Namens wiederholter Abschnitt Elemente im Kontextmenü verwendet. Wenn diese Eigenschaft für ein Inhaltssteuerelement, die nicht vom Typ wiederholter Abschnitt ist aufgerufen wird, schlägt der Aufruf mit: "Diese Eigenschaft kann nur verwendet werden mit wiederholter Abschnitt Inhaltssteuerelemente."  <br/> |
|**InsertRepeatingSectionItemBefore** als **ContentControl** <br/> |Fügt ein wiederholten Abschnitt Element vor dem aktuellen Element und gibt das neue wiederholten Abschnitt-Element zurück. Wenn diese Methode für ein Inhaltssteuerelement, die nicht vom Typ wiederholter Abschnitt-Element ist aufgerufen wird, schlägt der Aufruf mit: "Diese Eigenschaft kann nur verwendet werden mit wiederholter Abschnitt Element von Inhaltssteuerelementen."  <br/> |
|**InsertRepeatingSectionItemAfter** als **ContentControl** <br/> |Fügt ein wiederholten Abschnitt-Element nach dem aktuellen Element und gibt das neue wiederholten Abschnitt-Element zurück. Wenn diese Methode für ein Inhaltssteuerelement, die nicht vom Typ wiederholter Abschnitt-Element ist aufgerufen wird, schlägt der Aufruf mit: "Diese Eigenschaft kann nur verwendet werden mit wiederholter Abschnitt Element von Inhaltssteuerelementen."  <br/> |
   
In Tabelle 5 sind die wichtigsten Elemente des  **RepeatingSectionItem**-Objekts aufgeführt. 
  
**Tabelle 5: RepeatingSectionItem-Objektelemente**

|**Member**|**Beschreibung**|
|:-----|:-----|
|**Range** als **Range** <br/> |Gibt den Bereich des angegebenen wiederholten Abschnitt Elements, ausgenommen die Start- und Endtags zurück.  <br/> |
|**Delete** <br/> |Löscht das angegebene wiederholte Abschnittselement.  <br/> |
|**InsertItemAfter** als **RepeatingSectionItem** <br/> |Fügt ein wiederholtes Abschnittselement nach dem angegebenen Element hinzu und gibt das neue Element zurück.  <br/> |
|**InsertItemBefore** als **RepeatingSectionItem** <br/> |Fügt ein wiederholtes Abschnittselement vor dem angegebenen Element hinzu und gibt das neue Element zurück.  <br/> |
   
In Tabelle 6 sind die wichtigsten Elemente des **RepeatingSectionItemColl**-Objekts aufgeführt. 
  
**Tabelle 6: RepeatingSectionItemColl-Objektelemente**

|**Member**|**Beschreibung**|
|:-----|:-----|
|**Item** als **RepeatingSectionItem** <br/> |Gibt ein einzelnes wiederholtes Abschnittselement zurück.  <br/> |
   
In Tabelle 7 ist das neue Element der **WdContentControlType**-Enumeration für Steuerelemente für wiederkehrende Abschnittsinhalte gezeigt. 
  
**Tabelle 7: WdContentControlType-Enumerationsergänzung**

|**Konstante**|**Beschreibung**|
|:-----|:-----|
|**wdContentControlRepeatingSection** <br/> |Stellt ein Inhaltssteuerelement dar, das ein einzelnes Element in einem wiederholten Abschnitt enthält.  <br/> |
   
### <a name="code-sample"></a>Codebeispiel
<a name="WordCC_RepeatingSection"> </a>

Das folgende Codebeispiel zeigt, wie Steuerelemente für wiederkehrende Abschnittsinhalte programmgesteuert verwendet werden.
  
```vb
Sub testRepeatingSectionControl()
   Dim objRange As Range
   Dim objTable As Table
   Dim objCustomPart As CustomXMLPart
   Dim objCC As ContentControl
   Dim objCustomNode As CustomXMLNode
   
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   objCustomPart.LoadXML ("<books>" & _
       "<book><title>Everyday Italian</title>" & _
       "<author>Giada De Laurentiis</author></book>" & _
       "<book><title>Harry Potter</title>" & _
       "<author>J K. Rowling</author></book>" & _
       "<book><title>Learning XML</title>" & _
       "<author>Erik T. Ray</author></book></books>")
   
   Set objRange = ActiveDocument.Paragraphs(1).Range
   Set objTable = ActiveDocument.Tables.Add(objRange, 2, 2)
   With objTable.Borders
       .InsideLineStyle = wdLineStyleSingle
       .OutsideLineStyle = wdLineStyleDouble
   End With
   Set objRange = objTable.Cell(1, 1).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/title[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Cell(1, 2).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/author[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Rows(1).Range
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlRepeatingSection, objRange)
   objCC.XMLMapping.SetMapping ("/books[1]/book")
End Sub
```

### <a name="open-xml-file-format-changes-for-repeating-section-content-controls"></a>Open XML-Dateiformatänderungen für Steuerelemente für wiederkehrende Abschnittsinhalte
<a name="WordCC_RepeatingSection"> </a>

Die Datei Format Darstellung eines wiederholten Abschnitt Inhaltssteuerelements verwendet die Elementnamen Werte im Allgemeinen usw. als das vorhandene XML-Markup; jedoch die \<Sdt\> Element, das den äußeren wiederholten Abschnitt Container darstellt im Word 2013-Namespace vorhanden ist, um die Kompatibilität mit früheren Versionen von Word sicherzustellen.
  
Die einzelnen wiederholten Elemente im Steuerelement für wiederkehrende Abschnittsinhalte (die jedes einzelnes Element umgeben) werden über die vorhandene WordprocessingML-Darstellung als Rich-Text-Inhaltssteuerelemente gespeichert. In Tabelle 8 sind die neuen Elemente im WordprocessingML-Schema für Steuerelemente für wiederkehrende Abschnittsinhalte aufgeführt.
  
**Tabelle 8: Neue Elemente im WordprocessingML-Schema für Steuerelemente für wiederkehrende Abschnittsinhalte**

|**Element**|**Beschreibung**|
|:-----|:-----|
|\<w15:repeatingSection\>  <br/> |Gibt ein Steuerelement für wiederkehrende Abschnittsinhalte an. Dieses Element schließt sich mit allen anderen Steuerelementtypen gegenseitig aus und verfügt nicht über untergeordnete Elemente oder Attribute.  <br/> |
|\<w15:repeatingSectionItem\>  <br/> |Gibt ein Steuerelement für wiederkehrende Abschnittsinhaltselemente an. Dieses Element schließt sich mit allen anderen Steuerelementtypen gegenseitig aus und verfügt nicht über untergeordnete Elemente oder Attribute.  <br/> |
|\<w15:doNotAllowInsertDeleteSection\>  <br/> |Gibt an, dass der Benutzer kann nicht hinzufügen oder Löschen von Abschnitten mithilfe der Benutzeroberfläche in Word 2013.  <br/> |
|\<w15:sectionTitle\>  <br/> |Gibt den Namen von wiederholten Abschnittselementen an (und wird im Kontextmenü verwendet, wenn das Steuerelement ausgewählt wird).  <br/> |
   

  

