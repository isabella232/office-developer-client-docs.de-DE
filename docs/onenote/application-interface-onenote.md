---
title: Anwendungsschnittstelle (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'Die Application-Schnittstelle enthält die Methoden Hilfe abrufen, bearbeiten und Aktualisieren von OneNote-Informationen und Inhalte. Die Methoden sind in vier allgemeine Kategorien:'
ms.openlocfilehash: 25bb1aa570f6c36aa04140d9256d277bee65152b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790901"
---
# <a name="application-interface-onenote"></a>Anwendungsschnittstelle (OneNote)

Die **Application** -Schnittstelle enthält die Methoden Hilfe abrufen, bearbeiten und Aktualisieren von OneNote-Informationen und Inhalte. Die Methoden sind in vier allgemeine Kategorien: 
  
- **Notebook-Struktur** &ndash; Methoden zum Arbeiten mit Notebook-Struktur, einschließlich derjenigen für ermitteln, öffnen, ändern, schließen und Löschen von Notizbücher, Abschnitte und Abschnittsgruppen. 
    
- **Seiteninhalt** &ndash; Methoden zum Arbeiten mit Seiten und Seiteninhalt, einschließlich derjenigen für ermitteln, ändern, speichern und Löschen von Inhalt. Seiteninhalt enthält binäre Objekte, wie Freihand- und Bilder, und Textobjekte, wie Konturen. 
    
- **Navigation** &ndash; Methoden zum Suchen, Verknüpfen mit und Navigation auf Seiten und Objekte. 
    
- **Funktionale** &ndash; Alle Methoden, die bestimmte Aktionen ausführen oder in OneNote Parameter festlegen. 
    
Darüber hinaus enthält **die Anwendungsschnittstelle** eine Anzahl von *Eigenschaften* und *Ereignisse* . 
  
## <a name="notebook-structure-methods"></a>Notebook-Methoden für Datenstruktur
<a name="ON14DevRef_Application_NotebookStructure"> </a>

In diesem Abschnitt beschriebenen Methoden können Sie ermitteln, öffnen, ändern, schließen und Löschen von OneNote-Notizbüchern, Abschnittsgruppen und Abschnitte.
  
### <a name="gethierarchy-method"></a>GetHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft die Notizbuch Knoten Hierarchiestruktur, ausgehend von den Knoten, die Sie angeben (alle Notizbücher oder eine einzelne Notizbuch, Abschnittsgruppe oder Abschnitt), und erweitern Sie nach unten für alle untergeordneten Elemente auf der Ebene, die Sie angeben.  <br/> |
|**Syntax** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Parameter** <br/> | _bstrStartNodeID_ &ndash; Den Knoten (Notizbuch, Abschnitt Gruppen- oder Abschnitt), dessen untergeordnete Objekte werden soll. Wenn Sie eine null-Zeichenfolge übergeben (""), die Methode ruft alle Knoten unterhalb des Stammknotens (d. h., alle Notizbücher, Abschnittsgruppen und Abschnitte). Wenn Sie ein Notizbuch, Abschnitt Gruppen- oder Abschnittsknoten angeben, ruft die Methode nur untergeordnete Objekte des Knotens ab.  <br/><br/>_hsScope_ &ndash; Der niedrigsten untergeordnete Knotenebene werden soll. Angenommen, wenn Sie Seiten angeben, ruft die Methode alle Knoten so weit nach unten als der Seitenebene. Wenn Sie Abschnitte angeben, ruft die Methode nur Abschnitt Knoten unterhalb des Notizbuchs ab. Weitere Informationen finden Sie unter der **HierarchyScope** -Enumeration im Thema [Enumerationen](enumerations-onenote-developer-reference.md#odc_HierarchyScope) .  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Ausgabeparameter) ein Zeiger auf die Zeichenfolge, die in der OneNote die XML-Ausgabe geschrieben werden sollen.  <br/><br/>_xsSchema_ &ndash; (Optional) die Version des OneNote-XML-Schemas, vom Typ **XMLSchema**, die ausgegeben werden soll. Sie können angeben, ob Sie XML-Schema Version 2013, 2010, 2007, oder die aktuelle Version.  <br/><br/>**Hinweis**: Es wird empfohlen Festlegen einer Version von OneNote (beispielsweise **xs2013**) anstelle von **XsCurrent** verwenden oder es leer lassen, da dadurch das Add-in zukünftige Versionen von OneNote entwickelt.           |
   
Die GetHierarchy-Methode gibt eine Zeichenfolge in OneNote 2013 XML-Format standardmäßig, oder die bevorzugte XML-Schema-Version festlegen kann mithilfe des Parameters optional _XsSchema_ zurück. 
  
Abhängig von den Parametern, die Sie weitergeben, kann die **GetHierarchy** -Methode verschiedenen Listen (beispielsweise alle Notizbücher, alle Abschnitte in alle Notizbücher, alle Seiten innerhalb eines bestimmten Bereichs oder alle Seiten innerhalb einer bestimmten Notizbuch) zurück. Für jeden Knoten bietet die zurückgegebene XML-Zeichenfolge Eigenschaften (beispielsweise Abschnitt oder Seite Titel, ID und Zeitpunkt der letzten Änderung). 
  
Nicht alle Kombinationen von Startknoten und des Umfangs sind ungültig. Angenommen, wenn Sie angeben, ein Abschnitt Knoten und einen Bereich Notizbuch beginnen, **GetHierarchy** null gibt ein Ergebnis zurück, da ein Notizbuch in der Knotenhierarchie als ein Abschnitt höher ist. 
  
Im folgenden C#-Beispiel veranschaulicht die **GetHierarchy** -Methode verwenden, um die gesamte OneNote-Hierarchie, einschließlich aller Notizbücher, nach unten zu der Seitenebene abzurufen. Kopiert die Ausgabezeichenfolge in die Zwischenablage, aus der Sie die Zeichenfolge in einem Text-Editor zur Prüfung einfügen können. 
  
```cs
static void GetEntireHierarchy()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(null, 
            OneNote.HierarchyScope.hsPages, out strXML);
        Clipboard.SetText(strXML);
        MessageBox.Show("The XML has been copied to the clipboard");
    }

```

### <a name="updatehierarchy-method"></a>UpdateHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung**|Ändert oder die Hierarchie der Notizbücher aktualisiert. Beispielsweise können Sie hinzufügen, Abschnitte oder Abschnittsgruppen in einem Notizbuch hinzufügen ein neues Notizbuchs, Abschnitte innerhalb eines Notizbuchs zu verschieben, ändern Sie den Namen eines Abschnitts, Seiten zu einem Abschnitt hinzufügen oder Ändern der Reihenfolge von Seiten in einem Abschnitt.|
|**Syntax**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Parameter**| _bstrChangesXmlIn_ &ndash; Eine Zeichenfolge, die OneNote-XML-Code, der angibt, die Hierarchie Änderungen enthält vornehmen. Beispielsweise wenn Sie einen neuen Abschnitt einfügen möchten, können Sie ein **Abschnitt** Element hinzufügen in der XML-Zeichenfolge, um anzugeben, wo Sie den neuen Abschnitt hinzugefügt werden soll. Wenn Sie den Namen eines vorhandenen Abschnitts ändern möchten, können Sie alternativ beibehalten der ID Abschnitt und ändern Sie das **Name** -Attribut in der XML-Code.<br/><br/>_xsSchema_ &ndash; (Optional) der OneNote-Schemaversion von der Zeichenfolge _BstrChangesXmln_. Dieser Wert optionale wird Angabe die Version des OneNote-XML-Schemas, die die Zeichenfolge _BstrChangesXmlIn_ wird verwendet. Wenn dieser Wert nicht angegeben ist, wird OneNote wird vorausgesetzt, dass der XML-Code im Schema Version _XsCurrent_ist. <br/><br/>**Hinweis**: Es wird empfohlen Festlegen einer Version von OneNote (beispielsweise **xs2013**) anstelle von **XsCurrent** verwenden oder es leer lassen, da dadurch das Add-in zukünftige Versionen von OneNote entwickelt.           |
   
Wenn Sie nur eine partielle OneNote-XML-Zeichenfolge für den _BstrChangesXmlIn_ -Parameter übergeben, versucht OneNote, die Änderungen abzuleiten gewünschten. Wenn Sie ein **Notizbuch** -Element, die nur einen Abschnitt enthält enthalten, fügt der OneNote im Abschnitt nach bestehende Abschnitte an. Wenn der Vorgang, die von den Ihnen angegebenen mehrdeutig ist, kann das Ergebnis jedoch schwer zu ermitteln sein. Beispielsweise kann ein vorhandenes Notizbuchs enthält vier Abschnitte, und die XML-Zeichenfolge, die Sie weitergeben umfasst das Notizbuch und nur die vierte und erste Abschnitte (in dieser Reihenfolge), OneNote die zweiten und dritten Abschnitten vor der vierte Abschnitt oder nach dem ersten Abschnitt platzieren . 
  
Sie können nicht die **UpdateHierarchy** -Methode verwenden, um Teil eines Notizbuchs zu löschen. D. h., löscht übergeben eine XML-Zeichenfolge, die nur einen Teil einer vorhandenen Hierarchie enthält Abschnitte nicht, die nicht in der Zeichenfolge enthalten sind. Verwenden Sie die **DeleteHierarchy** -Methode, um Teil einer Hierarchie zu löschen. 
  
Der folgende C#-Code zeigt eine Möglichkeit, die **UpdateHierarchy** -Methode verwenden, um die OneNote-Hierarchie ändern, indem Sie den Namen eines vorhandenen Abschnitts. XML-Code aus der Beispieldatei mit dem Namen ChangeSectionName.xml im Stamm von Laufwerk C, in einem XML-Dokument geladen und übergibt dann die XML-Struktur des Dokuments an die-Methode liest. 
  
```cs
static void UpdateExistingHierarchy()
    {
        OneNote.Application onApplication = new OneNote.Application();
        
        // Get the XML from the file.
        XmlTextReader reader = new XmlTextReader("C:\\ChangeSectionName.xml");
        reader.WhitespaceHandling = WhitespaceHandling.None;
        XmlDocument xmlDocIn = new XmlDocument();
        xmlDocIn.Load(reader);
        
        // Update the hierarchy.
        onApplication.UpdateHierarchy(xmlDocIn.OuterXml,
        OneNote.XMLSchema.xs2007);   
    }

```

Der folgende XML-Code ist ein Auszug der ChangeSectionName.xml-Datei, die an die-Methode des vorherigen C#-Codes übergibt. Wenn die XML-Daten an die **UpdateHierarchy** -Methode übergeben wird, wird es den Namen eines der Abschnitte in der vorhandenen Hierarchie (durch den Wert des **Name** -Attributs in "Meine umbenannt im Abschnitt" ändern). Klicken Sie dann entfernt alle Abschnitte mit Ausnahme des, dessen Name geändert wurde. Darüber hinaus wird der Code entfernt unnötige Attribute vom **Abschnitt** Zielelement, einschließlich von Attributen **ZuletztGeändertUm**, **IsCurrentlyViewed**und **Farbe** , wobei nur der **Name**, **ID**und ** Pfad** Attribute erhalten bleibt. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

Der vorherigen XML-Code wurde mit dem Code im Beispiel für die **GetHierarchy** -Methode, die wie folgt geändert wird, zum Einschränken des Bereichs in Abschnitten dargestellt abgerufen. 
  
```cs
static void GetAllSections()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(System.String.Empty, 
            OneNote.HierarchyScope.hsSections, out strXML);
        Clipboard.SetText(strXML.ToString());
        MessageBox.Show("The XML has been copied to the Clipboard");
    }

```

Im folgenden C#-Beispiel zeigt eine vollständige Konsolenanwendung, das durchsucht für einen Bereich mit dem Namen " `Sample_Section`", fordert den Benutzer zur Eingabe eines neuen Namens für den Abschnitt, und klicken Sie dann die **UpdateHierarchy** -Methode verwendet, um den Namen des Abschnitts auf den Namen ändern, die der Benutzer eingegeben haben. Ändern Sie vor dem Ausführen des Codes " `Sample_Section`" auf den Namen eines Abschnitts, der in der OneNote-Hierarchie vorhanden ist.
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "http://schemas.microsoft.com/office/onenote/2013/onenote";
        string outputXML;
        Application onApplication = new Application();
        onApplication.GetHierarchy(null, HierarchyScope.hsSections, out outputXML);
        // Load a new XmlDocument.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.LoadXml(outputXML);
        XmlNamespaceManager nsmgr = new XmlNamespaceManager(xmlDoc.NameTable);
            nsmgr.AddNamespace("one", strNamespace);
        // Search for the section named "Sample_Section".
        XmlNode xmlNode = xmlDoc.SelectSingleNode("//one:Section[@name='Sample_Section']", nsmgr);
        // Prompt for a new section title.
        System.Console.Write("Please enter a new title for the section: ");
        string input = System.Console.ReadLine();
        xmlNode.Attributes["name"].Value = input; 
        // Update the section with the new title.
        onApp.UpdateHierarchy(xmlNode.OuterXml);
        System.Console.Write("Done!\n");
    }

```

### <a name="openhierarchy-method"></a>OpenHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Öffnet ein Abschnittsgruppe oder eines Abschnitts, die Sie angeben.  <br/> |
|**Syntax** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Parameter** <br/> | _bstrPath_ &ndash; Den Pfad, den Sie öffnen möchten. Ein Notizbuch oder einer Gruppe in einem Notizbuch kann _BstrPath_ ein Ordnerpfad oder den Pfad zum Abschnitt ONE-Datei sein. Wenn Sie den Pfad zum Abschnitt ONE-Datei angeben, müssen Sie die Erweiterung One auf die Datei Pfadzeichenfolge einbeziehen.  <br/><br/>_bstrRelativeToObjectID_ &ndash; Die OneNote-ID des übergeordneten Objekts (Notizbuch oder Gruppe), unter dem das neue Objekt geöffnet werden soll. Wenn der Parameter _BstrPath_ ein absoluter Pfad ist, übergeben Sie können eine leere Zeichenfolge ("") für _BstrRelativeToObjectID_. Alternativ können Sie übergeben die Objekt-ID der Notizbuch oder Gruppe, die sollte enthalten das Objekt (Bereich oder Abschnittsgruppe), das Sie erstellen möchten, und geben Sie den Dateinamen (z. B. section1.one) des Objekts, die Sie unter dem erstellen möchten. das übergeordnete Objekt.  <br/><br/>_pbstrObjectID_ &ndash; (Ausgabeparameter) die Objekt-ID, die OneNote-Notizbuch, Abschnittsgruppe oder Abschnitt, der die **OpenHierarchy** -Methode öffnet zurückgibt. Dieser Parameter ist ein Zeiger auf die Zeichenfolge, in dem die Methode zum Schreiben der ID ab.  <br/><br/>_cftlfNotExist_ &ndash; (Optional) ein Aufzählungswert aus der [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType) -Enumeration. Wenn Sie einen Wert für _CftIfNotExist_übergeben, erstellt die **OpenHierarchy** -Methode den Abschnittsgruppe oder Abschnittsdatei unter dem angegebenen Pfad nur, wenn die Datei nicht bereits vorhanden ist.  <br/> |
   
Wenn Sie eine Gruppe, die nicht in einem geöffneten Notizbuch ist angeben, wird die **OpenHierarchy** -Methode die Abschnittsgruppe als Notizbuch geöffnet. Wenn Sie einen Abschnitt, der nicht in einem geöffneten Notizbuch ist angeben, wird die **OpenHierarchy** -Methode im Abschnitt in der Gruppe der letzte geöffnet Abschnitte-Abschnitt geöffnet. Wenn Sie angeben, einer Gruppe oder eines Abschnitts, der bereits in einem geöffneten Notizbuch ist, passiert nichts, da der Abschnittsgruppe oder eines Abschnitts bereits sowie geöffnet ist. In jedem Fall gibt **OpenHierarchy** die Objekt-ID für den Abschnittsgruppe, Notizbuch oder Abschnitt, die Sie angeben, zurück, sodass Sie es in andere Vorgänge verwenden können. 
  
Sie können auch die **OpenHierarchy** -Methode verwenden, neue Abschnitte, anstatt dies durch das Importieren von XML zu erstellen. 
  
Der folgende Code veranschaulicht, wie Sie die **OpenHierarchy** -Methode im Abschnitt Besprechungen in Arbeit Notizbuch öffnen, und rufen Sie die ID für den Abschnitt. Wenn der Abschnitt nicht bereits vorhanden ist, erstellt es in OneNote in der, den von Ihnen angegebenen Speicherort. 
  
```cs
static void OpenSection()
    {
        String strID;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.OpenHierarchy("C:\\Documents and Settings\\user\\My Documents\\OneNote Notebooks\\Work\\Meetings.one", 
        System.String.Empty, out strID, OneNote.CreateFileType.cftSection);
    }

```

### <a name="deletehierarchy-method"></a>DeleteHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Löscht alle Hierarchy-Objekt (im Abschnittsgruppe, Abschnitt oder Seite) aus der Hierarchie der OneNote-Notizbuch.  <br/> |
|**Syntax** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Parameter** <br/> | _bstrObjectID_ &ndash; Die OneNote-ID des zu löschenden Objekts. Das Objekt kann ein Abschnittsgruppe, Abschnitt oder Seite sein.  <br/><br/>_dateExpectedLastModified_ &ndash; (Optional), das Datum und die Uhrzeit, die das zu löschende Objekt zuletzt glaubt geändert. Wenn Sie einen Wert ungleich NULL für diesen Parameter übergeben, wird mit dem Update OneNote fortgesetzt, nur, wenn der Wert, den Sie weitergeben entspricht, das tatsächliche Datum und Zeit, die das Objekt zuletzt geändert wurde. Übergeben einen Wert für diesen Parameter wird verhindert, dass versehentlich überschrieben werden Benutzer, die seit der letzten des Objekts Änderung bearbeitet.  <br/><br/>_deletePermanently_ &ndash; (Optional) **true** , wenn Inhalte; endgültig löschen **false** zum Verschieben der Inhalts in die OneNote Papierkorb für das entsprechende Notizbuch (Standardeinstellung). Wenn das Notizbuch in OneNote 2007-Format ist, ist keine Papierkorb vorhanden, damit der Inhalt dauerhaft gelöscht wird.  <br/> |
   
### <a name="createnewpage-method"></a>CreateNewPage-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Fügt eine neue Seite in den Abschnitt, den Sie angeben. Die neue Seite wird als der letzten Seite des Abschnitts hinzugefügt.  <br/> |
|**Syntax** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Parameter** <br/> | _bstrSectionID_ &ndash; Eine Zeichenfolge, die OneNote-ID des Abschnitts enthält, in dem Sie die neue Seite erstellen möchten.  <br/><br/>_pbstrPageID_ &ndash; (Ausgabeparameter) ein Zeiger auf die Zeichenfolge, die in dem die Methode die OneNote-ID für die neu erstellte Seite schreibt.  <br/><br/>_npsNewPageStyle_ &ndash; Einen Wert aus der **NewPageStyle** -Enumeration, die das Format der zu erstellenden Seite angibt.  <br/> |
   
Der OneNote-API enthält die **CreateNewPage** -Methode als verwenden können. Erzielen Sie dasselbe Ergebnis, größere Kontrolle über wie die neue Seite in der Hierarchie durch Aufrufen der Methode **UpdateHierarchy** positioniert wird. Die **UpdateHierarchy** -Methode können Sie auch Unterseiten gleichzeitig zu erstellen, wie Sie eine neue Seite erstellen. 
  
### <a name="closenotebook-method"></a>CloseNotebook-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Schließt das angegebene Notizbuch.  <br/> |
|**Syntax** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Parameter** <br/> | _bstrNotebookID_ &ndash; Die OneNote-ID des Notizbuchs zu schließen.  <br/><br/>_erzwingen_ &ndash; (Optional) **true** das Notizbuch schließen, auch wenn es sind Änderungen in das Notizbuch, das vor dem Schließen; OneNote nicht synchronisiert werden kann andernfalls **false** (Standardeinstellung).  <br/> |
   
Die **CloseNotebook** -Methode können Sie das Notizbuch schließen die von das Ihnen angegebenen. Wenn Sie diese Methode aufrufen, OneNote synchronisiert offline-Dateien mit aktuellen Notizbuch Inhalt, bei Bedarf und schließt dann das angegebene Notizbuch. Nach Beendigung der Methode wird das Notizbuch nicht mehr in der Liste der geöffneten Notizbücher auf der OneNote-Benutzeroberfläche (UI) angezeigt. 
  
### <a name="gethierarchyparent-method"></a>GetHierarchyParent-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft die OneNote-ID für das übergeordnete Objekt eines OneNote-Objekts.  <br/> |
|**Syntax** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Parameter** <br/> | _bstrObjectID_ &ndash; Eine Zeichenfolge, die die OneNote-ID des Objekts, von denen enthält, das übergeordnete Objekt zu erhalten soll.  <br/><br/>_pbstrParentID_ &ndash; (Ausgabeparameter) ein Zeiger auf die Zeichenfolge, die in dem die Methode die OneNote-ID des übergeordneten Objekts schreibt.  <br/> |
   
Wenn das OneNote-Objekt besitzt kein übergeordnetes Objekt (beispielsweise, wenn ein Benutzer auf das übergeordnete Element eines Notizbuchs abrufen möchte), wird eine Ausnahme ausgelöst.
  
### <a name="getspeciallocation-method"></a>Methode "getspeciallocation"

|||
|:-----|:-----|
|**Beschreibung** <br/> |Sucht den Pfad zu dem Speicherort, wo bestimmte Sonderzeichen wie Sicherungen, abgelegte Notizen und das Standardnotizbuch in OneNote gespeichert werden.  <br/> |
|**Syntax** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Parameter** <br/> | _slToGet_ &ndash; Eine der [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) -Enumerationswerte, der den Speicherort der Ordner mit Sonderfunktion abzurufenden angibt.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; (Ausgabeparameter) ein Zeiger auf die Zeichenfolge, die in die OneNote den Pfad des Ordners spezielle geschrieben werden soll.  <br/> |
   
Mit dieser Methode können Sie um den Speicherort des Ordners abgelegte Notes auf dem Datenträger zu bestimmen. Dies ist der Ordner, in dem speichert OneNote-Notizen, die erstellt werden, wenn Sie ein Element in OneNote ziehen sowie Hinweise, die direkt aus anderen Programmen (beispielsweise solche, die beim Klicken auf **Senden an OneNote** in Microsoft Outlook oder Microsoft stammen Internet Explorer). 
  
## <a name="page-content-methods"></a>Seiteninhalt-Methoden
<a name="ON14DevRef_Application_PageContent"> </a>

In diesem Abschnitt beschriebenen Methoden können Sie ermitteln, aktualisieren und löschen Sie den Inhalt auf den Seiten in OneNote-Notizbüchern sowie zum Veröffentlichen von Inhalten OneNote.
  
### <a name="getpagecontent-method"></a>GetPageContent-Methode

|||
|:-----|:-----|
|**Beschreibung**|Dient zum Abrufen der gesamte Inhalt der angegebenen Seite (im OneNote-XML-Format).|
|**Syntax**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Parameter**| _bstrPageId_ &ndash; Die OneNote-ID auf der Seite, deren Inhalte, die Sie abrufen möchten.<br/><br/>_pbstrPageXmlOut_ &ndash; (Ausgabeparameter) ein Zeiger auf die Zeichenfolge, die in die OneNote die XML-Ausgabe geschrieben werden soll.<br/><br/>_pageInfoToExport_ &ndash; (Optional) gibt an, ob die **GetPageContent** -Methode Binärinhalt zurückgegeben wird, in den XML-Code und die Base64-codierte eingebettet. Binärer Inhalt kann beispielsweise Bilder und Freihanddaten enthalten. Der Parameter _PageInfoToExport_ gibt zudem, ob Sie die Auswahl in der XML-Code markiert, der die **GetPageContent** -Methode zurückgibt. Ein Aufzählungswert aus der [PageInfo-Klasse](enumerations-onenote-developer-reference.md#odc_PageInfo) -Aufzählung dauert.<br/><br/>_xsSchema_ &ndash; (Optional) die Version des OneNote-XML-Schemas, vom Typ **XMLSchema**, die ausgegeben werden soll. Sie können angeben, ob Sie XML-Schema Version 2013, 2010, 2007, oder die aktuelle Version. <br/><br/>**Hinweis**: Es wird empfohlen Festlegen einer Version von OneNote (beispielsweise **xs2013**) anstelle von **XsCurrent** verwenden oder es leer lassen, da dadurch das Add-in zukünftige Versionen von OneNote entwickelt.           |
   
Standardmäßig werden zur Vermeidung von überzähligen Länge in der XML-Zeichenfolge, die sie zurückgibt, OneNote keine binären Inhalt in den XML-Code eingebettet. Den gleichen Gründen ist es nicht einrichten mit Auswahl Attribute der aktuellen Auswahl markiert. Binäre Objekte umfassen eine OneNote-ID in ihre Tags an. Wenn ein binäres Objekt erhalten möchten, rufen Sie die Methode **GetBinaryPageContent** und übergeben sie die OneNote-ID, die Sie aus der **GetPageContent** -Methode abrufen. Verwenden Sie die **GetPageContent** -Methode, wenn Sie die binären Daten nicht sofort benötigen. 
  
### <a name="updatepagecontent-method"></a>UpdatePageContent-Methode

|||
|:-----|:-----|
|**Beschreibung**|Aktualisiert oder ändert die Inhalte auf der Seite.|
|**Syntax**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Parameter**| _bstrPageChangesXmlIn_ &ndash; Eine Zeichenfolge, die OneNote-XML-Code enthält, der die Änderungen enthält, die Sie zur Seite machen möchten.<br/><br/>_dateExpectedLastModified_ &ndash; (Optional) Datum und Uhrzeit, die Sie vorstellen die Seite zu aktualisierende zuletzt geändert. Wenn Sie einen Wert ungleich NULL für diesen Parameter übergeben, wird nur, wenn der Wert, den Sie weitergeben entspricht, das tatsächliche Datum und Uhrzeit der letzten Änderung die Seite mit dem Update OneNote fortgesetzt. Übergeben einen Wert für diesen Parameter wird verhindert, dass versehentlich überschrieben bearbeitet Benutzer, die seit des letzten Mal, das die Seite geändert wurde.<br/><br/>_xsSchema_ &ndash; (Optional) die Version des OneNote-XML-Schemas, vom Typ **XMLSchema**, die ausgegeben werden soll. Sie können angeben, ob Sie XML Schema-Version 2013, 2010, 2007, oder die aktuelle Version. <br/><br/>**Hinweis**: Es wird empfohlen Festlegen einer Version von OneNote (beispielsweise **xs2013**) anstelle von **XsCurrent** verwenden oder es leer lassen, da dadurch das Add-in zukünftige Versionen von OneNote entwickelt.<br/><br/>_erzwingen_ (Optional) **true** , wenn Inhalt der Seite aktualisieren, auch wenn unbekannte Daten auf der Seite einer zukünftigen Version von OneNote vorhanden ist; andernfalls **false** (Standardeinstellung). |
   
Sie können diese Methode verwenden, um der Seite auf verschiedene Weise ändern. Beispielsweise können Sie die **UpdatePageContent** -Methode verwenden, um eine Gliederung zu einer Seite hinzufügen, ändern Sie den Inhalt einer Gliederung, Hinzufügen von Bildern, Freihand hinzufügen, Verschieben von Inhalten oder Ändern von Text in Pfade. 
  
Sie können eine genauere beispielsweise die **GetPageContent** -Methode exportieren eine vorhandene Seite, einige Änderungen an den XML-Code für die Seite vornehmen, und klicken Sie dann die **UpdatePageContent** -Methode verwenden, um die gesamte Seite erneut importieren verwenden. Oder Sie können diese Methode verwenden, um neue Page-Objekte wie Bilder, an das Ende einer bereits vorhandenen Seite hinzufügen. 
  
Die einzigen Objekte, die Sie in der XML-Code hinzufügen müssen, die Sie an die **UpdatePageContent** -Methode übergeben werden Seitenebenen-Objekte (wie Gliederungen Bilder auf der Seite oder Druckfarbe auf der Seite), die geändert wurden. Diese Methode nicht ändern oder Entfernen von Seitenebenen-Objekten, die Sie nicht in der _BstrPageChangesXmlIn_ -Parameter angeben. Die Methode ersetzt vollständig Seitenebenen-Objekte, wie Pfade, die mit den IDs der Objekte übereinstimmen, die Sie weitergeben. Daher müssen Sie alle Objekte der Seitenebene vollständig angeben, in Ihrem Code, einschließlich ihrer vorhandenen Inhalt und die Änderungen, die Sie für diese machen möchten. 
  
Wenn die Seite eine Gliederung und ein Hintergrundbild für die Seite enthält, können Sie beispielsweise ersetzen die Gliederung und das Bild vollständig angeben der Gliederung in den XML-Code mit der ID des vorhandenen Gliederung und nicht das Bild im Code einschließlich unverändert lassen. Da die überarbeitete Gliederung, die Sie vollständig in den Code eingeben die vorhandene Gliederung ersetzt, müssen Sie den gesamten Inhalt der Gliederung einbeziehen.
  
Darüber hinaus ändert die **UpdatePageContent** -Methode nur Elementeigenschaften, die Sie in der _BstrPageChangesXmlIn_ -Parameter angeben. Wenn Sie einige, aber nicht alle Eigenschaften des Elements **PageSettings** angeben, bleiben die Eigenschaften, die Sie nicht angeben, z. B. unverändert. 
  
Im folgenden Beispiel wird gezeigt, wie Sie die **UpdatePageContent** -Methode zum Ändern des Titels einer Seite und Hinzufügen von Beispieltext zur Seite. Ersetzen Sie vor Ausführung des Codes, eine gültige Seiten-ID für die Seiten-ID im Code dargestellt, damit der Code auf Ihrem Computer funktioniert. Sie können die Seiten-ID für eine Seite abrufen, indem Sie mithilfe der Methode **GetHierarchy** und Untersuchen der Ausgabe. 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"http://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
            ID=\"{3428B7BB-EF39-4B9C-A167-3FAE20630C37}{1}{B0}\">" +
            "    <one:PageSettings RTL=\"false\" color=\"automatic\">" +
            "        <one:PageSize>" +
            "            <one:Automatic/>" +
            "        </one:PageSize>" +
            "        <one:RuleLines visible=\"false\"/>" +
            "    </one:PageSettings>" +
            "    <one:Title style=\"font-family:Calibri;
                 font-size:17.0pt\" lang=\"en-US\">" +
            "        <one:OE alignment=\"left\">" +
            "            <one:T>" +
            "                <![CDATA[My Sample Page]]>" +
            "            </one:T>" +
            "        </one:OE>" +
            "    </one:Title>" +
            "    <one:Outline >" +
            "        <one:Position x=\"120\" y=\"160\"/>" +
            "        <one:Size width=\"120\" height=\"15\"/>" +
            "        <one:OEChildren>" +
            "            <one:OE alignment=\"left\">" +
            "                <one:T>" +
            "                    <![CDATA[Sample Text]]>" +
            "                </one:T>" +
            "            </one:OE>" +
            "        </one:OEChildren>" +
            "    </one:Outline>" +
            "</one:Page>";
        // Update the page content.
        onApplication.UpdatePageContent(strImportXML, System.DateTime.MinValue);
    }

```

### <a name="getbinarypagecontent-method"></a>GetBinaryPageContent-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Gibt ein binäres Objekt wie Freihand oder Bilder auf einer OneNote-Seite als Base-64-codierte Zeichenfolge zurück.  <br/> |
|**Syntax** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Parameter** <br/> | _bstrPageID_ &ndash; Die OneNote-ID der Seite, die binäre abzurufenden Objekts enthält.  <br/><br/>_bstrCallBackID_ &ndash; Die OneNote-ID des binary-Objekts abrufen möchten. Diese ID, bezeichnet als ein **CallbackID**ist in den OneNote-XML-Code für eine Seite, die von der **GetPageContent** -Methode zurückgegeben.  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; (Ausgabeparameter) ein Zeiger auf eine Zeichenfolge, die in die OneNote das binäre Objekt als Base-64-codierte Zeichenfolge schreibt.  <br/> |
   
### <a name="deletepagecontent-method"></a>DeletePageContent-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Löscht ein Objekt &ndash; wie etwa eine **Gliederung**, **Freihand**oder **Bild** -Objekt aus einer Seite.  <br/> |
|**Syntax** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Parameter** <br/> | _bstrPageID_ &ndash; Die OneNote-ID der Seite, die zu löschenden Objekts enthält.  <br/><br/>_bstrObjectID_ &ndash; Die OneNote-ID des Objekts, das Sie löschen möchten.  <br/><br/>_dateExpectedLastModified_ &ndash; (Optional), die die Seite, die Inhalt enthält zu löschende zuletzt glaubt Datum und Uhrzeit geändert. Wenn Sie einen Wert ungleich NULL für diesen Parameter übergeben, wird nur, wenn der Wert, den Sie weitergeben entspricht, das tatsächliche Datum und Uhrzeit der letzten Änderung die Seite OneNote der Löschvorgang fortgesetzt. Übergeben einen Wert für diesen Parameter verhindert, dass versehentlich überschreiben bearbeiteten Benutzer seit dem letzten Mal, das die Seite geändert wurde.  <br/><br/>_erzwingen_ &ndash; (Optional) **true** , wenn der Inhalt der Seite aktualisieren, auch wenn unbekannte Daten auf der Seite einer zukünftigen Version von OneNote; vorhanden ist andernfalls **false** (Standardeinstellung).  <br/> |
   
### <a name="publish-method"></a>Publish-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Exportiert die angegebene Seite in eine Datei in einem beliebigen Format, die OneNote unterstützt.  <br/> |
|**Syntax** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID der zu exportierenden Hierarchie.  <br/><br/>_bstrTargetFilePath_ &ndash; Den absoluten Pfad zu dem Speicherort, in der Sie die resultierende Ausgabedatei speichern möchten. Die Datei, die von die Ihnen angegebenen muss eine sein, die an diesem Speicherort nicht bereits vorhanden ist.  <br/><br/>_pfPublishFormat_ &ndash; Eine der [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) -Enumerationswerte, der das Format angibt, in dem die veröffentlichte Seite (z. B., MTHML, PDF und usw.) werden soll.  <br/><br/>_bstrCLSIDofExporter_ &ndash; Die Klasse-ID (CLSID) des einer registrierten COM-Anwendung, die Microsoft Windows exportieren kann Erweiterte Metadateien (EMF). Die COM-Anwendung muss **IMsoDocExporter** -Schnittstelle implementieren. Dieser Parameter wird angegeben, um die Drittentwickler ihre eigenen Code zum Veröffentlichen von OneNote-Inhalt in einem benutzerdefinierten Format schreiben zulassen. Weitere Informationen zu **IMsoDocExporter** -Schnittstelle finden Sie unter [Extending the Office 2007 Fixed-Format Export Feature](http://msdn.microsoft.com/en-us/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
OneNote unterstützt derzeit die folgenden Dateiformate:
  
- MHTML-Dateien (MHT)
- Adobe Acrobat PDF-Dateien (PDF)
- XML Paper Specification (XPS)-Dateien (XML Paper Specification)
- OneNote 2013, 2010 oder 2007-Dateien (One)
- OneNote-Paket-Dateien (ONEPKG)
- Microsoft Word-Dokumente (DOC oder DOCX)
- Erweiterte Microsoft Windows-Metadateien (EMF)
- HTML-Dateien (HTML)
    
Diese Methode erzeugt genau die gleichen Ergebnisse, indem Sie auf **Veröffentlichen** auf der Benutzeroberfläche und das Format angeben, erhalten würden. 
  
## <a name="navigation-methods"></a>Navigationsmethoden
<a name="ON14DevRef_Application_Navigation"> </a>

In diesem Abschnitt beschriebenen Methoden können Sie suchen, navigieren zu, und Verknüpfen mit OneNote-Notizbüchern, Abschnittsgruppen, Abschnitte, Seiten und Page-Objekte.
  
### <a name="navigateto-method"></a>NavigateTo (Methode)

|||
|:-----|:-----|
|**Beschreibung** <br/> |Navigiert zu dem angegebenen Objekt (z. B. Abschnitte, Seiten und **Gliederung** Schemaelemente in Seiten).  <br/> |
|**Syntax** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameter** <br/> | _bstrHierarchyObjectID_ &ndash; Die OneNote-ID des Objekts in der OneNote-Hierarchie zu navigieren soll.  <br/><br/>_bstrObjectID_ &ndash; Die OneNote-ID für das Objekt, auf der OneNote-Seite zu dem navigiert werden soll.  <br/><br/>_fNewWindow_ &ndash; (Optional) **true** , wenn angegebene Objekt in einem neuen OneNote-Fenster öffnen. **"false"** wird ein neues OneNote-Fenster im nicht nicht geöffnet, falls geöffnet ist.  <br/> |
   
### <a name="navigatetourl-method"></a>NavigateToUrl-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Wenn einen Link OneNote übergeben (Onenote: / /), wird das OneNote-Fenster auf den entsprechenden Speicherort in OneNote geöffnet. Wenn der Link externe an OneNote (beispielsweise http:// oder file:///) ist, wird das Sicherheitsdialogfeld angezeigt. Bei Kündigung OneNote versucht, öffnen Sie den Link, und ein **HResult.hrObjectDoesNotExist** -Fehler zurückgegeben.  <br/> |
|**Syntax** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameter** <br/> | _bstrUrl_ &ndash; Eine Zeichenfolge, die angibt, wo Sie zu navigieren. Dies könnte ein OneNote-Link oder eine beliebige andere URL, beispielsweise eine Webadresse Link oder im Netzwerk.  <br/><br/>_fNewWindow_ &ndash; (Optional) **true** , wenn die angegebene URL in einem neuen OneNote-Fenster geöffnet. **"false"** wird ein neues OneNote-Fenster im nicht nicht geöffnet, falls geöffnet ist.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>GetHyperLinkToObject-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft einen OneNote Hyperlink zu der angegebenen Notizbuch, Abschnittsgruppe, Abschnitt, Seite oder Page-Objekt ab.  <br/> |
|**Syntax** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID für das Notizbuch, Abschnittsgruppe, Abschnitt oder Seite für die Sie einen Hyperlink erstellen möchten.  <br/><br/>_bstrPageContentObjectID_ &ndash; (Optional) die OneNote-ID für das Objekt auf der Seite für die Sie einen Hyperlink erstellen möchten. Das Objekt kann beispielsweise eine Gliederung oder eine **Gliederung** Element sein. Wenn Sie übergeben Sie eine leere Zeichenfolge (""), der zurückgegebene Link verweist auf das Notizbuch, Abschnittsgruppe Abschnitt oder Seite, die Sie in der _BstrHierarchyID_ -Parameter angegeben. Wenn Sie eine nicht leere Zeichenfolge für den _BstrPageContentObjectID_ -Parameter übergeben, muss der Parameter _BstrHierarchyID_ einen Verweis auf die Seite, die das angegebene Objekt enthält.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (Ausgabeparameter) ein Zeiger auf eine Zeichenfolge, die in dem die **GetHyperlinkToObject** -Methode den Hyperlinktext Ausgabe schreibt.  <br/> |
   
Wenn Sie versuchen, um den resultierenden Link zu navigieren, OneNote wird geöffnet und zeigt das angegebene Objekt im Browser.
  
### <a name="getwebhyperlinktoobject-method"></a>GetWebHyperlinktoObject-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Gibt einen Hyperlink auf ein Objekt, das in der OneNote-WebClient öffnet.  <br/> |
|**Syntax** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID für das Notizbuch im Abschnitt Gruppe, Abschnitt oder Seite für die Sie einen Webhyperlink möchten.  <br/><br/>_bstrPageContentObjectID_ &ndash; (Optional) die OneNote-ID für das Objekt auf der Seite für die Sie einen Hyperlink erstellen möchten. Das Objekt kann beispielsweise eine Gliederung oder eine **Gliederung** Element sein. Wenn Sie übergeben Sie eine leere Zeichenfolge (""), der zurückgegebene Link verweist auf das Notizbuch, Abschnittsgruppe Abschnitt oder Seite, die Sie in der _BstrHierarchyID_ -Parameter angegeben. Wenn Sie eine nicht leere Zeichenfolge für den _BstrPageContentObjectID_ -Parameter übergeben, muss der Parameter _BstrHierarchyID_ einen Verweis auf die Seite, die das angegebene Objekt enthält.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (Ausgabeparameter) ein Zeiger auf eine Zeichenfolge, die in dem die **GetWebHyperlinkToObject** -Methode den Hyperlinktext Ausgabe schreibt. Wenn ein Web-Hyperlink für das Notizbuch erstellt werden kann, wird ein Nullwert zurückgegeben.  <br/> |
   
### <a name="findpages-method"></a>FindPages-Methode

|||
|:-----|:-----|
|**Beschreibung**|Gibt eine Liste von Seiten, die der angegebenen Abfrage entsprechen.|
|**Syntax**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameter**| _bstrStartNodeID_ &ndash; (Stamm, Notizbuch, Abschnittsgruppe oder Abschnitt) den Knoten Unterschreitung die Suche nach Inhalten. Dieser Parameter legt den Gültigkeitsbereich für die Suche.<br/><br/>_bstrSearchString_ &ndash; Die zu suchende Zeichenfolge. Übergeben Sie genau die gleiche Zeichenfolge, die Sie in das Suchfeld in der OneNote-UI eingeben möchten. Sie können bitweise Operatoren wie **und** und **oder**, der vollständig in Großbuchstaben sein muss.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Ausgabeparameter) ein Zeiger auf eine Zeichenfolge, die in die OneNote die Ausgabe XML-Zeichenfolge geschrieben werden soll. Die resultierende XML-Zeichenfolge enthält die Notebook-Hierarchie im Stammverzeichnis nach unten zur und einschließlich Seiten, die die zu suchende Zeichenfolge entsprechen. Beispielsweise wird die **FindPages** -Methode nicht Abschnitten aufgelistet, die keine Übereinstimmung Seite in der Hierarchie haben. Wenn nur eine Seite in einem einzigen Abschnitt mit der Zeichenfolge übereinstimmt, enthält die zurückgegebene Hierarchie ebenfalls den Pfad für diese Abschnitte und Seiten, aber für keine andere Teile der Hierarchie Notizbuch.<br/><br/>_fIncludeUnindexedPages_ &ndash; (Optional) **true,** um Seiten zu suchen, die nicht von der Windows-Suche indiziert wurden anderenfalls **false**.<br/><br/>_fDisplay_ &ndash; (Optional) **true** , wenn auch für die Suche in der Benutzeroberfläche für den Benutzer ausführen, so als würde der Benutzer es selbst eingegeben hätten. **"false"** zum Ausführen der Abfrage ohne Änderung der Benutzeroberfläche (Standardeinstellung).<br/><br/>_xsSchema_ &ndash; (Optional) der OneNote-Schemaversion von der Zeichenfolge _PbstrHierarchyXmlOut_. Dieser optionale Wert wird verwendet, die Version des OneNote-XML-Schemas an, die _PbstrHierarchyXmlOut_ -Zeichenfolge enthält. Wenn dieser Wert nicht angegeben ist, wird OneNote wird vorausgesetzt, dass der XML-Code im Schema Version _XsCurrent_ist. <br/><br/>**Hinweis**: Es wird empfohlen Festlegen einer Version von OneNote (beispielsweise **xs2013**) anstelle von **XsCurrent** verwenden oder es leer lassen, da dadurch das Add-in zukünftige Versionen von OneNote entwickelt.           |
   
 **FindPages** funktioniert nur, wenn Sie Microsoft Search 3.0 oder 4.0 auf Ihrem Computer installiert haben. Windows Vista und Windows 7 enthalten diese Komponente. Wenn Sie eine frühere Version von Windows ausgeführt werden, müssen Sie [Windows Search](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) für **FindPages** zu installieren. 
  
### <a name="findmeta-method"></a>FindMeta-Methode

|||
|:-----|:-----|
|**Beschreibung**|Gibt eine Liste von OneNote-Objekten, die Metadaten enthalten, die mit den angegebenen Abfragebegriff übereinstimmt.|
|**Syntax**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameter**| _bstrStartNodeID_ &ndash; (Stamm, Notizbuch, Abschnittsgruppe oder Abschnitt) den Knoten Unterschreitung die Suche nach Inhalten. Dieser Parameter legt den Gültigkeitsbereich für die Suche.<br/><br/>_bstrSearchStringName_ &ndash; Die zu suchende Zeichenfolge. Übergeben Sie in einem beliebigen Teil des Metadatennamens. Wenn Sie eine leere Zeichenfolge oder einen null-Wert übergeben, werden alle Objekte, denen Metadaten der Abfrage übereinstimmen.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Ausgabeparameter) ein Zeiger auf eine Zeichenfolge, die in die OneNote die Ausgabe XML-Zeichenfolge geschrieben werden soll. Die resultierende XML-Zeichenfolge enthält die Notebook-Hierarchie im Stammverzeichnis nach unten zur und einschließlich Seiten, die die zu suchende Zeichenfolge entsprechen. Beispielsweise wird die **FindPages** -Methode nicht Abschnitten aufgelistet, die keine Übereinstimmung Seite in der Hierarchie haben. Wenn nur eine Seite in einem einzigen Abschnitt mit der Zeichenfolge übereinstimmt, enthält die zurückgegebene Hierarchie ebenfalls den Pfad für diese Abschnitte und Seiten, aber für keine andere Teile der Hierarchie Notizbuch.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (Optional) **true,** um Seiten zu suchen, die nicht von der Windows-Suche indiziert wurden anderenfalls **false**.<br/><br/>_xsSchema_ &ndash; (Optional) der OneNote-Schemaversion von der Zeichenfolge _PbstrHierarchyXmlOut_. Dieser optionale Wert wird verwendet, die Version des OneNote-XML-Schemas an, die _PbstrHierarchyXmlOut_ -Zeichenfolge enthält. Wenn dieser Wert nicht angegeben ist, wird OneNote wird vorausgesetzt, dass der XML-Code im Schema Version _XsCurrent_ist. <br/><br/>**Hinweis**: Es wird empfohlen Festlegen einer Version von OneNote (beispielsweise **xs2013**) anstelle von **XsCurrent** verwenden oder es leer lassen, da dadurch das Add-in zukünftige Versionen von OneNote entwickelt.           |
   
**FindMeta** funktioniert nur, wenn Sie Microsoft Windows Search 3.0 oder 4.0 auf Ihrem Computer installiert haben. Windows Vista und Windows 7 enthalten diese Komponente. Wenn Sie eine frühere Version von Windows ausgeführt werden, müssen Sie [Windows Search](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) für **FindMeta** zu installieren. 
  
## <a name="functional-methods"></a>Funktionale Methoden
<a name="ON14DevRef_Application_Functional"> </a>

In diesem Abschnitt beschriebenen Methoden können Sie bestimmte Aktionen ausführen, oder legen Sie die Parameter in der OneNote-Anwendung.
  
### <a name="mergefiles-method"></a>MergeFiles-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht Benutzern das Zusammenführen von Änderungen für dieselbe Datei zu einem Dokument. Damit die Dateien auf die gleiche berücksichtigt werden müssen sie die gleiche OneNote-ID aufweisen.  <br/> |
|**Syntax** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Parameter** <br/> | _bstrBaseFile_ &ndash; Die Pfadzeichenfolge auf den Speicherort der One von der Anfangszustand der Datei.  <br/><br/>_bstrClientFile_ &ndash; Die Pfadzeichenfolge auf den Speicherort der One des zweiten Satzes von Änderungen an der zugrunde liegenden Datei nach dem Ändern der Server mit der Basis zusammengeführt werden verbunden werden soll.  <br/><br/>_bstrServerFile_ &ndash; Die Pfadzeichenfolge auf den Speicherort der One der ersten Reihe von Änderungen an der Basisdatei verbunden werden soll.  <br/><br/>_bstrTargetFile_ &ndash; Die Pfadzeichenfolge auf den Speicherort der Datei mit den verbundenen Änderungen One.  <br/> |
   
Die **MergeFiles** -Methode wurde für mobile Szenarien für die direkte Verwendung in der mehrere Versionen einer OneNote-Datei vorhanden sein können. 
  
### <a name="mergesections-method"></a>MergeSections-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Führt den Inhalt von einem Bereich in ein anderes in OneNote zusammen.  <br/> |
|**Syntax** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Parameter** <br/> | _bstrSectionSourceId_ &ndash; Die OneNote-ID des Abschnitts zusammengeführt werden sollen.  <br/><br/>_bstrSectionDestinationId_ &ndash; Die OneNote-ID des Abschnitts zusammengeführt werden sollen. In diesem Zielabschnitt wird im Abschnitt Quelle zusammengeführt werden.  <br/> |
   
Diese Methode führt die gleiche Operation wie das **Zusammenführen in einen anderen Abschnitt** -Feature, das angezeigt wird, wenn Sie einen Abschnitt mit der rechten Maustaste. 
  
### <a name="quickfiling-method"></a>QuickFiling-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Gibt eine Instanz des Dialogfelds [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog) , die verwendet werden kann, um eine Position innerhalb der OneNote-Hierarchie auszuwählen.  <br/> |
|**Syntax** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>SyncHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Erzwingt OneNote das angegebene Objekt mit der Quelldatei auf dem Datenträger zu synchronisieren.  <br/> |
|**Syntax** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID des Objekts synchronisiert werden.  <br/> |
   
### <a name="setfilinglocation-method"></a>SetFilingLocation-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht Benutzern, um anzugeben, wo und wie bestimmte Arten von Inhalten in OneNote eingereicht werden sollte.  <br/> |
|**Syntax** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Parameter** <br/> | _flToSet_ &ndash; Der Objekttyp des Speicherorts für schnelle Ablage festgelegt.  <br/><br/>_fltToSet_ &ndash; Der Speicherort, an dem Sie den Typ der Datei.  <br/><br/>_bstrFilingSectionID_ &ndash; Die OneNote-ID des Abschnitts oder Seite, an welcher Stelle Sie festlegen möchten. Wenn dies nicht anwendbar ist, kann der Benutzer in Null oder eine leere Zeichenfolge übergeben.  <br/> |
   
Die Arten von Inhalten, die archiviert werden kann, zählen Outlook-Elemente und Webnotizen von Internet Explorer, die über den Befehl **Senden an OneNote** in jeder Anwendung in OneNote importiert werden. Der Speicherort ablegen von Elementen, die in OneNote gedruckt werden, kann auch mit dieser Methode festgelegt werden. 
  
## <a name="properties"></a>Eigenschaften
<a name="ON14DevRef_Application_Properties"> </a>

In diesem Abschnitt werden die Eigenschaften der **Application** -Schnittstelle beschrieben. 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**Windows** <br/> |Ermöglicht Benutzern den Zugriff auf die geöffnete OneNote-Fenster. Diese Eigenschaft ermöglicht Benutzern bestimmte Fenstereigenschaften zu durchlaufen, die Gruppe von OneNote-Fenster. Weitere Informationen finden Sie unter [Windows-Schnittstellen](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Gibt die **COMAddIns** -Auflistung für OneNote. Diese Auflistung enthält alle COM-add-Ins, die an OneNote verfügbar sind. Die **Count** -Eigenschaft der **COMAddins** -Auflistung gibt die Anzahl der verfügbaren COM-add-ins zurück. Weitere Informationen finden Sie unter der [COMAddIns](http://msdn.microsoft.com/en-us/library/office/ff865489.aspx) -Objekt.  <br/> |
|**LanguageSettings** <br/> |Können Sie einige APIs, um die common Language-Einstellungen von OneNote ändern zugreifen.  <br/> |
   
## <a name="events"></a>Ereignisse
<a name="ON14DevRef_Application_Events"> </a>

In diesem Abschnitt werden die Ereignisse der Application-Schnittstelle beschrieben.
  
> [!CAUTION]
> Ereignisse können derzeit in verwaltetem Code hinzugefügt werden. 
  
### <a name="onnavigate-event"></a>OnNavigate-Ereignis

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht einem Benutzer zuweisen eine Funktion aufgerufen werden, wenn die OneNote UI Weg von der aktuellen Position OneNote navigiert wird.  <br/> |
|**Syntax** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>OnHierarchyChange-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht einem Benutzer das Zuweisen einer Funktion aufgerufen werden jedes Mal, wenn die Änderungen der OneNote-Hierarchie (beispielsweise das Hinzufügen oder Löschen von Seiten oder Abschnitte verschieben). Hierarchie Änderungen gestapelter werden werden, wenn mehrere Änderungen fast gleichzeitig oder auftreten, OneNote das Ereignis einmal auslöst.  <br/> |
|**Syntax** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Parameter** <br/> | _bstrActivePageID_ &ndash; Übergibt die OneNote-ID der aktiven Seite.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [OneNote-Entwicklerreferenz](onenote-developer-reference.md)

