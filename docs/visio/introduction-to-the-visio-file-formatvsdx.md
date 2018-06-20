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
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="5b3bf-103">Einführung in das Visio-Dateiformat (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="5b3bf-104">Erfahren Sie mehr über das neue Dateiformat in Visio 2013, einige hochrangige Konzepte für die Arbeit mit dem Visio 2013-Dateiformat programmgesteuert durchsuchen, und erstellen Sie eine einfache Konsolenanwendung, die ein Visio 2013-Testdatei.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b3bf-105">**In diesem Artikel** [Einführung in die](#vis15_IntroVSDX_Intro) [Was ist das Visio 2013-Dateiformat "Detail"?](#vis15_IntroVSDX_What)                   </span><span class="sxs-lookup"><span data-stu-id="5b3bf-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="5b3bf-106">[Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat](#vis15_IntroVSDX_Scenarios) [Erkunden Sie programmgesteuert das Visio 2013-Dateiformat](#vis15_IntroVSDX_Explore) [Weitere Ressourcen](#vis15_IntroVSDX_Resources)                    </span><span class="sxs-lookup"><span data-stu-id="5b3bf-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="5b3bf-107">Einführung</span><span class="sxs-lookup"><span data-stu-id="5b3bf-107">Introduction</span></span>
<span data-ttu-id="5b3bf-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="5b3bf-108"></span></span>

<span data-ttu-id="5b3bf-109">Visio 2013 führt ein neues Dateiformat (.vsdx) für Visio, die von der Visio-Binärdateiformat (.vsd) und das Dateiformat Visio XML-Zeichnung (VDX) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="5b3bf-110">Da das Visio 2013-Dateiformat Open Packaging-Konventionen und XML-basiert, können Entwickler, die mit diesen Technologien vertraut sind schnell zum programmgesteuerten arbeiten mit Visio 2013-Dateien informieren.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="5b3bf-111">Entwickler, die mit dem Dateiformat Visio XML-Zeichnung (VDX) aus früheren Versionen von Visio vertraut sind, können viele der gleichen XML-Strukturen in den Teilen des vsdx-Dateiformat suchen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="5b3bf-112">Interoperabilität mit Visio-Dateien ist wesentlich komplexer, da Drittanbietersoftware Visio-Dateien auf einer Ebene der Datei Format bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="5b3bf-113">Das Visio 2013-Dateiformat wird auf Visio Services in Microsoft SharePoint Server 2013, ohne dass ein "zwischengeschaltete" Dateiformat für die Veröffentlichung in SharePoint Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="5b3bf-114">Es gibt mehrere Dateitypen, durch Erweiterung, die das Visio 2013-Dateiformat umfassen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="5b3bf-115">Dieser Erweiterungen umfassen:</span><span class="sxs-lookup"><span data-stu-id="5b3bf-115">These extensions include:</span></span>
  
- <span data-ttu-id="5b3bf-116">.vsdx (Visio-Zeichnung)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="5b3bf-117">.vsdm (Visio-Makro aktivierte Zeichnung)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="5b3bf-118">.vssx (Visio-Schablone)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="5b3bf-119">.vssm (Visio-Makro aktivierte Schablone)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="5b3bf-120">.vstx (Visio-Vorlage)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="5b3bf-121">.vstm (Visio-Vorlage mit Makros)</span><span class="sxs-lookup"><span data-stu-id="5b3bf-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="5b3bf-p104">Nur die makrofähigen Dateien (.vsdm, .vssm, .vstm) können VBA-Makros speichern. Sie können Makros nicht in Dateien mit einer VSDX-, VSSX- oder VSTX-Erweiterung speichern.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="5b3bf-124">Was ist das Visio 2013-Dateiformat "Detail"?</span><span class="sxs-lookup"><span data-stu-id="5b3bf-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="5b3bf-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="5b3bf-125"></span></span>

<span data-ttu-id="5b3bf-126">Das Visio 2013-Dateiformat verwendet die Open Verpackung Conventions (OPC), die eine strukturierte Möglichkeit zum Speichern von Anwendungsdaten mit den zugehörigen Ressourcen mit einem Container des einige Sort─for wird eine ZIP-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="5b3bf-127">Grundlegende Ebene ist eine Visio 2013-Datei wirklich eine ZIP-Container, der andere Typen von Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="5b3bf-128">Sie können sogar Speichern einer Zeichnung in Visio 2013 als eine vsdx-Datei, benennen Sie die Erweiterung der Datei in "\*ZIP" die Datei wie folgt einen Ordner aus, die Inhalte finden Sie unter in Windows Explorer, und klicken Sie dann auf Öffnen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="5b3bf-129">Dieser Artikel enthält nur eine kurze Übersicht über die Open Packaging-Konventionen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="5b3bf-130">Finden Sie detaillierte Abdeckung der Konventionen in anderen Artikeln: > Weitere Informationen zu den Open Packaging Conventions selbst, finden Sie unter [OPC: ein neuer Standard für Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="5b3bf-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span></span> <span data-ttu-id="5b3bf-131">> Weitere Informationen zu Open Packaging-Konventionen und deren Verwendung in Microsoft Office-Dateien finden Sie unter [Grundlagen der Open Packaging-Konventionen](http://msdn.microsoft.com/en-us/library/ee361919.aspx) und [Einführung in die Microsoft Office (2007) Open XML-Dateiformaten](http://msdn.microsoft.com/en-us/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="5b3bf-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](http://msdn.microsoft.com/en-us/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="5b3bf-132">Pakete und Paketteile</span><span class="sxs-lookup"><span data-stu-id="5b3bf-132">Packages and Package Parts</span></span>

<span data-ttu-id="5b3bf-133">Wie zuvor gestartet wird, sind Visio 2013-Dateien ZIP-Container oder "Pakete", die anderen Dateien (mit der Bezeichnung "Paketteile") darin enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="5b3bf-134">Ein pakettei kann es sich um eine XML-Datei, eines Bilds, sogar einer VBA-Lösung sein.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="5b3bf-135">Die Teile im Paket können in zwei Hauptkategorien, "Dokumentteile" und "Beziehung Teile." weiter unterteilt werden</span><span class="sxs-lookup"><span data-stu-id="5b3bf-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="5b3bf-136">Die Dokumentteile enthalten die tatsächlichen Inhalte und Metadaten der Visio-Datei, wie der Name der Datei, die erste Seite und alle Formen, die er enthält, und sogar die datenverbindungen für die Formen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="5b3bf-137">Bilder und Textdateien, in dem Paket gelten Dokumentteile.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="5b3bf-138">Beziehung Teile werden weiter unten in diesem Artikel ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5b3bf-139">Wenn Sie eine Visio 2013-Datei mithilfe eines ZIP-Dienstprogramms öffnen, sehen Sie möglicherweise mehrere Ordner, die in der ZIP-Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="5b3bf-140">Sie können auch diese untergeordneten Adressen wie mit einem Dienstprogramm ZIP-Ordner bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="5b3bf-141">Diese "Ordner" wird jedoch untergeordnete Adressen innerhalb der ZIP-Paket keine eigentlichen Ordner darstellen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="5b3bf-142">Sie können die programmgesteuerte Entsprechung von Ordnern diese Sub-Adressen in Ihrer Lösung entwickelt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="5b3bf-p109">Paketteile (sowohl Dokumentteile und Beziehungsteile) verfügen über verknüpfte Inhaltstypen. Diese Inhaltstypen sind Zeichenfolgen, die einen MIME-Medientyp definieren. Diese Inhaltstypen bestimmen und prüfen die Art der MIME-Typen, die in der Datei enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="5b3bf-146">Beziehungen</span><span class="sxs-lookup"><span data-stu-id="5b3bf-146">Relationships</span></span>

<span data-ttu-id="5b3bf-147">Die Beziehung Teile (die Enden mit der Erweiterung "\*rels" und befinden sich in einem Ordner "_rels") wird beschrieben, wie die Teile im Paket miteinander in Beziehung stehen, und geben Sie die Struktur der Datei.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="5b3bf-148">Ein eigenständiges XML-Dokument wird die Beziehung zwischen über-und untergeordneten Elemente die Beziehung zwischen Entitäten miteinander ermittelt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="5b3bf-149">Andere Dateien möglicherweise andere Hierarchien oder Ordnerstruktur Datei verwenden, um die Interaktion von Inhalten in der Datei beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="5b3bf-150">Für das Visio 2013-Dateiformat ist das Paket gültige Visio-Datei aus, wenn sie die korrekte Liste der Webparts enthält und das Paket die Beziehungen zwischen den Teilen enthält.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="5b3bf-p111">Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen im Paket beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einem angegebenen Quell- (definiert durch den Namen und dem Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beziehungsteile werden beispielsweise verwendet, um zu beschreiben, welche Shape-Master mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander zusammenhängen oder wie Bilder und Objekte mit einer bestimmten Seite zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="5b3bf-154">Ähnlichkeiten und Unterschiede mit Visio VDX-schema</span><span class="sxs-lookup"><span data-stu-id="5b3bf-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="5b3bf-155">Wie bereits erwähnt, enthalten die frühere Versionen von Visio auch eine XML-basierte Datei Format, das Visio XML-Zeichnungsformat oder VDX.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="5b3bf-156">(In früheren Versionen von Visio, wird das Schema für den Visio-XML-Zeichnungsformat verwendet DatadiagramML bezeichnet.) Einige Teile von der Visio-XML-Schema haben dieselbe zwischen den beiden Dateiformate waren.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="5b3bf-157">Das **Windows** -Element und die untergeordneten Elemente bleiben beispielsweise Unchanged─with der Ausnahme, dass das **Windows** -Element jetzt ein Stammelement eines XML-Dokuments (window.xml) ist.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="5b3bf-158">Der größte Unterschied zwischen dem XML-Zeichnung und das Visio 2013-Dateiformat ist der Verpackung.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="5b3bf-159">Eine Datei im Format von XML-Zeichnung konnte wie eine normale eigenständige XML bearbeitet werden; das Visio 2013-Dateiformat muss als Paket bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="5b3bf-160">In der Visio 2013 hat der XML-Code in Webparts für einfacher Verbrauch aufgeteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="5b3bf-161">Eine andere bedeutende Änderung erfolgt ist, dass das Visio 2013-Dateiformat alle Dokumenteigenschaften im Dokumentteile beschrieben durch die OPC-standard (app.xml, core.xml, Benutzer.XML) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="5b3bf-162">Es ist jedoch eine bedeutende Änderung, die alle Visio-Entwickler berücksichtigen müssen: die Einführung der **Zelle**, **Zeile**und **im Abschnitt** Elemente.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="5b3bf-163">In der XML-Zeichnungsdateiformat Schema werden einzelne Zeilen und Zellen im ShapeSheet durch benannten Elemente dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="5b3bf-164">Angenommen Sie, dass Sie ein Dokument mit einer einzelnen Seite mit einer Form mit dem **PinX** Wert "2" (d. h., dass die Pin Drehung der Form 2 Zoll vom linken Rand der Zeichnung ist).</span><span class="sxs-lookup"><span data-stu-id="5b3bf-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="5b3bf-165">Im folgenden Code wird das relevante Markup für diese Einstellung im Dateiformat XML-Zeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="5b3bf-166">Hier ist das **PinX** -Element ein untergeordnetes Element des **XForm** -Elements, das wiederum ein untergeordnetes Element des **Shape** -Elements ist.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="5b3bf-167">Dieses Modell der Visio ShapeSheet-Benutzeroberfläche, in dem die Zelle **PinX** im Abschnitt **Shape Transform** eines Shapes enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="5b3bf-168">In Visio 2013-Dateiformat alle Zellen in der ShapeSheet─ **PinX** **LinePattern**, eine **X** -Zelle in einer **MoveTo** -Zeile in einem **Geometrie** -Abschnitt etc.─are durch einen Typ von XML-Element, **das Zellenelement** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="5b3bf-169">Verschiedene **Zelle** Elemente werden durch den Wert für das Attribut **N** voneinander individuated.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="5b3bf-170">Im obigen Beispiel ist daher die Daten in die Zelle **PinX** im ShapeSheet in eine VSDX-Datei wie im folgenden Code gezeigt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="5b3bf-171">**Das Zellenelement für **DrehbezX** (wie bei anderen einzelnen, benannten Zellen "Singleton Zellen" wie **LinePattern** oder **LockSelect**aufgerufen)** ist ein direktes untergeordnetes Element des **Shape** -Elements.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="5b3bf-172">Keine eindeutigen Elements ist erforderlich, um die Zeile, die Zelle **PinX enthält,** darstellen, wie jeder Form eine **PinX**nur verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="5b3bf-173">Was geschieht mit Abschnitten, die Tabellendaten wie **geometrischen** Abschnitte enthalten?</span><span class="sxs-lookup"><span data-stu-id="5b3bf-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="5b3bf-174">Für die Zellen in den Abschnitten das Visio 2013-Dateiformatschema **Abschnitt** verwendet und **Zeile** Elements─also definierten nach **N** -Attribut oder **T** -Attribut als Below─to dargestellt, die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="5b3bf-175">Dasselbe Shape aus dem vorherigen Beispiel kann beispielsweise Daten im Abschnitt **"Geometry" 1** enthalten, die den folgenden Code in das Schema der XML-Zeichnung aussieht.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="5b3bf-176">Es sieht jedoch wie der folgende Code in der Datei Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="5b3bf-177">Entwicklerszenarien für die Arbeit mit dem Visio 2013-Dateiformat</span><span class="sxs-lookup"><span data-stu-id="5b3bf-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="5b3bf-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="5b3bf-178"></span></span>

<span data-ttu-id="5b3bf-179">Wie oben beschrieben, nutzt das Visio 2013-Dateiformat mehrere dokumentiertes Technologien wie ZIP-Dateien und XML zum Speichern von Daten.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="5b3bf-180">Um eine Zeichnung auf Dateiebene Visio 2013 zu bearbeiten, eine Lösung benötigen nur für die .NET Framework-Namespaces und Klassen im Zusammenhang mit der Arbeit mit ZIP-Dateien oder XML, wie [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) oder [System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx)verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="5b3bf-181">Der wichtigste Vorteil des Dateiformats für Visio 2013-Entwickler ist, können Sie lesen und in Visio 2013-Dateien schreiben ohne Automatisieren der Visio-Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="5b3bf-182">Einige Szenarien, die Sie als Entwickler sollten, für das Arbeiten mit Visio 2013-Dateiformat, gehören:</span><span class="sxs-lookup"><span data-stu-id="5b3bf-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="5b3bf-183">Überprüfen die einzelne Visio 2013-Dateien für bestimmte Daten.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="5b3bf-184">Sie können ein Element aus der ZIP-Container selektiv lesen, ohne die gesamte Datei extrahieren.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="5b3bf-185">Aktualisieren von Bibliotheken mit Visio 2013-Dateien mit spezifischem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="5b3bf-186">Sie können das Logo in allen Hintergrundblätter neue branding Richtlinien entsprechend programmgesteuert ändern.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="5b3bf-187">Erstellen von Anwendungen, die Visio 2013-Dateien zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="5b3bf-188">Beispielsweise können Sie ein Tool erstellen, die ein Visio-Workflowdiagramm liest und führt dann eine eigene Geschäftslogik basierend auf diesen Workflow.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="5b3bf-189">Achten Sie darauf, dass die meisten Lösungen, die auf einem Clientcomputer ausgeführt werden können, auch auf einem Server ausgeführt werden können, da diese Lösungen standardmäßige .NET Framework-Assemblys verwenden!</span><span class="sxs-lookup"><span data-stu-id="5b3bf-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="5b3bf-190">Programmatisches Ermitteln des Visio 2013-Dateiformats</span><span class="sxs-lookup"><span data-stu-id="5b3bf-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="5b3bf-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="5b3bf-191"></span></span>

<span data-ttu-id="5b3bf-192">Die einfachste und grundlegende Aufgabe für alle Arbeiten mit dem Visio 2013-Dateiformat (engl.) wird die Datei als Paket öffnen und den Zugriff auf einzelne Teile im Paket.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="5b3bf-193">Die **System.IO.Packaging.Package** in die WindowsBase.dll enthält viele Klassen, mit denen Sie öffnen und Bearbeiten von Paketen und WebParts.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="5b3bf-194">Im folgenden Codebeispiel können Sie sehen, wie eine VSDX-Datei geöffnet wird, die Liste der Teile im Paket gelesen werden und Informationen über jeden Teil abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="5b3bf-195">So öffnen Sie eine VSDX-Datei und zeigen die Dokumentteile an</span><span class="sxs-lookup"><span data-stu-id="5b3bf-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="5b3bf-196">Öffnen Sie Visio 2013, und erstellen Sie ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="5b3bf-197">Erstellen Sie ein neues Dokument, und speichern Sie es auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="5b3bf-198">Öffnen Sie Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="5b3bf-199">Klicken Sie im Menü **Datei** auf **neu**, und wählen Sie dann ** Project **.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-199">On the **File** menu, choose **New**, and then choose ** Project **.</span></span>
    
5. <span data-ttu-id="5b3bf-200">Unter **Visual c#** oder **Visual Basic**erweitern Sie **Windows**, und wählen Sie dann **Konsolenanwendung**.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="5b3bf-201">Geben Sie im Feld **Name den Namen** 'VisioFileExplorer'.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="5b3bf-202">Das Konsolenanwendungsprojekt wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="5b3bf-203">Klicken Sie im **Projektmappen-Explorer**-Maustaste auf **VisioFileExplorer**, und klicken Sie dann auf **Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="5b3bf-204">Klicken Sie im Dialogfeld **Verweis hinzufügen** unter **Assemblies**erweitern Sie **Framework**, und wählen Sie dann **WindowsBase aus**.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="5b3bf-205">Fügen Sie den folgenden Code in die Lösung ein.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="5b3bf-p126">Drücken Sie F5 zum Debuggen der Lösung. Wenn das Programm die Ausführung abgeschlossen hat, drücken Sie eine beliebige Taste, um es zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="5b3bf-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b3bf-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b3bf-208">See also</span></span>
<span data-ttu-id="5b3bf-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="5b3bf-209"></span></span>

<span data-ttu-id="5b3bf-210">Weitere Informationen über das Visio 2013-Dateiformat, die Open Packaging-Konvention oder zum programmgesteuerten arbeiten mit Visio 2013or Office OpenXML-Dateien finden Sie unter den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="5b3bf-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="5b3bf-211">Visio für Entwickler</span><span class="sxs-lookup"><span data-stu-id="5b3bf-211">Visio for developers</span></span>](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- <span data-ttu-id="5b3bf-212">[OPC: ein neuer Standard für das Verpacken Ihrer Daten](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="5b3bf-212">[OPC: A New Standard for Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="5b3bf-213">Grundlagen der Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="5b3bf-213">Essentials of the Open Packaging Conventions</span></span>](http://msdn.microsoft.com/en-us/library/ee361919.aspx)
    
- [<span data-ttu-id="5b3bf-214">Einführung in die Office (2007) Open XML-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="5b3bf-214">Introducing the Office (2007) Open XML File Formats</span></span>](http://msdn.microsoft.com/en-us/library/aa338205.aspx)
    

