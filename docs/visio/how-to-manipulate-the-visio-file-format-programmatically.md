---
title: Programmgesteuertes Bearbeiten des Visio-Dateiformats
manager: lindalu
ms.date: 09/17/2021
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Erstellen Sie eine Lösung in Visual Studio 2012 zum Lesen des neuen Dateiformatpakets in Visio 2013, zum Auswählen von Paketteilen, Ändern von Daten in Paketteilen und Hinzufügen von Paketteilen.
ms.localizationpriority: high
ms.openlocfilehash: 762522a972b7c51eb5daa98388cf26e736d12cde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618826"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Programmgesteuertes Bearbeiten des Visio-Dateiformats

![Thema mit Anleitung](media/mod_icon_howto.png)
  
Erfahren Sie, wie Sie in Visual Studio 2012 eine Lösung zum Lesen des neuen Dateiformatpakets in Visio 2013, zum Auswählen von Paketteilen, Ändern von Daten in Paketteilen und Hinzufügen von Paketteilen erstellen.
   
## <a name="visio-file-format-manipulation-essentials"></a>Grundlegendes zum Bearbeiten des Visio-Dateiformats
<a name="vis15_ManipulateFF_Essentials"> </a>

In früheren Versionen von Visio wurden Dateien in einem proprietären Binärdateiformat (.vsd) oder einem einzelnen Dokument im Visio-XML-Zeichnungsdateiformat (.vdx) gespeichert. In Visio 2013 wird ein neues Dateiformat (.vsdx) eingeführt, das auf XML- und ZIP-Archivtechnologien basiert. Genauso wie in früheren Versionen von Visio werden Dateien in einem einzelnen Container gespeichert. Im Gegensatz zu Legacydateien kann jedoch das neue Dateiformat ohne Automatisierung der Visio 2013-Anwendung geöffnet, gelesen, aktualisiert, geändert und erstellt werden. Entwickler, die mit der Bearbeitung von XML oder dem Arbeiten mit dem [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8)-Namespace vertraut sind, können im Handumdrehen programmgesteuert mit den ersten Schritten mit dem neuen Dateiformat beginnen. Entwickler, die mit dem Visio-XML-Zeichnungsdateiformat aus früheren Versionen gearbeitet haben, stellen fest, dass viele der Strukturen aus diesem Format im neuen Dateiformat beibehalten wurden. 
  
In diesem Artikel wird das programmgesteuerte Arbeiten mit dem Visio 2013-Dateiformat mithilfe von Microsoft .NET Framework 4.5, C# oder Visual Basic und Visual Studio 2012 behandelt. Sie erfahren, wie Sie eine Visio 2013-Datei öffnen, Dokumentteile innerhalb der Datei auswählen, Daten in Dokumentteilen ändern und neue Dokumentteile erstellen.
  
> [!NOTE]
> In den Codebeispielen in diesem Artikel wird angenommen, dass Sie über elementare Kenntnisse der Klassen in den [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8)- und [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8)-Namespaces verfügen. > In diesem Artikel wird des Weiteren vorausgesetzt, dass Sie über Kenntnisse der Konzepte und der Terminologie der Open Packaging-Konventionen (Open Packaging Conventions, OPC) verfügen. Sie sollten mit den Konzepten „Pakete“, „Dokumentteile“ oder „Paketteile“ und „Beziehungen“ vertraut sein. Weitere Informationen finden Sie unter [OPC: Ein neuer Standard für das Verpacken Ihrer Daten](/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data.md). > Der Code veranschaulicht, wie LINQ-Abfragen (Language-Integrated Query) zum Auswählen von XML erstellt werden. Die meisten Codebeispiele verwenden die Abfragesyntax zum Erstellen von LINQ-Abfragen. Sie können alle der im Code bereitgestellten LINQ-Abfragen umschreiben, indem Sie die LINQ-Methodensyntax verwenden, falls erforderlich. Weitere Informationen zur LINQ-Abfragesyntax und -Methodensyntax finden Sie unter [LINQ-Abfragesyntax versus -Methodensyntax (C#)](/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq.md)> In Tabelle 1 sind die grundlegenden Themen gezeigt, mit denen Sie vertraut sein sollten, bevor Sie diesen Artikel durcharbeiten. 
  
**Tabelle 1. Grundlegende Konzepte für die Bearbeitung des Visio 2013-Dateiformats**

|**Titel des Artikels**|**Beschreibung**|
|:-----|:-----|
|[Einführung in das Visio-Dateiformat (.vsdx)](introduction-to-the-visio-file-formatvsdx.md) <br/> |In dieser allgemeinen Übersicht werden einige der wichtigsten Features des Visio 2013-Dateiformats beschrieben. Es werden die Open Packaging-Konventionen (OPC) und deren Anwendung auf das Visio 2013-Dateiformat erläutert. Es sind auch einige Unterschiede zwischen dem Visio 2013-Dateiformat und dem früheren Visio-XML-Zeichnungsdateiformat (.vdx) aufgeführt.  <br/> |
|[OPC: Ein neuer Standard für das Verpacken Ihrer Daten](/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data.md) <br/> |In diesem MSDN Magazine-Artikel werden die Open Packaging-Konventionen als Konzept beschrieben.  <br/> |
|[Grundlagen der Open Packaging-Konventionen](https://docs.microsoft.com/previous-versions/office/office-12/ee361919(v=office.12)) <br/> [Einführung in die Microsoft Office (2007) Open XML-Dateiformate](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12)) <br/> |In diesen beiden Artikeln wird erläutert, wie die Open Packaging-Konventionen auf Microsoft Office-Dateien angewendet wurden. Sie enthalten Beschreibungen der Funktionsweise von Beziehungen in einem Paket und enthalten auch einige Codebeispiele.  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>Erstellen einer VSDX-Datei und einer neuen Visual Studio-Lösung
<a name="vis15_ManipulateFF_CreateFile"> </a>

Bevor Sie beginnen, die Verfahren in diesem Artikel durchzuarbeiten, müssen Sie eine Visio 2013-Datei erstellen, die Sie öffnen und bearbeiten können. Die in den Codebeispielen in diesem Artikel verwendete Zeichnung enthält eine einzelne Seite mit zwei verbundenen Shapes; eines der Shapes ist dabei ein „Anfangs-/Ende“-Shape aus der Vorlage „ Standardflussdiagramm“.
  
Verwenden Sie das folgende Verfahren, um eine neue Visio 2013-Datei zur Verwendung in den übrigen Verfahren in diesem Artikel zu erstellen.
  
### <a name="to-create-new-file-in-visio-2013"></a>So erstellen Sie eine neue Datei in Visio 2013

1. Öffnen Sie Visio 2013.
    
2. Erstellen Sie ein neues Dokument basierend auf der Vorlage „Standardflussdiagramm“, indem Sie **Kategorien**, **Flussdiagramm**, **Standardflussdiagramm**, **Erstellen** auswählen.
    
3. Ziehen Sie aus dem Fenster **Shapes** ein **Anfangs-/Ende**-Shape auf den Zeichenbereich. 
    
4. Wählen Sie das neue Anfangs-/Ende-Shape im Zeichenbereich aus, und geben Sie „Prozess beginnen“ ein.
    
5. Ziehen Sie aus dem Fenster **Shapes** ein **Prozess**-Shape auf den Zeichenbereich. 
    
6. Wählen Sie das neue Prozess-Shape im Zeichenbereich aus, und geben Sie „Eine Aufgabe ausführen“ ein.
    
7. Wählen Sie im Kontextmenü für das Anfangs-/Ende-Shape **Dem Zeichenblatt einen Verbinder hinzufügen** aus, und ziehen Sie dann einen Verbinder zwischen dem Anfangs-/Ende- und dem Prozess-Shape auf dem Zeichenbereich, wie in Abbildung 1 dargestellt.
    
    **Abbildung 1. Einfache Visio 2013-Zeichnung**
    
     ![Ein mit einem Prozess-Shape verbundenes Anfangs-/Ende-Shape](media/vis15_SimpleFlowchart.png)
  
8. Speichern Sie die Datei auf dem Desktop als VSDX-Datei, indem Sie **Datei**, **Speichern unter**, **Computer**, **Desktop** auswählen.
    
    Geben Sie im Dialogfeld **Speichern unter** im Feld **Dateiname** „Visio-Paket“ ein, wählen Sie in der Liste **Dateityp** die Option **Visio-Zeichnung (\*.vsdx)** aus, und klicken Sie dann die auf Schaltfläche **Speichern**. 
    
9. Schließen Sie die Datei und dann Visio 2013.
    
> [!TIP]
> Manchmal öffnet Visio eine Datei selbst dann erfolgreich, wenn es Probleme mit der Datei gibt. Um sicherzustellen, dass Sie in Visio über Dateiprobleme benachrichtigt werden, sollten Sie beim Testen von Lösungen, bei denen Visio-Dateien auf Paketebene bearbeitet werden, Warnungen beim Öffnen von Dateien aktivieren. > Um Warnungen beim Öffnen von Dateien zu aktivieren, wählen Sie in Visio 2013 **Datei**, **Optionen**, **Erweitert** aus. Klicken Sie unter **Speichern/Öffnen** auf **Warnungen beim Öffnen einer Datei anzeigen**. 
  
Bei diesen Verfahren wird eine Windows-Konsolenanwendung zum Bearbeiten der Datei „Visio-Paket.vsdx“ verwendet. Verwenden Sie das folgende Verfahren, um eine neue Windows-Konsolenanwendung in Visual Studio 2012 zu erstellen und einzurichten.
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>So öffnen Sie eine neue Lösung in Visual Studio 2012

1. Klicken Sie im Menü **Datei** auf **Neu** und dann auf **Projekt**.
    
2. Erweitern Sie im Dialogfeld **Neues Projekt** entweder **Visual C#** oder **Visual Basic**, und wählen Sie dann **Windows**, **Konsolenanwendung** aus.
    
    Geben Sie im Feld **Name** „VisioFileAccessor“ ein, wählen Sie einen Speicherort für das Projekt aus, und klicken Sie dann auf die Schaltfläche **OK**. 
    
3. Wählen Sie im Menü **Projekt** **Verweis hinzufügen** aus. 
    
    Wählen Sie im Dialogfeld **Verweis-Manager** unter **Assemblys** die Option **Framework** aus, und fügen Sie dann einen Verweis auf die Komponenten **System.Xml** und **WindowsBase** hinzu. 
    
4. Fügen Sie in der Datei „Program.cs“ oder „Module1.vb“ für das Projekt die folgenden **Using**-Direktiven (**Imports**-Anweisungen in Visual Basic) hinzu: 
    
    ```cs
    using System.Xml;
    using System.Xml.Linq;
    using System.IO;
    using System.IO.Packaging;
    using System.Text;
    
    ```

    ```vb
    Imports System.Xml
    Imports System.Xml.Linq
    Imports System.IO
    Imports System.IO.Packaging
    Imports System.Text
    
    ```

5. Fügen Sie ebenfalls in der Datei „Program.cs“ oder „Module1.vb“ vor dem Ende der **Main**-Methode der **Program**-Klasse (**Module1** in Visual Basic) den folgenden Code hinzu, durch den die Ausführung der Konsolenanwendung angehalten wird, bis der Benutzer eine Taste drückt. 
    
    ```cs
    // This code stops the execution of the console application
    // so you can read the output.
    Console.WriteLine("Press any key to continue ...");
    Console.ReadKey();
    
    ```

    ```vb
    ' This code stops the execution of the console application
    ' so you can read the output.
    Console.WriteLine("Press any key to continue ...")
    Console.ReadKey()
    ```

## <a name="open-a-visio-2013-file-as-a-package"></a>Öffnen einer Visio 2013-Datei als Paket
<a name="vis15_ManipulateFF_OpenPackage"> </a>

Bevor Sie die Daten in der Datei bearbeiten können, müssen Sie zuerst die Datei in einem [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8)-Objekt öffnen, das im [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8)-Namespace enthalten ist. Das **Package**-Objekt stellt die Visio-Datei als Ganzes dar. Es macht Elemente verfügbar, mit denen Sie einzelne Dokumentteile innerhalb des Dateipakets auswählen können. Die **Package**-Klasse macht insbesondere die statische [Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8)-Methode verfügbar, die Sie zum Öffnen einer Datei als Paket verwenden. Sie macht auch eine [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8)-Methode zum Schließen des Pakets verfügbar, wenn Sie damit fertig sind. 
  
> [!TIP]
> Verwenden Sie als bewährte Methode einen **Using**-Block, um die Visio-Datei im **Package**-Objekt zu öffnen, damit Sie das Dateipaket nicht explizit schließen müssen, wenn Sie damit fertig sind. Sie können die **Package.Close**-Methode auch explizit im **finally**-Block einer **try/catch/finally**-Konstruktion aufrufen. 
  
Verwenden Sie den folgenden Code, um den vollständigen Pfad der Datei „Visio-Package.vsdx“ mithilfe eines [FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8)-Objekts abzurufen, übergeben Sie den Pfad als Argument an die **Package.Open**-Methode, und geben Sie dann ein **Package**-Objekt an den aufrufenden Code zurück. 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>So öffnen Sie eine VSDX-Datei als Paket

1. Fügen Sie nach der **Main**-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) den folgenden Code hinzu. 
    
    ```cs
    private static Package OpenPackage(string fileName, 
        Environment.SpecialFolder folder)
    {
        Package visioPackage = null;
        // Get a reference to the location 
        // where the Visio file is stored.
        string directoryPath = System.Environment.GetFolderPath(
            folder);
        DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
        // Get the Visio file from the location.
        FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
        if (fileInfos.Count() > 0)
        {
            FileInfo fileInfo = fileInfos[0];
            string filePathName = fileInfo.FullName;
            // Open the Visio file as a package with
            // read/write file access.
            visioPackage = Package.Open(
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite);
            }
            // Return the Visio file as a package.
            return visioPackage;
    }
    ```

    ```vb
    Private Function OpenPackage(fileName As String, _
        folder As Environment.SpecialFolder) As Package
        Dim visioPackage As Package = Nothing
        ' Get a reference to the location
        ' where the Visio file is stored.
        Dim directoryPath As String = System.Environment.GetFolderPath( _
            folder)
        Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
        ' Get the Visio file from the location.
        Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
        If (fileInfos.Count() > 0) Then
            Dim fileInfo As FileInfo = fileInfos(0)
            Dim filePathName As String = fileInfo.FullName
            ' Open the Visio file as a package 
            ' with read/write access.
            visioPackage = Package.Open( _
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite)
            End If
        ' Return the Visio file as a package.
        Return visioPackage
    End Function
    
    ```

2. Fügen Sie in der **Main**-Methode der **Program**-Klasse (oder **Module1** in Visual Basic) den folgenden Code hinzu. 
    
    ```cs
    // Open the Visio file in a Package object.
    using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
        Environment.SpecialFolder.Desktop))
    {
    }
    
    ```

    ```vb
    ' Open the Visio file in a Package object.
    Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
        Environment.SpecialFolder.Desktop)
    End Using
    
    ```

## <a name="select-and-read-package-parts-from-a-package"></a>Auswählen und Lesen von Paketteilen aus einem Paket
<a name="vis15_ManipulateFF_SelectPart"> </a>

Nachdem Sie die Visio 2013-Datei als Paket geöffnet haben, können Sie auf die darin enthaltenen Dokumentteile mithilfe der [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx)-Klasse zugreifen, die im **System.IO.Packaging**-Namespace enthalten ist. **PackagePart**-Objekte können einzeln oder als Sammlung instanziiert werden. Die **Package**-Klasse macht eine [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx)-Methode und eine [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx)-Methode zum Abrufen von **PackagePart**-Objekten aus dem **Package** verfügbar. Die **Package.GetParts**-Methode gibt eine Instanz der [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx)-Klasse zurück, mit der Sie dann wie mit jeder anderen Sammlung, die die [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2)-Schnittstelle implementiert, interagieren können. 
  
Verwenden Sie den Code in dem folgenden Verfahren, um ein **PackagePartCollection**-Objekt aus der **Package** als Sammlung abzurufen, durchlaufen Sie die **PackagePart**-Objekte in der Sammlung, und schreiben Sie den URI und Inhaltstyp von allen **PackagePart** in die Konsole. 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>So durchlaufen Sie die Paketteile in einem Paket

1. Fügen Sie nach der `OpenPackage`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) den folgenden Code hinzu. 
    
    ```cs
    private static void IteratePackageParts(Package filePackage)
    {
        
        // Get all of the package parts contained in the package
        // and then write the URI and content type of each one to the console.
        PackagePartCollection packageParts = filePackage.GetParts();
        foreach (PackagePart part in packageParts)
        {
            Console.WriteLine("Package part URI: {0}", part.Uri);
            Console.WriteLine("Content type: {0}", part.ContentType.ToString());
        }
    }
    
    ```

    ```vb
    Private Sub IteratePackageParts(filePackage As Package)
        ' Get all of the package parts contained in the package
        ' and then write the URI and content type of each one to the console.
        Dim packageParts As PackagePartCollection = filePackage.GetParts()
        For Each part In packageParts
            Console.WriteLine("Package part: {0}", part.Uri)
            Console.WriteLine("Content type: {0}", part.ContentType.ToString())
        Next
    End Sub 
    
    ```

2. Fügen Sie den folgenden Code innerhalb des **using**-Blocks in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) hinzu: 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
Die Konsolenanwendung erstellt eine Ausgabe, die der folgenden ähnlich ist (ein Teil der Ausgabe wurde aus Platzgründen weggelassen):
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
In den meisten Fällen müssen Sie einen **PackagePart** auswählen, ohne alle anderen zu durchlaufen. Sie erhalten ein **PackagePart**-Objekt aus einem **Package**, indem Sie seine Beziehung zum **Package** oder einem anderen **PackagePart** verwenden. Eine Beziehung im Visio 2013-Dateiformat ist eine diskrete Einheit, die beschreibt, wie ein Dokumentteil mit dem Dateipaket verknüpft ist oder wie die beiden Dokumentteile miteinander verknüpft sind. Das Visio 2013-Dateipaket selbst hat beispielsweise eine Beziehung zu seinem Visio-Dokumentteil, und das Visio-Dokumentteil hat eine Beziehung zu dem Windows-Teil. Diese Beziehungen werden als Instanzen der [PackageRelationship](/dotnet/api/system.io.packaging.packagerelationship.md)- oder [PackageRelationshipCollection](/dotnet/api/system.io.packaging.packagerelationshipcollection.md)-Klasse dargestellt. 

Die **Package**-Klasse macht mehrere Methoden zum Abrufen der in ihr enthaltenen **PackageRelationship**- oder **PackageRelationshipCollection**-Objekte verfügbar. Sie können die [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx)-Methode verwenden, um ein **PackageRelationshipCollection**-Objekt zu instanziieren, das **PackageRelationship**-Objekte eines einzigen bestimmten Typs enthält. Natürlich ist es für die Verwendung der **Package.GetRelationshipsByType**-Methode erforderlich, dass Sie den benötigten Beziehungstyp kennen. Beziehungstypen sind Zeichenfolgen im XML-Namespaceformat. Beispielsweise ist der Beziehungstyp des Visio-Dokumentteils https://schemas.microsoft.com/visio/2010/relationships/document. 
  
Sobald Sie die Beziehung eines **PackagePart** zum **Package** oder zu einem anderen **PackagePart** kennen (d. h., Sie haben ein **PackageRelationship**-Objekt, das auf den gewünschten **PackagePart** verweist), können Sie diese Beziehung verwenden, um den URI dieses **PackagePart** abzurufen. Sie übergeben dann den URI an die **Package.GetPart**-Methode, um den **PackagePart** zurückzugeben.
  
> [!NOTE]
> Sie können auch einen Verweis auf einen bestimmten **PackagePart** abrufen, indem Sie nur die **Package.GetPart**-Methode und den URI des **PackagePart** verwenden. Auf diese Weise umgehen Sie den Schritt, in dem Sie die Beziehungen des Paketteils abrufen. Einige Paketteile im Visio-Dateipaket können jedoch an anderen Speicherorten als ihren Standardspeicherorten in einem Paket gespeichert werden. Sie können nicht davon ausgehen, dass sich ein Paketteil für jede Datei immer an demselben URI befindet. > In diesem Fall wird stattdessen empfohlen, Beziehungen zu verwenden, um auf einzelne **PackagePart**-Objekte zuzugreifen. 
  
Gehen Sie folgendermaßen vor, um einen **PackagePart** (das Visio-Dokumentteil) mithilfe der **PackageRelationship** aus dem **Package** abzurufen, das auf das Teil verweist. 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>So wählen Sie ein bestimmtes Paketteil im Paket nach Beziehung aus

1. Fügen Sie nach der `IteratePackageParts`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) die folgende Methode hinzu. 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        string relationship)
    {
        
        // Use the namespace that describes the relationship 
        // to get the relationship.
        PackageRelationship packageRel = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart part = null;
        // If the Visio file package contains this type of relationship with 
        // one of its parts, return that part.
        if (packageRel != null)
        {
            // Clean up the URI using a helper class and then get the part.
            Uri docUri = PackUriHelper.ResolvePartUri(
                new Uri("/", UriKind.Relative), packageRel.TargetUri);
            part = filePackage.GetPart(docUri);
        }
        return part;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, relationship As String) _
        As PackagePart
        ' Use the namespace that describes the relationship 
        ' to get the relationship.
        Dim packageRel As PackageRelationship = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
        Dim part As PackagePart = Nothing
        ' If the Visio file package contains this type of relationship with 
        ' one of its parts, return that part.
        If Not IsNothing(packageRel) Then
            ' Clean up the URI using a helper class and then get the part.
            Dim docUri = PackUriHelper.ResolvePartUri( _
                New Uri("/", UriKind.Relative), packageRel.TargetUri)
            part = filePackage.GetPart(docUri)
        End If
        Return part
    End Function
    
    ```

2. Ersetzen Sie den Code im **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) durch den folgenden Code: 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "http://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "http://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

Wie bereits erwähnt, können Sie auch **PackagePart**-Objekte mithilfe ihrer Beziehung zu anderen **PackagePart**-Objekten abrufen. Dies ist wichtig, da bei einem Visio-Dokument beliebiger Komplexität der Großteil der **PackagePart**-Objekte keine Beziehung zum **Package** hat. Beispielsweise hat ein einzelnes Seiteninhaltsteil in dem Dateipaket (d. h. /visio/pages/page1.xml) eine Beziehung zu dem Seitenindexteil (d. h. /visio/pages/pages.xml), jedoch nicht zum Dateipaket selbst. Wenn Sie nicht über den genauen URI der einzelnen Seite in dem Paket verfügen, können Sie seine Beziehung zu dem Seitenindexteil verwenden, um einen Verweis darauf abzurufen.
  
Die **PackagePart**-Klasse macht eine [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx)-Methode verfügbar, die Sie verwenden können, um ein **PackageRelationshipCollection**-Objekt zurückzugeben, das nur einen Typ von **PackageRelationship**-Objekt enthält. Nachdem Sie die **PackageRelationshipCollection** haben, können Sie die benötigte **PackageRelationship** aus der Sammlung auswählen und dann auf das **PackagePart**-Objekt verweisen. 
  
Verwenden Sie den folgenden Code, um ein **PackagePart** aus dem **Package** mithilfe seiner Beziehung zu (Abrufen eines **PackageRelationship**-Objekts aus) einem anderen **PackagePart** abzurufen.
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>So wählen Sie ein bestimmtes Paketteil durch seine Beziehung zu einem anderen Paketteil aus

1. Fügen Sie nach der `GetPackagePart`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) die folgende Überladungsmethode hinzu. 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        PackagePart sourcePart, string relationship)
    {
        // This gets only the first PackagePart that shares the relationship
        // with the PackagePart passed in as an argument. You can modify the code
        // here to return a different PackageRelationship from the collection.
        PackageRelationship packageRel = 
            sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart relatedPart = null;
        if (packageRel != null)
        {
            // Use the PackUriHelper class to determine the URI of PackagePart
            // that has the specified relationship to the PackagePart passed in
            // as an argument.
            Uri partUri = PackUriHelper.ResolvePartUri(
                sourcePart.Uri, packageRel.TargetUri);
            relatedPart = filePackage.GetPart(partUri);
        }
        return relatedPart;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, 
        sourcePart As PackagePart, relationship As String) As PackagePart
        ' This gets only the first PackagePart that shares the relationship
        ' with the PackagePart passed in as an argument. You can modify the
        ' code to return a different PackageRelationship from the collection.
        Dim packageRel As PackageRelationship = sourcePart. _
            GetRelationshipsByType(relationship).FirstOrDefault()
        Dim relatedPart As PackagePart = Nothing
        If Not IsNothing(packageRel) Then
            ' Use the PackUriHelper class to determine the URI of the 
            ' PackagePart that has the specified relationship to the 
            ' PackagePart passed in as an argument.
            Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
                sourcePart.Uri, packageRel.TargetUri)
            relatedPart = filePackage.GetPart(partUri)
        End If
        Return relatedPart
    End Function
    ```

2. Fügen Sie den folgenden Code zum **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) unter dem Code aus dem vorherigen Verfahren hinzu: (Löschen Sie nicht den Code, den Sie im vorherigen Verfahren hinzugefügt haben.)  
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "http://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "http://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "http://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "http://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

Bevor Sie Änderungen an dem XML-Code vornehmen können, der in einem Dokumentteil enthalten ist, müssen Sie zuerst das XML-Dokument in ein Objekt laden, mit dem Sie mithilfe der [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx)-Klasse oder der [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx)-Klasse den XML-Code lesen können. Beide Klassen machen Methoden für Aufgaben verfügbar, z. B. das Auswählen von XML-Elementen, die in XML-Dokumenten enthalten sind, das Erstellen, Lesen und Schreiben von Attributen sowie das Einfügen neuer XML-Elemente in ein Dokument. 
  
Mit der **XDocument**-Klasse können Sie die XML-Daten mithilfe von LINQ abfragen. Mit LINQ können Sie ganz einfach einzelne Elemente aus einem XML-Dokument auswählen, indem Sie Abfragen erstellen anstatt alle Elemente in einer Sammlung zu durchlaufen und nach den benötigten Elementen zu suchen. Aus diesen Gründen verwenden die folgenden Verfahren in diesem Artikel die **XDocument**-Klasse und andere Klassen des **System.Xml.Linq**-Namespace für die Arbeit mit XML. 
  
Verwenden Sie das folgende Verfahren, um ein **PackagePart** als XML-Dokument in einem **XDocument**-Objekt zu öffnen. 
  
### <a name="to-read-the-xml-in-a-package-part"></a>So lesen Sie den XML-Code in einem Paketteil

1. Fügen Sie nach der letzten Überladung der `GetPackagePart`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) die folgende Methode hinzu.  
    
    ```cs
    private static XDocument GetXMLFromPart(PackagePart packagePart)
    {
        XDocument partXml = null;
        // Open the packagePart as a stream and then 
        // open the stream in an XDocument object.
        Stream partStream = packagePart.GetStream();
        partXml = XDocument.Load(partStream);
        return partXml;
    }
    ```

    ```vb
    Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
        Dim partXml As XDocument = Nothing
        ' Open the packagePart as a stream and then
        ' open the stream in an an XDocument object.
        Dim partStream As Stream = packagePart.GetStream()
        partXml = XDocument.Load(partStream)
        Return partXml
    End Function
    ```

2. Fügen Sie den folgenden Code zum **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) unter dem Code aus dem vorherigen Verfahren hinzu: 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a>Auswählen und Ändern von XML-Daten in einem Paketteil
<a name="vis15_ManipulateFF_ChangeXML"> </a>

Nachdem Sie ein Dokumentteil in ein **XDocument**-Objekt geladen haben, können Sie LINQ zum Auswählen von XML-Elementen und zum Vornehmen von Änderungen an dem XML-Dokument verwenden. Sie können XML-Daten ändern, hinzufügen oder entfernen und dann das XML-Dokument wieder in dem Dokumentteil speichern. 
  
Die häufigste Aufgabe beim Bearbeiten des Visio-Dateiformats besteht in der Auswahl bestimmter XML-Elemente oder Sammlungen von Elementen im Dokument. Der **System.Xml.Linq**-Namespace beinhaltet die [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx)-Klasse, die ein XML-Element darstellt. Die **XElement**-Klasse ermöglicht den Zugriff auf die Daten in der Visio-Datei auf einer präzisen Ebene, von einzelnen **Shape**-Elementen hin zu **ValidationRule**-Elementen (als Beispiele). 
  
Verwenden Sie den folgenden Code, um die **Shape**-Elemente aus einem **XDocument** (mit einem Seiteninhaltsteil) und dann ein bestimmtes **Shape**-Element auszuwählen. 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>So wählen Sie ein bestimmtes Element in einem Paketteil aus

1. Fügen Sie nach der `GetXMLFromPart`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) die folgende Methode hinzu. 
        
    ```cs
    private static IEnumerable<XElement> GetXElementsByName(
        XDocument packagePart, string elementType)
    {
        // Construct a LINQ query that selects elements by their element type.
        IEnumerable<XElement> elements = 
            from element in packagePart.Descendants() 
            where element.Name.LocalName == elementType 
            select element;
        // Return the selected elements to the calling code.
        return elements.DefaultIfEmpty(null);
    }
    
    ```

    ```vb
    Private Function GetXElementsByName(partXML As XDocument, _
        elementType As String) As IEnumerable(Of XElement)
        ' Construct a LINQ query that selects elements by their element type.
        Dim elements As IEnumerable(Of XElement) =
            From element In partXML.Descendants()
            Where element.Name.LocalName = elementType
            Select element
        ' If there aren't any elements of the specified type
        ' in the document, return Nothing to the calling code.
        Return elements.DefaultIfEmpty(Nothing)
    End Function
    ```

2. Fügen Sie nach der `GetXElementsByName`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt die folgende Methode hinzu. 
    
    ```cs
    private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
        string attributeName, string attributeValue) 
    {
        // Construct a LINQ query that selects elements from a group
        // of elements by the value of a specific attribute.
        IEnumerable<XElement> selectedElements = 
            from el in elements
            where el.Attribute(attributeName).Value == attributeValue
            select el;
        // If there aren't any elements of the specified type
        // with the specified attribute value in the document,
        // return null to the calling code.
        return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
    }
    ```

    ```vb
    Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
        attributeName As String, attributeValue As String) As XElement
        ' Construct a LINQ query that selects elements from a group
        ' of elements by the value of a specific attribute.
        Dim selectedElements As IEnumerable(Of XElement) =
            From el In elements
            Where el.Attribute(attributeName).Value = attributeValue
            Select el
        ' If there aren't any elements of the specified type 
        ' with the specified attribute value in the document,
        ' return Nothing to the calling code.
        Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
    End Function
    
    ```

3. Fügen Sie den folgenden Code zum **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) unter dem Code aus dem vorherigen Verfahren hinzu: 
    
    ```cs
    // Get all of the shapes from the page by getting
    // all of the Shape elements from the pageXML document.
    IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
    // Select a Shape element from the shapes on the page by 
    // its name. You can modify this code to select elements
    // by other attributes and their values.
    XElement startEndShapeXML = 
        GetXElementByAttribute(shapesXML, "NameU", "Start/End");
    
    ```

    ```vb
    ' Get all of the shapes from the page by getting
    ' all of the Shape elements from the pageXML document.
    Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
        pageXML, "Shape")
    ' Select a Shape element from the shapes on the page by
    ' its name. You can modify this code to select elements
    ' by other attributes and their values.
    Dim startEndShapeXML As XElement = GetXElementByAttribute( _
        shapesXML, "NameU", "Start/End")
    ```

Nachdem Sie einen Verweis auf ein **XElement**-Objekt innerhalb eines **XDocument**-Objekts abgerufen haben, können Sie diesen wie alle anderen XML-Daten bearbeiten und auf diese Weise die in der Visio-Datei enthaltenen Daten ändern. Wenn ein Shape beim Öffnen in Visio Text aufweist, enthält das entsprechende **Shape**-Element mindestens ein **Text**-Element. Wenn Sie den Wert dieses **Text**-Elements ändern, wird der Text des Shapes geändert, wenn die Datei in Visio angezeigt wird. 
  
Fügen Sie den folgenden Code zu dem **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) hinzu, um den Text in dem Anfangs-/Ende-Shape von „Prozess beginnen“ in „Prozess anfangen“ zu ändern. 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> Im vorherigen Codebeispiel weisen der vorhandene Shape-Text und die zum Ersetzen des Texts verwendete Zeichenfolge die gleiche Anzahl von Zeichen auf. Beachten Sie auch, dass sich durch die LINQ-Abfrage der Wert des letzten untergeordneten Knotens des zurückgegebenen Elements ändert (in diesem Fall ein Textknoten). Dies geschieht, um zu verhindern, dass die Einstellungen des **cp**-Elements, das ein untergeordnetes Element des **Text**-Elements ist, geändert werden. > Dies kann eine Dateiinstabilität verursachen, wenn Sie Shape-Text programmgesteuert durch Überschreiben aller untergeordneten Elemente des **Text**-Elements ändern. Wie im Beispiel oben wird die Textformatierung durch **cp**-Elemente unter dem **Text**-Element in der Datei dargestellt. Die Definition der Formatierung wird im übergeordneten **Section**-Element gespeichert. Wenn diese beiden Informationen inkonsistent werden, verhält sich die Datei möglicherweise nicht wie erwartet. Visio beseitigt viele Inkonsistenzen, es ist aber besser sicherzustellen, dass alle programmgesteuerten Änderungen konsistent sind, damit Sie das endgültige Verhalten der Datei steuern. 
  
Wenn Sie Änderungen an dem XML-Code eines Dokumentteils vornehmen, sind diese Änderungen nur im Speicher vorhanden. Um die Änderungen in der Datei zu speichern, müssen Sie die XML-Daten wieder in dem Dokumentteil speichern.
  
Der folgende Code verwendet die [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx)-Klasse und die [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx)-Klasse, um die XML-Daten zurück in den Paketteil zu schreiben. Sie können zwar die [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx)-Methode verwenden, um die XML-Daten wieder in dem Teil zu speichern, mit der **XmlWriter**- und **XmlWriterSettings**-Klasse können Sie jedoch eine genauere Kontrolle über die Ausgabe erreichen und den Typ der Codierung angeben. Die **XDocument**-Klasse macht eine [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx)-Methode verfügbar, die ein **XmlWriter**-Objekt verwendet und XML wieder in einen Stream schreibt. 
  
Gehen Sie folgendermaßen vor, um die XML-Daten von der Visio-Seite im Seiteninhaltsteil zu speichern.
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>So speichern Sie die geänderten XML-Daten wieder in dem Paket

1. Fügen Sie nach der `GetXElementByAttribute`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt die folgende Methode hinzu. 
    
    ```cs
    private static void SaveXDocumentToPart(PackagePart packagePart, 
        XDocument partXML)
    {
        
        // Create a new XmlWriterSettings object to 
        // define the characteristics for the XmlWriter
        XmlWriterSettings partWriterSettings = new XmlWriterSettings();
        partWriterSettings.Encoding = Encoding.UTF8;
        // Create a new XmlWriter and then write the XML
        // back to the document part.
        XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
            partWriterSettings);
        partXML.WriteTo(partWriter);
        // Flush and close the XmlWriter.
        partWriter.Flush();
        partWriter.Close();
    }
    ```

    ```vb
    Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
        partXML As XDocument)
        ' Create a new XmlWriterSettings object to 
        ' define the characteristics for the XmlWriter.
        Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
        partWriterSettings.Encoding = Encoding.UTF8
        ' Create a new XmlWriter and then write the XML
        ' back to the document part.
        Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
        partXML.WriteTo(partWriter)
        ' Flush and close the XmlWriter.
        partWriter.Flush()
        partWriter.Close()
    End Sub
    ```

2. Fügen Sie den folgenden Code zum **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) unter dem Code aus dem vorherigen Verfahren hinzu: 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
4. Öffnen Sie die Datei „Visio-Paket.vsdx“ in Visio 2013. 
    
Das Anfangs-/Ende-Shape sollte nun den Text „Prozess anfangen“ enthalten.
  
## <a name="recalculate-data-in-the-file"></a>Neuberechnen von Daten in der Datei

Einige Änderungen an den Daten in einer Datei machen es möglicherweise erforderlich, dass Visio das Dokument beim Öffnen der Datei neu berechnet. Visio bietet viel Logik für ein Diagramm, insbesondere für Shape-Beziehungen (d. h. wenn ein Shape von einem anderen abhängt) und Verbindungs-Shapes. Wenn ein Teil der Daten, auf denen die benutzerdefinierte Logik beruht, geändert wird, muss Visio die Änderungen an alle betroffenen berechneten Daten in der Datei verteilen. 
  
Das Visio 2013-Dateiformat enthält unterschiedliche Verfahren, die Sie zum Neuberechnen von Daten in der Datei verwenden können. Es gibt drei Arten von Szenarien, die Sie berücksichtigen müssen, wenn Sie überlegen, ob Sie die Visio-Datei neu berechnen und wie Sie dafür vorgehen:
  
- Die geänderten Daten haben keine Auswirkungen auf andere Werte in dem Dateiformat. Sie müssen keine zusätzlichen Anweisungen zu Visio hinzufügen, um das Dokument neu zu berechnen. Wie zuvor gezeigt, können Sie den Text eines Shapes häufig ändern, ohne das Dokument neu zu berechnen.
    
- Die Änderungen an den Daten sind auf das Ändern der Werte von ShapeSheet-Zellen im XML-Code beschränkt, und gibt es andere ShapeSheet-Werte, die von diesen Daten abhängig sind. In diesem Fall müssen Sie eine XML-Verarbeitungsanweisung (mithilfe der [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)-Klasse) zu dem **Cell**-Element hinzufügen, das geändert wurde. Die **ThemeIndex**-Zelle für ein Shape hat beispielsweise Auswirkungen auf die Werte mehrerer anderer ShapeSheet-Zellen, die in dem Shape enthalten sind. Wenn Sie die **ThemeIndex**-Zelle innerhalb der Datei selbst ändern (z. B. das **Cell**-Element mit dem **N**-Wert "ThemeIndex"), müssen Sie eine Verarbeitungsanweisung zu dem **Cell**-Element hinzufügen, damit die abhängigen Werte aktualisiert werden. 
    
- Die Änderungen an den Daten haben Einfluss auf die Position eines Verbinders oder von Verbindungspunkten. Eine weitere Situation besteht, wenn es viele Änderungen an den ShapeSheet-Daten gibt und Sie das ganze Dokument mit einer einzigen Anweisung neu berechnen möchten (anstatt einzelne Verarbeitungsanweisungen für jede Änderung hinzuzufügen). In diesem Fall können Sie Visio anweisen, das gesamte Dokument beim Öffnen neu zu berechnen. Hierfür fügen Sie eine **RecalcDocument**-Eigenschaft zu dem Teil des Visio-Pakets für benutzerdefinierte Dateieigenschaften (/docProps/custom.XML) hinzu. Das Anpassen der Position oder der Größe von Shapes in einem verbundenen Diagramm ist ein Beispiel für diese Art von Szenario. 
    
    Bitte beachten Sie, dass es sich hierbei in puncto Leistung um die kostspieligste Option handelt.
    
Gehen Sie folgendermaßen vor, um ein **Cell**-Element in ein **Shape**-Element einzufügen, wobei andere **Cell**-Elemente in dem gleichen **Shape** aufgrund des neuen Werts neu berechnet werden müssen. Das neue **Cell**-Element enthält eine Verarbeitungsanweisung als untergeordnetes Element, um Visio darüber zu informieren, dass lokal einige Neuberechnungen ausgeführt werden müssen. 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>So berechnen Sie die Werte für ein einzelnes Shape neu

1. Ersetzen Sie den Code aus den beiden vorherigen Beispielen (Ändern des Shape-Texts und Aufrufen von `SaveXDocumentToPart`) im **Using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) durch den folgenden Code. 
    
    ```cs
    // Insert a new Cell element in the Start/End shape that adds an arbitrary
    // local ThemeIndex value. This code assumes that the shape does not 
    // already have a local ThemeIndex cell.
    startEndShapeXML.Add(new XElement("Cell",
        new XAttribute("N", "ThemeIndex"),
        new XAttribute("V", "25"),
        new XProcessingInstruction("NewValue", "V")));
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Insert a new Cell element in the shape that adds an arbitrary local
    ' ThemeIndex value. This code assumes that the shape does not
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
3. Öffnen Sie die Datei „Visio-Paket.vsdx“ in Visio 2013. Das Anfangs-/Ende-Shape sollte nun eine andere Füllfarbe haben.
    
Die Farbe des Shapes basiert auf dem Wert der **ThemeIndex**-Zelle – sie bestimmt, von welchen aktiven Designs das Shape erbt. Im vorherigen Beispiel wird festgelegt, dass das Shape von einem anderen Design erbt (die **ThemeIndex**-Zelle ist auf den Wert "25" festgelegt). Wenn Sie keine Verarbeitungsanweisung verwenden, wird die Textfarbe des Shapes – die auch von der **ThemeIndex**-Zelle beeinflusst wird – nicht neu berechnet. Die Füllfarbe des Shapes würde sich in Weiß ändern, sein Text würde jedoch weiß bleiben – sodass der Text nicht lesbar wäre. Ohne die Verarbeitungsanweisung aktualisiert Visio das Shape möglicherweise auch später, sodass sich die Datei in einem instabilen Zustand befindet, in dem Formatierungswerte des Shapes unvorhersehbar aktualisiert werden könnten. 
  
Wenn Sie Daten in der Datei ändern, aufgrund derer Visio das Dokument neu berechnen muss (z. B. Ändern der Position eines verbundenen Shapes und damit einhergehende Umleitung der Verbinder), müssen Sie eine Neuberechnungsanweisung zur Visio-Datei hinzufügen. Die Anweisung wird durch Hinzufügen eines **property**-Elements mit einem **name**-Attributwert von „RecalcDocument“ zu dem XML-Code des Teils des Visio-Dateipakets für benutzerdefinierte Dateieigenschaften erstellt. Als bewährte Methode sollten Sie den Teil für benutzerdefinierte Dateieigenschaften überprüfen, um sicherzustellen, dass nicht bereits eine "RecalcDocument"-Anweisung in der Datei registriert wurde. 
  
Verwenden Sie den folgenden Code, um den Wert der **PinY**-Zelle des Anfangs-/Ende-Shapes aus den vorherigen Beispielen zu ändern. Der Code wählt das **Cell**-Element aus, das die **PinY**-Zelldaten als **XElement**-Objekt enthält, indem der Wert seines **N**-Attributs verwendet wird. Der Code fügt dann eine Neuberechnungsanweisung zu dem Teil der Visio-Datei für benutzerdefinierte Dateieigenschaften hinzu. 
  
> [!NOTE]
> Dieser Code basiert auf der `GetPackagePart`- und `SaveXDocumentToPart`-Methode, die zuvor erstellt wurden. 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>So berechnen Sie das gesamte Dokument beim Öffnen neu

1. Fügen Sie nach der `SaveXDocumentToPart`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt die folgende Methode hinzu. 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "http://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
            "custom-properties");
        XDocument customPartXML = GetXMLFromPart(customPart);
        // Check to see whether document recalculation has already been 
        // set for this document. If it hasn't, use the integer
        // value returned by CheckForRecalc as the property ID.
        int pidValue = CheckForRecalc(customPartXML);
        if (pidValue > -1)
        {
            XElement customPartRoot = customPartXML.Elements().ElementAt(0);
            // Two XML namespaces are needed to add XML data to this 
            // document. Here, we're using the GetNamespaceOfPrefix and 
            // GetDefaultNamespace methods to get the namespaces that 
            // we need. You can specify the exact strings for the 
            // namespaces, but that is not recommended.
            XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
            XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
            // Construct the XML for the new property in the XDocument.Add method.
            // This ensures that the XNamespace objects will resolve properly, 
            // apply the correct prefix, and will not default to an empty namespace.
            customPartRoot.Add(
                new XElement(customPropsSchemaNS + "property",
                    new XAttribute("pid", pidValue.ToString()),
                    new XAttribute("name", "RecalcDocument"),
                    new XAttribute("fmtid", 
                        "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                    new XElement(customVTypesNS + "bool", "true")
                ));
        }
        // Save the Custom Properties package part back to the package.
        SaveXDocumentToPart(customPart, customPartXML);
    }
    ```

    ```vb
    Private Sub RecalcDocument(filePackage As Package)
            ' Get the Custom File Properties part from the package and
            ' then extract the XML from it.
            Dim customPart As PackagePart = GetPackagePart(filePackage, _
                "http://schemas.openxmlformats.org/officeDocument/2006/" + _
                "relationships/custom-properties")
            Dim customPartXML As XDocument = GetXMLFromPart(customPart)
            ' Check to see whether document recalculation has already been
            ' set for this document. If it hasn't, use the integer
            ' value returned by CheckForRecalc as the property ID.
            Dim pidValue As Integer = CheckForRecalc(customPartXML)
            If (pidValue > 1) Then
                Dim customPartRoot As XElement = _
                    customPartXML.Elements().ElementAt(0)
                ' Two XML namespaces are needed to add XML data to this 
                ' document. Here, we're using the GetNamespaceOfPrefix and
                ' GetDefaultNamespace methods to get the namespaces that
                ' we need. You can specify the exact strings for the 
                ' namespaces, but that is not recommended.
                Dim customVTypesNS As XNamespace = _
                    customPartRoot.GetNamespaceOfPrefix("vt")
                Dim customPropsSchemaNS As XNamespace = _
                    customPartRoot.GetDefaultNamespace()
                ' Contruct the XML for the new property in the XDocument.Add
                ' method. This ensures that the XML namespaces resolve 
                ' properly, apply the correct prefix, and do not default to 
                ' an empty namespace.
                customPartRoot.Add( _
                    New XElement(customPropsSchemaNS + "property", _
                        New XAttribute("pid", pidValue.ToString()), _
                        New XAttribute("name", "RecalcDocument"), _
                        New XAttribute("fmtid", _
                            "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                        New XElement(customVTypesNS + "bool", "true") _
                ))
            ' Save the Custom Properties package part back to the package.
            SaveXDocumentToPart(customPart, customPartXML)
            End If
        End Sub
    ```

2. Fügen Sie nach der `RecalcDocument`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt die folgende Methode hinzu. 
    
    ```cs
    private static int CheckForRecalc(XDocument customPropsXDoc) 
    {
        
        // Set the inital pidValue to -1, which is not an allowed value.
        // The calling code tests to see whether the pidValue is 
        // greater than -1.
        int pidValue = -1;
        // Get all of the property elements from the document. 
        IEnumerable<XElement> props = GetXElementsByName(
            customPropsXDoc, "property");
        // Get the RecalcDocument property from the document if it exists already.
        XElement recalcProp = GetXElementByAttribute(props, 
            "name", "RecalcDocument");
        // If there is already a RecalcDocument instruction in the 
        // Custom File Properties part, then we don't need to add another one. 
        // Otherwise, we need to create a unique pid value.
        if (recalcProp != null)
        {
            return pidValue;
        }
        else
        {
            // Get all of the pid values of the property elements and then
            // convert the IEnumerable object into an array.
            IEnumerable<string> propIDs = 
                from prop in props
                where prop.Name.LocalName == "property"
                select prop.Attribute("pid").Value;
            string[] propIDArray = propIDs.ToArray();
            // Increment this id value until a unique value is found.
            // This starts at 2, because 0 and 1 are not valid pid values.
            int id = 2;
            while (pidValue == -1)
            {
                if (propIDArray.Contains(id.ToString()))
                {
                    id++;
                }
                else
                {
                    pidValue = id;
                }
            }
        }
        return pidValue;
    }
    
    ```

    ```vb
    Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
        ' Set the initial pidValue to -1, which is not an allowed value. 
        ' The calling code test to see whether the pidValue is
        ' greater than -1.
        Dim pidValue As Integer = -1
        ' Get all of the property elements from the document.
        Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
            customPropsXDoc, "property")
        ' Get the RecalcDocument property from the document if 
        ' it exists already.
        Dim recalcProp As XElement = GetXElementByAttribute(props, _
            "name", "RecalcDocument")
        ' If there is already a RecalcDocument instruction in the 
        ' Custom File Properties part, then we don't need another one.
        ' Otherwise, we need to create a unique pid value.
        If Not IsNothing(recalcProp) Then
            Return pidValue
        Else
            ' Get all of the pid values of the proeprty elements and then
            ' convert the IEnumerable object into an array.
            Dim propIDs As IEnumerable(Of String) = _
            From prop In props
            Where prop.Name.LocalName = "property"
            Select prop.Attribute("pid").Value
            Dim propIDArray As String() = propIDs.ToArray()
            ' Increment this id value until a unique value is found.
            ' This starts at 2, because 0 and 1 are not valid pid values.
            Dim id As Integer = 2
            While (pidValue = -1)
                If (propIDArray.Contains(id.ToString())) Then
                    id = id + 1
                Else
                    pidValue = id
                End If
            End While
        End If
        Return pidValue
    End Function
    ```

3. Ersetzen Sie den Code aus dem vorherigen Beispiel im **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) durch den folgenden Code: 
    
    ```cs
    // Change the shape's horizontal position on the page 
    // by getting a reference to the Cell element for the PinY 
    // ShapeSheet cell and changing the value of its V attribute.
    XElement pinYCellXML = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY");
    pinYCellXML.SetAttributeValue("V", "2");
    // Add instructions to Visio to recalculate the entire document
    // when it is next opened.
    RecalcDocument(visioPackage);
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Change the shape's horizontal position on the page
    ' by getting a reference to the Cell element for the PinY
    ' ShapeSheet cell and changing the value of its V attribute.
    Dim pinYCellXML As XElement = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY")
    pinYCellXML.SetAttributeValue("V", "2")
    ' Add instructions to Visio to recalculate the entire document
    ' when it is next opened.
    RecalcDocument(visioPackage)
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

4. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
5. Öffnen Sie die Datei „Visio-Paket.vsdx“ in Visio 2013. 
    
Das Anfangs-/Ende-Shape sollte sich nun 5 cm vom unteren Rand der Zeichnung befinden. Der Verbinder zwischen dem Anfangs-/Ende-Shape und dem Prozess-Shape sollte so umgeleitet worden sein, dass die Änderung im Layout berücksichtigt wird. Wenn die **RecalcDocument**-Eigenschaft nicht zu der Datei hinzugefügt worden wäre, wäre die Shape-Position geändert worden, aber der Verbinder wäre nicht an die neue Position des Shapes umgeleitet worden. 
  
## <a name="add-a-new-package-part-to-a-package"></a>Hinzufügen eines neuen Paketteils zu einem Paket
<a name="vis15_ManipulateFF_AddNewPart"> </a>

Eines der häufigsten Szenarien für das Ändern eines Dateipakets ist das Hinzufügen eines neuen Dokumentteils zum Paket. Wenn Sie beispielsweise eine Seite zu der Visio-Zeichnung hinzufügen möchten, indem Sie dem Paket Inhalte hinzufügen, müssen Sie ein Seiteninhaltsteil zu dem Paket hinzufügen. 
  
Das Verfahren zum Hinzufügen eines neuen Teils zu dem Paket ist einfach: 
  
1. Sie erstellen das XML-Dokument mit den Daten für **PackagePart**. Sie müssen besonders auf die XML-Namespaces Acht geben, die das Schema für den bestimmten Typ des XML-Dokuments festlegen, den Sie erstellen.
    
2. Sie erstellen eine neue Datei für die XML-Daten und speichern die Datei an einem Speicherort im **Package**.
    
3. Sie erstellen die erforderlichen Beziehungen zwischen dem neuen **PackagePart** und dem **Package** oder anderen **PackagePart**-Objekten. 
    
4. Sie aktualisieren alle vorhandenen Teile, die auf das neue Teil verweisen müssen. Wenn Sie beispielsweise ein neues Seiteninhaltsteil (eine neue Seite) zu der Datei hinzufügen, müssen Sie auch das Seitenindexteil (/visio/pages/pages.xml-Datei) aktualisieren, um die richtigen Informationen zu der neuen Seite einzuschließen.
    
Gehen Sie folgendermaßen vor, um ein neues Menübanderweiterungsteil in der Visio-Datei zu erstellen. Das neue Menübanderweiterungsteil fügt dem Menüband eine neue Registerkarte mit einer einzigen Gruppe hinzu, die eine einzige Schaltfläche enthält.
  
### <a name="to-create-a-new-package-part"></a>So erstellen Sie ein neues Paketteil

1. Fügen Sie nach der `CheckForRecalc`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Verfahren die folgende Methode hinzu. 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "http://schemas.microsoft.com/office/2006/01/customui";
        XDocument customUIXDoc = new XDocument(
            new XDeclaration("1.0", "utf-8", "true"),
            new XElement(customUINS + "customUI",
                new XElement(customUINS + "ribbon",
                    new XElement(customUINS + "tabs",
                        new XElement(customUINS + "tab",
                            new XAttribute("id", "customTab"),
                            new XAttribute("label", "CUSTOM"),
                            new XElement(customUINS + "group",
                                new XAttribute("id", "customGroup"),
                                new XAttribute("label", "Custom Group"),
                                new XElement(customUINS + "button",
                                    new XAttribute("id", "customButton"),
                                    new XAttribute("label", "Custom Button"),
                                    new XAttribute("size", "large"),
                                    new XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        );
        return customUIXDoc;
    }
    ```

    ```vb
    Private Function CreateCustomUI() As XDocument
        ' Add a new Custom User Interface document part to the package.
        ' This code adds a new CUSTOM tab to the ribbon for this
        ' document. The tab has one group that contains one button.
        Dim customUINS As XNamespace = _
            "http://schemas.microsoft.com/office/2006/01/customui"
        Dim customUIXML = New XDocument( _
            New XDeclaration("1.0", "utf-8", "true"), _
            New XElement(customUINS + "customUI", _
                New XElement(customUINS + "ribbon",
                    New XElement(customUINS + "tabs",
                        New XElement(customUINS + "tab",
                            New XAttribute("id", "customTab"),
                            New XAttribute("label", "CUSTOM"),
                            New XElement(customUINS + "group",
                                New XAttribute("id", "customGroup"),
                                New XAttribute("label", "Custom Group"),
                                New XElement(customUINS + "button",
                                    New XAttribute("id", "customButton"),
                                    New XAttribute("label", "Custom Button"),
                                    New XAttribute("size", "large"),
                                    New XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        )
        Return customUIXML
    End Function
    ```

2. Fügen Sie nach der `CreateCustomUI`-Methode in der **Program**-Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt die folgende Methode hinzu. 
    
    ```cs
    private static void CreateNewPackagePart(Package filePackage, 
        XDocument partXML, Uri packageLocation, string contentType, 
        string relationship)
    {
        // Need to check first to see whether the part exists already.
        if (!filePackage.PartExists(packageLocation))
        {
            // Create a new blank package part at the specified URI 
            // of the specified content type.
            PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
                contentType);
            // Create a stream from the package part and save the 
            // XML document to the package part.
            using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
                FileAccess.ReadWrite))
            {
                partXML.Save(partStream);
            }
        }
        // Add a relationship from the file package to this
        // package part. You can also create relationships
        // between an existing package part and a new part.
        filePackage.CreateRelationship(packageLocation,
            TargetMode.Internal,
            relationship);
    }
    ```

    ```vb
    Private Sub CreateNewPackagePart(filePackage As Package, _
        partXML As XDocument, packageLocation As Uri, contentType As String, _
        relationship As String)
        ' Need to check first to see whether the part exists already.
        If Not (filePackage.PartExists(packageLocation)) Then
            ' Create a new blank package part at the specified URI
            ' of the specified content type.
            Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
                contentType)
            ' Create a stream from the package part and save the
            ' XML document to the package part.
            Using partStream As Stream = newPart.GetStream(FileMode.Create, _
                FileAccess.ReadWrite)
                partXML.Save(partStream)
            End Using
            ' Add a relationship from the file package to this
            ' package part. You can also create relationships
            ' between an existing package part and a new part.
            filePackage.CreateRelationship(packageLocation, _
                TargetMode.Internal, relationship)
        End If
    End Sub
    ```

3. Ersetzen Sie den gesamten Code im **using**-Block in der **Main**-Methode der **Program**-Klasse (der **Using**-Block der **Main**-Methode in **Module1** in Visual Basic) durch den folgenden Code: 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
5. Öffnen Sie die Datei „Visio-Paket.vsdx“ in Visio 2013, und wählen Sie dann die Registerkarte **Benutzerdefiniert** aus. 
    
Das benutzerdefinierte Menüband sieht wie in Abbildung 2 aus, wenn die Datei in Visio 2013 geöffnet wird.
  
 **Abbildung 2. Benutzerdefinierte Registerkarte im Visio 2013-Menüband**
  
![Eine benutzerdefinierte Registerkarte im Menüband](media/vis15_CustomRibbonTab.PNG)
  
Der von der `CreateCustomUI`-Methode erstellte XML-Code sieht wie folgt aus. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a>Danksagung

Wir möchten uns für die Mitwirkung von Visio MVP **Al Edlund** bei der Erstellung der Codebeispiele bedanken, die in diesem technischen Artikel enthalten sind. Al Edlund ist ein anerkannter Experte für die Bearbeitung des Visio-Dateiformats, einschließlich des Visio-XML-Zeichnungsformats (.vdx) und des neuen Visio-Dateiformats (vsdx). Er hat Projekte erstellt, bei denen die Visio-Dateiformate programmgesteuert durchsucht und die Strukturen darin verfügbar gemacht werden. 
  
Weitere Informationen zur Arbeit von Al Edlund im Zusammenhang mit dem Visio-Dateiformat finden Sie weiter unten in den Links im Abschnitt „Zusätzliche Ressourcen“.
  
## <a name="see-also"></a>Siehe auch

- Von Al Edlund:
    
  - [pkgVisio – Visio 2013-XML-Bearbeitung](https://pkgvisio.codeplex.com/documentation)-Projekt auf CodePlex. 
    
  - [pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be)-Video auf YouTube. 
    
  - [pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be)-Video auf YouTube. 
    
- [Visio Developer Center](https://developer.microsoft.com/visio)
    
- [Bearbeiten von Dokumenten im Office Open XML-Format](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12))
    
- [Erstellen eines Dokuments mit Namespaces (C#) (LINQ to XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140))
    
- [Hinzufügen von benutzerdefinierten XML-Elementen zu Dokumenten ohne Starten von Microsoft Office](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90))
- 
