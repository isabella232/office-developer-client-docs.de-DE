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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699072"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="4a2fc-103">Einführung in das Visio-Dateiformat (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="4a2fc-104">Erfahren Sie mehr über das neue Dateiformat in Visio 2013, ermitteln Sie einige hochrangige Konzepte für die programmatische Arbeit mit dem Visio 2013-Dateiformat, und erstellen Sie eine einfache Konsolenanwendung, die eine Visio 2013-Datei überprüft.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-104">Learn about the new file format in vis15short, explore some high-level concepts for working with the vis15short file format programmatically, and create a simple console application that examines a vis15short file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a2fc-105">**Inhalt dieses Artikels**         [Einführung](#vis15_IntroVSDX_Intro)          [Was ist das integrierte Visio 2013-Dateiformat?](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="4a2fc-106">[Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat](#vis15_IntroVSDX_Scenarios)          [Das Visio 2013-Dateiformat programmgesteuert erkunden](#vis15_IntroVSDX_Explore)          [Zusätzliche Ressourcen](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="4a2fc-107">Einführung</span><span class="sxs-lookup"><span data-stu-id="4a2fc-107">Introduction</span></span>
<span data-ttu-id="4a2fc-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="4a2fc-108"></span></span>

<span data-ttu-id="4a2fc-109">Visio 2013 führt ein neues Dateiformat (.vsdx) für Visio ein, das das Visio-Binärdateiformat (.vsd) und Visio-XML-Zeichnungsdateiformat (.vdx) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="4a2fc-110">Da das Visio 2013-Dateiformat auf Open Packaging-Konventionen und XML-basiert, können Entwickler, die mit diesen Technologien vertraut sind, schnell lernen, wie man programmgesteuert mit Visio 2013-Dateien arbeitet.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="4a2fc-111">Entwickler, die mit dem Visio-XML-Zeichnungsdateiformat (.vdx) früherer Visio-Versionen vertraut sind, finden viele gleiche XML-Strukturen innerhalb der Bestandteile des VSDX-Dateiformats wieder.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="4a2fc-112">Die Interoperabilität mit Visio-Dateien wird erheblich erhöht, da Visio-Dateien auf Dateiformatebene mit Drittanbietersoftware bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="4a2fc-113">Das Visio 2013-Dateiformat wird in Visio Services in Microsoft SharePoint Server 2013 unterstützt, und es wird kein "zwischengeschaltetes" Dateiformat für die Veröffentlichung auf SharePoint Server benötigt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="4a2fc-114">Es gibt im weiteren Sinne verschiedene Datentypen, die das Visio 2013-Dateiformat umfassen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-114">There are several file types, by extension, that comprise the vis15short file format. These extensions include:</span></span> <span data-ttu-id="4a2fc-115">Zu diesen Erweiterungen zählen:</span><span class="sxs-lookup"><span data-stu-id="4a2fc-115">These extensions include:</span></span>
  
- <span data-ttu-id="4a2fc-116">.vsdx (Visio-Zeichnung)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="4a2fc-117">.vsdm (Visio-Zeichnung mit Makros)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="4a2fc-118">vssx (Visio-Schablone)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="4a2fc-119">.vsdm (Visio-Schablone mit Makros)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="4a2fc-120">vstx (Visio-Vorlage)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="4a2fc-121">.vstm (Visio-Vorlage mit Makros)</span><span class="sxs-lookup"><span data-stu-id="4a2fc-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="4a2fc-p104">Nur die makrofähigen Dateien (.vsdm, .vssm, .vstm) können VBA-Makros speichern. Sie können Makros nicht in Dateien mit einer VSDX-, VSSX- oder VSTX-Erweiterung speichern.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="4a2fc-124">Was ist das integrierte Visio 2013-Dateiformat?</span><span class="sxs-lookup"><span data-stu-id="4a2fc-124">What is the Visio 2013 file format “under the hood”?</span></span>
<span data-ttu-id="4a2fc-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="4a2fc-125"></span></span>

<span data-ttu-id="4a2fc-126">Das Visio 2013-Dateiformat verwendet die Open Packing-Konventionen (OPC), die eine strukturierte Möglichkeit zum Speichern von Anwendungsdaten mit verwandten Ressourcen definieren, wofür ein Container, wie z.B. eine Zip-Datei, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="4a2fc-127">Grundlegend ist eine Visio 2013-Datei ein Zip-Container, der andere Dateitypen enthält.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="4a2fc-128">Sie können eine Zeichnung in Visio 2013 als VSDX-Datei speichern, die Erweiterung der Datei in "\*.zip" im Windows-Explorer umbenennen, und die Datei dann wie einen Ordner öffnen, um den Inhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="4a2fc-129">Dieser Artikel bietet nur einen kurzen Überblick über die Open Packaging-Konventionen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-129">This article contains only a brief overview of the Open Packaging Conventions. You can find more detailed coverage of the conventions in other articles:</span></span> <span data-ttu-id="4a2fc-130">In anderen Artikeln finden Sie detaillierte Angaben zu den Konventionen. >  Weitere Informationen über die Open Packaging-Konventionen an sich finden Sie unter [OPC: Ein neuer Standard für das Verpacken Ihrer Daten](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="4a2fc-131">>  Weitere Informationen über die Open Packaging-Konventionen und deren Verwendung in Microsoft Office-Dateien finden Sie unter [Grundlagen der Open Packaging-Konventionen](https://msdn.microsoft.com/library/ee361919.aspx) und [Einführung in die Microsoft Office (2007) Open XML-Dateiformate](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-131">For more information about the Open Packaging Conventions and their use in officenv files, see  Essentials of the Open Packaging Conventions http://msdn.microsoft.com/en-us/library/ee361919.aspx  and  Introducing the Office (2007) Open XML File Formats http://msdn.microsoft.com/en-us/library/aa338205.aspx .</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="4a2fc-132">Pakete und Paketteile</span><span class="sxs-lookup"><span data-stu-id="4a2fc-132">Packages and Package Parts</span></span>

<span data-ttu-id="4a2fc-133">Wie bereits erwähnt sind Visio 2013-Dateien Zip-Container oder "Pakete", die andere Dateien ("Paketteile") enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="4a2fc-134">Ein Paketteil kann eine XML-Datei, ein Bild oder sogar eine VBA-Lösung sein.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="4a2fc-135">Die Teile innerhalb des Pakets können weiterhin in zwei Kategorien unterteilt werden: "Dokumentteile" und "Beziehungsteile".</span><span class="sxs-lookup"><span data-stu-id="4a2fc-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="4a2fc-136">Die Dokumentteile enthalten den eigentlichen Inhalt und Metadaten der Visio-Datei, z. B. den Namen der Datei, die erste Seite und alle Formen, die sie enthält, und sogar die Datenverbindungen für die Formen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="4a2fc-137">Bilder und Textdateien im Paket werden als Dokumentteile bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="4a2fc-138">Beziehungsteile werden später in diesem Artikel noch genauer erläutert.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4a2fc-139">Wenn Sie eine Visio 2013-Datei über ein Zip-Programm öffnen, sehen Sie möglicherweise mehrere Ordner, die sich innerhalb des Zip-Pakets befinden.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="4a2fc-140">Sie können diese untergeordneten Adressen wie Ordner mit einem Zip-Programm bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="4a2fc-141">Diese "Ordner" stellen jedoch untergeordnete Adressen innerhalb des Zip-Pakets und keine tatsächlichen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="4a2fc-142">Sie können nicht die programmgesteuerte Entsprechung von Ordnern verwenden, um in Ihrer Lösung mit diesen untergeordneten Adressen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="4a2fc-p109">Paketteile (sowohl Dokumentteile und Beziehungsteile) verfügen über verknüpfte Inhaltstypen. Diese Inhaltstypen sind Zeichenfolgen, die einen MIME-Medientyp definieren. Diese Inhaltstypen bestimmen und prüfen die Art der MIME-Typen, die in der Datei enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="4a2fc-146">Beziehungen</span><span class="sxs-lookup"><span data-stu-id="4a2fc-146">Relationships</span></span>

<span data-ttu-id="4a2fc-147">Die Beziehungsteile (die auf die Erweiterung "\*rels" enden und in einem "_rels"-Ordner gespeichert sind) beschreiben, wie die Teile innerhalb des Pakets miteinander in Beziehung stehen, und stellen die Struktur der Datei bereit.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="4a2fc-148">Ein eigenständiges XML-Dokument verwendet die übergeordnete/untergeordnete Beziehung der Elemente, um die Beziehung zwischen den Entitäten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="4a2fc-149">Andere Dateien verwenden möglicherweise andere Hierarchien oder Dateiordnerstrukturen, um die Interaktion der Inhalte in der Datei zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="4a2fc-150">Für das Visio 2013-Dateiformat ist das Paket eine gültige Visio-Datei, wenn es den richtigen Satz von Teilen und die Beziehungen zwischen den Teilen enthält.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="4a2fc-p111">Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen im Paket beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einem angegebenen Quell- (definiert durch den Namen und dem Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beziehungsteile werden beispielsweise verwendet, um zu beschreiben, welche Shape-Master mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander zusammenhängen oder wie Bilder und Objekte mit einer bestimmten Seite zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="4a2fc-154">Ähnlichkeiten und Unterschiede mit dem Visio-VDX-Schema</span><span class="sxs-lookup"><span data-stu-id="4a2fc-154">Similarities and differences with visnvshort VDX schema</span></span>

<span data-ttu-id="4a2fc-155">Wie bereits erwähnt, enthalten die früheren Versionen von Visio auch ein XML-basiertes Dateiformat, das Visio-XML-Zeichnungsformat oder .vdx.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="4a2fc-156">(In früheren Versionen von Visio wird das Schema für das Visio-XML-Zeichnungsformat als DatadiagramML bezeichnet.) Einige Teile aus dem Visio-XML-Schema sind in beiden Dateiformaten gleich.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="4a2fc-157">Das **Windows**-Element und seine untergeordneten Elemente sind z. B. gleich geblieben, allerdings mit der Ausnahme, dass das **Windows**-Element jetzt ein Stammelement eines XML-Dokuments (window.xml) ist.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="4a2fc-158">Der größte Unterschied zwischen dem XML-Zeichnungsformat und dem Visio 2013-Dateiformat ist das Verpacken.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="4a2fc-159">Eine Datei im XML-Zeichnungsformat kann wie eine normale eigenständige XML bearbeitet werden ; das Visio 2013-Dateiformat muss als Paket bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="4a2fc-160">In Visio 2013 wird die XML für eine leichtere Verarbeitung in Teile eingeteilt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="4a2fc-161">Eine weitere bemerkenswerte Änderung besteht darin, dass das Visio 2013-Dateiformat alle Dokumenteigenschaften in vom OPC-Standard beschriebenen Dokumentteilen (app.xml, core.xml, custom.xlm) speichert.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="4a2fc-162">Es gibt jedoch eine wesentliche Änderung, über die sich alle Visio-Entwickler bewusst sein müssen: die Einführung der Elemente **Zelle**, **Zeile** und **Abschnitt**.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="4a2fc-163">Im XML-Zeichnungsdateiformat-Schema werden einzelne Zeilen und Zellen im ShapeSheet durch benannte Elemente dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="4a2fc-164">Nehmen wir z. B. einmal an, dass Sie ein Dokument mit einer einzelnen Seite besitzen, das eine Form mit einem **PinX**-Wert von "2" enthält (d. h., die Drehachse der Form befindet sich 2 Zoll vom linken Rand der Zeichnung entfernt).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="4a2fc-165">Das relevante Markup für diese Einstellung im XML-Zeichnungsdateiformat wird im folgenden Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="4a2fc-166">Hier ist das **PinX**-Element ein untergeordnetes Element des **XForm**-Elements, das wiederum ein untergeordnetes Element des **Shape**-Elements ist.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element. This models the visnvshort ShapeSheet UI, where the PinX cell is included in the Shape Transform section of a shape.</span></span> <span data-ttu-id="4a2fc-167">Dies formt die Visio-ShapeSheet-Benutzeroberfläche, wobei die Zelle **PinX** im Abschnitt **Shape Transform** einer Form enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-167">Here, the PinX element is a child of the XForm element, which is in turn a child of the Shape element. This models the visnvshort ShapeSheet UI, where the PinX cell is included in the Shape Transform section of a shape.</span></span> 
  
<span data-ttu-id="4a2fc-168">Im Visio 2013-Dateiformat werden alle Zellen im ShapeSheet, d. h. **PinX**, **LinePattern**, eine **X**-Zelle in einer **MoveTo**-Zeile in einem **Geometry**-Abschnitt etc., von einem XML-Element des Typs **Zelle** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="4a2fc-169">Andere **Cell**-Elemente unterscheiden sich jeweils durch den Wert Ihres **N**-Attributs voneinander.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="4a2fc-170">Folglich werden im Beispiel oben die in der **PinX**-Zelle des ShapeSheets enthaltenen Daten wie im folgenden Code dargestellt in einer VSDX-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="4a2fc-171">Das **Cell**-Element für **PinX** (sowie andere einzelne, benannte Zellen, die auch "Singleton-Zellen" genannt werden, wie z.B. **LinePattern** oder **LockSelect**) ist ein direkt untergeordnetes Element des **Shape**-Elements.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-171">The **Cell** element for **PinX** (as well as other individual, named cells called “singleton cells” like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element. No unique element is needed to represent the row that contains the PinX cell, as each shape can only have one PinX.</span></span> <span data-ttu-id="4a2fc-172">Es wird kein eindeutiges Element benötigt, um die Zeile darzustellen, die die **PinX**-Zelle enthält, da jede Form nur eine **PinX** aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-172">The **Cell** element for **PinX** (as well as other individual, named cells called “singleton cells” like LinePattern or LockSelect) is a direct child of the Shape element. No unique element is needed to represent the row that contains the PinX cell, as each shape can only have one PinX.</span></span>
  
<span data-ttu-id="4a2fc-173">Wie sieht es mit Abschnitten aus, die tabellarische Daten enthalten, wie z. B. **Geometry**-Abschnitte?</span><span class="sxs-lookup"><span data-stu-id="4a2fc-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="4a2fc-174">Das Visio 2013-Dateiformat-Schema verwendet zum Aufbewahren der Daten der Zellen in diesen Abschnitten \*\*Section- und Row-Elemente, die wie unten dargestellt durch ihre N-Attribute oder T-Attribute unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="4a2fc-175">Beispielsweise kann die gleiche Form aus dem vorherigen Beispiel Daten im **Geometry 1**-Abschnitt enthalten, die aussehen wie der folgende Code im XML-Zeichnungsschema.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="4a2fc-176">Es sieht jedoch wie der folgende Code in der Visio 2013-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-176">However, it looks like the following code in the vis15short file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="4a2fc-177">Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat</span><span class="sxs-lookup"><span data-stu-id="4a2fc-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="4a2fc-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="4a2fc-178"></span></span>

<span data-ttu-id="4a2fc-179">Wie oben beschrieben nutzt das Visio 2013-Dateiformat mehrere gängige Technologien wie Zip-Dateien und XML, um Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="4a2fc-180">Um eine Visio 2013-Zeichnung auf Dateiebene zu bearbeiten, muss eine Lösung nur die .NET Framework-Namespaces und Klassen im Zusammenhang mit der Arbeit mit Zip-Dateien oder XML verwenden, wie z. B. [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) oder [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="4a2fc-181">Der wichtigste Vorteil des Visio 2013-Dateiformats besteht für Entwickler darin, dass Visio 2013-Dateien gelesen werden können und darin geschrieben werden kann, ohne dass die Visio-Clientanwendung automatisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="4a2fc-182">Einige Szenarien, die Sie als Entwickler berücksichtigen sollten, wenn Sie mit dem Visio 2013-Dateiformat arbeiten:</span><span class="sxs-lookup"><span data-stu-id="4a2fc-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="4a2fc-183">Einzelne Visio 2013-Dateien auf bestimmte Daten überprüfen</span><span class="sxs-lookup"><span data-stu-id="4a2fc-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="4a2fc-184">Sie können ein Element aus dem Zip-Container selektiv lesen, ohne die gesamte Datei extrahieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-184">Checking individual vis15short files for specific data. You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="4a2fc-185">Aktualisieren von Bibliotheken der Visio 2013-Dateien mit bestimmten Inhalten</span><span class="sxs-lookup"><span data-stu-id="4a2fc-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="4a2fc-186">Sie können das Logo in allen Hintergrundseiten programmatisch ändern, um neue Brandingrichtlinien widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-186">Updating libraries of vis15short files with specific content. You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="4a2fc-187">Erstellen von Anwendungen, die Visio 2013-Dateien verwenden</span><span class="sxs-lookup"><span data-stu-id="4a2fc-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="4a2fc-188">Beispielsweise können Sie ein Tool erstellen, das ein Visio-Workflowdiagramm liest und dann seine eigene Geschäftslogik auf Grundlage dieses Workflows ausführt.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-188">Creating applications that consume vis15short files. For example, you can build a tool that reads a visnvshort workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="4a2fc-189">Achten Sie darauf, dass die meisten Lösungen, die auf einem Clientcomputer ausgeführt werden können, auch auf einem Server ausgeführt werden können, da diese Lösungen standardmäßige .NET Framework-Assemblys verwenden!</span><span class="sxs-lookup"><span data-stu-id="4a2fc-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="4a2fc-190">Das Visio 2013-Dateiformat programmgesteuert erkunden</span><span class="sxs-lookup"><span data-stu-id="4a2fc-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="4a2fc-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="4a2fc-191"></span></span>

<span data-ttu-id="4a2fc-192">Der einfachste und grundlegendste Vorgang bei der Arbeit mit dem Visio 2013-Dateiformat besteht darin, die Datei als Paket zu öffnen und dann auf einzelne Elemente im Paket zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-192">The most basic and fundamental task for any developer working with the vis15short file format is opening the file as a package and then accessing individual parts within the package. The System.IO.Packaging.Package in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> <span data-ttu-id="4a2fc-193">Das **System.IO.Packaging.Package** in der WindowsBase.dll enthält viele Klassen, mit denen Sie Pakete und Teile öffnen und bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-193">The most basic and fundamental task for any developer working with the vis15short file format is opening the file as a package and then accessing individual parts within the package. The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="4a2fc-194">Im folgenden Codebeispiel können Sie sehen, wie eine VSDX-Datei geöffnet wird, die Liste der Teile im Paket gelesen werden und Informationen über jeden Teil abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="4a2fc-195">Öffnen einer .vsdx-Datei und Anzeigen der Dokumentteile</span><span class="sxs-lookup"><span data-stu-id="4a2fc-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="4a2fc-196">Öffnen Sie Visio 2013, und erstellen Sie ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-196">Open vis15short and create a new document.</span></span>
    
2. <span data-ttu-id="4a2fc-197">Erstellen Sie ein neues Dokument, und speichern Sie es auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="4a2fc-198">Öffnen Sie Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="4a2fc-199">Wählen Sie im Menü **Datei** **Neu** aus, und wählen Sie dann \*\* Projekt \*\*.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-199">On the **File** menu, point to **New**, and then choose Project.</span></span>
    
5. <span data-ttu-id="4a2fc-200">Erweitern Sie unter \*\*visuelle C# \*\* oder **Visual Basic** **Windows**, und wählen Sie dann **Console Application**.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="4a2fc-201">Geben Sie in das Feld **Name** den Eintrag "VisioFileExplorer" ein.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-201">In the Name box, type SampleUdf.</span></span> <span data-ttu-id="4a2fc-202">Das Konsolenanwendungsprojekt wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-202">In the Name box, type ‘VisioFileExplorer’. The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="4a2fc-203">Klicken Sie im **Solution Explorer** mit der rechten Maustaste auf **VisioFileExplorer**, und klicken Sie dann auf **Add Reference**.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="4a2fc-204">Erweitern Sie im **Add Reference**-Dialogfeld unter **Assemblies** **Framework**, und wählen Sie dann **WindowsBase** aus.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="4a2fc-205">Fügen Sie den folgenden Code in die Lösung ein.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="4a2fc-p126">Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a2fc-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a2fc-208">See also</span></span>
<span data-ttu-id="4a2fc-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="4a2fc-209"></span></span>

<span data-ttu-id="4a2fc-210">Weitere Informationen über das Visio 2013-Dateiformat, die Open Packaging-Konvention oder die programmatische Arbeit mit Visio 2013- oder Office-Open XML-Dateien finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4a2fc-210">For more information about the vis15short file format, the Open Packaging Convention, or how to work with vis15shortor Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="4a2fc-211">Visio für Entwickler</span><span class="sxs-lookup"><span data-stu-id="4a2fc-211">New in Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="4a2fc-212">[OPC: Ein neuer Standard für das Verpacken Ihrer Daten](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-212">[OPC: A New Standard for Packaging Your Datahttp://msdn.microsoft.com/en-us/magazine/cc163372.aspx](https://msdn.microsoft.com/magazine/cc163372.aspx)</span></span>
    
- [<span data-ttu-id="4a2fc-213">Grundlagen der Open Packaging-Konventionen</span><span class="sxs-lookup"><span data-stu-id="4a2fc-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="4a2fc-214">Einführung in die Microsoft Office (2007) Open XML-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="4a2fc-214">Introducing the Office (2007) Open XML File Formatshttp://msdn.microsoft.com/en-us/library/aa338205.aspx</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

