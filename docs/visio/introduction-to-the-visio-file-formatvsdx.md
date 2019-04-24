---
title: Einführung in das Visio-Dateiformat (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Erfahren Sie mehr über das neue Dateiformat in Visio 2013, ermitteln Sie einige hochrangige Konzepte für die programmatische Arbeit mit dem Visio 2013-Dateiformat, und erstellen Sie eine einfache Konsolenanwendung, die eine Visio 2013-Datei überprüft.
localization_priority: Priority
ms.openlocfilehash: 74c0f05a1db280386f3dc9dfd23da73a9b2daaf5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357274"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Einführung in das Visio-Dateiformat (.vsdx)

Erfahren Sie mehr über das neue Dateiformat in Visio 2013, ermitteln Sie einige hochrangige Konzepte für die programmatische Arbeit mit dem Visio 2013-Dateiformat, und erstellen Sie eine einfache Konsolenanwendung, die eine Visio 2013-Datei überprüft.
  
|||
|:-----|:-----|
|**Inhalt dieses Artikels**         [Einführung](#vis15_IntroVSDX_Intro)          [Was ist das integrierte Visio 2013-Dateiformat?](#vis15_IntroVSDX_What)          [Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat](#vis15_IntroVSDX_Scenarios)          [Das Visio 2013-Dateiformat programmgesteuert erkunden](#vis15_IntroVSDX_Explore)          [Zusätzliche Ressourcen](#vis15_IntroVSDX_Resources)||
   
## <a name="introduction"></a>Einführung
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 führt ein neues Dateiformat (.vsdx) für Visio ein, das das Visio-Binärdateiformat (.vsd) und Visio-XML-Zeichnungsdateiformat (.vdx) ersetzt. Da das Visio 2013-Dateiformat auf Open Packaging-Konventionen und XML-basiert, können Entwickler, die mit diesen Technologien vertraut sind, schnell lernen, wie man programmgesteuert mit Visio 2013-Dateien arbeitet. Entwickler, die mit dem Visio-XML-Zeichnungsdateiformat (.vdx) früherer Visio-Versionen vertraut sind, finden viele gleiche XML-Strukturen innerhalb der Bestandteile des VSDX-Dateiformats wieder. Die Interoperabilität mit Visio-Dateien wird erheblich erhöht, da Visio-Dateien auf Dateiformatebene mit Drittanbietersoftware bearbeitet werden können. Das Visio 2013-Dateiformat wird in Visio Services in Microsoft SharePoint Server 2013 unterstützt, und es wird kein "zwischengeschaltetes" Dateiformat für die Veröffentlichung auf SharePoint Server benötigt.
  
Es gibt im weiteren Sinne verschiedene Datentypen, die das Visio 2013-Dateiformat umfassen. Zu diesen Erweiterungen zählen:
  
- .vsdx (Visio-Zeichnung)
    
- .vsdm (Visio-Zeichnung mit Makros)
    
- vssx (Visio-Schablone)
    
- .vsdm (Visio-Schablone mit Makros)
    
- vstx (Visio-Vorlage)
    
- .vstm (Visio-Vorlage mit Makros)
    
> [!NOTE]
> Nur die makrofähigen Dateien (.vsdm, .vssm, .vstm) können VBA-Makros speichern. Sie können Makros nicht in Dateien mit einer VSDX-, VSSX- oder VSTX-Erweiterung speichern. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Was ist das integrierte Visio 2013-Dateiformat?
<a name="vis15_IntroVSDX_What"> </a>

Das Visio 2013-Dateiformat verwendet die Open Packing-Konventionen (OPC), die eine strukturierte Möglichkeit zum Speichern von Anwendungsdaten mit verwandten Ressourcen definieren, wofür ein Container, wie z.B. eine Zip-Datei, verwendet wird. Grundlegend ist eine Visio 2013-Datei ein Zip-Container, der andere Dateitypen enthält. Sie können eine Zeichnung in Visio 2013 als VSDX-Datei speichern, die Erweiterung der Datei in "\*.zip" im Windows-Explorer umbenennen, und die Datei dann wie einen Ordner öffnen, um den Inhalt anzuzeigen.
  
> [!NOTE]
>  Dieser Artikel bietet nur einen kurzen Überblick über die Open Packaging-Konventionen. In anderen Artikeln finden Sie detaillierte Angaben zu den Konventionen. >  Weitere Informationen über die Open Packaging-Konventionen an sich finden Sie unter [OPC: Ein neuer Standard für das Verpacken Ihrer Daten](https://msdn.microsoft.com/magazine/cc163372.aspx). >  Weitere Informationen über die Open Packaging-Konventionen und deren Verwendung in Microsoft Office-Dateien finden Sie unter [Grundlagen der Open Packaging-Konventionen](https://msdn.microsoft.com/library/ee361919.aspx) und [Einführung in die Microsoft Office (2007) Open XML-Dateiformate](https://msdn.microsoft.com/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Pakete und Paketteile

Wie bereits erwähnt sind Visio 2013-Dateien Zip-Container oder "Pakete", die andere Dateien ("Paketteile") enthalten. Ein Paketteil kann eine XML-Datei, ein Bild oder sogar eine VBA-Lösung sein. Die Teile innerhalb des Pakets können weiterhin in zwei Kategorien unterteilt werden: "Dokumentteile" und "Beziehungsteile". Die Dokumentteile enthalten den eigentlichen Inhalt und Metadaten der Visio-Datei, z. B. den Namen der Datei, die erste Seite und alle Formen, die sie enthält, und sogar die Datenverbindungen für die Formen. Bilder und Textdateien im Paket werden als Dokumentteile bezeichnet. Beziehungsteile werden später in diesem Artikel noch genauer erläutert.
  
> [!NOTE]
> Wenn Sie eine Visio 2013-Datei über ein Zip-Programm öffnen, sehen Sie möglicherweise mehrere Ordner, die sich innerhalb des Zip-Pakets befinden. Sie können diese untergeordneten Adressen wie Ordner mit einem Zip-Programm bearbeiten. Diese "Ordner" stellen jedoch untergeordnete Adressen innerhalb des Zip-Pakets und keine tatsächlichen Ordner dar. Sie können nicht die programmgesteuerte Entsprechung von Ordnern verwenden, um in Ihrer Lösung mit diesen untergeordneten Adressen zu arbeiten. 
  
Paketteile (sowohl Dokumentteile und Beziehungsteile) verfügen über verknüpfte Inhaltstypen. Diese Inhaltstypen sind Zeichenfolgen, die einen MIME-Medientyp definieren. Diese Inhaltstypen bestimmen und prüfen die Art der MIME-Typen, die in der Datei enthalten sein können.
  
### <a name="relationships"></a>Beziehungen

Die Beziehungsteile (die auf die Erweiterung "\*rels" enden und in einem "_rels"-Ordner gespeichert sind) beschreiben, wie die Teile innerhalb des Pakets miteinander in Beziehung stehen, und stellen die Struktur der Datei bereit. Ein eigenständiges XML-Dokument verwendet die übergeordnete/untergeordnete Beziehung der Elemente, um die Beziehung zwischen den Entitäten zu bestimmen. Andere Dateien verwenden möglicherweise andere Hierarchien oder Dateiordnerstrukturen, um die Interaktion der Inhalte in der Datei zu beschreiben. Für das Visio 2013-Dateiformat ist das Paket eine gültige Visio-Datei, wenn es den richtigen Satz von Teilen und die Beziehungen zwischen den Teilen enthält. 
  
Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen im Paket beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einem angegebenen Quell- (definiert durch den Namen und dem Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beziehungsteile werden beispielsweise verwendet, um zu beschreiben, welche Shape-Master mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander zusammenhängen oder wie Bilder und Objekte mit einer bestimmten Seite zusammenhängen. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Ähnlichkeiten und Unterschiede mit dem Visio-VDX-Schema

Wie bereits erwähnt, enthalten die früheren Versionen von Visio auch ein XML-basiertes Dateiformat, das Visio-XML-Zeichnungsformat oder .vdx. (In früheren Versionen von Visio wird das Schema für das Visio-XML-Zeichnungsformat als DatadiagramML bezeichnet.) Einige Teile aus dem Visio-XML-Schema sind in beiden Dateiformaten gleich. Das **Windows**-Element und seine untergeordneten Elemente sind z. B. gleich geblieben, allerdings mit der Ausnahme, dass das **Windows**-Element jetzt ein Stammelement eines XML-Dokuments (window.xml) ist. 
  
Der größte Unterschied zwischen dem XML-Zeichnungsformat und dem Visio 2013-Dateiformat ist das Verpacken. Eine Datei im XML-Zeichnungsformat kann wie eine normale eigenständige XML bearbeitet werden ; das Visio 2013-Dateiformat muss als Paket bearbeitet werden. In Visio 2013 wird die XML für eine leichtere Verarbeitung in Teile eingeteilt. Eine weitere bemerkenswerte Änderung besteht darin, dass das Visio 2013-Dateiformat alle Dokumenteigenschaften in vom OPC-Standard beschriebenen Dokumentteilen (app.xml, core.xml, custom.xlm) speichert.
  
Es gibt jedoch eine wesentliche Änderung, über die sich alle Visio-Entwickler bewusst sein müssen: die Einführung der Elemente **Zelle**, **Zeile** und **Abschnitt**. Im XML-Zeichnungsdateiformat-Schema werden einzelne Zeilen und Zellen im ShapeSheet durch benannte Elemente dargestellt. Nehmen wir z. B. einmal an, dass Sie ein Dokument mit einer einzelnen Seite besitzen, das eine Form mit einem **PinX**-Wert von "2" enthält (d. h., die Drehachse der Form befindet sich 2 Zoll vom linken Rand der Zeichnung entfernt). Das relevante Markup für diese Einstellung im XML-Zeichnungsdateiformat wird im folgenden Code dargestellt. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Hier ist das **PinX**-Element ein untergeordnetes Element des **XForm**-Elements, das wiederum ein untergeordnetes Element des **Shape**-Elements ist. Dies formt die Visio-ShapeSheet-Benutzeroberfläche, wobei die Zelle **PinX** im Abschnitt **Shape Transform** einer Form enthalten ist. 
  
Im Visio 2013-Dateiformat werden alle Zellen im ShapeSheet, d. h. **PinX**, **LinePattern**, eine **X**-Zelle in einer **MoveTo**-Zeile in einem **Geometry**-Abschnitt etc., von einem XML-Element des Typs **Zelle** dargestellt. Andere **Cell**-Elemente unterscheiden sich jeweils durch den Wert Ihres **N**-Attributs voneinander. Folglich werden im Beispiel oben die in der **PinX**-Zelle des ShapeSheets enthaltenen Daten wie im folgenden Code dargestellt in einer VSDX-Datei gespeichert. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

Das **Cell**-Element für **PinX** (sowie andere einzelne, benannte Zellen, die auch "Singleton-Zellen" genannt werden, wie z.B. **LinePattern** oder **LockSelect**) ist ein direkt untergeordnetes Element des **Shape**-Elements. Es wird kein eindeutiges Element benötigt, um die Zeile darzustellen, die die **PinX**-Zelle enthält, da jede Form nur eine **PinX** aufweisen kann.
  
Wie sieht es mit Abschnitten aus, die tabellarische Daten enthalten, wie z. B. **Geometry**-Abschnitte? Das Visio 2013-Dateiformat-Schema verwendet zum Aufbewahren der Daten der Zellen in diesen Abschnitten **Section- und Row-Elemente, die wie unten dargestellt durch ihre N-Attribute oder T-Attribute unterschieden werden. Beispielsweise kann die gleiche Form aus dem vorherigen Beispiel Daten im **Geometry 1**-Abschnitt enthalten, die aussehen wie der folgende Code im XML-Zeichnungsschema. 
  
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

Es sieht jedoch wie der folgende Code in der Visio 2013-Datei aus.
  
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

Wie oben beschrieben nutzt das Visio 2013-Dateiformat mehrere gängige Technologien wie Zip-Dateien und XML, um Daten zu speichern. Um eine Visio 2013-Zeichnung auf Dateiebene zu bearbeiten, muss eine Lösung nur die .NET Framework-Namespaces und Klassen im Zusammenhang mit der Arbeit mit Zip-Dateien oder XML verwenden, wie z. B. [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) oder [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).
  
Der wichtigste Vorteil des Visio 2013-Dateiformats besteht für Entwickler darin, dass Visio 2013-Dateien gelesen werden können und darin geschrieben werden kann, ohne dass die Visio-Clientanwendung automatisiert werden muss. Einige Szenarien, die Sie als Entwickler berücksichtigen sollten, wenn Sie mit dem Visio 2013-Dateiformat arbeiten:
  
- Einzelne Visio 2013-Dateien auf bestimmte Daten überprüfen Sie können ein Element aus dem Zip-Container selektiv lesen, ohne die gesamte Datei extrahieren zu müssen.
    
- Aktualisieren von Bibliotheken der Visio 2013-Dateien mit bestimmten Inhalten Sie können das Logo in allen Hintergrundseiten programmatisch ändern, um neue Brandingrichtlinien widerzuspiegeln.
    
- Erstellen von Anwendungen, die Visio 2013-Dateien verwenden Beispielsweise können Sie ein Tool erstellen, das ein Visio-Workflowdiagramm liest und dann seine eigene Geschäftslogik auf Grundlage dieses Workflows ausführt.
    
Achten Sie darauf, dass die meisten Lösungen, die auf einem Clientcomputer ausgeführt werden können, auch auf einem Server ausgeführt werden können, da diese Lösungen standardmäßige .NET Framework-Assemblys verwenden!
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Das Visio 2013-Dateiformat programmgesteuert erkunden
<a name="vis15_IntroVSDX_Explore"> </a>

Der einfachste und grundlegendste Vorgang bei der Arbeit mit dem Visio 2013-Dateiformat besteht darin, die Datei als Paket zu öffnen und dann auf einzelne Elemente im Paket zuzugreifen. Das **System.IO.Packaging.Package** in der WindowsBase.dll enthält viele Klassen, mit denen Sie Pakete und Teile öffnen und bearbeiten können. 
  
Im folgenden Codebeispiel können Sie sehen, wie eine VSDX-Datei geöffnet wird, die Liste der Teile im Paket gelesen werden und Informationen über jeden Teil abgerufen werden können.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Öffnen einer .vsdx-Datei und Anzeigen der Dokumentteile

1. Öffnen Sie Visio 2013, und erstellen Sie ein neues Dokument.
    
2. Erstellen Sie ein neues Dokument, und speichern Sie es auf dem Desktop.
    
3. Öffnen Sie Visual Studio 2012.
    
4. Wählen Sie im Menü **Datei** **Neu** aus, und wählen Sie dann ** Projekt **.
    
5. Erweitern Sie unter **visuelle C# ** oder **Visual Basic** **Windows**, und wählen Sie dann **Console Application**.
    
6. Geben Sie in das Feld **Name** den Eintrag "VisioFileExplorer" ein. Das Konsolenanwendungsprojekt wird geöffnet. 
    
7. Klicken Sie im **Projektmappen-Explorer** mit der rechten Maustaste auf **VisioFileExplorer**, und klicken Sie dann auf **Verweis hinzufügen**. 
    
8. Erweitern Sie im Dialogfeld **Verweis hinzufügen** unter **Assemblies** den Knoten **Framework**, und wählen Sie dann **WindowsBase** aus.
    
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

Weitere Informationen über das Visio 2013-Dateiformat, die Open Packaging-Konvention oder die programmatische Arbeit mit Visio 2013- oder Office-Open XML-Dateien finden Sie in den folgenden Themen:
  
- [Visio für Entwickler](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: Ein neuer Standard für das Verpacken Ihrer Daten](https://msdn.microsoft.com/magazine/cc163372.aspx).
    
- [Grundlagen der Open Packaging-Konventionen](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Einführung in die Microsoft Office (2007) Open XML-Dateiformate](https://msdn.microsoft.com/library/aa338205.aspx)
    

