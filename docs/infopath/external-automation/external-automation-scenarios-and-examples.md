---
title: Szenarios für die externe Automatisierung und Beispiele
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Automatisieren von Infopath 2007, Formularen [InfoPath 2007], Programmgesteuertes Hinzufügen von Daten, Automatisierung [InfoPath 2007], externe Szenarien
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Die Member bereitgestellt von Microsoft Office InfoPath-primären interop-Assembly (Microsoft.Office.Interop.InfoPath.dll) und der InfoPath XML-Interopassembly (Microsoft.Office.Interop.InfoPath.Xml.dll) Schreiben von verwaltetem Code für die Automatisierung von Support InfoPath.
ms.openlocfilehash: 1c76e5cb659c9d3f39eec4a7e517ab57c98c858a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790630"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="e5065-104">Szenarios für die externe Automatisierung und Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5065-104">External automation scenarios and examples</span></span>

<span data-ttu-id="e5065-105">Die Member bereitgestellt von Microsoft Office InfoPath-primären interop-Assembly (Microsoft.Office.Interop.InfoPath.dll) und der InfoPath XML-Interopassembly (Microsoft.Office.Interop.InfoPath.Xml.dll) Schreiben von verwaltetem Code für die Automatisierung von Support InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e5065-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="e5065-106">Einrichten von Verweisen auf die primäre Interopassembly für Microsoft Office InfoPath und InfoPath-XML-Interop-Assemblys</span><span class="sxs-lookup"><span data-stu-id="e5065-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="e5065-107">Zum Schreiben von verwalteten Codes für die Automatisierung von InfoPath müssen Sie Verweise auf die primären Interop-Microsoft InfoPath und InfoPath XML-interop-Assemblys einrichten.</span><span class="sxs-lookup"><span data-stu-id="e5065-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="e5065-108">Die primäre Interopassembly für Microsoft InfoPath bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell von IPEDITOR verfügbar gemacht werden. DLL-Datei mithilfe der Member des [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="e5065-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="e5065-109">InfoPath XML-interop-Assembly bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell verfügbar gemacht werden von Microsoft XML Core Services (MSXML) mithilfe der Member des Namespaces [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/de-de/library/microsoft.office.interop.infopath.xml) .</span><span class="sxs-lookup"><span data-stu-id="e5065-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/de-de/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e5065-110">Benutzer von verwaltetem Code Anwendungen, die Automatisierung von InfoPath müssen InfoPath, die primäre Interopassembly für Microsoft Office InfoPath und InfoPath XML Interop-Assembly auf ihren Computern installiert haben.</span><span class="sxs-lookup"><span data-stu-id="e5065-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="e5065-111">Die Option **.NET-Programmierunterstützung für** im InfoPath-Setupprogramm wird für eine Standardinstallation von InfoPath auf **vom Arbeitsplatz starten** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e5065-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="e5065-112">Daher werden wie lange als .NET Framework 1.1 Redistributable oder .NET Framework 1.1 Software Development Kit (SDK) oder höher installiert ist, diese Interop-Assemblys auch standardmäßig installiert.</span><span class="sxs-lookup"><span data-stu-id="e5065-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="e5065-113">Wenn diese Interop-Assemblys nicht auf dem Computer eines Benutzers verfügbar sind, müssen Sie bestätigen, dass das .NET Framework 1.1 oder höher installiert ist, und führen Sie **Programme und Funktionen** aus der **Systemsteuerung** ändern Sie Setup und Festlegen der **.NET-Programmierung Unterstützung** Option von InfoPath auf **vom Arbeitsplatz starten**.</span><span class="sxs-lookup"><span data-stu-id="e5065-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="e5065-114">Die folgenden Verfahren wird beschrieben, wie Verweise auf die primären Interop-Microsoft Office InfoPath und InfoPath XML Interop-Assemblys in Visual Studio-Projekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="e5065-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="e5065-115">Wenn Sie einen Verweis auf die primäre Interopassembly für Microsoft.Office.Interop.InfoPath festgelegt, legen Sie einen Verweis auf **Die Typbibliothek von Microsoft InfoPath 3.0** auf der Registerkarte **COM** im Dialogfeld **Verweis hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="e5065-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="e5065-116">Auch wenn Sie einen Verweis auf die Registerkarte **COM** festgelegt, wird ein Verweis auf die primäre Interopassembly für Microsoft.Office.Interop.InfoPath.dll eingerichtet, die das InfoPath-Setup-Programm in den globalen Assemblycache (GAC) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5065-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="e5065-117">Legen Sie einen Verweis auf die primäre Interopassembly für Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="e5065-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="e5065-118">Öffnen Sie ein Projekt mit verwaltetem Code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e5065-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="e5065-119">Klicken Sie im **Projektmappen-Explorer**Maustaste auf **Verweise**, und klicken Sie dann auf **Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e5065-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="e5065-120">Doppelklicken Sie auf **Microsoft InfoPath 3.0-Typbibliothek**auf der Registerkarte **COM** , und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5065-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="e5065-121">Wenn Sie einen Verweis auf die Interop-Assembly Microsoft.Office.Interop.InfoPath.Xml festgelegt, navigieren Sie zur Microsoft.Office.Interop.InfoPath.Xml.dll-Datei, die standardmäßig im < _Laufwerk_> installiert ist: \Programme\Microsoft Office\OFFICE14 Ordner .</span><span class="sxs-lookup"><span data-stu-id="e5065-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="e5065-122">Auch wenn Sie die Kopie der Assembly im lokalen Dateisystem angeben, richtet dieses Verfahren einen Verweis auf die Microsoft.Office.Interop.InfoPath.Xml.dll-Assembly, die das InfoPath-Setup-Programm in den globalen Assemblycache (GAC) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5065-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="e5065-123">Stellen Sie einen Verweis auf die Microsoft.Office.Interop.InfoPath.Xml-Interopassembly</span><span class="sxs-lookup"><span data-stu-id="e5065-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="e5065-124">Öffnen Sie oder erstellen Sie ein Projekt Visual Studio mit verwaltetem Code, wie ein **Konsolenanwendungsprojekt** oder **Windows-Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="e5065-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="e5065-125">Klicken Sie im **Projektmappen-Explorer**Maustaste auf **Verweise**, und klicken Sie dann auf **Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e5065-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="e5065-126">Klicken Sie auf der Registerkarte **.NET** auf **Durchsuchen**, navigieren Sie zu dem < _Laufwerk_>: \Programme\Microsoft Office\OFFICE14-Ordner, und klicken Sie dann auf Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="e5065-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="e5065-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5065-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="e5065-128">Automatisieren Sie ändern des Werts eines Felds</span><span class="sxs-lookup"><span data-stu-id="e5065-128">Automate changing the value of a field</span></span>

<span data-ttu-id="e5065-129">Angenommen Sie, einen Kunden des Benutzers von einer InfoPath-Formularvorlage Umsatzbericht kürzlich seinen Namen von "Company A" die "Unternehmen b" geändert.</span><span class="sxs-lookup"><span data-stu-id="e5065-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="e5065-130">Ein Entwickler wird gefragt, Code schreiben, der die Umsatzbericht Formulare aus dieser Formularvorlage entsprechend ändern gespeichert automatisch aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5065-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="e5065-131">Im folgende Szenario wird vorausgesetzt, ein Formular, das ein Textfeld enthält, das an ein Feld mit dem Namen CustomerName gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="e5065-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="e5065-132">Erstellen Sie die Beispielvorlage Formular und das Formular</span><span class="sxs-lookup"><span data-stu-id="e5065-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="e5065-133">Öffnen von InfoPath und erstellen Sie eine leere Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="e5065-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="e5065-134">Hinzufügen eines **Textfeld** -Steuerelements auf das Formular, und nennen Sie das Feld auf das Steuerelement CustomerName gebunden.</span><span class="sxs-lookup"><span data-stu-id="e5065-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="e5065-135">Klicken Sie im Aufgabenbereich **Felder** mit der rechten Maustaste in des Ordners **MyFields** , und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="e5065-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="e5065-136">Wählen Sie auf der Registerkarte **Details** , und fügen Sie den folgenden Wert **Namespace:**, und fügen Sie diese in Editor oder einem anderen Speicherort, in dem Sie es abrufen können.</span><span class="sxs-lookup"><span data-stu-id="e5065-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="e5065-137">Dieser Wert benötigen später Sie für den Wert der Eigenschaft **SelectionNamespaces** in Ihrem Code festlegen.</span><span class="sxs-lookup"><span data-stu-id="e5065-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="e5065-138">Veröffentlichen Sie die Formularvorlage in einen Ordner namens C:\Test, und akzeptieren Sie den Standardnamen Vorlage1.</span><span class="sxs-lookup"><span data-stu-id="e5065-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="e5065-139">Öffnen Sie die Formularvorlage, fügen Sie den Namen "Firma A" zum Textfeld an das CustomerName-Feld gebunden, und speichern Sie das Formular als "Form1".</span><span class="sxs-lookup"><span data-stu-id="e5065-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="e5065-140">Erstellen Sie eine verwaltetem Code zum Ändern des Namens von 'Unternehmen A' auf 'Unternehmen B'</span><span class="sxs-lookup"><span data-stu-id="e5065-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="e5065-141">Öffnen Sie Visual Studio, und erstellen Sie eine neue Visual c# oder Visual Basic-Konsolenanwendungsprojekt mit dem Namen UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="e5065-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="e5065-142">Richten Sie Verweise auf die primären Interop-Microsoft Office InfoPath und InfoPath XML Interop-Assemblys, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5065-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="e5065-143">Fügen Sie den folgenden Code, um die Datei Program.cs oder Module1.vb ein und stellt sicher, dass den Wert des Namespaces in der Einstellung für die **SelectionNamespaces** -Eigenschaft mit dem Wert aktualisiert, die Sie beim Erstellen des Beispielformulars kopiert.</span><span class="sxs-lookup"><span data-stu-id="e5065-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="e5065-144">Klicken Sie zum Kompilieren und Ausführen der Konsolenanwendung im Menü **Debuggen** auf **Debuggen starten** .</span><span class="sxs-lookup"><span data-stu-id="e5065-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="e5065-145">Die Anwendung öffnet das Formular gespeichert wird, als Form1.xml und Durchlaufen aller CustomerName-Elemente, die den Wert Unternehmen A enthalten und ändert diesen Wert in Unternehmen B. Wenn der Vorgang abgeschlossen ist, wird eine neue Kopie des Formulars als Form2.xml im Ordner "C:\Test" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e5065-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="e5065-146">Öffnen eines Formulars und Auffüllen von Feldwerten automatisieren</span><span class="sxs-lookup"><span data-stu-id="e5065-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="e5065-147">Im folgenden Beispiel wird ein leeres Formular öffnen, und füllen den Vornamen, Nachnamen und Adressfelder im Formular automatisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e5065-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="e5065-148">In diesem Szenario wird ein Formular mit drei Textfeldern, die an die Felder FirstName, LastName und Adresse gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="e5065-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="e5065-149">Erstellen Sie die Beispielvorlage Formular und das Formular</span><span class="sxs-lookup"><span data-stu-id="e5065-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="e5065-150">Öffnen von InfoPath und erstellen Sie ein leeres Formular.</span><span class="sxs-lookup"><span data-stu-id="e5065-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="e5065-151">Drei Textfeld-Steuerelemente auf dem Formular hinzufügen, und nennen Sie die Felder gebundenen Steuerelemente: FirstName, LastName und Adresse.</span><span class="sxs-lookup"><span data-stu-id="e5065-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="e5065-152">Fügen Sie die gewünschten Felder hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5065-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="e5065-153">Klicken Sie im Aufgabenbereich **Felder** mit der rechten Maustaste in des Ordners **MyFields** , und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="e5065-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="e5065-154">Wählen Sie auf der Registerkarte **Details** , und fügen Sie den folgenden Wert **Namespace:**, und fügen Sie diese in Editor oder einem anderen Speicherort, in dem Sie es abrufen können.</span><span class="sxs-lookup"><span data-stu-id="e5065-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="e5065-155">Dieser Wert benötigen später Sie für den Wert der Eigenschaft **SelectionNamespaces** in Ihrem Code festlegen.</span><span class="sxs-lookup"><span data-stu-id="e5065-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="e5065-156">Veröffentlichen Sie die Formularvorlage in einen Ordner namens C:\Temp, und akzeptieren Sie den Standardnamen Vorlage1.</span><span class="sxs-lookup"><span data-stu-id="e5065-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="e5065-157">Öffnen Sie die Formularvorlage, und speichern Sie ein leeres Formular als "Form1" c:\temp.</span><span class="sxs-lookup"><span data-stu-id="e5065-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="e5065-158">Erstellen einer Anwendung mit verwaltetem Code Konsole zum Öffnen des Formulars, und füllen Sie die Felder</span><span class="sxs-lookup"><span data-stu-id="e5065-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="e5065-159">Öffnen Sie Visual Studio, und erstellen Sie eine neue Visual c# oder Visual Basic-Konsolenanwendungsprojekt mit dem Namen OpenForm.</span><span class="sxs-lookup"><span data-stu-id="e5065-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="e5065-160">Richten Sie Verweise auf die primären Interop-Microsoft Office InfoPath und InfoPath XML Interop-Assemblys, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5065-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="e5065-161">Fügen Sie den folgenden Code, um die Datei Program.cs oder Module1.vb ein und stellt sicher, dass den Wert des Namespaces in der Einstellung für die **SelectionNamespaces** -Eigenschaft mit dem Wert aktualisiert, die Sie beim Erstellen des Beispielformulars kopiert.</span><span class="sxs-lookup"><span data-stu-id="e5065-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="e5065-162">Klicken Sie im Menü **Debuggen** auf **Debuggen starten** , um zu kompilieren und Ausführen der Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="e5065-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="e5065-163">Die Anwendung wird beim Öffnen des Formulars als Form1.xml gespeichert und füllen Sie die Felder FirstName, LastName und Adresse mit den Werten, die im Code angegebene und speichern Sie das Formular, das InfoPath geöffnet lassen.</span><span class="sxs-lookup"><span data-stu-id="e5065-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e5065-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5065-164">See also</span></span>

- [<span data-ttu-id="e5065-165">Über die Microsoft Office InfoPath primären Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="e5065-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="e5065-166">Über die InfoPath-XML-Interop-Assembly</span><span class="sxs-lookup"><span data-stu-id="e5065-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

