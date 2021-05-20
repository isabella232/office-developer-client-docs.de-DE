---
title: Szenarien für die externe Automatisierung und Beispiele
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Automatisieren von infopath 2007,Formularen [InfoPath 2007], Programmgesteuertes Hinzufügen von Daten,Automatisierung [InfoPath 2007], externe Szenarien
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Die von der primären Microsoft.Office.Interop.InfoPath.dll-Interop-Assembly (Microsoft Office) und der InfoPath XML-Interop-Assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) bereitgestellten Member unterstützen das Schreiben von verwalteten Code zum Automatisieren von InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537815"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="a1518-104">Szenarien für die externe Automatisierung und Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1518-104">External automation scenarios and examples</span></span>

<span data-ttu-id="a1518-105">Die von der primären Microsoft.Office.Interop.InfoPath.dll-Interop-Assembly (Microsoft Office) und der InfoPath XML-Interop-Assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) bereitgestellten Member unterstützen das Schreiben von verwalteten Code zum Automatisieren von InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a1518-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="a1518-106">Einrichten von Verweisen auf die Microsoft Office primären Interop- und InfoPath XML-Interopassemblys</span><span class="sxs-lookup"><span data-stu-id="a1518-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="a1518-107">Um verwalteten Code für die Automatisierung von InfoPath zu schreiben, müssen Sie Verweise auf die primäre Microsoft InfoPath-Inop und die InfoPath-XML-Interopassemblys einrichten.</span><span class="sxs-lookup"><span data-stu-id="a1518-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="a1518-108">Die primäre Interop-Assembly von Microsoft InfoPath bietet Unterstützung für die Interoperabilität mit dem com-Objektmodell, das von IPEDITOR.DLL mithilfe der Member des [Microsoft.Office.Interop.InfoPath-Namespaces](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="a1518-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="a1518-109">Die InfoPath XML-Interop-Assembly bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell, das von Microsoft XML Core Services (MSXML) mithilfe der Member desMicrosoft.Office.Interop.InfoPath.Xml[verfügbar](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="a1518-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a1518-110">Benutzer von Anwendungen mit verwalteten Code, die InfoPath automatisieren, müssen InfoPath, die primäre Interop-Assembly Microsoft Office InfoPath und die InfoPath-XML-Interop-Assembly auf ihren Computern installiert haben.</span><span class="sxs-lookup"><span data-stu-id="a1518-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="a1518-111">Die **Option .NET Programmability Support** im InfoPath-Setupprogramm ist für eine typische Installation von InfoPath auf Von **Meinem Computer** ausführen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1518-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="a1518-112">Solange das .NET Framework 1.1 Redistributable oder .NET Framework 1.1 Software Development Kit (SDK) oder höher installiert ist, werden diese Interopassemblys standardmäßig ebenfalls installiert.</span><span class="sxs-lookup"><span data-stu-id="a1518-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="a1518-113">Wenn diese Interopassemblys auf dem Computer eines Benutzers nicht verfügbar sind, müssen Sie bestätigen, dass .NET Framework 1.1  oder höher installiert ist, und dann Programme und **Features** in der Systemsteuerung ausführen, um das Setup zu ändern und die **Option .NET-Programmierbarkeitsunterstützung** von InfoPath auf Von Meinem Computer ausführen zu **setzen.**</span><span class="sxs-lookup"><span data-stu-id="a1518-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="a1518-114">In den folgenden Verfahren wird beschrieben, wie Verweise auf die primäre Microsoft Office InfoPath und die InfoPath-XML-Interopassemblys in einem Visual Studio werden.</span><span class="sxs-lookup"><span data-stu-id="a1518-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="a1518-115">So legen Sie einen Verweis auf Microsoft. Office.Interop.InfoPath primäre Interop-Assembly einen Verweis auf **die Microsoft InfoPath 3.0-Typbibliothek** auf der Registerkarte **COM** des Dialogfelds Verweis hinzufügen festlegen. </span><span class="sxs-lookup"><span data-stu-id="a1518-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="a1518-116">Obwohl Sie einen Verweis  auf der Registerkarte COM festlegen, wird ein Verweis auf die primäre Interop-Assembly Microsoft.Office.Interop.InfoPath.dll eingerichtet, die vom InfoPath-Setupprogramm im globalen Assemblycache (Global Assembly Cache, GAC) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="a1518-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="a1518-117">Legen Sie einen Verweis auf Microsoft. Office.Interop.InfoPath primäre Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="a1518-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="a1518-118">Öffnen Sie ein Visual Studio verwalteten Codeprojekts.</span><span class="sxs-lookup"><span data-stu-id="a1518-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="a1518-119">Klicken **Sie im Projektmappen-Explorer** mit der rechten **Maustaste auf Verweise,** und klicken Sie dann **auf Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a1518-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="a1518-120">**Doppelklicken** Sie auf der Registerkarte COM auf **Microsoft InfoPath 3.0-Typbibliothek,** und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1518-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="a1518-121">Navigieren Sie zum Festlegen eines Verweises auf die Microsoft.Office.Interop.InfoPath.Xml-Interop-Assembly zu der Microsoft.Office.Interop.InfoPath.Xml.dll-Datei, die standardmäßig im Ordner _<-Laufwerk_>:\Programme\Microsoft Office\OFFICE14 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a1518-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="a1518-122">Obwohl Sie die Kopie der Assembly im lokalen Dateisystem angeben, wird mit diesem Verfahren ein Verweis auf die Microsoft.Office.Interop.InfoPath.Xml.dll-Assembly eingerichtet, die vom InfoPath-Setupprogramm im globalen Assemblycache (GAC) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="a1518-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="a1518-123">Festlegen eines Verweises auf die Microsoft.Office.Interop.InfoPath.Xml-Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="a1518-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="a1518-124">Öffnen oder erstellen Sie Visual Studio verwalteten Codeprojekt, z. B. eine **Konsolenanwendung** **oder Windows Anwendung.**</span><span class="sxs-lookup"><span data-stu-id="a1518-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="a1518-125">Klicken **Sie im Projektmappen-Explorer** mit der rechten **Maustaste auf Verweise,** und klicken Sie dann **auf Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a1518-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="a1518-126">Klicken Sie auf der Registerkarte **.NET** auf **Durchsuchen,** navigieren Sie zum <-Laufwerk >:\Programme\Microsoft Office\OFFICE14-Ordner, und klicken Sie dann auf Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="a1518-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="a1518-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1518-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="a1518-128">Automatisieren des Änderns des Werts eines Felds</span><span class="sxs-lookup"><span data-stu-id="a1518-128">Automate changing the value of a field</span></span>

<span data-ttu-id="a1518-129">Angenommen, einer der Kunden des Benutzers einer Formularvorlage für InfoPath-Verkaufsbericht hat kürzlich seinen Namen von "Unternehmen A" in "Unternehmen B" geändert.</span><span class="sxs-lookup"><span data-stu-id="a1518-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="a1518-130">Ein Entwickler wird aufgefordert, Code zu schreiben, der die in dieser Formularvorlage gespeicherten Verkaufsberichtsformulare automatisch aktualisiert, um die Namensänderung widerspiegeln zu können.</span><span class="sxs-lookup"><span data-stu-id="a1518-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="a1518-131">Im folgenden Szenario wird ein Formular angenommen, das ein Textfeld enthält, das an ein Feld mit dem Namen customerName gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="a1518-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="a1518-132">Erstellen der Beispielformularvorlage und des Formulars</span><span class="sxs-lookup"><span data-stu-id="a1518-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="a1518-133">Öffnen Sie InfoPath, und erstellen Sie eine leere Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="a1518-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="a1518-134">Fügen Sie dem Formular ein **Textfeldsteuerelement** hinzu, und benennen Sie das feld, das an das Steuerelement customerName gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="a1518-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="a1518-135">Klicken Sie **im Aufgabenbereich** Felder mit der rechten Maustaste auf den **Ordner myFields,** und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="a1518-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="a1518-136">Wählen Sie **auf** der Registerkarte Details den Folgenden Namespace aus, und kopieren Sie **ihn,** und fügen Sie ihn dann Editor oder an einem anderen Speicherort ein, an dem Sie ihn abrufen können.</span><span class="sxs-lookup"><span data-stu-id="a1518-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="a1518-137">Sie benötigen diesen Wert später zum Festlegen des Werts der **SelectionNamespaces-Eigenschaft** in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="a1518-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="a1518-138">Veröffentlichen Sie die Formularvorlage in einem Ordner namens C:\Test, und akzeptieren Sie den Standardnamen Template1.</span><span class="sxs-lookup"><span data-stu-id="a1518-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="a1518-139">Öffnen Sie die Formularvorlage, fügen Sie den Namen "Unternehmen A" zum Textfeld hinzu, das an das Feld customerName gebunden ist, und speichern Sie das Formular dann als "Form1".</span><span class="sxs-lookup"><span data-stu-id="a1518-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="a1518-140">Erstellen einer Konsolenanwendung für verwalteten Code, um den Namen von "Unternehmen A" in "Unternehmen B" zu ändern</span><span class="sxs-lookup"><span data-stu-id="a1518-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="a1518-141">Öffnen Visual Studio, und erstellen Sie eine neue visual C# oder Visual Basic-Konsolenanwendung namens UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="a1518-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="a1518-142">Richten Sie Verweise auf die Microsoft Office primären Interop- und InfoPath-XML-Interopassemblys ein, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1518-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="a1518-143">Fügen Sie der Datei Program.cs oder Module1.vb den folgenden Code hinzu, um den Wert des Namespaces in der Einstellung für die **SelectionNamespaces-Eigenschaft** mit dem Wert zu aktualisieren, den Sie beim Erstellen des Beispielformulars kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="a1518-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace UpdateCustomer
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp = 
                new Microsoft.Office.Interop.InfoPath.Application();
            // Get a reference the XDocuments collection 
            // and open the sample form.
            XDocumentsCollection myXDocs = myApp.XDocuments;
            XDocument myXDoc = myXDocs.Open("C:\\Test\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Access the XML DOM for the underlying XML document using
            // the DOM property. Note that you must cast to the 
            // IXMLDOMDocument2 type from the
            // Microsoft.Office.Interop.InfoPath.Xml namespace
            // to access the XML DOM.
            IXMLDOMDocument2 myXMLDoc = myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace 
            // value below with that of your sample form.
            myXMLDoc.setProperty("SelectionNamespaces",
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Select all instances of customerName that contain 
            //'Company A'.
            IXMLDOMNodeList myNames = 
                myXMLDoc.selectNodes(
                "//my:customerName[. = 'Company A']");
            // Check to determine if any nodes were returned.
            if (myNames.length < 1)
            Console.WriteLine(
                "No elements containing 'Company A' were found.");
            // Loop through the list updating to 'Company B'.
            IXMLDOMNode myName = myNames.nextNode();
            while (myName != null)
            {
                myName.text = "Company B";
                myName = myNames.nextNode();
            }
            // Save the updated form as Form2.xml and close out.
            myXDoc.SaveAs("C:\\Test\\Form2.xml");
            myXDocs.Close(0);
            myApp.Quit(false);
            Console.WriteLine("Finished!");
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application()
          ' Get a reference the XDocuments collection 
          ' and open the sample form.
          Dim myXDocs As XDocumentsCollection = myApp.XDocuments
          Dim myXDoc As XDocument = myXDocs.Open( _
            "C:\\Test\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Access the XML DOM for the underlying XML document using
          ' the DOM property. Note that you must cast to the 
          ' IXMLDOMDocument2 type from the
          ' Microsoft.Office.Interop.InfoPath.Xml namespace
          ' to access the XML DOM.
          Dim myXMLDoc As IXMLDOMDocument2 = _
            DirectCast(myXDoc.DOM, IXMLDOMDocument2)
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace 
          ' value below with that of your sample form.
          myXMLDoc.setProperty("SelectionNamespaces", _
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Select all instances of customerName that contain 
          ''Company A'.
          Dim myNames As IXMLDOMNodeList = _
      myXMLDoc.selectNodes("//my:customerName[. = 'Company A']")
          ' Check to determine if any nodes were returned.
          If (myNames.length < 1) Then
            Console.WriteLine( _
                "No elements containing 'Company A' were found.")
          Else
            ' Loop through the list updating to 'Company B'.
            Dim myName As IXMLDOMNode = myNames.nextNode()
            While (myName IsNot Nothing)
                myName.text = "Company B"
                myName = myNames.nextNode()
            End While
          End If
          ' Save the updated form as Form2.xml and close out.
          myXDoc.SaveAs("C:\\Test\\Form2.xml")
          myXDocs.Close(0)
          myApp.Quit(False)
          Console.WriteLine("Finished!")
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="a1518-144">Klicken **Sie im Menü Debuggen** auf Debuggen **starten,** um die Konsolenanwendung zu kompilieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a1518-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="a1518-145">Die Anwendung öffnet das als Form1.xml gespeicherte Formular und führt eine Schleife durch alle customerName-Elemente, die den Wert Company A enthalten, und ändert den Wert in Unternehmen B. Nach Abschluss des Vorgangs wird eine neue Kopie des Formulars Form2.xml im Ordner "C:\Test" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a1518-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="a1518-146">Automatisieren des Öffnens eines Formulars und Auffüllen von Feldwerten</span><span class="sxs-lookup"><span data-stu-id="a1518-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="a1518-147">Im folgenden Beispiel wird das Öffnen eines leeren Formulars und das Auffüllen der Felder Vorname, Nachname und Adresse im Formular automatisiert.</span><span class="sxs-lookup"><span data-stu-id="a1518-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="a1518-148">In diesem Szenario wird ein Formular mit drei Textfeldern angenommen, die an die Felder FirstName, LastName und Address gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="a1518-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="a1518-149">Erstellen der Beispielformularvorlage und des Formulars</span><span class="sxs-lookup"><span data-stu-id="a1518-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="a1518-150">Öffnen Sie InfoPath, und erstellen Sie ein leeres Formular.</span><span class="sxs-lookup"><span data-stu-id="a1518-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="a1518-151">Fügen Sie dem Formular drei Textfeldsteuerelemente hinzu, und benennen Sie die an die Steuerelemente gebundenen Felder: FirstName, LastName und Address.</span><span class="sxs-lookup"><span data-stu-id="a1518-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="a1518-152">Fügen Sie alle anderen Felder hinzu, die Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="a1518-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="a1518-153">Klicken Sie **im Aufgabenbereich** Felder mit der rechten Maustaste auf den **Ordner myFields,** und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="a1518-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="a1518-154">Wählen Sie **auf** der Registerkarte Details den Folgenden Namespace aus, und kopieren Sie **ihn,** und fügen Sie ihn dann Editor oder an einem anderen Speicherort ein, an dem Sie ihn abrufen können.</span><span class="sxs-lookup"><span data-stu-id="a1518-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="a1518-155">Sie benötigen diesen Wert später zum Festlegen des Werts der **SelectionNamespaces-Eigenschaft** in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="a1518-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="a1518-156">Veröffentlichen Sie die Formularvorlage in einem Ordner namens C:\Temp, und akzeptieren Sie den Standardnamen Template1.</span><span class="sxs-lookup"><span data-stu-id="a1518-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="a1518-157">Öffnen Sie die Formularvorlage, und speichern Sie ein leeres Formular als "Form1" in C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="a1518-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="a1518-158">Erstellen einer Konsolenanwendung für verwalteten Code zum Öffnen des Formulars und Auffüllen der Felder</span><span class="sxs-lookup"><span data-stu-id="a1518-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="a1518-159">Öffnen Visual Studio, und erstellen Sie eine neue Visual C# oder Visual Basic-Konsolenanwendung namens OpenForm.</span><span class="sxs-lookup"><span data-stu-id="a1518-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="a1518-160">Richten Sie Verweise auf die Microsoft Office primären Interop- und InfoPath-XML-Interopassemblys ein, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1518-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="a1518-161">Fügen Sie der Datei Program.cs oder Module1.vb den folgenden Code hinzu, um den Wert des Namespaces in der Einstellung für die **SelectionNamespaces-Eigenschaft** mit dem Wert zu aktualisieren, den Sie beim Erstellen des Beispielformulars kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="a1518-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace OpenForm
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp=
                new Microsoft.Office.Interop.InfoPath.Application();
            // Create an InfoPath XDocument variable and open 
            // the blank form.
            XDocument myXDoc = myApp.XDocuments.Open(
                "c:\\temp\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Create an IXMLDOMDocument2 variable and access 
            // the XML DOM from the underlying XML document
            // using the DOM property of the XDocument object. 
            // Note that you must cast to IXMLDOMDocument2 to do so.
            IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace
            // value below with that of your sample form.
            doc.setProperty("SelectionNamespaces","xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Pre-populate the fields with specified values.
            doc.selectSingleNode("//my:FirstName").text="My Name";
            doc.selectSingleNode("//my:LastName").text="My LastName";
            doc.selectSingleNode("//my:Address").text="My Address";
            // Save the form, leaving InfoPath open.
            myXDoc.Save();
            
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application
          ' Create an InfoPath XDocument variable and open 
          ' the blank form.
          Dim myXDoc As XDocument = myApp.XDocuments.Open( _
            "c:\\temp\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Create an IXMLDOMDocument2 variable and access 
          ' the XML DOM from the underlying XML document
          ' using the DOM property of the XDocument object.
          Dim doc As IXMLDOMDocument2 = myXDoc.DOM
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace
          ' value below with that of your sample form.
          doc.setProperty("SelectionNamespaces", "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="a1518-162">Klicken Sie **im Menü Debuggen** auf **Debuggen starten,** um die Konsolenanwendung zu kompilieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a1518-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="a1518-163">Die Anwendung öffnet das als Form1.xml gespeicherte Formular und füllt die Felder FirstName, LastName und Address mit den im Code angegebenen Werten aus, und speichern Sie dann das Formular, und lassen Sie InfoPath geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a1518-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a1518-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1518-164">See also</span></span>

- [<span data-ttu-id="a1518-165">Informationen zur Microsoft Office InfoPath Primary Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="a1518-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="a1518-166">Informationen zur InfoPath XML Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="a1518-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

