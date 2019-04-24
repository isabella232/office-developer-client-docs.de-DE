---
title: Szenarien für die externe Automatisierung und Beispiele
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Automatisieren von InfoPath 2007, Formularen [InfoPath 2007], Hinzufügen von Daten programmgesteuert, Automatisierung [InfoPath 2007], externe Szenarien
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Die Mitglieder, die von der primären Interop-Assembly von Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) und der InfoPath-XML-Interop-Assembly (Microsoft. Office. Interop. InfoPath. Xml. dll) bereitgestellt werden, unterstützen das Schreiben von verwaltetem Code für die Automatisierung InfoPath.
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310199"
---
# <a name="external-automation-scenarios-and-examples"></a>Szenarien für die externe Automatisierung und Beispiele

Die Mitglieder, die von der primären Interop-Assembly von Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) und der InfoPath-XML-Interop-Assembly (Microsoft. Office. Interop. InfoPath. Xml. dll) bereitgestellt werden, unterstützen das Schreiben von verwaltetem Code für die Automatisierung InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Einrichten von Verweisen auf die XML-Interop-Assemblys von Microsoft Office InfoPath Primary Interop und InfoPath

Zum Schreiben von verwaltetem Code für die Automatisierung von InfoPath müssen Sie Verweise auf die Microsoft InfoPath Primary Interoperability und die XML-Interop-Assemblys von InfoPath erstellen. Die primäre Interop-Assembly von Microsoft InfoPath bietet Unterstützung für die Interoperabilität mit dem von IPEDITOR verfügbar gemachten COM-Objektmodell. DLL mithilfe der Member des [Microsoft. Office. Interop. InfoPath-](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) Namespaces. Die XML-Interop-Assembly von InfoPath bietet Unterstützung für die Interoperabilität mit dem COM-Objektmodell, das von Microsoft XML Core Services (MSXML) mithilfe der Member des [Microsoft. Office. Interop. InfoPath. XML-](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) Namespaces verfügbar gemacht wird. 
  
> [!IMPORTANT]
> Benutzer von Anwendungen mit verwaltetem Code, die InfoPath automatisieren, müssen InfoPath, die primäre Interop-Assembly von Microsoft Office InfoPath und die InfoPath-XML-Interop-Assembly auf ihren Computern installiert haben. Die Option **.NET-Programmierunterstützung** im InfoPath-Setupprogramm wird für eine typische Installation von InfoPath auf " **Arbeitsplatz** " festgelegt.
>  
> Solange das .NET Framework 1,1 Redistributable oder .NET Framework 1,1 Software Development Kit (SDK) oder höher installiert ist, werden diese Interop-Assemblys auch standardmäßig installiert. Wenn diese Interop-Assemblys auf dem Computer eines Benutzers nicht verfügbar sind, müssen Sie bestätigen, dass .NET Framework 1,1 oder höher installiert ist, und dann **Programme und Funktionen** aus der **System** Steuerung ausführen, um das Setup zu ändern und die **.net-Programmierbarkeit festzulegen. Support** Option von InfoPath, die **von meinem Computer aus ausgeführt**werden soll. 
  
In den folgenden Verfahren wird beschrieben, wie Sie Verweise auf Microsoft Office InfoPath Primary Interop und die InfoPath-XML-Interop-Assemblys in einem Visual Studio-Projekt festlegen.
  
Wenn Sie einen Verweis auf die primäre Interop-Assembly von Microsoft. Office. Interop. InfoPath festlegen möchten, legen Sie auf der Registerkarte **com** des Dialogfelds **Verweis hinzufügen** einen Verweis auf die **microsoft InfoPath-Typbibliothek 3,0** fest. Auch wenn Sie einen Verweis auf der Registerkarte **com** festlegen, wird ein Verweis auf die primäre Interop-Assembly von Microsoft. Office. Interop. InfoPath. dll festgelegt, die im globalen ASSEMBLYCACHE (GAC) vom InfoPath-Setupprogramm installiert wird. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Festlegen eines Verweises auf die primäre Interop-Assembly von Microsoft. Office. Interop. InfoPath

1. Öffnen Sie ein Visual Studio-Projekt mit verwaltetem Code.
    
2. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf **Verweise**, und klicken Sie dann auf **Verweis hinzufügen**.
    
3. Doppelklicken Sie auf der Registerkarte **com** auf **Microsoft InfoPath 3,0**-Typbibliothek, und klicken Sie dann auf **OK**.
    
Wenn Sie einen Verweis auf die Interop-Assembly Microsoft. Office. Interop. InfoPath. XML festlegen möchten, navigieren Sie zur Datei Microsoft. Office. Interop. InfoPath. Xml. dll, die standardmäßig im Ordner < _Drive_>: \Programme\Microsoft Office\OFFICE14 installiert ist. . Auch wenn Sie die Kopie der Assembly im lokalen Dateisystem angeben, richtet dieses Verfahren einen Verweis auf die Microsoft. Office. Interop. InfoPath. Xml. dll-Assembly ein, die vom InfoPath-Setupprogramm im globalen Assemblycache (GAC) installiert wird.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Festlegen eines Verweises auf die Microsoft. Office. Interop. InfoPath. XML-Interop-Assembly

1. Öffnen oder erstellen Sie ein Visual Studio-Projekt mit verwaltetem Code, beispielsweise eine **Konsolenanwendung** oder eine **Windows-Anwendung**.
    
2. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf **Verweise**, und klicken Sie dann auf **Verweis hinzufügen**.
    
3. Klicken Sie auf der Registerkarte **.net** auf **Durchsuchen**, navigieren Sie zum Ordner < _Drive_>: \Programme\Microsoft Office\OFFICE14, und klicken Sie dann auf Microsoft. Office. Interop. InfoPath. Xml. dll.
    
4. Klicken Sie auf **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatisieren des Änderns des Werts eines Felds

Angenommen, einer der Kunden des Benutzers einer InfoPath-Formularvorlage für den Umsatzbericht hat kürzlich seinen Namen von "Firma A" in "Firma B" geändert. Ein Entwickler wird aufgefordert, Code zu schreiben, mit dem die von dieser Formularvorlage gespeicherten Umsatzberichtsformulare automatisch aktualisiert werden, um die Namensänderung widerzuspiegeln. Im folgenden Szenario wird davon ausgegangen, dass ein Formular, das ein Textfeld enthält, das an ein Feld mit dem Namen CustomerName gebunden ist.
  
### <a name="create-the-sample-form-template-and-form"></a>Erstellen der Beispielformularvorlage und des Formulars

1. Öffnen Sie InfoPath, und erstellen Sie eine leere Formularvorlage.
    
2. Fügen Sie dem Formular ein **Textfeld** -Steuerelement hinzu, und nennen Sie das Feld, das an das Steuerelement customerName gebunden ist.
    
3. Klicken Sie im Aufgabenbereich **Felder** mit der rechten Maustaste auf den Ordner myFields, und klicken Sie dann auf **Eigenschaften**. ****
    
4. Wählen Sie auf der Registerkarte **Details** den folgenden **Namespace**aus, und kopieren Sie ihn, und fügen Sie diesen in den Editor oder einen anderen Speicherort ein, an dem Sie ihn abrufen können. Sie benötigen diesen Wert später zum Festlegen des Werts der **SelectionNamespaces** -Eigenschaft im Code. 
    
5. Veröffentlichen Sie die Formularvorlage in einem Ordner mit dem Namen C:\Test, und übernehmen Sie den Standardnamen Template1. 
    
6. Öffnen Sie die Formularvorlage, fügen Sie den Namen "Firma A" zum Textfeld hinzu, das an das Feld CustomerName gebunden ist, und speichern Sie das Formular dann als "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Erstellen Sie eine Konsolenanwendung mit verwaltetem Code, um den Namen von "Firma A" zu "Firma B" zu ändern.

1. Öffnen Sie Visual Studio, und erstellen Sie eine neue Visual C#-oder Visual Basic-Konsolenanwendung mit dem Namen UpdateCustomer.
    
2. Stellen Sie, wie oben beschrieben, Verweise auf die Microsoft Office InfoPath Primary Interop-und InfoPath-Interop-Assemblys her.
    
3. Fügen Sie der Datei Program.cs oder Module1. vb den folgenden Code hinzu, und stellen Sie sicher, dass der Wert des Namespaces in der Einstellung für die **SelectionNamespaces** -Eigenschaft mit dem Wert aktualisiert wird, den Sie beim Erstellen des Beispielformulars kopiert haben. 
    
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
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

4. Klicken Sie im Menü **Debuggen** auf **Debuggen starten** , um die Konsolenanwendung zu kompilieren und auszuführen. 
    
   Die Anwendung öffnet das als Form1. xml gespeicherte Formular und durchläuft alle customerName-Elemente, die den Wert Company A enthalten, und ändert diesen Wert in Firma B. Wenn der Vorgang abgeschlossen ist, wird eine neue Kopie des Formulars im Ordner C:\Test als Form2. XML gespeichert. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatisieren des Öffnens eines Formulars und Auffüllen von Feldwerten

Im folgenden Beispiel wird das Öffnen eines leeren Formulars und das Auffüllen der Felder Vorname, Nachname und Adresse im Formular automatisiert. In diesem Szenario wird davon ausgegangen, dass ein Formular drei Textfelder enthält, die an Felder mit dem Namen FirstName, LastName und Address gebunden sind.
  
### <a name="create-the-sample-form-template-and-form"></a>Erstellen der Beispielformularvorlage und des Formulars

1. Öffnen Sie InfoPath, und erstellen Sie ein leeres Formular.
    
2. Fügen Sie dem Formular drei Textfeld-Steuerelemente hinzu, und nennen Sie die Felder, die an die Steuerelemente gebunden sind: FirstName, LastName und Address. Fügen Sie alle anderen gewünschten Felder hinzu.
    
3. Klicken Sie im Aufgabenbereich **Felder** mit der rechten Maustaste auf den Ordner myFields, und klicken Sie dann auf **Eigenschaften**. ****
    
4. Wählen Sie auf der Registerkarte **Details** den folgenden **Namespace**aus, und kopieren Sie ihn, und fügen Sie diesen in den Editor oder einen anderen Speicherort ein, an dem Sie ihn abrufen können. Sie benötigen diesen Wert später zum Festlegen des Werts der **SelectionNamespaces** -Eigenschaft im Code. 
    
5. Veröffentlichen Sie die Formularvorlage in einem Ordner mit dem Namen C:\Temp, und übernehmen Sie den Standardnamen Template1.
    
6. Öffnen Sie die Formularvorlage, und speichern Sie ein leeres Formular als "Form1" in C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Erstellen einer Konsolenanwendung mit verwaltetem Code zum Öffnen des Formulars und zum Auffüllen der Felder

1. Öffnen Sie Visual Studio, und erstellen Sie eine neue Visual C#-oder Visual Basic-Konsolenanwendung mit dem Namen OpenForm.
    
2. Stellen Sie, wie oben beschrieben, Verweise auf die Microsoft Office InfoPath Primary Interop-und InfoPath-Interop-Assemblys her.
    
3. Fügen Sie der Datei Program.cs oder Module1. vb den folgenden Code hinzu, und stellen Sie sicher, dass der Wert des Namespaces in der Einstellung für die **SelectionNamespaces** -Eigenschaft mit dem Wert aktualisiert wird, den Sie beim Erstellen des Beispielformulars kopiert haben. 
    
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
            doc.setProperty("SelectionNamespaces","xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
          doc.setProperty("SelectionNamespaces", "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. Klicken Sie im Menü **Debuggen** auf **Debuggen starten** , um die Konsolenanwendung zu kompilieren und auszuführen. 
    
   Die Anwendung öffnet das als Form1. xml gespeicherte Formular und füllt die Felder FirstName, LastName und Address mit den im Code angegebenen Werten, und speichern Sie das Formular, und lassen Sie InfoPath geöffnet. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen zur Microsoft Office InfoPath Primary Interop-Assembly](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Informationen zur InfoPath XML Interop-Assembly](about-the-infopath-xml-interop-assembly.md)

