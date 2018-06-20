---
title: Das Visio-Dateiformat programmgesteuert bearbeiten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: ''
ms.openlocfilehash: 92ef2c084409dbe017951ff7dfdbf93839ff4b51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797169"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Das Visio-Dateiformat programmgesteuert bearbeiten

![Thema mit Anleitung](media/mod_icon_howto.png)
  
Hier erfahren Sie, wie Sie eine Lösung in Visual Studio 2012, um den neuen Datei Format Paket in Visio 2013 lesen, wählen Sie Teile im Paket, ändern Sie die Daten in einem Webpart und hinzufügen neue Komponenten für das Paket zu erstellen.
  
|||
|:-----|:-----|
|**In diesem Artikel** [Visio-Datei Format Manipulation essentials](#vis15_ManipulateFF_Essentials) [Erstellen Sie eine vsdx-Datei und eine neue Visual Studio-Lösung](#vis15_ManipulateFF_CreateFile) [Öffnen Sie eine Visio 2013-Datei als Paket](#vis15_ManipulateFF_OpenPackage) [Wählen Sie aus, und Lesen Sie Paketteile aus einem Paket](#vis15_ManipulateFF_SelectPart) [Wählen Sie aus, und ändern Sie XML-Daten in einem Paket-Webpart](#vis15_ManipulateFF_ChangeXML) [Neuberechnen von Daten in der Datei](#vis15_ManipulateFF_Recalculate) [Hinzufügen eines neuen Paket-Webparts zu einem Paket](#vis15_ManipulateFF_AddNewPart) [Danksagung](#vis15_ManipulateFF_Ackn) [Weitere Ressourcen](#vis15_ManipulateFF_Additional)                                                                                         ||
   
## <a name="visio-file-format-manipulation-essentials"></a>Grundlegendes zum Bearbeiten des Visio-Dateiformats
<a name="vis15_ManipulateFF_Essentials"> </a>

Frühere Versionen von Visio gespeicherte Dateien in einem proprietären binären Dateiformat (.vsd) oder ein einzelnes Dokument Visio XML-Zeichnung-Dateiformat (VDX). Visio 2013 führt ein neues Dateiformat (.vsdx), die auf XML- und ZIP-Archiv-Technologie basiert. Wie in früheren Versionen von Visio werden die Dateien in einem einzelnen Container gespeichert. Im Gegensatz zu Legacydateien jedoch kann das neue Dateiformat geöffnet, lesen, aktualisiert und werden, geändert, ohne die Automatisierung Visio 2013-Anwendung erstellt. Entwickler, die mit der Bearbeitung von XML und zum Arbeiten mit den [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) -Namespace vertraut sind können schnell die ersten Schritte beim Arbeiten mit dem neuen Dateiformat programmgesteuert. Entwickler, die mit dem Visio-XML-Zeichnung Format aus vorherigen Versionen gearbeitet haben können feststellen, dass viele die Strukturen von dieses Format in das neue Dateiformat beibehalten haben. 
  
In diesem Artikel untersuchen wir zum Arbeiten mit dem Visio 2013-Dateiformat programmgesteuert mithilfe der Microsoft .NET Framework 4.5, c# oder Visual Basic und Visual Studio 2012. Sie können die Informationen zum Öffnen einer Visio 2013-Datei, wählen Sie in der Datei Dokumentteile, Ändern von Daten in Webparts und erstellen einen neuen Dokumentteil.
  
> [!NOTE]
> Die folgenden Codebeispiele in diesem Artikel wird davon ausgegangen, dass Sie ein rudimentäre Verständnis der Klassen im [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) und [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) -Namespace verfügen. > In diesem Artikel wird davon ausgegangen, dass Sie die Konzepte und Terminologie der Open Packaging Conventions verstehen. Sie sollten einige gute Kenntnisse im Umgang mit den Konzepten der Pakete, Dokumentteile oder Paketteile und Beziehungen verfügen. Weitere Informationen finden Sie unter [OPC: ein neuer Standard für Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > Der Code veranschaulicht das Erstellen von LINQ (Language-Integrated Query) Abfragen, um XML auszuwählen. Die meisten der Codebeispiele verwenden die Abfragesyntax für die Erstellung von LINQ-Abfragen. Sie können keines der LINQ-Abfragen im Code durch verwenden die Syntax der LINQ-Methode bereitgestellt, bei Bedarf umschreiben. Weitere Informationen zu LINQ-Abfragesyntax und Methodensyntax finden Sie unter [LINQ-Abfragesyntax und Methodensyntax (c#)](http://msdn.microsoft.com/en-us/library/bb397947.aspx)> in Tabelle 1 sind die wichtigsten Themen, die Sie mit vertraut sein sollten, bevor Sie über die in diesem Artikel verwendet werden. 
  
**In Tabelle 1. Kernkonzepte für das Bearbeiten des Visio 2013-Dateiformats**

|**Titel des Artikels**|**Beschreibung**|
|:-----|:-----|
|[Einführung in das Visio-Dateiformat (.vsdx) (engl.)](introduction-to-the-visio-file-formatvsdx.md) <br/> |Diese Übersicht beschreibt einige der wichtigsten Features in das Visio 2013-Dateiformat. Außerdem wird die Open Packaging-Konventionen (OPC) erläutert, wie sie das Visio 2013-Dateiformat angewendet wurden. Es sind auch einige Unterschiede zwischen dem Visio 2013-Dateiformat und der vorherigen Dateiformat für Visio XML-Zeichnung (VDX) aufgeführt.  <br/> |
|[OPC: Ein neuer Standard für das Verpacken Ihrer Daten](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx) <br/> |In diesem MSDN Magazine-Artikel werden die Open Packaging-Konventionen als Konzept beschrieben.  <br/> |
|[Grundlagen der Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx) <br/> [Einführung in die Office (2007) Open XML-Dateiformate](http://msdn.microsoft.com/en-us/library/aa338205.aspx) <br/> |Diese beiden Artikel erläutern, wie die Open Packaging-Konventionen auf Microsoft Office-Dateien angewendet wurden. Sie enthalten eine Beschreibung der Funktionsweise Beziehungen in einem Paket und auch einige Codebeispiele enthalten.  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>Erstellen einer VSDX-Datei und einer neuen Visual Studio-Lösung
<a name="vis15_ManipulateFF_CreateFile"> </a>

Vor Beginn Durcharbeiten der Verfahren in diesem Artikel müssen Sie zum Erstellen einer Visio 2013-Datei zum Öffnen und bearbeiten. Die Zeichnung in die Codebeispiele in diesem Artikel verwendeten enthält eine einzelne Seite mit zwei verbundene Shapes auf dem eines der Shapes wird eine Form "Start-/End" aus der Vorlage "Standardflussdiagramm".
  
Verwenden Sie das folgende Verfahren zum Erstellen einer neuen Visio 2013-Datei, in der restlichen Schritte in diesem Artikel zu verwenden.
  
### <a name="to-create-new-file-in-visio-2013"></a>So erstellen neue Datei in Visio 2013

1. Öffnen Sie Visio 2013.
    
2. Erstellen Sie ein neues Dokument basierend auf der Standardflussdiagramm-Vorlage durch Auswählen von **Kategorien**, **Flussdiagramm**, **Standardflussdiagramm**, **Erstellen**.
    
3. Ziehen Sie aus dem Fenster **Shapes** einer **Start-/End** -Shape des Zeichenbereichs ab. 
    
4. Wählen Sie den neuen Start-/End Shapes auf Zeichenbereich aus, und geben Sie "Prozess beginnen".
    
5. Ziehen Sie aus dem Fenster **Shapes** ein **Prozess** -Shape auf des Zeichenbereichs ab. 
    
6. Wählen Sie die neue Prozess-Shape auf Zeichenbereich aus, und geben Sie "Eine Aufgabe ausführen".
    
7. Im Kontextmenü für die Anfangs-/Form **Hinzufügen einen Verbinder auf der Seite**wählen Sie aus, und zeichnen Sie dann eine Verbindung zwischen dem Start-/End und dem Prozess-Shapes auf des Zeichenbereichs ab, wie in Abbildung 1 dargestellt.
    
    **Abbildung 1. Einfache Visio 2013-Zeichnung**
    
     ![Ein mit einem Prozess-Shape verbundenes Start-/End-Shape](media/vis15_SimpleFlowchart.png)
  
8. Speichern Sie die Datei auf Ihrem Desktop als eine vsdx-Datei, indem Sie auf **Datei**, **Speichern unter**, **Computer**, **Desktop**.
    
    Geben Sie im Dialogfeld **Speichern unter** Visio-Paket in das Feld **Dateiname"** ", wählen **Visio-Zeichnung (\*.vsdx)** im Feld **Dateityp** der Liste, und klicken Sie dann auf die Schaltfläche **Speichern** . 
    
9. Schließen Sie die Datei, und schließen Sie dann Visio 2013.
    
> [!TIP]
> In einigen Fällen Visio öffnet eine Datei erfolgreich auch, wenn Probleme mit der Datei. Um sicherzustellen, dass Visio über Probleme Datei darüber informiert werden, sollten Sie die Datei öffnen Warnungen aktivieren beim Testen von Lösungen, die Visio-Dateien auf Dateiebene Paket bearbeiten. > Wählen Sie die **Datei**, **Optionen**, **Erweitert**, um Datei öffnen Warnungen in Visio 2013 zu aktivieren. Wählen Sie unter **Speichern/Öffnen** **Datei öffnen Warnungen anzeigen**. 
  
Verwenden eine Konsolenanwendung Windows dieser Verfahren zum Bearbeiten der Datei "Visio Package.vsdx". Verwenden Sie das folgende Verfahren zum Erstellen und richten Sie eine neue Windows Konsolenanwendung in Visual Studio 2012.
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Zum Erstellen einer neuen Lösung in Visual Studio 2012

1. Wählen Sie im Menü **Datei** , **neu**, **Projekt**.
    
2. Klicken Sie im Dialogfeld **Neues Projekt** erweitern Sie, **Visual c#** oder **Visual Basic**, und wählen Sie dann **Windows**, **Console Application**.
    
    Geben Sie im Feld **Name** 'VisioFileAccessor', wählen Sie einen Speicherort für das Projekt, und wählen Sie dann auf die Schaltfläche **OK** . 
    
3. Wählen Sie im Menü **Projekt** **Verweis hinzufügen** aus. 
    
    Klicken Sie im Dialogfeld **Verweis-Manager** unter **Assemblys**wählen Sie **Framework**, und fügen Sie einen Verweis auf die Komponenten **System.Xml** und **WindowsBase aus** . 
    
4. Fügen Sie in der Datei Program.cs oder Module1.vb für das Projekt die folgenden **using** -Direktiven (**Imports** -Anweisungen in Visual Basic): 
    
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

5. Auch vor dem Ende der **Main** -Methode der **Programm** -Klasse (**Module1** in Visual Basic), fügen Sie folgenden Code, der die Ausführung der Konsolenanwendung bis wird in der Datei Program.cs oder Module1.vb der Benutzer eine Taste drückt. 
    
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

## <a name="open-a-visio-2013-file-as-a-package"></a>Öffnen Sie eine Visio 2013-Datei als Paket
<a name="vis15_ManipulateFF_OpenPackage"> </a>

Bevor Sie die Daten in der Datei bearbeiten können, müssen Sie zuerst die Datei in einem [Paket](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) -Objekt öffnen, in dem in den [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) -Namespace enthalten ist. Das **Paket** -Objekt stellt die Visio-Datei als Ganzes. Macht Member, mit die Sie einzelne Dokumentteile in dem Dateipaket auswählen können. Insbesondere macht die **Paket** -Klasse die statische [Open (String FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) -Methode, die Sie zum Öffnen einer Datei als Paket verwenden. Macht auch [für das Paket schließen, nachdem Sie haben eine Close()-Methode](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) Verarbeitung beendet. 
  
> [!TIP]
> Es empfiehlt sich verwenden Sie einen Block **mithilfe** die Visio-Datei im **Paket** -Objekt geöffnet, damit Sie nicht, das Dateipaket explizit zu schließen, wenn Sie mit ihm fertig sind. Sie können auch explizit in **finally** -Block **Try/Catch/finally** konstruiert die **Package.Close** -Methode aufrufen. 
  
Verwenden Sie den folgenden Code, um den vollständigen Pfad für die Datei "Visio Package.vsdx" mithilfe eines [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) -Objekts erhalten möchten, übergeben Sie den Pfad als Argument an die **Package.Open** -Methode und klicken Sie dann ein **Paket** an den aufrufenden Code zurück. 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>So öffnen Sie eine VSDX-Datei als Paket

1. Fügen Sie nach der **Main** -Methode in der **Anwendung** -Klasse (oder **Module1** in Visual Basic) den folgenden Code hinzu. 
    
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

2. Fügen Sie in der **Main** -Methode des **Programms** -Klasse (oder **Module1** in Visual Basic) den folgenden Code ein. 
    
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

Sobald Sie die Visio 2013-Datei als Paket geöffnet haben, können Sie die Dokumentteile darin enthaltenen unter Verwendung der in den **System.IO.Packaging** -Namespace enthalten [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) -Klasse zugreifen. **PackagePart** -Objekte können einzeln oder als Sammlung instanziiert werden. Die **Paket** -Klasse stellt eine [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) -Methode und eine [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) -Methode zum Abrufen von **PackagePart** -Objekte aus dem **Paket**. Die **Package.GetParts** -Methode wird eine Instanz der [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) -Klasse, die Sie dann wie jede andere Auflistung interagieren können, die implementiert die [IEnumerator\<T\> ](https://msdn.microsoft.com/library/System.Collections.Generic.IEnumerator`1.aspx) Schnittstelle. 
  
Verwenden Sie Code in das folgende Verfahren, um ein **PackagePartCollection** -Objekt aus dem **Paket** als Sammlung abgerufen, die **PackagePart** -Objekte in der Auflistung durchlaufen und schreiben den URI und Inhaltstyp der einzelnen **PackagePart **in der Konsole angezeigt. 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>So durchlaufen Sie die Paketteile in einem Paket

1. Nach der `OpenPackage` -Methode in die **Programm** -Klasse (oder **Module1** in Visual Basic) fügen Sie den folgenden Code hinzu. 
    
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

2. Fügen Sie den folgenden Code in den Block **verwenden** , in der **Main** -Methode der **Programm** -Klasse ( **Using** -Block der **Main** -Methode in **Module1** in Visual Basic): 
    
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
  
Mehr häufig als nicht müssen Sie eine **PackagePart** auswählen, ohne das zum Durchlaufen aller Folien. Sie können ein **PackagePart** -Objekt aus einem **Paket** mithilfe von seine Beziehung zu einem **Paket** oder einer anderen **PackagePart**abrufen. Eine Beziehung in das Visio 2013-Dateiformat eine einzelne Entität, die beschreibt die Beziehung eines Dokumentteils ist zu einem Dateipaket oder wie zwei Dokumentteile bezieht sich auf miteinander. Beispielsweise das Visio 2013 Dateipaket selbst verfügt über eine Beziehung mit seinerseits Visio-Dokument und das Visio-Dokument Teil hat eine Beziehung mit dem Windows-Webpart. Auf diese Beziehungen werden als Instanzen der Klassen [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) oder [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) dargestellt. 
  
Die **Paket** -Klasse stellt mehrere Methoden zum Abrufen der Beziehungen, die sie als **PackageRelationship** oder **PackageRelationshipCollection** -Objekte enthält. Die [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) -Methode können Sie um ein **PackageRelationshipCollection** -Objekt zu instanziieren, das einen bestimmten Typ **PackageRelationship** -Objekte enthält. Verwendung der **Package.GetRelationshipsByType** -Methode erfordert natürlich, dass Sie bereits den Beziehungstyp kennen, den Sie benötigen. Beziehungstypen sind Zeichenfolgen in XML-Format-Namespace. Der der Beziehungstyp des Visio-Dokuments Teils ist beispielsweise http://schemas.microsoft.com/visio/2010/relationships/document. 
  
Wenn Sie die Beziehung zwischen einem **PackagePart** auf das **Paket** oder auf einem anderen **PackagePart** wissen (d. h., Sie haben ein **PackageRelationship** -Objekt, das die **PackagePart** verweist auf die gewünschte), können die Beziehung den URI des, **PackagePart**abgerufen. Übergeben Sie dann den URI der **Package.GetPart** -Methode, um die **PackagePart**zurückzugeben.
  
> [!NOTE]
> Sie können auch einen Verweis auf eine bestimmte **PackagePart** mithilfe Abrufen die **Package.GetPart** -Methode und der URI eines der **PackagePart**umgehen den Schritt, in dem Sie das Paket des Teils Beziehungen erhalten. Einige Paketteile im Paket Visio-Datei können jedoch an andere Speicherorte als den Standardspeicherorten in einem Paket gespeichert werden. Sie können nicht annehmen, dass ein pakettei immer an den gleichen URI für jede Datei befindet. > Ist es ratsam, Beziehungen verwenden, um die einzelnen **PackagePart** -Objekte zuzugreifen. 
  
Gehen Sie zum Abrufen einer **PackagePart** (Visio-Dokument Teil) mithilfe der **PackageRelationship** aus dem **Paket** , das den Teil verweist. 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>So wählen Sie ein bestimmtes Paketteil im Paket nach Beziehung aus

1. Nach der `IteratePackageParts` -Methode in die **Programm** -Klasse (oder **Module1** in Visual Basic) fügen Sie die folgende Methode hinzu. 
    
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

2. Ersetzen Sie den Code in den **using** -Block in der **Main** -Methode der **Programm** -Klasse ( **Using** -Block der **Main** -Methode in **Module1** in Visual Basic), durch den folgenden Code. 
    
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

Wie bereits erwähnt, können Sie auch **PackagePart** -Objekte abrufen, mit deren Beziehung zu anderen **PackagePart** -Objekten. Dies ist wichtig, da die meisten Objekte **PackagePart** für eine beliebige Komplexität der Visio-Dokument, eine Beziehung mit dem **Paket**verfügen. Ein einzelner Seiteninhalten Teil im Dateipaket (d. h., /visio/pages/page1.xml) verfügt beispielsweise über eine Beziehung mit dem Webpart Seitenindex (d. h., /visio/pages/pages.xml), jedoch nicht für das Dateipaket selbst. Wenn Sie nicht über den exakten den URI einer einzelnen Seite im Paket verfügen, können Sie seine Beziehung zu den Seitenindex Teil, einen Verweis hinzu.
  
Die **PackagePart** -Klasse stellt eine [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) -Methode, die Sie verwenden können, um ein **PackageRelationshipCollection** -Objekt zurückzugeben, die nur einen **PackageRelationship** -Objekt enthält. Nachdem Sie die **PackageRelationshipCollection**haben, können Sie die **PackageRelationship** auswählen, dass Sie aus der Auflistung benötigen, und klicken Sie dann auf das **PackagePart** -Objekt verweisen. 
  
Mithilfe des folgenden Codes einen **PackagePart** aus dem **Paket** abgerufen werden, mithilfe von dessen Beziehung (Abrufen von einem **PackageRelationship** -Objekt) einer anderen **PackagePart**.
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>So wählen Sie ein bestimmtes Paketteil durch seine Beziehung zu einem anderen Paketteil aus

1. Nach der `GetPackagePart` -Methode in die **Programm** -Klasse (oder **Module1** in Visual Basic) fügen Sie die folgenden Überladung-Methode. 
    
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

2. Fügen Sie den folgenden Code auf den Block **verwenden** in der **Main** -Methode der **Programm** -Klasse (die **Using** -Block mit der **Main** -Methode in **Module1** in Visual Basic), unter dem Code aus der vorherigen Prozedur. (Löschen Sie den Code, den Sie im vorherigen Verfahren hinzugefügt haben nicht.) 
    
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

Bevor Sie Änderungen an den XML-Code in einen Dokumentteil enthalten vornehmen können, müssen Sie zuerst das XML-Dokument in ein Objekt geladen werden, die Sie den XML-Code, mit dem [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) -Klasse oder [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) -Klasse lesen können. Beide Klassen verfügbar machen für Aufgaben wie das Auswählen von XML-Elemente in der XML-Dokumenten enthaltenen Methoden. Erstellen, lesen und Schreiben von Attributen; und neue XML-Elemente in ein Dokument einfügt. 
  
Der beiden können die **XDocument** -Klasse Sie den XML-Code mithilfe von LINQ-Abfragen. Mit LINQ können Sie problemlos einzelne Elemente aus einem XML-Dokument auswählen, durch Erstellen von Abfragen, statt aller Elemente in einer Auflistung durchlaufen und Tests für die Elemente, die Sie benötigen. Aus diesem Grund verwenden Sie die folgenden Verfahren in diesem Artikel die **XDocument** -Klasse und anderer Klassen des n: **System.Xml.Linq** Namespaces für das Arbeiten mit XML. 
  
Verwenden Sie das folgende Verfahren, um eine **PackagePart** als XML-Dokument in ein **XDocument** -Objekt zu öffnen. 
  
### <a name="to-read-the-xml-in-a-package-part"></a>So lesen Sie den XML-Code in einem Paketteil

1. Nach der letzten Überladung für die `GetPackagePart` -Methode in die **Programm** -Klasse (oder **Module1** in Visual Basic) fügen Sie die folgende Methode hinzu. 
    
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

2. Fügen Sie den folgenden Code auf den Block **verwenden** in der **Main** -Methode der **Programm** -Klasse (die **Using** -Block mit der **Main** -Methode in **Module1** in Visual Basic), unter dem Code aus der vorherigen Prozedur. 
    
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

Nachdem Sie einen Dokumentteil in einem **XDocument** -Objekt geladen haben, können Sie LINQ wählen Sie XML-Elemente und das XML-Dokument zu ändern. Sie können XML-Daten ändern, hinzufügen oder Entfernen von Daten und speichern Sie das XML-Dokument in den Dokumentteil zurück. 
  
Die am häufigsten verwendete Aufgabe zum Bearbeiten von der Visio-Dateiformat entspricht dem bestimmten XML-Elemente oder Sammlungen von Elementen im Dokument auswählen. Der **System.Xml.Linq** -Namespace enthält die [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) -Klasse, die XML-Elements darstellt. **XElement** -Klasse erhalten Sie Zugriff auf die Daten, die in der Visio-Datei auf einer Ebene Differenzierte Sicherung von einzelnen **Shape** -Elementen zu **ValidationRule** -Elemente (als Beispiele) enthalten sind. 
  
Verwenden Sie den folgenden Code, die **Form** -Elemente aus ein **XDocument-Objekt** (mit einer Seite Inhaltsverzeichnis-Webpart) auszuwählen, und klicken Sie dann auf ein bestimmtes **Shape** -Element auswählen. 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>So wählen Sie ein bestimmtes Element in einem Paketteil aus

1. Nach der `GetXMLFromPart` -Methode in die **Programm** -Klasse (oder **Module1** in Visual Basic) fügen Sie die folgende Methode hinzu. 
    
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

2. Nach der `GetXElementsByName` -Methode in der **Program** -Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt, fügen Sie die folgende Methode hinzu. 
    
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

3. Fügen Sie den folgenden Code auf den Block **verwenden** in der **Main** -Methode der **Programm** -Klasse (die **Using** -Block mit der **Main** -Methode in **Module1** in Visual Basic), unter dem Code aus der vorherigen Prozedur. 
    
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

Nachdem Sie einen Verweis auf ein **XElement** -Objekt enthaltenen **XDocument** -Objekt gelangt sind, können Sie wie alle anderen XML-Daten zu bearbeiten und somit ändern Sie die Daten, die in der Visio-Datei enthalten sind. Beispielsweise wird eine Form Text enthält, wenn es in Visio geöffnet wird, das entsprechende Element **Shape** mindestens ein **Text** -Element enthalten. Wenn Sie den Wert dieses Elements **Text** zu ändern, wird der Text des Shapes geändert, wenn die Datei in Visio angezeigt wird. 
  
Fügen Sie den folgenden Code auf den Block **verwenden** in der **Main** -Methode der **Programm** -Klasse ( **Using** -Block der **Main** -Methode in **Module1** in Visual Basic), um den Text in der Form Start-/End aus "Beginnen Sie mit dem Prozess" ändern Klicken Sie auf "Start-Prozess". 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName = "Text"
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
    Where element.Name.LocalName = "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> Im vorherigen Codebeispiel werden der vorhandenen Shape-Text und die Zeichenfolge zu ersetzen, die gleiche Anzahl von Zeichen. Beachten Sie außerdem, dass die LINQ-Abfrage der Wert der den letzten untergeordneten Knoten des zurückgegebenen Elements ändert (die in diesem Fall ein Textknoten ist). Dies erfolgt, um zu vermeiden, ändern die Einstellungen des **cp** -Elements, das ein untergeordnetes Element des Elements **Text** ist. > Es ist möglich, die Datei instabil, wenn Sie Shape-Text programmgesteuert ändern, indem Sie alle untergeordneten Elemente des **Text** -Elements überschrieben. Wie im obigen Beispiel wird der Text-Formatierung durch **cp** Elemente unter dem **Text** -Element in der Datei dargestellt. Die Definition der Formatierung wird im übergeordneten **Abschnitt** Element gespeichert. Wenn diese zwei Datenelemente Informationen inkonsistent werden, klicken Sie dann die Datei verhält sich möglicherweise nicht wie erwartet. Visio heals viele Inkonsistenzen, aber es ist besser, stellen Sie sicher, dass programmgesteuerten Änderungen konsistent sind, damit Sie das ultimate Verhalten der Datei steuern. 
  
Wenn Sie Änderungen an dem XML-Code eines Dokumentteils vornehmen, sind diese Änderungen nur im Speicher vorhanden. Um die Änderungen in der Datei zu speichern, müssen Sie die XML-Daten wieder in dem Dokumentteil speichern.
  
Mit dem folgende Code wird der [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) -Klasse und [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) den XML-Code in das Paket Webpart Zurückschreiben verwendet. Zwar die [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) -Methode zum Speichern des XML-Codes wieder mit dem Webpart, das **XmlWriter können** und **XmlWriterSettings** Klassen Sie eine genauere Kontrolle über die Ausgabe, einschließlich der Angabe des Typs der Codierung können. Die **XDocument** -Klasse stellt eine [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) -Methode, die ein **XmlWriter** -Objekts und schreibt XML in einem Stream-Objekt zurück. 
  
Verwenden Sie das folgende Verfahren, um die XML-Daten aus dem Visio-Zeichenblatt wieder auf der Seite Inhaltsverzeichnis-Webpart zu speichern.
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>So speichern Sie die geänderten XML-Daten wieder in dem Paket

1. Nach der `GetXElementByAttribute` -Methode in der **Program** -Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt, fügen Sie die folgende Methode hinzu. 
    
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

2. Fügen Sie den folgenden Code auf den Block **verwenden** in der **Main** -Methode der **Programm** -Klasse (die **Using** -Block mit der **Main** -Methode in **Module1** in Visual Basic), unter dem Code aus der vorherigen Prozedur. 
    
  ```cs
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

3. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
4. Öffnen Sie die Visio-Package.vsdx-Datei in Visio 2013. 
    
Das Anfangs-/Ende-Shape sollte nun den Text „Prozess anfangen“ enthalten.
  
## <a name="recalculate-data-in-the-file"></a>Neuberechnen von Daten in der Datei
<a name="vis15_ManipulateFF_Recalculate"> </a>

Einige Änderungen an den Daten in einer Datei erfordern möglicherweise, Visio, das Dokument neu zu berechnen, wenn sie die Datei geöffnet wird. Visio enthält viele der Logik für ein Diagramm, insbesondere für diagrammbeziehungen des Shapes (d. h., wenn ein Shape auf einem anderen je nach) und Verbinden von Formen. Wenn die Daten, die auf die benutzerdefinierte Logik beruht geändert wird, muss Visio die Änderungen an alle betroffenen berechneten Daten in der Datei weitergegeben. 
  
Das Visio 2013-Dateiformat enthält eine Reihe von Techniken, die Sie verwenden können, um Daten in der Datei neu zu berechnen. Es gibt drei Arten von Szenarien, die Sie berücksichtigen müssen, wenn Sie sich entscheiden, ob Sie die Visio-Datei und wie Sie ihn neu zu berechnen, müssen:
  
- Die Änderungen an den Daten wirken sich nicht auf andere Werte im Dateiformat aus. Sie müssen nicht zu Visio, um das Dokument neu zu berechnen, etwaige zusätzlichen Anweisungen hinzufügen. Wie bereits gezeigt, können Sie häufig Text einer Form ändern, ohne das Dokument neu zu berechnen.
    
- Die Änderungen an den Daten sind zum Ändern der Werte von ShapeSheet-Zellen in den XML-Code beschränkt, und sind andere ShapeSheet-Werte, die auf diese Daten abhängen. In diesem Fall müssen Sie durch Hinzufügen ein XML verarbeitungsanweisung (mithilfe der Klasse ["XProcessingInstruction"](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) ) auf die **Zelle** -Element, das geändert wurde. Beispielsweise wirkt sich die Zelle **ThemeIndex** für ein Shape auf die Werte der mehrere andere ShapeSheet-Zellen in der Form aus. Wenn Sie die Zelle **ThemeIndex** in der Datei selbst **(beispielsweise das Zellenelement mit einem **N** -Wert von "ThemeIndex")** ändern, müssen Sie eine verarbeitungsanweisung **das Zellenelement** hinzufügen, damit die abhängigen Werte aktualisiert werden . 
    
- Die Änderungen an den Daten bestimmen den Speicherort der eine Verbindung mit der Realität Punkt. Eine andere Situation ist, wenn es viele Änderungen an der ShapeSheet-Daten und das gesamte Dokument mit einer Anweisung (anstatt einzelne verarbeitungsanweisungen für jede Änderung) neu berechnet werden soll. In diesem Fall können Sie anweisen, Visio, das gesamte Dokument neu zu berechnen, wenn es geöffnet wird. Zu diesem Zweck Hinzufügen einer **RecalcDocument** -Eigenschaft auf den benutzerdefinierten Dateieigenschaften Teil (/ docProps/custom.XML) des Visio-Pakets. Anpassen der Position oder die Größe des Shapes in ein verbundenes Diagramm ist ein Beispiel für diese Art von Szenario. 
    
    Bitte beachten Sie, dass es sich hierbei in puncto Leistung um die kostspieligste Option handelt.
    
Verwenden Sie das folgende Verfahren zum Einfügen einer **Zelle** -Element in ein **Form** -Element, in denen andere **Zelle** Elemente in der gleichen **Shape** aufgrund der neue Wert neu berechnet werden müssen. Das neue Element **Zelle** enthält eine verarbeitungsanweisung als untergeordnetes Element, um Visio zu informieren, die einige lokale neuberechnung ausführen muss. 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>So berechnen Sie die Werte für ein einzelnes Shape neu

1. Ersetzen Sie den Code aus den vorherigen beiden Beispielen (ändern den Text des Shapes und dem Aufruf von `SaveXDocumentToPart`) in den **using** -Block in der **Main** -Methode der **Programm** -Klasse (den **Using** Block mit der **Main** -Methode in **Module1** in Visual Basic) durch den folgenden Code. 
    
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
  ' alrady have a local ThemeIndex cell.
  startEndShapeXML.Add(New XElement("Cell", _
      New XAttribute("N", "ThemeIndex"),
      New XAttribute("V", "25"),
      New XProcessingInstruction("NewValue", "V")))
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

2. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
3. Öffnen Sie die Visio-Package.vsdx-Datei in Visio 2013. Das Start-/End-Shape sollte jetzt eine anderen Füllfarbe haben.
    
Die Farbe des Shapes auf dem Wert der Zelle **ThemeIndex** nutzt – es wird bestimmt, welche der aktiven Designs von die Form erbt. Im vorherigen Beispiel wird die Form festgelegt, von einem unterschiedlichen Design erbt (die Zelle **ThemeIndex** ist auf den Wert "25" festgelegt). Wenn Sie eine verarbeitungsanweisung Textfarbe des Shapes nicht verwenden – die wird auch durch die Zelle **ThemeIndex** beeinflusst – wird nicht neu berechnet. Füllfarbe der Form würde zu Weiß geändert, doch dessen Text würde weißen – Verlassen des Texts kann nicht gelesen werden. Ohne den verarbeitungsanweisung ist es zudem möglich, dass Visio möglicherweise Shape aktualisieren zu einem späteren Zeitpunkt, wobei die Datei in einem instabilen Zustand, in dem die Formatierung Werte der Form möglicherweise nicht ordnungsgemäß aktualisiert werden konnte. 
  
Wenn Sie Daten in der Datei, die benötigt Visio ändern, das Dokument (z. B. Ändern der Position einer Form verbunden und daher die Verbinder umleiten erzwingen) neu zu berechnen, müssen Sie eine neuberechnung-Anweisung Visio-Datei hinzufügen. Die Anweisung wird durch Hinzufügen einer **Property-** Element mit dem **Name** -Attributwert "RecalcDocument" zu den XML-Code des benutzerdefinierten Dateieigenschaften Teils des Pakets für Visio-Datei erstellt. Es empfiehlt sich sollten Sie das Webpart benutzerdefinierte Dateieigenschaften, um sicherzustellen, dass eine Anweisung "RecalcDocument" bereits in der Datei registriert wurde noch nicht überprüfen. 
  
Verwenden Sie den folgenden Code, um den Wert der Zelle **PinY** des Shapes Start-/End aus den vorherigen Beispielen zu ändern. Im Code wird das **Zelle** -Element, das die Zelldaten **DrehbezY** als **XElement** -Objekt enthält, mit dem Wert des Attributs **N** ausgewählt. Der Code fügt dann eine neuberechnung-Anweisung in den benutzerdefinierten Dateieigenschaften Teil der Visio-Datei. 
  
> [!NOTE]
> Dieser Code nutzt die `GetPackagePart` und `SaveXDocumentToPart` zuvor erstellten Methoden. 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>So berechnen Sie das gesamte Dokument beim Öffnen neu

1. Nach der `SaveXDocumentToPart` -Methode in der **Program** -Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt, fügen Sie die folgende Methode hinzu. 
    
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

2. Nach der `RecalcDocument` -Methode in der **Program** -Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt, fügen Sie die folgende Methode hinzu. 
    
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

3. Ersetzen Sie den Code aus dem vorherigen Beispiel in den **using** -Block in der **Main** -Methode der **Programm** -Klasse (die **Using** -Block mit der **Main** -Methode in **Module1** in Visual Basic), durch den folgenden Code ein. 
    
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
    
5. Öffnen Sie die Visio-Package.vsdx-Datei in Visio 2013. 
    
Das Start-/End-Shape sollte jetzt 2 Zoll vom unteren Rand der Zeichnung. Der Verbinder zwischen dem Start-/End-Shape und den Prozess-Shape sollte umgeleitet haben, um die Änderung im Layout zu unterstützen. Wenn die **RecalcDocument** -Eigenschaft nicht in der Datei wurden, die Position der Form würde geändert wurde, aber würde der Verbindung nicht an die neue Position der Form umgeleitet haben. 
  
## <a name="add-a-new-package-part-to-a-package"></a>Hinzufügen eines neuen Paketteils zu einem Paket
<a name="vis15_ManipulateFF_AddNewPart"> </a>

Eines der am häufigsten verwendeten Szenarien zum Ändern eines Pakets Datei wird ein neuen Dokumentteils zum Paket hinzufügen. Wenn Sie die Visio-Zeichnung durch Hinzufügen von Inhalt zum Paket eine Seite hinzufügen möchten, müssen Sie beispielsweise das Paket einer Seite Inhaltsverzeichnis-Webpart hinzufügen. 
  
Das Verfahren zum Hinzufügen eines neuen Teils zu dem Paket ist einfach:  
  
1. Erstellen Sie das XML-Dokument mit den Daten, für die **PackagePart**. Sie möchten besonders auf die XML-Namespaces Zahlen, die das Schema für den bestimmten Typ des XML-Dokuments zu steuern, die Sie erstellen.
    
2. Sie erstellen eine neue Datei, um den XML-Code enthalten, und speichern Sie die Datei an einen Speicherort im **Paket**.
    
3. Erstellen Sie die erforderlichen Beziehungen zwischen der neuen **PackagePart** und das **Paket** oder sonstigen Objekte, **PackagePart** . 
    
4. Sie aktualisieren alle vorhandenen Teile, die auf das neue Teil verweisen müssen. Wenn Sie beispielsweise ein neues Seiteninhaltsteil (eine neue Seite) zu der Datei hinzufügen, müssen Sie auch das Seitenindexteil (/visio/pages/pages.xml-Datei) aktualisieren, um die richtigen Informationen zu der neuen Seite einzuschließen.
    
Verwenden Sie das folgende Verfahren, um eine neue Komponente der Menüband-Erweiterbarkeit in der Visio-Datei zu erstellen. Des neuen Teils der Menüband-Erweiterbarkeit fügt dem Menüband eine neue Registerkarte mit einer Gruppe, die eine einzelne Schaltfläche enthält.
  
### <a name="to-create-a-new-package-part"></a>So erstellen Sie ein neues Paketteil

1. Nach der `CheckForRecalc` -Methode in der **Program** -Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Verfahren fügen Sie die folgende Methode hinzu. 
    
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

2. Nach der `CreateCustomUI` -Methode in der **Program** -Klasse (oder **Module1** in Visual Basic) aus dem vorherigen Schritt, fügen Sie die folgende Methode hinzu. 
    
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

3. Ersetzen Sie der Code in die **Verwendung** in der **Main** -Methode der **Programm** -Klasse (die **Using** -Block mit der **Main** -Methode in **Module1** in Visual Basic), blockieren durch den folgenden Code. 
    
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
    
5. Öffnen Sie die Visio-Package.vsdx-Datei in Visio 2013, und wählen Sie dann auf die Registerkarte **Benutzerdefiniert** . 
    
Benutzerdefinierte Menüband sieht wie in Abbildung 2 beim Öffnen der Datei in Visio 2013.
  
 **Abbildung 2. Benutzerdefinierte Registerkarte im Menüband Visio 2013**
  
![Eine benutzerdefinierte Registerkarte im Menüband](media/vis15_CustomRibbonTab.PNG)
  
Der XML-Code erstellt die `CreateCustomUI` Methode sieht folgendermaßen aus. 
  
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
<a name="vis15_ManipulateFF_Ackn"> </a>

Wir möchten erkennt den Beitrag und die Eingabe von Visio MVP **Al Edlund** bei der Erstellung der Codebeispiele, die in diesem technischen Artikel enthalten sind. Al ist eine erkannten Expert in Bearbeiten von der Visio-Dateiformat, einschließlich das Format für Visio-XML-Zeichnung (VDX) und das neue Visio-Dateiformat (.vsdx). Al Projekte, die die Visio-Dateiformate programmgesteuert erkunden erstellt wurden, und macht die Strukturen innerhalb. 
  
Weitere Informationen zur Arbeit mit dem Visio-Dateiformat des Al finden Sie die Links in den folgenden Abschnitt Weitere Ressourcen.
  
## <a name="see-also"></a>Siehe auch
<a name="vis15_ManipulateFF_Additional"> </a>

- Von Al Edlund:
    
  - Bei CodePlex [PkgVisio - Visio 2013-XML-Bearbeitung](http://pkgvisio.codeplex.com/documentation) -Projekt. 
    
  - Sie Videos auf YouTube die aus [pkgVisio_pt1](http://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) . 
    
  - Sie Videos auf YouTube die aus [pkgVisio_pt2](http://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) . 
    
- [Visio Developer Center](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Bearbeiten von Dokumenten im Office Open XML-Formate](http://msdn.microsoft.com/en-us/library/aa982683%28v=office.12%29.aspx)
    
- [Erstellen eines Dokuments mit Namespaces (c#) (LINQ to XML)](http://msdn.microsoft.com/en-us/library/bb387075.aspx)
    
- [Hinzufügen von benutzerdefinierten XML-Komponenten für Dokumente ohne Starten von Microsoft Office](http://msdn.microsoft.com/en-us/library/bb608597%28VS.90%29.aspx)
    

