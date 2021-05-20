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
# <a name="external-automation-scenarios-and-examples"></a>Szenarien für die externe Automatisierung und Beispiele

Die von der primären Microsoft.Office.Interop.InfoPath.dll-Interop-Assembly (Microsoft Office) und der InfoPath XML-Interop-Assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) bereitgestellten Member unterstützen das Schreiben von verwalteten Code zum Automatisieren von InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Einrichten von Verweisen auf die Microsoft Office primären Interop- und InfoPath XML-Interopassemblys

Um verwalteten Code für die Automatisierung von InfoPath zu schreiben, müssen Sie Verweise auf die primäre Microsoft InfoPath-Inop und die InfoPath-XML-Interopassemblys einrichten. Die primäre Interop-Assembly von Microsoft InfoPath bietet Unterstützung für die Interoperabilität mit dem com-Objektmodell, das von IPEDITOR.DLL mithilfe der Member des [Microsoft.Office.Interop.InfoPath-Namespaces](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) verfügbar gemacht wird. Die InfoPath XML-Interop-Assembly bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell, das von Microsoft XML Core Services (MSXML) mithilfe der Member desMicrosoft.Office.Interop.InfoPath.Xml[verfügbar](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) gemacht wird. 
  
> [!IMPORTANT]
> Benutzer von Anwendungen mit verwalteten Code, die InfoPath automatisieren, müssen InfoPath, die primäre Interop-Assembly Microsoft Office InfoPath und die InfoPath-XML-Interop-Assembly auf ihren Computern installiert haben. Die **Option .NET Programmability Support** im InfoPath-Setupprogramm ist für eine typische Installation von InfoPath auf Von **Meinem Computer** ausführen festgelegt.
>  
> Solange das .NET Framework 1.1 Redistributable oder .NET Framework 1.1 Software Development Kit (SDK) oder höher installiert ist, werden diese Interopassemblys standardmäßig ebenfalls installiert. Wenn diese Interopassemblys auf dem Computer eines Benutzers nicht verfügbar sind, müssen Sie bestätigen, dass .NET Framework 1.1  oder höher installiert ist, und dann Programme und **Features** in der Systemsteuerung ausführen, um das Setup zu ändern und die **Option .NET-Programmierbarkeitsunterstützung** von InfoPath auf Von Meinem Computer ausführen zu **setzen.** 
  
In den folgenden Verfahren wird beschrieben, wie Verweise auf die primäre Microsoft Office InfoPath und die InfoPath-XML-Interopassemblys in einem Visual Studio werden.
  
So legen Sie einen Verweis auf Microsoft. Office.Interop.InfoPath primäre Interop-Assembly einen Verweis auf **die Microsoft InfoPath 3.0-Typbibliothek** auf der Registerkarte **COM** des Dialogfelds Verweis hinzufügen festlegen.  Obwohl Sie einen Verweis  auf der Registerkarte COM festlegen, wird ein Verweis auf die primäre Interop-Assembly Microsoft.Office.Interop.InfoPath.dll eingerichtet, die vom InfoPath-Setupprogramm im globalen Assemblycache (Global Assembly Cache, GAC) installiert wird. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Legen Sie einen Verweis auf Microsoft. Office.Interop.InfoPath primäre Interop-Assembly

1. Öffnen Sie ein Visual Studio verwalteten Codeprojekts.
    
2. Klicken **Sie im Projektmappen-Explorer** mit der rechten **Maustaste auf Verweise,** und klicken Sie dann **auf Verweis hinzufügen**.
    
3. **Doppelklicken** Sie auf der Registerkarte COM auf **Microsoft InfoPath 3.0-Typbibliothek,** und klicken Sie dann auf **OK**.
    
Navigieren Sie zum Festlegen eines Verweises auf die Microsoft.Office.Interop.InfoPath.Xml-Interop-Assembly zu der Microsoft.Office.Interop.InfoPath.Xml.dll-Datei, die standardmäßig im Ordner _<-Laufwerk_>:\Programme\Microsoft Office\OFFICE14 installiert ist. Obwohl Sie die Kopie der Assembly im lokalen Dateisystem angeben, wird mit diesem Verfahren ein Verweis auf die Microsoft.Office.Interop.InfoPath.Xml.dll-Assembly eingerichtet, die vom InfoPath-Setupprogramm im globalen Assemblycache (GAC) installiert wird.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Festlegen eines Verweises auf die Microsoft.Office.Interop.InfoPath.Xml-Interop-Assembly

1. Öffnen oder erstellen Sie Visual Studio verwalteten Codeprojekt, z. B. eine **Konsolenanwendung** **oder Windows Anwendung.**
    
2. Klicken **Sie im Projektmappen-Explorer** mit der rechten **Maustaste auf Verweise,** und klicken Sie dann **auf Verweis hinzufügen**.
    
3. Klicken Sie auf der Registerkarte **.NET** auf **Durchsuchen,** navigieren Sie zum <-Laufwerk >:\Programme\Microsoft Office\OFFICE14-Ordner, und klicken Sie dann auf Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Klicken Sie auf **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatisieren des Änderns des Werts eines Felds

Angenommen, einer der Kunden des Benutzers einer Formularvorlage für InfoPath-Verkaufsbericht hat kürzlich seinen Namen von "Unternehmen A" in "Unternehmen B" geändert. Ein Entwickler wird aufgefordert, Code zu schreiben, der die in dieser Formularvorlage gespeicherten Verkaufsberichtsformulare automatisch aktualisiert, um die Namensänderung widerspiegeln zu können. Im folgenden Szenario wird ein Formular angenommen, das ein Textfeld enthält, das an ein Feld mit dem Namen customerName gebunden ist.
  
### <a name="create-the-sample-form-template-and-form"></a>Erstellen der Beispielformularvorlage und des Formulars

1. Öffnen Sie InfoPath, und erstellen Sie eine leere Formularvorlage.
    
2. Fügen Sie dem Formular ein **Textfeldsteuerelement** hinzu, und benennen Sie das feld, das an das Steuerelement customerName gebunden ist.
    
3. Klicken Sie **im Aufgabenbereich** Felder mit der rechten Maustaste auf den **Ordner myFields,** und klicken Sie dann auf **Eigenschaften**.
    
4. Wählen Sie **auf** der Registerkarte Details den Folgenden Namespace aus, und kopieren Sie **ihn,** und fügen Sie ihn dann Editor oder an einem anderen Speicherort ein, an dem Sie ihn abrufen können. Sie benötigen diesen Wert später zum Festlegen des Werts der **SelectionNamespaces-Eigenschaft** in Ihrem Code. 
    
5. Veröffentlichen Sie die Formularvorlage in einem Ordner namens C:\Test, und akzeptieren Sie den Standardnamen Template1. 
    
6. Öffnen Sie die Formularvorlage, fügen Sie den Namen "Unternehmen A" zum Textfeld hinzu, das an das Feld customerName gebunden ist, und speichern Sie das Formular dann als "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Erstellen einer Konsolenanwendung für verwalteten Code, um den Namen von "Unternehmen A" in "Unternehmen B" zu ändern

1. Öffnen Visual Studio, und erstellen Sie eine neue visual C# oder Visual Basic-Konsolenanwendung namens UpdateCustomer.
    
2. Richten Sie Verweise auf die Microsoft Office primären Interop- und InfoPath-XML-Interopassemblys ein, wie oben beschrieben.
    
3. Fügen Sie der Datei Program.cs oder Module1.vb den folgenden Code hinzu, um den Wert des Namespaces in der Einstellung für die **SelectionNamespaces-Eigenschaft** mit dem Wert zu aktualisieren, den Sie beim Erstellen des Beispielformulars kopiert haben. 
    
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

4. Klicken **Sie im Menü Debuggen** auf Debuggen **starten,** um die Konsolenanwendung zu kompilieren und auszuführen. 
    
   Die Anwendung öffnet das als Form1.xml gespeicherte Formular und führt eine Schleife durch alle customerName-Elemente, die den Wert Company A enthalten, und ändert den Wert in Unternehmen B. Nach Abschluss des Vorgangs wird eine neue Kopie des Formulars Form2.xml im Ordner "C:\Test" gespeichert. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatisieren des Öffnens eines Formulars und Auffüllen von Feldwerten

Im folgenden Beispiel wird das Öffnen eines leeren Formulars und das Auffüllen der Felder Vorname, Nachname und Adresse im Formular automatisiert. In diesem Szenario wird ein Formular mit drei Textfeldern angenommen, die an die Felder FirstName, LastName und Address gebunden sind.
  
### <a name="create-the-sample-form-template-and-form"></a>Erstellen der Beispielformularvorlage und des Formulars

1. Öffnen Sie InfoPath, und erstellen Sie ein leeres Formular.
    
2. Fügen Sie dem Formular drei Textfeldsteuerelemente hinzu, und benennen Sie die an die Steuerelemente gebundenen Felder: FirstName, LastName und Address. Fügen Sie alle anderen Felder hinzu, die Sie möchten.
    
3. Klicken Sie **im Aufgabenbereich** Felder mit der rechten Maustaste auf den **Ordner myFields,** und klicken Sie dann auf **Eigenschaften**.
    
4. Wählen Sie **auf** der Registerkarte Details den Folgenden Namespace aus, und kopieren Sie **ihn,** und fügen Sie ihn dann Editor oder an einem anderen Speicherort ein, an dem Sie ihn abrufen können. Sie benötigen diesen Wert später zum Festlegen des Werts der **SelectionNamespaces-Eigenschaft** in Ihrem Code. 
    
5. Veröffentlichen Sie die Formularvorlage in einem Ordner namens C:\Temp, und akzeptieren Sie den Standardnamen Template1.
    
6. Öffnen Sie die Formularvorlage, und speichern Sie ein leeres Formular als "Form1" in C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Erstellen einer Konsolenanwendung für verwalteten Code zum Öffnen des Formulars und Auffüllen der Felder

1. Öffnen Visual Studio, und erstellen Sie eine neue Visual C# oder Visual Basic-Konsolenanwendung namens OpenForm.
    
2. Richten Sie Verweise auf die Microsoft Office primären Interop- und InfoPath-XML-Interopassemblys ein, wie oben beschrieben.
    
3. Fügen Sie der Datei Program.cs oder Module1.vb den folgenden Code hinzu, um den Wert des Namespaces in der Einstellung für die **SelectionNamespaces-Eigenschaft** mit dem Wert zu aktualisieren, den Sie beim Erstellen des Beispielformulars kopiert haben. 
    
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

4. Klicken Sie **im Menü Debuggen** auf **Debuggen starten,** um die Konsolenanwendung zu kompilieren und auszuführen. 
    
   Die Anwendung öffnet das als Form1.xml gespeicherte Formular und füllt die Felder FirstName, LastName und Address mit den im Code angegebenen Werten aus, und speichern Sie dann das Formular, und lassen Sie InfoPath geöffnet. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen zur Microsoft Office InfoPath Primary Interop-Assembly](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Informationen zur InfoPath XML Interop-Assembly](about-the-infopath-xml-interop-assembly.md)

