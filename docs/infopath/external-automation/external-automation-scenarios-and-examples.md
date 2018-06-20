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
# <a name="external-automation-scenarios-and-examples"></a>Szenarios für die externe Automatisierung und Beispiele

Die Member bereitgestellt von Microsoft Office InfoPath-primären interop-Assembly (Microsoft.Office.Interop.InfoPath.dll) und der InfoPath XML-Interopassembly (Microsoft.Office.Interop.InfoPath.Xml.dll) Schreiben von verwaltetem Code für die Automatisierung von Support InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Einrichten von Verweisen auf die primäre Interopassembly für Microsoft Office InfoPath und InfoPath-XML-Interop-Assemblys

Zum Schreiben von verwalteten Codes für die Automatisierung von InfoPath müssen Sie Verweise auf die primären Interop-Microsoft InfoPath und InfoPath XML-interop-Assemblys einrichten. Die primäre Interopassembly für Microsoft InfoPath bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell von IPEDITOR verfügbar gemacht werden. DLL-Datei mithilfe der Member des [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) -Namespace. InfoPath XML-interop-Assembly bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell verfügbar gemacht werden von Microsoft XML Core Services (MSXML) mithilfe der Member des Namespaces [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Benutzer von verwaltetem Code Anwendungen, die Automatisierung von InfoPath müssen InfoPath, die primäre Interopassembly für Microsoft Office InfoPath und InfoPath XML Interop-Assembly auf ihren Computern installiert haben. Die Option **.NET-Programmierunterstützung für** im InfoPath-Setupprogramm wird für eine Standardinstallation von InfoPath auf **vom Arbeitsplatz starten** festgelegt.
>  
> Daher werden wie lange als .NET Framework 1.1 Redistributable oder .NET Framework 1.1 Software Development Kit (SDK) oder höher installiert ist, diese Interop-Assemblys auch standardmäßig installiert. Wenn diese Interop-Assemblys nicht auf dem Computer eines Benutzers verfügbar sind, müssen Sie bestätigen, dass das .NET Framework 1.1 oder höher installiert ist, und führen Sie **Programme und Funktionen** aus der **Systemsteuerung** ändern Sie Setup und Festlegen der **.NET-Programmierung Unterstützung** Option von InfoPath auf **vom Arbeitsplatz starten**. 
  
Die folgenden Verfahren wird beschrieben, wie Verweise auf die primären Interop-Microsoft Office InfoPath und InfoPath XML Interop-Assemblys in Visual Studio-Projekt festlegen.
  
Wenn Sie einen Verweis auf die primäre Interopassembly für Microsoft.Office.Interop.InfoPath festgelegt, legen Sie einen Verweis auf **Die Typbibliothek von Microsoft InfoPath 3.0** auf der Registerkarte **COM** im Dialogfeld **Verweis hinzufügen** . Auch wenn Sie einen Verweis auf die Registerkarte **COM** festgelegt, wird ein Verweis auf die primäre Interopassembly für Microsoft.Office.Interop.InfoPath.dll eingerichtet, die das InfoPath-Setup-Programm in den globalen Assemblycache (GAC) installiert ist. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Legen Sie einen Verweis auf die primäre Interopassembly für Microsoft.Office.Interop.InfoPath

1. Öffnen Sie ein Projekt mit verwaltetem Code Visual Studio.
    
2. Klicken Sie im **Projektmappen-Explorer**Maustaste auf **Verweise**, und klicken Sie dann auf **Verweis hinzufügen**.
    
3. Doppelklicken Sie auf **Microsoft InfoPath 3.0-Typbibliothek**auf der Registerkarte **COM** , und klicken Sie dann auf **OK**.
    
Wenn Sie einen Verweis auf die Interop-Assembly Microsoft.Office.Interop.InfoPath.Xml festgelegt, navigieren Sie zur Microsoft.Office.Interop.InfoPath.Xml.dll-Datei, die standardmäßig im < _Laufwerk_> installiert ist: \Programme\Microsoft Office\OFFICE14 Ordner . Auch wenn Sie die Kopie der Assembly im lokalen Dateisystem angeben, richtet dieses Verfahren einen Verweis auf die Microsoft.Office.Interop.InfoPath.Xml.dll-Assembly, die das InfoPath-Setup-Programm in den globalen Assemblycache (GAC) installiert ist.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Stellen Sie einen Verweis auf die Microsoft.Office.Interop.InfoPath.Xml-Interopassembly

1. Öffnen Sie oder erstellen Sie ein Projekt Visual Studio mit verwaltetem Code, wie ein **Konsolenanwendungsprojekt** oder **Windows-Anwendung**.
    
2. Klicken Sie im **Projektmappen-Explorer**Maustaste auf **Verweise**, und klicken Sie dann auf **Verweis hinzufügen**.
    
3. Klicken Sie auf der Registerkarte **.NET** auf **Durchsuchen**, navigieren Sie zu dem < _Laufwerk_>: \Programme\Microsoft Office\OFFICE14-Ordner, und klicken Sie dann auf Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Klicken Sie auf **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatisieren Sie ändern des Werts eines Felds

Angenommen Sie, einen Kunden des Benutzers von einer InfoPath-Formularvorlage Umsatzbericht kürzlich seinen Namen von "Company A" die "Unternehmen b" geändert. Ein Entwickler wird gefragt, Code schreiben, der die Umsatzbericht Formulare aus dieser Formularvorlage entsprechend ändern gespeichert automatisch aktualisiert wird. Im folgende Szenario wird vorausgesetzt, ein Formular, das ein Textfeld enthält, das an ein Feld mit dem Namen CustomerName gebunden ist.
  
### <a name="create-the-sample-form-template-and-form"></a>Erstellen Sie die Beispielvorlage Formular und das Formular

1. Öffnen von InfoPath und erstellen Sie eine leere Formularvorlage.
    
2. Hinzufügen eines **Textfeld** -Steuerelements auf das Formular, und nennen Sie das Feld auf das Steuerelement CustomerName gebunden.
    
3. Klicken Sie im Aufgabenbereich **Felder** mit der rechten Maustaste in des Ordners **MyFields** , und klicken Sie dann auf **Eigenschaften**.
    
4. Wählen Sie auf der Registerkarte **Details** , und fügen Sie den folgenden Wert **Namespace:**, und fügen Sie diese in Editor oder einem anderen Speicherort, in dem Sie es abrufen können. Dieser Wert benötigen später Sie für den Wert der Eigenschaft **SelectionNamespaces** in Ihrem Code festlegen. 
    
5. Veröffentlichen Sie die Formularvorlage in einen Ordner namens C:\Test, und akzeptieren Sie den Standardnamen Vorlage1. 
    
6. Öffnen Sie die Formularvorlage, fügen Sie den Namen "Firma A" zum Textfeld an das CustomerName-Feld gebunden, und speichern Sie das Formular als "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Erstellen Sie eine verwaltetem Code zum Ändern des Namens von 'Unternehmen A' auf 'Unternehmen B'

1. Öffnen Sie Visual Studio, und erstellen Sie eine neue Visual c# oder Visual Basic-Konsolenanwendungsprojekt mit dem Namen UpdateCustomer.
    
2. Richten Sie Verweise auf die primären Interop-Microsoft Office InfoPath und InfoPath XML Interop-Assemblys, wie oben beschrieben.
    
3. Fügen Sie den folgenden Code, um die Datei Program.cs oder Module1.vb ein und stellt sicher, dass den Wert des Namespaces in der Einstellung für die **SelectionNamespaces** -Eigenschaft mit dem Wert aktualisiert, die Sie beim Erstellen des Beispielformulars kopiert. 
    
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

4. Klicken Sie zum Kompilieren und Ausführen der Konsolenanwendung im Menü **Debuggen** auf **Debuggen starten** . 
    
   Die Anwendung öffnet das Formular gespeichert wird, als Form1.xml und Durchlaufen aller CustomerName-Elemente, die den Wert Unternehmen A enthalten und ändert diesen Wert in Unternehmen B. Wenn der Vorgang abgeschlossen ist, wird eine neue Kopie des Formulars als Form2.xml im Ordner "C:\Test" gespeichert. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Öffnen eines Formulars und Auffüllen von Feldwerten automatisieren

Im folgenden Beispiel wird ein leeres Formular öffnen, und füllen den Vornamen, Nachnamen und Adressfelder im Formular automatisiert werden. In diesem Szenario wird ein Formular mit drei Textfeldern, die an die Felder FirstName, LastName und Adresse gebunden sind.
  
### <a name="create-the-sample-form-template-and-form"></a>Erstellen Sie die Beispielvorlage Formular und das Formular

1. Öffnen von InfoPath und erstellen Sie ein leeres Formular.
    
2. Drei Textfeld-Steuerelemente auf dem Formular hinzufügen, und nennen Sie die Felder gebundenen Steuerelemente: FirstName, LastName und Adresse. Fügen Sie die gewünschten Felder hinzu.
    
3. Klicken Sie im Aufgabenbereich **Felder** mit der rechten Maustaste in des Ordners **MyFields** , und klicken Sie dann auf **Eigenschaften**.
    
4. Wählen Sie auf der Registerkarte **Details** , und fügen Sie den folgenden Wert **Namespace:**, und fügen Sie diese in Editor oder einem anderen Speicherort, in dem Sie es abrufen können. Dieser Wert benötigen später Sie für den Wert der Eigenschaft **SelectionNamespaces** in Ihrem Code festlegen. 
    
5. Veröffentlichen Sie die Formularvorlage in einen Ordner namens C:\Temp, und akzeptieren Sie den Standardnamen Vorlage1.
    
6. Öffnen Sie die Formularvorlage, und speichern Sie ein leeres Formular als "Form1" c:\temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Erstellen einer Anwendung mit verwaltetem Code Konsole zum Öffnen des Formulars, und füllen Sie die Felder

1. Öffnen Sie Visual Studio, und erstellen Sie eine neue Visual c# oder Visual Basic-Konsolenanwendungsprojekt mit dem Namen OpenForm.
    
2. Richten Sie Verweise auf die primären Interop-Microsoft Office InfoPath und InfoPath XML Interop-Assemblys, wie oben beschrieben.
    
3. Fügen Sie den folgenden Code, um die Datei Program.cs oder Module1.vb ein und stellt sicher, dass den Wert des Namespaces in der Einstellung für die **SelectionNamespaces** -Eigenschaft mit dem Wert aktualisiert, die Sie beim Erstellen des Beispielformulars kopiert. 
    
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

4. Klicken Sie im Menü **Debuggen** auf **Debuggen starten** , um zu kompilieren und Ausführen der Konsolenanwendung. 
    
   Die Anwendung wird beim Öffnen des Formulars als Form1.xml gespeichert und füllen Sie die Felder FirstName, LastName und Adresse mit den Werten, die im Code angegebene und speichern Sie das Formular, das InfoPath geöffnet lassen. 
    
## <a name="see-also"></a>Siehe auch

- [Über die Microsoft Office InfoPath primären Interop-Assembly](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Über die InfoPath-XML-Interop-Assembly](about-the-infopath-xml-interop-assembly.md)

