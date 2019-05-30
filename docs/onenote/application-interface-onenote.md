---
title: Anwendungsschnittstelle (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'Die Anwendungsschnittstelle umfasst Methoden, mit denen OneNote-Informationen und -Inhalte abgerufen, bearbeitet und aktualisiert werden können. Die Methoden sind in vier allgemeine Kategorien unterteilt:'
localization_priority: Priority
ms.openlocfilehash: 295db4fcb64541ccf461fbd8d48dc19b89e6b1f8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537822"
---
# <a name="application-interface-onenote"></a>Anwendungsschnittstelle (OneNote)

Die **Anwendungsschnittstelle** umfasst Methoden, mit denen OneNote-Informationen und -Inhalte abgerufen, bearbeitet und aktualisiert werden können. Die Methoden sind in vier allgemeine Kategorien unterteilt: 
  
- **Notizbuchstruktur** &ndash; Methoden zum Arbeiten mit Notizbuchstrukturen, einschließlich derjenigen zum Entdecken, Öffnen, Ändern, Schließen und Löschen von Notizbüchern, Abschnittsgruppen und Abschnitten. 
    
- **Seiteninhalt** &ndash; Methoden zum Arbeiten mit Seiten und Seiteninhalten, einschließlich derjenigen zum Entdecken, Ändern, Speichern und Löschen von Seiteninhalten. Seiteninhalte umfassen binäre Objekte wie Freihand und Bilder sowie Textobjekte wie Gliederungen. 
    
- **Navigation** &ndash; Methoden zum Suchen nach, Verknüpfen mit und Navigieren zu Seiten und Objekten. 
    
- **Funktional** &ndash; Alle anderen Methoden, mit denen bestimmte Aktionen ausgeführt oder Parameter in OneNote festgelegt werden. 
    
Außerdem umfasst die **Anwendungsschnittstelle** eine Reihe von *Eigenschaften* und *Ereignissen*. 
  
## <a name="notebook-structure-methods"></a>Notizbuchstruktur-Methoden
<a name="ON14DevRef_Application_NotebookStructure"> </a>

Mit den in diesem Abschnitt beschriebenen Methoden können Sie OneNote-Notizbücher, Abschnittsgruppen und Abschnitte entdecken, öffnen, ändern, schließen und löschen.
  
### <a name="gethierarchy-method"></a>GetHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft die Hierarchiestruktur der Notizbuchknoten ab, beginnend mit dem von Ihnen angegebenen Knoten (alle Notizbücher oder ein einzelnes Notizbuch, eine Abschnittsgruppe oder ein Abschnitt) bis hinunter zu allen Nachfolgern auf der von Ihnen angegebenen Ebene.  <br/> |
|**Syntax** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Parameter** <br/> | _bstrStartNodeID_ &ndash; Der Knoten (Notizbuch, Abschnittsgruppe oder Abschnitt), dessen Nachfolger gewünscht sind. Wenn Sie eine NULL-Zeichenfolge ("") übergeben, ruft die Methode alle Knoten unterhalb des Stammknotens ab (d. h. alle Notizbücher, Abschnittsgruppen und Abschnitte). Wenn Sie ein Notizbuch, eine Abschnittsgruppe oder einen Abschnittsknoten angeben, ruft die Methode nur die Nachfolger dieses Knotens ab.  <br/><br/>_hsScope_ &ndash; Die gewünschte niedrigste Knotenebene von Nachfolgern. Wenn Sie beispielsweise Seiten angeben, ruft die Methode alle Knoten bis nach unten zur Seitenebene ab. Wenn Sie Abschnitte angeben, ruft die Methode nur Abschnittsknoten unterhalb des Notizbuchs ab. Weitere Informationen finden Sie unter der Enumeration **HierarchyScope** im Thema [Enumerations](enumerations-onenote-developer-reference.md#odc_HierarchyScope).  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die OneNote die XML-Ausgabe schreiben soll.  <br/><br/>_xsSchema_ &ndash; (Optional) Die Version des OneNote-XML-Schemas des Typs **XMLSchema**, das ausgegeben werden soll. Sie können angeben, ob Sie die XML-Schemaversion 2013, 2010, 2007 oder die aktuelle Version wünschen.  <br/><br/>**HINWEIS**: Wir empfehlen Ihnen, eine Version von OneNote anzugeben (z. B. **xs2013**), statt **xsCurrent** zu verwenden oder es leer zu lassen, da das Add-In so mit zukünftigen Versionen von OneNote arbeiten kann.           |
   
Die GetHierarchy-Methode gibt eine Zeichenfolge standardmäßig im OneNote 2013-XML-Format zurück. Sie können aber auch die bevorzugte XML-Schemaversion mithilfe des optionalen Parameters _xsSchema_ festlegen. 
  
Abhängig von den übergebenen Parametern kann die **GetHierarchy**-Methode verschiedene Listen zurückgeben (z. B. alle Notizbücher, alle Abschnitte in allen Notizbüchern, alle Seiten in einem bestimmten Abschnitt oder alle Seiten in einem bestimmten Notizbuch). Für jeden Knoten stellt die zurückgegebene XML-Zeichenfolge Eigenschaften bereit (z. B. den Abschnitts- oder Seitentitel, die ID und die Uhrzeit der letzten Änderung). 
  
Nicht alle Kombinationen aus Startknoten und Bereich sind gültig. Wenn Sie z. B. den Startknoten eines Abschnitts und einen Notizbuchbereich angeben, gibt **GetHierarchy** ein Null-Ergebnis zurück, da ein Notizbuch höher in der Knotenhierarchie steht als ein Abschnitt. 
  
Das folgende C#-Beispiel veranschaulicht, wie die **GetHierarchy**-Methode verwendet wird, um die gesamte OneNote-Hierarchie abzurufen, einschließlich aller Notizbücher bis auf Seitenebene. Die Ausgabezeichenfolge wird in die Zwischenablage kopiert, von wo aus Sie die Zeichenfolge zur Überprüfung in einen Texteditor einfügen können. 
  
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
|**Beschreibung**|Ändert oder aktualisiert die Hierarchie der Notizbücher. Sie können z. B. Abschnitte oder Abschnittsgruppen in ein Notizbuch einfügen, ein neues Notizbuch hinzufügen, Abschnitte in einem Notizbuch verschieben, den Namen eines Abschnitts ändern, Seiten zu einem Abschnitt hinzufügen oder die Reihenfolge von Seiten in einem Abschnitt ändern.|
|**Syntax**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Parameter**| _bstrChangesXmlIn_ &ndash; Eine Zeichenfolge, die OneNote XML-Code enthält, der die vorzunehmenden Hierarchie-Änderungen angibt. Wenn Sie beispielsweise einen neuen Abschnitt einfügen möchten, können Sie ein **Section**-Element in die XML-Zeichenfolge einfügen, um anzugeben, wo der neue Abschnitt eingefügt werden soll. Wenn Sie den Namen eines vorhandenen Abschnitts ändern möchten, können Sie auch die gleiche Abschnitt-ID beibehalten und das **name**-Attribut im XML-Code ändern.<br/><br/>_xsSchema_ &ndash; (Optional) Die OneNote-Schemaversion der Zeichenfolge _bstrChangesXmln_. Dieser optionale Wert wird verwendet, um die Version des OneNote-XML-Schemas anzugeben, im dem sich die _bstrChangesXmlIn_-Zeichenfolge befindet. Wenn dieser Wert nicht angegeben ist, setzt OneNote voraus, dass sich die XML in der Schemaversion _xsCurrent_ befindet. <br/><br/>**HINWEIS**: Wir empfehlen Ihnen, eine Version von OneNote anzugeben (z. B. **xs2013**), statt **xsCurrent** zu verwenden oder es leer zu lassen, da das Add-In so mit zukünftigen Versionen von OneNote arbeiten kann.           |
   
Wenn Sie nur eine partielle OneNote XML-Zeichenfolge für den _bstrChangesXmlIn_-Parameter weitergeben, versucht OneNote, die gewünschten Änderungen abzuleiten. Wenn Sie z. B. ein **Notizbuch**-Element einschließen, das nur einen Abschnitt enthält, fügt OneNote den Abschnitt nach einem vorhandenen Abschnitt ein. Wenn der Vorgang, den Sie angeben, nicht eindeutig ist, kann das Ergebnis jedoch schwer zu ermitteln sein. Wenn ein vorhandenes Notizbuch z. B. vier Abschnitte enthält und die übergebene XML-Zeichenfolge das Notizbuch und nur den vierten und ersten Abschnitt enthält (in dieser Reihenfolge), platziert OneNote möglicherweise den zweiten und dritten Abschnitt vor dem vierten oder nach dem ersten Abschnitt. 
  
Sie können nicht die **UpdateHierarchy**-Methode verwenden, um einen Teil eines Notizbuchs zu löschen. Dies bedeutet, dass bei der Übergabe einer XML-Zeichenfolge, die nur einen Teil einer vorhandenen Hierarchie enthält, keine Abschnitte gelöscht werden, die nicht in der Zeichenfolge enthalten sind. Verwenden Sie zum Löschen eines Teils einer Hierarchie die **DeleteHierarchy**-Methode. 
  
Der folgende C#-Code zeigt eine Möglichkeit für die Verwendung der **UpdateHierarchy**-Methode, um die OneNote-Hierarchie zu ändern, indem Sie den Namen eines vorhandenen Abschnitts ändern. XML-Code wird aus einer Beispieldatei mit dem Namen ChangeSectionName.xml im Stammverzeichnis von Laufwerk C gelesen, der dann in ein XML-Dokument geladen wird. Die XML-Struktur dieses Dokuments wird dann an die Methode übergeben. 
  
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

Der folgende XML-Code ist ein Auszug aus der ChangeSectionName.xml-Datei, die der vorherige C#-Code an die Methode übergibt. Wenn der XML-Code an die **UpdateHierarchy**-Methode weitergegeben wird, wird der Name einer der Abschnitte in der vorhandenen Hierarchie geändert (durch Ändern des Werts des **name**-Attributs in "Mein umbenannter Abschnitt"). Dann werden alle Abschnitte außer dem, dessen Name geändert wurde, entfernt. Darüber hinaus entfernt der Code nicht erforderliche Attribute aus dem Zielelement **Abschnitt**, einschließlich der Attribute **lastModifiedTime**, **isCurrentlyViewed** und **color**, wobei nur die Attribute **name**, **ID** und **path** erhalten bleiben. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

Der vorherige XML-Code wurde mit dem im Beispiel für die **GetHierarchy**-Methode verwendeten Code abgerufen, der wie folgt geändert wird, um den Bereich auf Abschnitte zu beschränken. 
  
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

Das folgende C#-Beispiel zeigt eine vollständige Konsolenanwendung, die nach einem Abschnitt mit dem Namen "`Sample_Section`" sucht, fordert den Benutzer zur Eingabe eines neuen Namens für den Abschnitt auf und verwendet dann die **UpdateHierarchy**-Methode, um den Abschnittsnamen in den Namen zu ändern, den der Benutzer eingegeben hat. Bevor Sie den Code ausführen, ändern Sie "`Sample_Section`" in den Namen eines Abschnitts, der in Ihrer OneNote-Hierarchie vorhanden ist.
  
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
|**Beschreibung** <br/> |Öffnet eine Abschnittsgruppe oder einen Abschnitt, den Sie angeben.  <br/> |
|**Syntax** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Parameter** <br/> | _bstrPath_ &ndash; Der Pfad, den Sie öffnen möchten. Für ein Notizbuch oder eine Abschnittsgruppe in einem Notizbuch kann _bstrPath_ ein Ordnerpfad oder der Pfad zu einer ONE-Abschnittsdatei sein. Wenn Sie den Pfad zu einer ONE-Abschnittsdatei angeben, müssen Sie die ONE-Erweiterung in die Dateipfad-Zeichenfolge einschließen.  <br/><br/>_bstrRelativeToObjectID_ &ndash; Die OneNote-ID des übergeordneten Objekts (Notizbuch oder Abschnittsgruppe), unter dem Sie das neue Objekt öffnen möchten. Wenn der _bstrPath_-Parameter ein absoluter Pfad ist, können Sie für _bstrRelativeToObjectID_ eine leere Zeichenfolge übergeben (""). Alternativ können Sie auch die Objekt-ID des Notizbuchs oder der Abschnittsgruppe weitergeben, die das Objekt enthalten sollte (Abschnitt oder Abschnittsgruppe), das Sie erstellen möchten. Geben Sie dann den Dateinamen (z. B. section1.one) des Objekts an, das Sie unter dem übergeordneten Objekt erstellen möchten.  <br/><br/>_pbstrObjectID_ &ndash; (Ausgabeparameter) Die Objekt-ID, die OneNote für das von der **OpenHierarchy**-Methode geöffnete Notizbuch, die geöffnete Abschnittsgruppe oder den geöffneten Abschnitt zurückgibt. Dieser Parameter ist ein Verweis auf die Zeichenfolge, in die die Methode die ID schreiben soll.  <br/><br/>_cftlfNotExist_ &ndash; (Optional) Ein aufgelisteter Wert aus der [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType)-Enumeration. Wenn Sie einen Wert für _cftIfNotExist_ übergeben, erstellt die **OpenHierarchy**-Methode die Abschnittsgruppe oder Abschnittsdatei nur unter dem angegebenen Pfad, wenn die Datei noch nicht vorhanden ist.  <br/> |
   
Wenn Sie eine Abschnittsgruppe angeben, die sich nicht in einem offenen Notizbuch befindet, öffnet die **OpenHierarchy**-Methode die Abschnittsgruppe als Notizbuch. Wenn Sie einen Abschnitt angeben, der sich nicht in einem offenen Notizbuch befindet, öffnet die **OpenHierarchy**-Methode den Abschnitt in der Abschnittsgruppe "Zuletzt geöffnete Abschnitte". Wenn Sie eine Abschnittsgruppe oder einen Abschnitt angeben, die bzw. der sich bereits in einem geöffneten Notizbuch befindet, geschieht nichts, da die Abschnittsgruppe oder der Abschnitt ebenfalls bereits geöffnet ist. Auf jeden Fall gibt **OpenHierarchy** die Objekt-ID für die Abschnittsgruppe, das Notizbuch oder den Abschnitt zurück, die/das/den Sie angeben haben, sodass Sie sie in anderen Vorgängen verwenden können. 
  
Sie können auch die **OpenHierarchy**-Methode verwenden, um neue Abschnitte zu erstellen, anstatt XML zu importieren. 
  
Der folgende Code veranschaulicht, wie Sie die **OpenHierarchy**-Methode zum Öffnen des Abschnitts "Besprechungen" im Arbeitsnotizbuch öffnen und die ID für den Abschnitt abrufen. Wenn der Abschnitt nicht bereits vorhanden ist, erstellt OneNote ihn am von Ihnen angegebenen Speicherort. 
  
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
|**Beschreibung** <br/> |Löscht alle Hierarchie-Objekte (eine Abschnittsgruppe, einen Abschnitt oder eine Seite) aus der Hierarchie des OneNote-Notizbuchs.  <br/> |
|**Syntax** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Parameter** <br/> | _bstrObjectID_ &ndash; Die OneNote-ID des Objekts, das Sie löschen möchten. Das Objekt kann eine Abschnittsgruppe, ein Abschnitt oder eine Seite sein.  <br/><br/>_dateExpectedLastModified_ &ndash; (Optional) Das Datum und die Uhrzeit, zu der das Objekt, das Sie löschen möchten, vermutlich zuletzt geändert wurde. Wenn Sie einen Wert ungleich NULL für diesen Parameter übergeben, fährt OneNote nur mit dem Update fort, wenn der Wert, den Sie übergeben, dem tatsächlichen Datum und der Zeit entspricht, zu der das Objekt zuletzt geändert wurde. Die Übergabe eines Werts für diesen Parameter verhindert, dass versehentlich Änderungen überschrieben werden, die Benutzer seit der letzten Änderung des Objekts vorgenommen haben.  <br/><br/>_deletePermanently_ &ndash; (Optional) **true**, um den Inhalt dauerhaft zu löschen; **false**, um den Inhalt in den OneNote-Papierkorb für das entsprechende Notizbuch (Standard) zu verschieben. Wenn das Notizbuch im OneNote 2007-Format vorliegt, ist kein Papierkorb vorhanden, sodass der Inhalt dauerhaft gelöscht wird.  <br/> |
   
### <a name="createnewpage-method"></a>CreateNewPage-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Fügt eine neue Seite am Ende des von Ihnen angegebenen Abschnitts hinzu. Die neue Seite wird als letzte Seite des Abschnitts hinzugefügt.  <br/> |
|**Syntax** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Parameter** <br/> | _bstrSectionID_ &ndash; Eine Zeichenfolge, die die OneNote-ID des Abschnitts enthält, in dem Sie eine neue Seite erstellen möchten.  <br/><br/>_pbstrPageID_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die die Methode die OneNote-ID für die neu erstellte Seite schreibt.  <br/><br/>_npsNewPageStyle_ &ndash; Ein Wert aus der **NewPageStyle**-Enumeration, der den Stil der Seite angibt, die erstellt werden soll.  <br/> |
   
Die OneNote-API umfasst die **CreateNewPage**-Methode als Serviceleistung. Sie können dasselbe Ergebnis mit einer höheren Kontrolle darüber, wie die neue Seite in der Hierarchie positioniert wird, erzielen, indem Sie die **UpdateHierarchy**-Methode aufrufen. Mit der **UpdateHierarchy**-Methode können Sie beim Erstellen der neuen Seite auch Unterseiten erstellen. 
  
### <a name="closenotebook-method"></a>CloseNotebook-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Schließt das angegebene Notizbuch.  <br/> |
|**Syntax** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Parameter** <br/> | _bstrNotebookID_ &ndash; Die OneNote-ID des Notizbuchs, das Sie schließen möchten.  <br/><br/>_force_ &ndash; (Optional) **true**, um das Notizbuch zu schließen, auch wenn Änderungen im Notizbuch vorliegen, die OneNote vor dem Schließen nicht synchronisieren kann; andernfalls **false** (Standard).  <br/> |
   
Sie können die **CloseNotebook**-Methode verwenden, um das angegebene Notizbuch zu schließen. Wenn Sie diese Methode aufrufen, synchronisiert OneNote bei Bedarf alle Offline-Dateien mit aktuellem Notizbuchinhalt und schließt dann das angegebene Notizbuch. Nachdem die Methode zurückgegeben wurde, wird das Notizbuch nicht mehr in der Liste der geöffneten Notizbücher der OneNote-Benutzeroberfläche (UI) angezeigt. 
  
### <a name="gethierarchyparent-method"></a>GetHierarchyParent-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft die OneNote-ID des übergeordneten Objekts eines OneNote-Objekts ab.  <br/> |
|**Syntax** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Parameter** <br/> | _bstrObjectID_ &ndash; Eine Zeichenfolge, die die OneNote-ID des Objekts enthält, von dem Sie das übergeordnete Objekt suchen möchten.  <br/><br/>_pbstrParentID_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die die Methode die OneNote-ID des übergeordneten Objekts schreibt.  <br/> |
   
Wenn das OneNote-Objekt kein übergeordnetes Objekt besitzt (wenn z. B. ein Benutzer das übergeordnete Element eines Notizbuchs abrufen möchte), wird eine Ausnahme ausgelöst.
  
### <a name="getspeciallocation-method"></a>GetSpecialLocation-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft den Pfad zu dem Speicherort ab, an dem OneNote bestimmte Sonderelemente, wie z. B. Sicherungen, nicht abgelegte Notizen und das Standardnotizbuch, speichert.  <br/> |
|**Syntax** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Parameter** <br/> | _slToGet_ &ndash; Einer der [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation)-Enumerationswerte, der den speziellen Ordnerspeicherort angibt, der abgerufen werden soll.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die OneNote den Pfad des speziellen Ordners schreiben soll.  <br/> |
   
Sie können diese Methode verwenden, um den Speicherort des Ordners "Nicht abgelegte Notizen" auf dem Datenträger zu ermitteln. Dies ist der Ordner, in dem OneNote Notizen speichert, die erstellt werden, wenn Sie ein Element in OneNote ziehen, sowie Notizen, die direkt aus anderen Anwendungen stammen (z. B. solche, die abgerufen werden, wenn Sie auf **An OneNote senden** in Microsoft Outlook oder Microsoft Internet Explorer klicken). 
  
## <a name="page-content-methods"></a>Seiteninhalt-Methoden
<a name="ON14DevRef_Application_PageContent"> </a>

Mit den in diesem Abschnitt beschriebenen Methoden können Sie Inhalte von Seiten in OneNote-Notizbüchern entdecken, aktualisieren und löschen sowie OneNote-Inhalte veröffentlichen.
  
### <a name="getpagecontent-method"></a>GetPageContent-Methode

|||
|:-----|:-----|
|**Beschreibung**|Ruft alle Inhalte (im OneNote XML-Format) der angegebenen Seite ab.|
|**Syntax**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Parameter**| _bstrPageId_ &ndash; Die OneNote-ID der Seite, deren Inhalt Sie abrufen möchten.<br/><br/>_pbstrPageXmlOut_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die OneNote die XML-Ausgabe schreiben soll.<br/><br/>_pageInfoToExport_ &ndash; (Optional): Gibt an, ob die **GetPageContent**-Methode binäre, in XML-Code eingebettete und Base-64-codierte Inhalte zurückgibt. Binäre Inhalte können beispielsweise Bilder und Freihanddaten enthalten. Der _pageInfoToExport_-Parameter gibt auch an, ob die Auswahl im XML-Code, den die **GetPageContent**-Methode zurückgibt, gekennzeichnet werden soll. Es wird ein Enumerationswert aus der [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo)-Enumeration verwendet.<br/><br/>_xsSchema_ &ndash; (Optional) Die Version des OneNote-XML-Schemas des Typs **XMLSchema**, das ausgegeben werden soll. Sie können angeben, ob Sie die XML-Schemaversion 2013, 2010, 2007 oder die aktuelle Version wünschen. <br/><br/>**HINWEIS**: Wir empfehlen Ihnen, eine Version von OneNote anzugeben (z. B. **xs2013**), statt **xsCurrent** zu verwenden oder es leer zu lassen, da das Add-In so mit zukünftigen Versionen von OneNote arbeiten kann.           |
   
Standardmäßig bettet OneNote keine binären Inhalte in den XML-Code ein, um übermäßige Längen in der zurückgegebenen Zeichenfolge zu vermeiden. Aus demselben Grund wird die aktuelle Auswahl nicht mit Auswahlattributen gekennzeichnet. Binäre Objekte enthalten eine OneNote-ID in Ihren eigenen Tags. Um ein binäres Objekt abzurufen, rufen Sie die **GetBinaryPageContent**-Methode auf und übergeben die OneNote-ID, die Sie von der **GetPageContent**-Methode erhalten haben. Verwenden Sie die **GetPageContent**-Methode, wenn Sie die binären Daten nicht sofort benötigen. 
  
### <a name="updatepagecontent-method"></a>UpdatePageContent-Methode

|||
|:-----|:-----|
|**Beschreibung**|Aktualisiert oder ändert den Inhalt auf der Seite.|
|**Syntax**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Parameter**| _bstrPageChangesXmlIn_ &ndash; Eine Zeichenfolge, die OneNote XML-Code enthält, der die Änderungen enthält, die Sie an der Seite vornehmen möchten.<br/><br/>_dateExpectedLastModified_ &ndash; (Optional) Das Datum und die Uhrzeit, zu der die Seite, die Sie aktualisieren möchten, vermutlich zuletzt geändert wurde. Wenn Sie einen Wert ungleich NULL für diesen Parameter übergeben, fährt OneNote nur mit dem Update fort, wenn der Wert, den Sie übergeben, dem tatsächlichen Datum und der Zeit entspricht, zu der die Seite zuletzt geändert wurde. Die Übergabe eines Werts für diesen Parameter verhindert, dass versehentlich Änderungen überschrieben werden, die Benutzer seit der letzten Änderung der Seite vorgenommen haben.<br/><br/>_xsSchema_ &ndash; (Optional) Die Version des OneNote-XML-Schemas des Typs **XMLSchema**, das ausgegeben werden soll. Sie können angeben, ob Sie die XML-Schemaversion 2013, 2010, 2007 oder die aktuelle Version wünschen. <br/><br/>**HINWEIS**: Wir empfehlen Ihnen, eine Version von OneNote anzugeben (z. B. **xs2013**), statt **xsCurrent** zu verwenden oder es leer zu lassen, da das Add-In so mit zukünftigen Versionen von OneNote arbeiten kann.<br/><br/>_force_(Optional) **true**, um den Inhalt der Seite zu aktualisieren, auch wenn auf der Seite unbekannte Daten von einer zukünftigen OneNote-Version vorhanden sind; andernfalls **false** (Standard). |
   
Sie können diese Methode verwenden, um die Seite auf verschiedene Arten zu ändern. Beispielsweise können Sie die **UpdatePageContent**-Methode verwenden, um eine Gliederung zu einer Seite hinzuzufügen, den Inhalt einer Gliederung zu ändern, Bilder hinzuzufügen, Freihandobjekte hinzuzufügen, Inhalte zu verschieben oder Text in Gliederungen zu ändern. 
  
Ein spezifischeres Beispiel wäre die Verwendung der **GetPageContent**-Methode, um eine vorhandene Seite zu exportieren, Änderungen am XML-Code für die Seite vorzunehmen und dann die **UpdatePageContent**-Methode zu verwenden, um die gesamte Seite erneut zu importieren. Oder Sie können diese Methode verwenden, um neue Seitenobjekte, wie z. B. Bilder, an das Ende einer vorhandenen Seite hinzuzufügen. 
  
Die einzigen Objekte, die Sie zu dem XML-Code hinzufügen müssen, den Sie an die **UpdatePageContent**-Methode übergeben, sind Seitenebene-Objekte (z. B. Gliederungen, Bilder auf der Seite oder Freihandobjekte auf der Seite), die nie geändert wurden. Diese Methode ändert oder entfernt keine Objekte auf Seitenebene, die Sie nicht im _bstrPageChangesXmlIn_-Parameter angegeben. Diese Methode ersetzt vollständig Objekte auf Seitenebene, wie z. B. Gliederungen, deren IDs mit denen der übergebenen Objekte übereinstimmen. Aus diesem Grund müssen Sie alle Objekte auf Seitenebene vollständig in Ihrem Code angeben, einschließlich der vorhandenen Inhalte und Änderungen, die Sie daran vornehmen möchten. 
  
Wenn Ihre Seite z. B. eine Gliederung und ein Hintergrundbild für die Seite enthält, können Sie die Gliederung ersetzen und das Bild unverändert lassen, indem Sie die Gliederung komplett im XML-Code angeben, die ID der vorhandenen Gliederung verwenden und das Bild nicht in den Code einschließlichen. Da die überarbeitete Gliederung, die Sie in den Code einschließen, die vorhandene Gliederung vollständig ersetzt, müssen Sie alle Inhalte der Gliederung einschließen.
  
Darüber hinaus ändert die **UpdatePageContent**-Methode nur Elementeigenschaften, die Sie im _bstrPageChangesXmlIn_-Parameter angeben. Wenn Sie z. B. einige, aber nicht alle Eigenschaften des **PageSettings**-Elements angeben, bleiben die Eigenschaften, die Sie nicht angeben, unverändert. 
  
Das folgende Beispiel zeigt, wie Sie mithilfe der **UpdatePageContent**-Methode den Titel einer Seite ändern und Beispieltext zur Seite hinzufügen. Ersetzen Sie vor dem Ausführen des Codes eine gültige Seiten-ID durch die im Code angezeigte Seiten-ID, damit der Code auf Ihrem Computer funktioniert. Sie können die Seiten-ID für eine Seite abrufen, indem Sie die **GetHierarchy**-Methode verwenden und die Ausgabe untersuchen. 
  
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
|**Beschreibung** <br/> |Gibt ein binäres Objekt, wie z. B. Freihand oder Bilder, auf einer OneNote-Seite als Base-64-codierte Zeichenfolge zurück.  <br/> |
|**Syntax** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Parameter** <br/> | _bstrPageID_ &ndash; Die OneNote-ID der Seite, die das binäre Objekt zum Abrufen enthält.  <br/><br/>_bstrObjectID_ &ndash; Die OneNote-ID des Objekts, das Sie abrufen möchten. Diese ID, die als **callbackID** bezeichnet wird, ist der OneNote XML-Code für eine von der **GetPageContent**-Methode zurückgegebene Seite.  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; (Ausgabeparameter) Ein Verweis auf eine Zeichenfolge, in die OneNote das binäre Objekt als Base-64-codierte Zeichenfolge schreibt.  <br/> |
   
### <a name="deletepagecontent-method"></a>DeletePageContent-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Löscht ein &ndash;-Objekt wie z. B. ein **Outline**-, **Freihand**- oder **Image**-Objekt von einer Seite.  <br/> |
|**Syntax** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Parameter** <br/> | _bstrPageID_ &ndash; Die OneNote-ID der Seite, die das Objekt zum Löschen enthält.  <br/><br/>_bstrObjectID_ &ndash; Die OneNote-ID des Objekts, das Sie löschen möchten.  <br/><br/>_dateExpectedLastModified_ &ndash; (Optional) Das Datum und die Uhrzeit, zu der die Seite, die Inhalte zum Löschen enthält, vermutlich zuletzt geändert wurde. Wenn Sie einen Wert ungleich NULL für diesen Parameter übergeben, fährt OneNote nur mit dem Löschen fort, wenn der Wert, den Sie übergeben, dem tatsächlichen Datum und der Zeit entspricht, zu der die Seite zuletzt geändert wurde. Die Übergabe eines Werts für diesen Parameter verhindert, dass versehentlich Änderungen überschrieben werden, die Benutzer seit der letzten Änderung der Seite vorgenommen haben.  <br/><br/>_force_ &ndash; (Optional) **true**, um den Inhalt der Seite zu aktualisieren, auch wenn auf der Seite unbekannte Daten von einer zukünftigen OneNote-Version vorhanden sind; andernfalls **false** (Standard).  <br/> |
   
### <a name="publish-method"></a>Publish-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Exportiert die Seite, die Sie angeben haben, in eine Datei in einem beliebigen Format, das OneNote unterstützt.  <br/> |
|**Syntax** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID der Hierarchie, die Sie exportieren möchten.  <br/><br/>_bstrTargetFilePath_ &ndash; Der absolute Pfad zu dem Speicherort, an dem Sie die resultierende Ausgabedatei speichern möchten. Die Datei, die Sie angeben, darf noch nicht an diesem Speicherort vorhanden sein.  <br/><br/>_pfPublishFormat_ &ndash; Einer der [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat)-Enumerationswerte, der das Format für die veröffentlichte Seite (z. B. MTHML, PDF usw.) angibt.  <br/><br/>_bstrCLSIDofExporter_ &ndash; Die Klassen-ID (CLSID) einer registrierten COM-Anwendung, die Microsoft Windows Enhanced Metafiles (EMF) exportieren kann. Die COM-Anwendung muss die **IMsoDocExporter**-Oberfläche implementieren. Dieser Parameter wird angegeben, um zu verhindern, dass Entwickler dritter Parteien ihren eigenen Code schreiben, um OneNote-Inhalte in einem benutzerdefinierten Format zu veröffentlichen. Weitere Informationen zur **IMsoDocExporter**-Schnittstelle finden Sie unter [Erweitern Sie das Office 2007-Format Export Feature](https://msdn.microsoft.com/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
OneNote unterstützt derzeit die folgenden Dateiformate:
  
- MHTML-Dateien (MHT)
- Adobe Acrobat-PDF-Dateien (PDF)
- XML Paper Specification-Dateien (XPS)
- OneNote 2013-, 2010- oder 2007-Dateien (ONE)
- OneNote-Paketdateien (ONEPKG)
- Microsoft Word-Dokumente (DOC oder DOCX)
- Microsoft Windows Enhanced Metafiles (EMF)
- HTML-Dateien (HTML)
    
Diese Methode erzeugt genau die gleichen Ergebnisse, die Sie auch durch Klicken auf **Publish** in der Benutzeroberfläche und Angabe des Formats erhalten würden. 
  
## <a name="navigation-methods"></a>Navigationsmethoden
<a name="ON14DevRef_Application_Navigation"> </a>

Mit den in diesem Abschnitt beschriebenen Methoden können Sie OneNote-Notizbücher, Abschnittsgruppen, Abschnitte, Seiten und Seitenobjekte finden, zu diesen navigieren und diese verlinken.
  
### <a name="navigateto-method"></a>NavigateTo-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Navigiert zu dem angegebenen Objekt (z. B. Abschnitte, Seiten und **Outline**-Elemente innerhalb der Seite).  <br/> |
|**Syntax** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameter** <br/> | _bstrHierarchyObjectID_ &ndash; Die OneNote-ID des Objekts, zu dem Sie in der OneNote-Hierarchie navigieren möchten.  <br/><br/>_bstrObjectID_ &ndash; Die OneNote-ID des Objekts, zu dem Sie auf der OneNote-Seite navigieren möchten.  <br/><br/>_fNewWindow_ &ndash; (Optional) **true**, um das angegebene Objekt in einem neuen OneNote-Fenster zu öffnen. **false** öffnet kein neues OneNote-Fenster, wenn eins geöffnet ist.  <br/> |
   
### <a name="navigatetourl-method"></a>NavigateToUrl-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Wenn einen Link OneNote übergeben (Onenote: / /), wird das OneNote-Fenster auf den entsprechenden Speicherort in OneNote geöffnet. Wenn sich der Link außerhalb von OneNote befindet (z. B. "https://" oder "file://"), wird ein Sicherheitsdialogfeld angezeigt. Bei Ablehnung versucht OneNote, den Link zu öffnen, und ein **HResult.hrObjectDoesNotExist**-Fehler wird zurückgegeben.  <br/> |
|**Syntax** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameter** <br/> | _bstrUrl_ &ndash; Eine Zeichenfolge, die angibt, wohin navigiert werden soll. Dies kann ein OneNote-Link oder eine beliebige andere URL sein, wie z. B. ein Weblink oder eine Netzwerkadresse.  <br/><br/>_fNewWindow_ &ndash; (Optional) **true**, um die angegebene URL in einem neuen OneNote-Fenster zu öffnen. **false** öffnet kein neues OneNote-Fenster, wenn eins geöffnet ist.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>GetHyperLinkToObject-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ruft einen OneNote-Hyperlink zum angegebenen Notizbuch, zur angegebenen Abschnittsgruppe, zum angegebenen Abschnitt, zur angegebenen Seite oder zum angegebenen Seitenobjekt ab.  <br/> |
|**Syntax** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID für das Notizbuch, die Abschnittsgruppe, den Abschnitt oder die Seite, für das/die/den Sie einen Hyperlink erstellen möchten.  <br/><br/>_bstrPageContentObjectID_ &ndash; (Optional) Die OneNote-ID für das Objekt auf der Seite, für das Sie einen Hyperlink erstellen möchten. Das Objekt kann z. B. eine Gliederung oder ein **outline**-Element sein. Wenn Sie eine leere Zeichenfolge übergeben (""), verweist der zurückgegebene Link auf das Notizbuch, die Abschnittsgruppe, den Abschnitt oder die Seite, das/die/der im _bstrHierarchyID_-Parameter angegeben wurde. Wenn Sie eine nicht leere Zeichenfolge für den _bstrPageContentObjectID_-Parameter übergeben, muss der _bstrHierarchyID_-Parameter ein Bezug auf die Seite sein, die das angegebene Objekt enthält.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (Ausgabeparameter) Ein Verweis auf eine Zeichenfolge, in die die **GetHyperlinkToObject**-Methode den Hyperlinktext der Ausgabe schreibt.  <br/> |
   
Wenn Sie versuchen, zum resultierenden Link zu navigieren, öffnet OneNote das angegebene Objekt im Browser.
  
### <a name="getwebhyperlinktoobject-method"></a>GetWebHyperlinktoObject-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Gibt einen Hyperlink zu einem Objekt zurück, das im OneNote-Webclient geöffnet wird.  <br/> |
|**Syntax** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID für das Notizbuch, die Abschnittsgruppe, den Abschnitt oder die Seite, für das/die/den Sie einen Webhyperlink erstellen möchten.  <br/><br/>_bstrPageContentObjectID_ &ndash; (Optional) Die OneNote-ID für das Objekt auf der Seite, für das Sie einen Hyperlink erstellen möchten. Das Objekt kann z. B. eine Gliederung oder ein **outline**-Element sein. Wenn Sie eine leere Zeichenfolge übergeben (""), verweist der zurückgegebene Link auf das Notizbuch, die Abschnittsgruppe, den Abschnitt oder die Seite, das/die/der im _bstrHierarchyID_-Parameter angegeben wurde. Wenn Sie eine nicht leere Zeichenfolge für den _bstrPageContentObjectID_-Parameter übergeben, muss der _bstrHierarchyID_-Parameter ein Bezug auf die Seite sein, die das angegebene Objekt enthält.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (Ausgabeparameter) Ein Verweis auf eine Zeichenfolge, in die die **GetWebHyperlinkToObject**-Methode den Hyperlinktext der Ausgabe schreibt. Wenn kein Webhyperlink für das Notizbuch erstellt werden kann, wird ein Null-Wert zurückgegeben.  <br/> |
   
### <a name="findpages-method"></a>FindPages-Methode

|||
|:-----|:-----|
|**Beschreibung**|Gibt eine Liste der Seiten zurück, die dem angegebenen Abfragebegriff entsprechen.|
|**Syntax**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameter**| _bstrStartNodeID_ &ndash; Der Knoten (Stamm, Notizbuch, Abschnittsgruppe oder Abschnitt), unter dem nach Inhalten gesucht werden soll. Dieser Parameter legt den Bereich für die Suche fest.<br/><br/>_bstrSearchString_ &ndash; Die Suchzeichenfolge. Geben Sie genau die gleiche Zeichenfolge weiter, die Sie in das Suchfeld der OneNote-UI eingeben würden. Sie können bitweise Operatoren verwenden, wie z. B. **UND** und **ODER**, die komplett in Großbuchstaben angegeben werden müssen.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die OneNote die XML-Ausgabezeichenfolge schreiben soll. Die resultierende XML-Zeichenfolge enthält die Notizbuchhierarchie vom Stamm bis hinunter zu den und einschließlich aller Seiten, die der Suchzeichenfolge entsprechen. Die **FindPages**-Methode listet z. B. keine Abschnitte auf, die nicht über Seitenübereinstimmungen in der Hierarchie verfügen. Wenn nur eine Seite in einem einzigen Abschnitt mit der Zeichenfolge übereinstimmt, enthält die zurückgegebene Hierarchie den Pfad zu dem Abschnitt und der Seite, aber keine anderen Bestandteile der Hierarchie des Notizbuchs.<br/><br/>_fIncludeUnindexedPages_ &ndash; (Optional) **true**, um Seiten zu suchen, die nicht von Windows Search indiziert wurden; andernfalls **false**.<br/><br/>_fDisplay_ &ndash; (Optional) **true**, um die Suche auf der Benutzeroberfläche für den Benutzer auszuführen, so als ob der Benutzer sie selbst eingegeben hätte. **false**, um die Abfrage ohne Änderung an der Benutzeroberfläche auszuführen (Standard).<br/><br/>_xsSchema_ &ndash; (Optional) Die OneNote-Schemaversion der Zeichenfolge _pbstrHierarchyXmlOut_. Dieser optionale Wert wird verwendet, um die Version des OneNote-XML-Schemas anzugeben, im dem sich die _pbstrHierarchyXmlOut_-Zeichenfolge befindet. Wenn dieser Wert nicht angegeben ist, setzt OneNote voraus, dass sich die XML in der Schemaversion _xsCurrent_ befindet. <br/><br/>**HINWEIS**: Wir empfehlen Ihnen, eine Version von OneNote anzugeben (z. B. **xs2013**), statt **xsCurrent** zu verwenden oder es leer zu lassen, da das Add-In so mit zukünftigen Versionen von OneNote arbeiten kann.           |
   
 **FindPages** funktioniert nur, wenn Sie Microsoft Search 3.0 oder 4.0 auf Ihrem Computer installiert haben. Windows Vista und Windows 7 enthalten diese Komponente. Wenn Sie eine frühere Version von Windows ausführen, müssen Sie [Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) installieren, damit **FindPages** funktioniert. 
  
### <a name="findmeta-method"></a>FindMeta-Methode

|||
|:-----|:-----|
|**Beschreibung**|Gibt eine Liste von OneNote-Objekten zurück, die Metadaten enthalten, die dem angegebenen Abfragebegriff entsprechen.|
|**Syntax**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameter**| _bstrStartNodeID_ &ndash; Der Knoten (Stamm, Notizbuch, Abschnittsgruppe oder Abschnitt), unter dem nach Inhalten gesucht werden soll. Dieser Parameter legt den Bereich für die Suche fest.<br/><br/>_bstrSearchStringName_ &ndash; Die Suchzeichenfolge. In einem beliebigen Teil des Namens der Metadaten übergeben. Wenn Sie eine leere Zeichenfolge oder einen Null-Wert übergeben, entsprechen alle Objekte, die Metadaten enthalten, der Abfrage.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Ausgabeparameter) Ein Verweis auf die Zeichenfolge, in die OneNote die XML-Ausgabezeichenfolge schreiben soll. Die resultierende XML-Zeichenfolge enthält die Notizbuchhierarchie vom Stamm bis hinunter zu den und einschließlich aller Seiten, die der Suchzeichenfolge entsprechen. Die **FindPages**-Methode listet z. B. keine Abschnitte auf, die nicht über Seitenübereinstimmungen in der Hierarchie verfügen. Wenn nur eine Seite in einem einzigen Abschnitt mit der Zeichenfolge übereinstimmt, enthält die zurückgegebene Hierarchie den Pfad zu dem Abschnitt und der Seite, aber keine anderen Bestandteile der Hierarchie des Notizbuchs.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (Optional) **true**, um Seiten zu suchen, die nicht von Windows Search indiziert wurden; andernfalls **false**.<br/><br/>_xsSchema_ &ndash; (Optional) Die OneNote-Schemaversion der Zeichenfolge _pbstrHierarchyXmlOut_. Dieser optionale Wert wird verwendet, um die Version des OneNote-XML-Schemas anzugeben, im dem sich die _pbstrHierarchyXmlOut_-Zeichenfolge befindet. Wenn dieser Wert nicht angegeben ist, setzt OneNote voraus, dass sich die XML in der Schemaversion _xsCurrent_ befindet. <br/><br/>**HINWEIS**: Wir empfehlen Ihnen, eine Version von OneNote anzugeben (z. B. **xs2013**), statt **xsCurrent** zu verwenden oder es leer zu lassen, da das Add-In so mit zukünftigen Versionen von OneNote arbeiten kann.           |
   
**FindMeta** funktioniert nur, wenn Sie Microsoft Windows Search 3.0 oder 4.0 auf Ihrem Computer installiert haben. Windows Vista und Windows 7 enthalten diese Komponente. Wenn Sie eine frühere Version von Windows ausführen, müssen Sie [Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) installieren, damit **FindMeta** funktioniert. 
  
## <a name="functional-methods"></a>Funktionale Methoden
<a name="ON14DevRef_Application_Functional"> </a>

Mit den in diesem Abschnitt beschriebenen Methoden können Sie bestimmte Aktionen ausführen oder Parameter innerhalb der OneNote-Anwendung festlegen.
  
### <a name="mergefiles-method"></a>MergeFiles-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht es Benutzern, Änderungen an derselben Datei in einer Datei zusammenführen. Damit die Dateien als gleich angesehen werden, müssen Sie die gleiche OneNote-ID besitzen.  <br/> |
|**Syntax** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Parameter** <br/> | _bstrBaseFile_ &ndash; Die Zeichenfolge für den Pfad zum Speicherort der ONE-Datei für den ursprünglichen Zustand der Datei.  <br/><br/>_bstrClientFile_ &ndash; Die Zeichenfolge für den Pfad zum Speicherort für die zweite Gruppe von Änderungen, die mit der Basisdatei zusammengeführt werden, nachdem die Änderungen der Serverdatei mit der Basis zusammengeführt wurden.  <br/><br/>_bstrServerFile_ &ndash; Die Zeichenfolge für den Pfad zum Speicherort für die ONE-Datei der ersten Gruppe von Änderungen, die mit der Basisdatei zusammengeführt werden.  <br/><br/>_bstrTargetFile_ &ndash; Die Zeichenfolge für den Pfad zum Speicherort der ONE-Datei mit den zusammengeführten Änderungen.  <br/> |
   
Die **MergeFiles**-Methode wurde für mobile Szenarien entwickelt, bei denen mehrere Versionen einer OneNote-Datei vorhanden sein können. 
  
### <a name="mergesections-method"></a>MergeSections-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Führt die Inhalte von einem Abschnitt mit einem anderen Abschnitt in OneNote zusammen.  <br/> |
|**Syntax** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Parameter** <br/> | _bstrSectionSourceId_ &ndash; Die OneNote-ID des Bereichs, der eingefügt werden soll.  <br/><br/>_bstrSectionDestinationId_ &ndash; Die OneNote-ID des Bereichs, in dem die Zusammenführung stattfinden soll. Der Quellabschnitt wird in diesen Zielabschnitt integriert.  <br/> |
   
Diese Methode führt denselben Vorgang wie das Feature **In einen anderen Abschnitt einfügen** aus, das angezeigt wird, wenn Sie mit der rechten Maustaste auf einen Abschnitt klicken. 
  
### <a name="quickfiling-method"></a>QuickFiling-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Gibt eine Instanz des [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog)-Dialogfelds zurück, die verwendet werden kann, um einen Speicherort in der OneNote-Hierarchiestruktur auszuwählen.  <br/> |
|**Syntax** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>SyncHierarchy-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Zwingt OneNote, das angegebene Objekt mit der Quelldatei auf dem Datenträger zu synchronisieren.  <br/> |
|**Syntax** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Parameter** <br/> | _bstrHierarchyID_ &ndash; Die OneNote-ID des Objekts, das synchronisiert werden soll.  <br/> |
   
### <a name="setfilinglocation-method"></a>SetFilingLocation-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht es Benutzern, anzugeben, wo und wie bestimmte Arten von Inhalten in OneNote abgelegt werden sollen.  <br/> |
|**Syntax** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Parameter** <br/> | _flToSet_ &ndash; Der Objekttyp des anzugebenden Ablageorts.  <br/><br/>_fltToSet_ &ndash; Der Speicherort, an dem der Typ abgelegt wird.  <br/><br/>_bstrFilingSectionID_ &ndash; Die OneNote-ID des Abschnitts oder der Seite für den/die ein Speicherort festgelegt werden soll. Wenn dies nicht zutrifft, kann der Benutzer einen Null-Wert oder eine leere Zeichenfolge übergeben.  <br/> |
   
Die Arten von Inhalten, die abgelegt werden können, umfassen Outlook-Elemente und Webnotizen von Internet Explorer, die in OneNote über den Befehl **An OneNote senden** importiert werden. Der Ablageort von Elementen, die in OneNote gedruckt werden, kann ebenfalls mit dieser Methode festgelegt werden. 
  
## <a name="properties"></a>Eigenschaften
<a name="ON14DevRef_Application_Properties"> </a>

In diesem Abschnitt werden die Eigenschaften der **Application**-Oberfläche beschrieben. 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**Windows** <br/> |Bietet Benutzern Zugriff auf geöffnete OneNote-Fenster. Diese Eigenschaft ermöglicht es Benutzern, die OneNote-Fenster aufzulisten und bestimmte Fenstereigenschaften zu ändern. Weitere Informationen finden Sie unter [Windows-Schnittstellen](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Gibt die **COMAddIns**-Sammlung für OneNote zurück. Diese Sammlung enthält alle COM-Add-Ins, die für OneNote verfügbar sind. Die **Count**-Eigenschaft der **COMAddins**-Sammlung gibt die Anzahl der verfügbaren COM-Add-Ins zurück. Weitere Informationen finden Sie unter [COMAddIns](https://msdn.microsoft.com/library/office/ff865489.aspx)-Objekt.  <br/> |
|**LanguageSettings** <br/> |Ermöglicht den Zugriff auf einige APIs, um die gängigen Spracheinstellungen von OneNote zu ändern.  <br/> |
   
## <a name="events"></a>Ereignisse
<a name="ON14DevRef_Application_Events"> </a>

In diesem Abschnitt werden die Ereignisse der Anwendungsoberfläche beschrieben.
  
> [!CAUTION]
> Ereignisse können derzeit nicht zu verwaltetem Code hinzugefügt werden. 
  
### <a name="onnavigate-event"></a>OnNavigate-Ereignis

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht es einem Benutzer, eine Funktion zuzuweisen, die aufgerufen wird, wenn die OneNote-Oberfläche von der aktuellen OneNote-Position navigiert wird.  <br/> |
|**Syntax** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>OnHierarchyChange-Methode

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht es einem Benutzer, eine Funktion zuzuweisen, die immer dann aufgerufen wird, wenn die OneNote-Hierarchie sich ändert (z. B. Hinzufügen oder Löschen von Seiten oder Verschieben von Abschnitten). Hierarchie-Änderungen werden gestapelt, wenn also mehrere Änderungen zur gleichen Zeit oder etwa zur gleichen Zeit eintreten, löst OneNote das Ereignis einmal aus.  <br/> |
|**Syntax** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Parameter** <br/> | _bstrActivePageID_ &ndash; Übergibt die OneNote-ID der aktiven Seite.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [OneNote-Entwicklerreferenz](onenote-developer-reference.md)

