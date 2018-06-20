---
title: Einführung in das Visio-Dateiformat (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Erfahren Sie mehr über das neue Dateiformat in Visio 2013, einige hochrangige Konzepte für die Arbeit mit dem Visio 2013-Dateiformat programmgesteuert durchsuchen, und erstellen Sie eine einfache Konsolenanwendung, die ein Visio 2013-Testdatei.
ms.openlocfilehash: aa3497af7c467c8f51ab80ab82071776568b4978
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797217"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Einführung in das Visio-Dateiformat (.vsdx)

Erfahren Sie mehr über das neue Dateiformat in Visio 2013, einige hochrangige Konzepte für die Arbeit mit dem Visio 2013-Dateiformat programmgesteuert durchsuchen, und erstellen Sie eine einfache Konsolenanwendung, die ein Visio 2013-Testdatei.
  
|||
|:-----|:-----|
|**In diesem Artikel** [Einführung in die](#vis15_IntroVSDX_Intro) [Was ist das Visio 2013-Dateiformat "Detail"?](#vis15_IntroVSDX_What)                             [Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat](#vis15_IntroVSDX_Scenarios) [Erkunden Sie programmgesteuert das Visio 2013-Dateiformat](#vis15_IntroVSDX_Explore) [Weitere Ressourcen](#vis15_IntroVSDX_Resources)                    ||
   
## <a name="introduction"></a>Einführung
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 führt ein neues Dateiformat (.vsdx) für Visio, die von der Visio-Binärdateiformat (.vsd) und das Dateiformat Visio XML-Zeichnung (VDX) ersetzt. Da das Visio 2013-Dateiformat Open Packaging-Konventionen und XML-basiert, können Entwickler, die mit diesen Technologien vertraut sind schnell zum programmgesteuerten arbeiten mit Visio 2013-Dateien informieren. Entwickler, die mit dem Dateiformat Visio XML-Zeichnung (VDX) aus früheren Versionen von Visio vertraut sind, können viele der gleichen XML-Strukturen in den Teilen des vsdx-Dateiformat suchen. Interoperabilität mit Visio-Dateien ist wesentlich komplexer, da Drittanbietersoftware Visio-Dateien auf einer Ebene der Datei Format bearbeiten kann. Das Visio 2013-Dateiformat wird auf Visio Services in Microsoft SharePoint Server 2013, ohne dass ein "zwischengeschaltete" Dateiformat für die Veröffentlichung in SharePoint Server unterstützt.
  
Es gibt mehrere Dateitypen, durch Erweiterung, die das Visio 2013-Dateiformat umfassen. Dieser Erweiterungen umfassen:
  
- .vsdx (Visio-Zeichnung)
    
- .vsdm (Visio-Makro aktivierte Zeichnung)
    
- .vssx (Visio-Schablone)
    
- .vssm (Visio-Makro aktivierte Schablone)
    
- .vstx (Visio-Vorlage)
    
- .vstm (Visio-Vorlage mit Makros)
    
> [!NOTE]
> Nur die makrofähigen Dateien (.vsdm, .vssm, .vstm) können VBA-Makros speichern. Sie können Makros nicht in Dateien mit einer VSDX-, VSSX- oder VSTX-Erweiterung speichern. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Was ist das Visio 2013-Dateiformat "Detail"?
<a name="vis15_IntroVSDX_What"> </a>

Das Visio 2013-Dateiformat verwendet die Open Verpackung Conventions (OPC), die eine strukturierte Möglichkeit zum Speichern von Anwendungsdaten mit den zugehörigen Ressourcen mit einem Container des einige Sort─for wird eine ZIP-Datei definiert. Grundlegende Ebene ist eine Visio 2013-Datei wirklich eine ZIP-Container, der andere Typen von Dateien enthält. Sie können sogar Speichern einer Zeichnung in Visio 2013 als eine vsdx-Datei, benennen Sie die Erweiterung der Datei in "\*ZIP" die Datei wie folgt einen Ordner aus, die Inhalte finden Sie unter in Windows Explorer, und klicken Sie dann auf Öffnen.
  
> [!NOTE]
>  Dieser Artikel enthält nur eine kurze Übersicht über die Open Packaging-Konventionen. Finden Sie detaillierte Abdeckung der Konventionen in anderen Artikeln: > Weitere Informationen zu den Open Packaging Conventions selbst, finden Sie unter [OPC: ein neuer Standard für Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > Weitere Informationen zu Open Packaging-Konventionen und deren Verwendung in Microsoft Office-Dateien finden Sie unter [Grundlagen der Open Packaging-Konventionen](http://msdn.microsoft.com/en-us/library/ee361919.aspx) und [Einführung in die Microsoft Office (2007) Open XML-Dateiformaten](http://msdn.microsoft.com/en-us/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Pakete und Paketteile

Wie zuvor gestartet wird, sind Visio 2013-Dateien ZIP-Container oder "Pakete", die anderen Dateien (mit der Bezeichnung "Paketteile") darin enthalten sein. Ein pakettei kann es sich um eine XML-Datei, eines Bilds, sogar einer VBA-Lösung sein. Die Teile im Paket können in zwei Hauptkategorien, "Dokumentteile" und "Beziehung Teile." weiter unterteilt werden Die Dokumentteile enthalten die tatsächlichen Inhalte und Metadaten der Visio-Datei, wie der Name der Datei, die erste Seite und alle Formen, die er enthält, und sogar die datenverbindungen für die Formen. Bilder und Textdateien, in dem Paket gelten Dokumentteile. Beziehung Teile werden weiter unten in diesem Artikel ausführlich beschrieben.
  
> [!NOTE]
> Wenn Sie eine Visio 2013-Datei mithilfe eines ZIP-Dienstprogramms öffnen, sehen Sie möglicherweise mehrere Ordner, die in der ZIP-Paket enthalten sind. Sie können auch diese untergeordneten Adressen wie mit einem Dienstprogramm ZIP-Ordner bearbeiten. Diese "Ordner" wird jedoch untergeordnete Adressen innerhalb der ZIP-Paket keine eigentlichen Ordner darstellen. Sie können die programmgesteuerte Entsprechung von Ordnern diese Sub-Adressen in Ihrer Lösung entwickelt. 
  
Paketteile (sowohl Dokumentteile und Beziehungsteile) verfügen über verknüpfte Inhaltstypen. Diese Inhaltstypen sind Zeichenfolgen, die einen MIME-Medientyp definieren. Diese Inhaltstypen bestimmen und prüfen die Art der MIME-Typen, die in der Datei enthalten sein können.
  
### <a name="relationships"></a>Beziehungen

Die Beziehung Teile (die Enden mit der Erweiterung "\*rels" und befinden sich in einem Ordner "_rels") wird beschrieben, wie die Teile im Paket miteinander in Beziehung stehen, und geben Sie die Struktur der Datei. Ein eigenständiges XML-Dokument wird die Beziehung zwischen über-und untergeordneten Elemente die Beziehung zwischen Entitäten miteinander ermittelt. Andere Dateien möglicherweise andere Hierarchien oder Ordnerstruktur Datei verwenden, um die Interaktion von Inhalten in der Datei beschreiben. Für das Visio 2013-Dateiformat ist das Paket gültige Visio-Datei aus, wenn sie die korrekte Liste der Webparts enthält und das Paket die Beziehungen zwischen den Teilen enthält. 
  
Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen im Paket beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einem angegebenen Quell- (definiert durch den Namen und dem Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beziehungsteile werden beispielsweise verwendet, um zu beschreiben, welche Shape-Master mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander zusammenhängen oder wie Bilder und Objekte mit einer bestimmten Seite zusammenhängen. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Ähnlichkeiten und Unterschiede mit Visio VDX-schema

Wie bereits erwähnt, enthalten die frühere Versionen von Visio auch eine XML-basierte Datei Format, das Visio XML-Zeichnungsformat oder VDX. (In früheren Versionen von Visio, wird das Schema für den Visio-XML-Zeichnungsformat verwendet DatadiagramML bezeichnet.) Einige Teile von der Visio-XML-Schema haben dieselbe zwischen den beiden Dateiformate waren. Das **Windows** -Element und die untergeordneten Elemente bleiben beispielsweise Unchanged─with der Ausnahme, dass das **Windows** -Element jetzt ein Stammelement eines XML-Dokuments (window.xml) ist. 
  
Der größte Unterschied zwischen dem XML-Zeichnung und das Visio 2013-Dateiformat ist der Verpackung. Eine Datei im Format von XML-Zeichnung konnte wie eine normale eigenständige XML bearbeitet werden; das Visio 2013-Dateiformat muss als Paket bearbeitet werden. In der Visio 2013 hat der XML-Code in Webparts für einfacher Verbrauch aufgeteilt wurde. Eine andere bedeutende Änderung erfolgt ist, dass das Visio 2013-Dateiformat alle Dokumenteigenschaften im Dokumentteile beschrieben durch die OPC-standard (app.xml, core.xml, Benutzer.XML) gespeichert werden.
  
Es ist jedoch eine bedeutende Änderung, die alle Visio-Entwickler berücksichtigen müssen: die Einführung der **Zelle**, **Zeile**und **im Abschnitt** Elemente. In der XML-Zeichnungsdateiformat Schema werden einzelne Zeilen und Zellen im ShapeSheet durch benannten Elemente dargestellt. Angenommen Sie, dass Sie ein Dokument mit einer einzelnen Seite mit einer Form mit dem **PinX** Wert "2" (d. h., dass die Pin Drehung der Form 2 Zoll vom linken Rand der Zeichnung ist). Im folgenden Code wird das relevante Markup für diese Einstellung im Dateiformat XML-Zeichnung angezeigt. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Hier ist das **PinX** -Element ein untergeordnetes Element des **XForm** -Elements, das wiederum ein untergeordnetes Element des **Shape** -Elements ist. Dieses Modell der Visio ShapeSheet-Benutzeroberfläche, in dem die Zelle **PinX** im Abschnitt **Shape Transform** eines Shapes enthalten ist. 
  
In Visio 2013-Dateiformat alle Zellen in der ShapeSheet─ **PinX** **LinePattern**, eine **X** -Zelle in einer **MoveTo** -Zeile in einem **Geometrie** -Abschnitt etc.─are durch einen Typ von XML-Element, **das Zellenelement** dargestellt. Verschiedene **Zelle** Elemente werden durch den Wert für das Attribut **N** voneinander individuated. Im obigen Beispiel ist daher die Daten in die Zelle **PinX** im ShapeSheet in eine VSDX-Datei wie im folgenden Code gezeigt gespeichert. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

**Das Zellenelement für **DrehbezX** (wie bei anderen einzelnen, benannten Zellen "Singleton Zellen" wie **LinePattern** oder **LockSelect**aufgerufen)** ist ein direktes untergeordnetes Element des **Shape** -Elements. Keine eindeutigen Elements ist erforderlich, um die Zeile, die Zelle **PinX enthält,** darstellen, wie jeder Form eine **PinX**nur verwendet werden kann.
  
Was geschieht mit Abschnitten, die Tabellendaten wie **geometrischen** Abschnitte enthalten? Für die Zellen in den Abschnitten das Visio 2013-Dateiformatschema **Abschnitt** verwendet und **Zeile** Elements─also definierten nach **N** -Attribut oder **T** -Attribut als Below─to dargestellt, die Daten enthalten. Dasselbe Shape aus dem vorherigen Beispiel kann beispielsweise Daten im Abschnitt **"Geometry" 1** enthalten, die den folgenden Code in das Schema der XML-Zeichnung aussieht. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Geom IX="0">
        <!--- Other cells and rows in the Geometry 1 section -->
        <LineTo IX="1">
            <X F="Width*0">0</X>
            <Y F="Height*0">0</Y>
        </LineTo>
    </Geom>
</Shape>

```

Es sieht jedoch wie der folgende Code in der Datei Visio 2013.
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Section N="Geometry" IX="0"> 
        <!--- Other cells and rows in the Geometry 1 section -->
        <Row IX="1" T="LineTo">
            <Cell V="0" N="X" V="Width*0" />
            <Cell V="0" N="Y" V="Height*0" />
        </Row>
    </Section>
</Shape>

```

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat
<a name="vis15_IntroVSDX_Scenarios"> </a>

Wie oben beschrieben, nutzt das Visio 2013-Dateiformat mehrere dokumentiertes Technologien wie ZIP-Dateien und XML zum Speichern von Daten. Um eine Zeichnung auf Dateiebene Visio 2013 zu bearbeiten, eine Lösung benötigen nur für die .NET Framework-Namespaces und Klassen im Zusammenhang mit der Arbeit mit ZIP-Dateien oder XML, wie [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) oder [System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx)verwenden.
  
Der wichtigste Vorteil des Dateiformats für Visio 2013-Entwickler ist, können Sie lesen und in Visio 2013-Dateien schreiben ohne Automatisieren der Visio-Clientanwendung. Einige Szenarien, die Sie als Entwickler sollten, für das Arbeiten mit Visio 2013-Dateiformat, gehören:
  
- Überprüfen die einzelne Visio 2013-Dateien für bestimmte Daten. Sie können ein Element aus der ZIP-Container selektiv lesen, ohne die gesamte Datei extrahieren.
    
- Aktualisieren von Bibliotheken mit Visio 2013-Dateien mit spezifischem Inhalt. Sie können das Logo in allen Hintergrundblätter neue branding Richtlinien entsprechend programmgesteuert ändern.
    
- Erstellen von Anwendungen, die Visio 2013-Dateien zu nutzen. Beispielsweise können Sie ein Tool erstellen, die ein Visio-Workflowdiagramm liest und führt dann eine eigene Geschäftslogik basierend auf diesen Workflow.
    
Achten Sie darauf, dass die meisten Lösungen, die auf einem Clientcomputer ausgeführt werden können, auch auf einem Server ausgeführt werden können, da diese Lösungen standardmäßige .NET Framework-Assemblys verwenden!
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Programmatisches Ermitteln des Visio 2013-Dateiformats
<a name="vis15_IntroVSDX_Explore"> </a>

Die einfachste und grundlegende Aufgabe für alle Arbeiten mit dem Visio 2013-Dateiformat (engl.) wird die Datei als Paket öffnen und den Zugriff auf einzelne Teile im Paket. Die **System.IO.Packaging.Package** in die WindowsBase.dll enthält viele Klassen, mit denen Sie öffnen und Bearbeiten von Paketen und WebParts. 
  
Im folgenden Codebeispiel können Sie sehen, wie eine VSDX-Datei geöffnet wird, die Liste der Teile im Paket gelesen werden und Informationen über jeden Teil abgerufen werden können.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>So öffnen Sie eine VSDX-Datei und zeigen die Dokumentteile an

1. Öffnen Sie Visio 2013, und erstellen Sie ein neues Dokument.
    
2. Erstellen Sie ein neues Dokument, und speichern Sie es auf dem Desktop.
    
3. Öffnen Sie Visual Studio 2012.
    
4. Klicken Sie im Menü **Datei** auf **neu**, und wählen Sie dann ** Project **.
    
5. Unter **Visual c#** oder **Visual Basic**erweitern Sie **Windows**, und wählen Sie dann **Konsolenanwendung**.
    
6. Geben Sie im Feld **Name den Namen** 'VisioFileExplorer'. Das Konsolenanwendungsprojekt wird geöffnet. 
    
7. Klicken Sie im **Projektmappen-Explorer**-Maustaste auf **VisioFileExplorer**, und klicken Sie dann auf **Verweis hinzufügen**. 
    
8. Klicken Sie im Dialogfeld **Verweis hinzufügen** unter **Assemblies**erweitern Sie **Framework**, und wählen Sie dann **WindowsBase aus**.
    
9. Fügen Sie den folgenden Code in die Lösung ein.
    
  ```cs
  using System;
  using System.Collections.Generic;
  using System.Linq;
  using System.Text;
  using System.IO;
  using System.IO.Packaging;
  using System.Diagnostics;
  namespace VisioFileExplorer
  {
      class Program
      {
          static void Main(string[] args)
          {    
              try
              {
                  Console.WriteLine("Opening the VSDX file ...");
                  // Need to get the folder path for the Desktop
                  // where the file is saved.
                  string dirPath = System.Environment.GetFolderPath(
                      System.Environment.SpecialFolder.Desktop);
                  DirectoryInfo myDir = new DirectoryInfo(dirPath);
                  // It is a best practice to get the file name string
                  // using a FileInfo object, but it isn't necessary.
                  FileInfo[] fInfos = myDir.GetFiles("*.vsdx");
                  FileInfo fi = fInfos[0];
                  string fName = fi.FullName;
                  // We're not going to do any more than open
                  // and read the list of parts in the package, although
                  // we can create a package or read/write what's inside.
                  using (Package fPackage = Package.Open(
                      fName, FileMode.Open, FileAccess.Read))
                  {
                      
                      // The way to get a reference to a package part is
                      // by using its URI. Thus, we're reading the URI
                      // for each part in the package.
                      PackagePartCollection fParts = fPackage.GetParts();
                      foreach (PackagePart fPart in fParts)
                      {
                          Console.WriteLine("Package part: {0}", fPart.Uri);
                      }
                  }   
              }
              catch (Exception err)
              {
                  Console.WriteLine("Error: {0}", err.Message);
              }
              finally
              {
                  Console.Write("\nPress any key to continue ...");
                  Console.ReadKey();
              }   
          }
      }
  }
  ```

  ```vb
  Imports System
  Imports System.Collections.Generic
  Imports System.Linq
  Imports System.Text
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Diagnostics
  Module Module1
      Sub Main()
          Try
              Console.WriteLine("Opening the VSDX file ...")
              ' Need to get the folder path for the Desktop
              ' or where the file is saved.
              Dim dirPath As String = System.Environment.GetFolderPath( _
                  System.Environment.SpecialFolder.Desktop)
              Dim myDir As New DirectoryInfo(dirPath)
              ' It is a best practice to get the file name string
              ' using a FileInfo object, but it isn't necessary.
              Dim fInfos As FileInfo() = myDir.GetFiles("*.vsdx")
              Dim fi As FileInfo = fInfos(0)
              Dim fName As String = fi.FullName
              ' We don't need to do any more than open
              ' and read the list of parts in the package, although
              ' we can create a package or read/write what's inside.
              Using fPackage As Package = Package.Open( _
                  fName, FileMode.Open, FileAccess.Read)
                  ' The way to get a reference to a document part is
                  ' by using its URI. Thus, we're reading the URI
                  ' for each document part in the package.
                  Dim fParts As PackagePartCollection = fPackage.GetParts()
                  For Each fPart As PackagePart In fParts
                      Console.WriteLine("Package part: {0}", fPart.Uri)
                  Next
              End Using
          Catch err As Exception
              Console.WriteLine("Error: {0}", err.Message)
          Finally
              Console.Write(vbLf &amp; "Press any key to continue ...")
              Console.ReadKey()
          End Try
      End Sub
  End Module
  
  ```

10. Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.
    
## <a name="see-also"></a>Siehe auch
<a name="vis15_IntroVSDX_Resources"> </a>

Weitere Informationen über das Visio 2013-Dateiformat, die Open Packaging-Konvention oder zum programmgesteuerten arbeiten mit Visio 2013or Office OpenXML-Dateien finden Sie unter den folgenden Ressourcen:
  
- [Visio für Entwickler](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [OPC: ein neuer Standard für das Verpacken Ihrer Daten](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).
    
- [Grundlagen der Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx)
    
- [Einführung in die Office (2007) Open XML-Dateiformate](http://msdn.microsoft.com/en-us/library/aa338205.aspx)
    

