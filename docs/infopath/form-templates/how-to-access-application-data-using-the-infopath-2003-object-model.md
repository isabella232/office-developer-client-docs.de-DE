---
title: Access-Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [Infopath 2007], den Zugriff auf Daten mithilfe von InfoPath 2003-kompatible Formularvorlagen, zugreifen auf Anwendungsdaten 2003-Objektmodells
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Das InfoPath 2003-kompatible Objektmodell bietet Objekte und Sammlungen, die den Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen zu einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF) verwendet werden können. Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der Benutzeroberfläche der Anwendung instanziiert wird.
ms.openlocfilehash: e9cf01ff2ffa939fce5af277e756e679478f8b39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790720"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="a961f-105">Access-Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="a961f-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="a961f-106">Das InfoPath 2003-kompatible Objektmodell bietet Objekte und Sammlungen, die den Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen zu einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a961f-106">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="a961f-107">Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der Benutzeroberfläche der [Anwendung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="a961f-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="a961f-108">Initialisiert eine InfoPath 2003-kompatible verwaltetem Code Formularvorlagenprojekt mit Visual Studio 2012 erstellt die `thisApplication` Variablen in der `_Startup` -Methode des die Formularklasse Code, die den Zugriff auf Member der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Schnittstelle verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a961f-108">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> <span data-ttu-id="a961f-109">Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Schnittstelle zum Zurückgeben der Anzahl Name und Version der ausgeführten Instanz von InfoPath verwendet.</span><span class="sxs-lookup"><span data-stu-id="a961f-109">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="a961f-110">Diese Informationen werden mithilfe der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode der [Anwenderschnittstelle: 2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) -Schnittstelle in einem Meldungsfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a961f-110">This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="a961f-111">In Visual C#-Beispiel, den Verweis auf die `\n` Zeichen in der Zeichenfolge für die Benachrichtigung an gerendert wird, indem InfoPath nicht verwalteter Code als Standard neu line Feed, der bewirkt, dass den Text zu unterbrechen und in einer neuen Zeile im Meldungsfeld platziert werden.</span><span class="sxs-lookup"><span data-stu-id="a961f-111">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box.</span></span> <span data-ttu-id="a961f-112">Wenn den neue Wert für den aktuellen Umgebung und Plattform definierten explizit verwenden möchten, verwenden Sie die **Environment.NewLine** -Eigenschaft stattdessen wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a961f-112">To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="a961f-113">Zugreifen auf Daten aus dem zugrunde liegenden XML-Dokument eines Formulars</span><span class="sxs-lookup"><span data-stu-id="a961f-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="a961f-114">Entwickler können die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle verwenden, Zugriff auf Informationen zu einem Formular zugrunde liegenden XML-Dokument, einschließlich eines Verweises auf eine XML-DOM Document Object Model (), die den XML-Quelldaten des Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="a961f-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="a961f-115">Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten, die von der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle wie gibt an, ob das zugrunde liegende XML-Dokument (mithilfe der [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) -Eigenschaft) geändert wurde und ob er wurde verfügbar ist digital signiert (mithilfe der [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="a961f-115">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property).</span></span> <span data-ttu-id="a961f-116">Das nächste Meldungsfeld verwendet die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle [DOM-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) Eigenschaft, um die Quell-XML-Daten des dem Formular zugrunde liegenden XML-Dokument anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a961f-116">The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

<span data-ttu-id="a961f-117">Die **Xml** -Eigenschaft verwendet, die im vorherigen Beispiel ist eine Eigenschaft der das XML-Objektmodell (DOM).</span><span class="sxs-lookup"><span data-stu-id="a961f-117">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM).</span></span> <span data-ttu-id="a961f-118">Weitere Informationen zum XML-DOM finden Sie unter der MSXML 5.0 SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a961f-118">For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="a961f-119">Zugreifen auf Daten aus der Formulardefinitionsdatei eines Formulars</span><span class="sxs-lookup"><span data-stu-id="a961f-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="a961f-120">Informationen zur XSF-Datei eines Formulars, einschließlich eines XML-DOM-Verweises auf den XML-Quelldaten, die er enthält, kann auch über die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="a961f-120">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface.</span></span> <span data-ttu-id="a961f-121">Diese Informationen erfolgt mithilfe der [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) -Eigenschaft, die einen Verweis auf das [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a961f-121">This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="a961f-122">Im folgenden Beispiel zeigt der erste Hinweis einige der Daten, die über die [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle, wie etwa den Uniform Resource Identifier (URI)-Speicherort (mithilfe der [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) -Eigenschaft) und die Versionsnummer (mithilfe der [verfügbar ist Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="a961f-122">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property).</span></span> <span data-ttu-id="a961f-123">Der nächste Hinweis verwendet die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) -Eigenschaft der [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle, um die Quell-XML-Code der XSF-Datei anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a961f-123">The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


