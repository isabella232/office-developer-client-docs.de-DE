---
title: Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], Zugreifen auf Daten mithilfe des 2003-Objektmodells,InfoPath 2003-kompatible Formularvorlagen, Zugreifen auf Anwendungsdaten
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der Application-Schnittstelle instanziiert wird.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437441"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="4dfa2-105">Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="4dfa2-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="4dfa2-106">Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF).</span><span class="sxs-lookup"><span data-stu-id="4dfa2-106">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="4dfa2-107">Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der [Application-Schnittstelle instanziiert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) wird.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="4dfa2-108">Ein infoPath 2003-kompatibles Formularvorlagenprojekt für verwalteten Code, das mit Visual Studio 2012 erstellt wurde, initialisiert die Variable in der Methode der `thisApplication` `_Startup` Formularcodeklasse, [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) die für den Zugriff auf die Elemente der Anwendungsschnittstelle verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-108">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> <span data-ttu-id="4dfa2-109">Im folgenden Beispiel werden die [Eigenschaften Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) der [Application-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) verwendet, um den Namen und die Versionsnummer der ausgeführten Instanz von InfoPath zurück zu geben.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-109">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="4dfa2-110">Diese Informationen werden mithilfe der [Alert-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) der [UI2-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) in einem Meldungsfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-110">This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="4dfa2-111">Im Visual C#-Beispiel wird der Verweis auf das Zeichen in der Zeichenfolge für die Warnungsnachricht von InfoPath ohne verwalteten Code als standardneuer Zeilenfeed gerendert, der bewirkt, dass der Text umbricht und in einer neuen Zeile im Meldungsfeld platziert  `\n` wird.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-111">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box.</span></span> <span data-ttu-id="4dfa2-112">Um explizit den neuen Zeilenwert zu verwenden, der für die aktuelle Umgebung und Plattform definiert wurde, sollten Sie die **Environment.NewLine**-Eigenschaft verwenden, wie dies im folgenden Beispiel dargestellt ist.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-112">To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="4dfa2-113">Zugreifen auf Daten aus dem zugrunde liegenden XML-Dokument eines Formulars</span><span class="sxs-lookup"><span data-stu-id="4dfa2-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="4dfa2-114">Entwickler können die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verwenden, um Zugriff auf Informationen zum einem Formular zugrunde liegenden XML-Dokument zu erhalten, einschließlich eines Verweises auf ein XML Document Object Model (DOM), das die Quell-XML-Daten des Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="4dfa2-115">Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die über die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verfügbar sind, z. B. ob das zugrunde liegende XML-Dokument geändert wurde (mithilfe der [IsDirty-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) und ob es digital signiert wurde (mithilfe der [IsSigned-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dfa2-115">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property).</span></span> <span data-ttu-id="4dfa2-116">Im nächsten Meldungsfeld wird die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verwendet, um die Quell-XML des dem Formular zugrunde liegenden XML-Dokuments zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-116">The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
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

<span data-ttu-id="4dfa2-p106">Die **xml**-Eigenschaft, die im vorangegangenen Beispiel verwendet wurde, ist eine Eigenschaft des XML-DOM (Document Object Model). Weitere Informationen zum XML-DOM finden Sie in der Dokumentation zum MSXML 5.0-SDK.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-p106">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM). For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="4dfa2-119">Zugreifen auf Daten aus der Formulardefinitionsdatei eines Formulars</span><span class="sxs-lookup"><span data-stu-id="4dfa2-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="4dfa2-120">Auf Informationen zur XSF-Datei eines Formulars, einschließlich eines XML-DOM-Verweises auf die in diesem Formular gespeicherten Quell-XML-Daten, kann auch über die [XDocument-Schnittstelle zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) werden.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-120">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface.</span></span> <span data-ttu-id="4dfa2-121">Auf diese Informationen wird mithilfe der [Solution-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) zugegriffen, die einen Verweis auf die [SolutionObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-121">This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="4dfa2-122">Im folgenden Beispiel zeigt die erste Warnung einige der Daten an, die über die [SolutionObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) verfügbar sind, z. B. den Speicherort des URI (Uniform Resource Identifier) (mithilfe der [URI-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) und dessen Versionsnummer (mithilfe der [Version-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dfa2-122">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property).</span></span> <span data-ttu-id="4dfa2-123">Die nächste Warnung verwendet die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) der [SolutionObject-Schnittstelle,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) um die Quell-XML der XSF-Datei zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="4dfa2-123">The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
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


