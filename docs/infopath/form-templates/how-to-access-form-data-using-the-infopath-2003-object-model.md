---
title: Zugreifen auf Formulardaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- xdocument-Schnittstelle [infopath 2007],InfoPath 2003-kompatible Formularvorlagen, Zugreifen auf Formulardaten,XDocumentsCollection-Schnittstelle [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und das Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments mithilfe der XDocument-Schnittstelle in Verbindung mit der XDocumentsCollection-Schnittstelle.
ms.openlocfilehash: 2d4e1affba8a2e42cf82f866905e674e2beeef03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631363"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Zugreifen auf Formulardaten mithilfe des InfoPath 2003-Objektmodells

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und das Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments mithilfe der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) in Verbindung mit der [XDocumentsCollection-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) 
  
Die **XDocument**-Schnittstelle gehört zu den nützlichsten Typen innerhalb des InfoPath-Objektmodells, da sie eine Vielzahl von Eigenschaften, Methoden und Ereignissen bereitstellt, die nicht nur mit dem einem Formular zugrunde liegenden XML-Dokument zusammenarbeiten, sondern auch viele der Aktionen ausführen, die über die InfoPath-Benutzeroberfläche verfügbar sind. In einem Projekt mit verwaltetem Code, das mithilfe des InfoPath 2003-kompatiblen Objektmodells erstellt wurde, wird eine Variable vom Typ **XDocument,** die benannt wird,  `thisXDocument` automatisch in der Methode der Klasse  `_StartUp` definiert, die Ereignishandler im Formularcode des Projekts enthält. Sie können die  `thisXDocument` Variable im Formularcode verwenden, um auf die **XDocument-Schnittstelle** und deren Member zuzugreifen. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Übersicht über die XDocumentsCollection-Schnittstelle

Die **XDocumentsCollection**-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, mit deren Hilfe Entwickler die in der Auflistung enthaltenen **XDocument**-Objekte verwalten können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)-Methode  <br/> |Schließt das angegebene Formular.  <br/> |
|[New-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx)  <br/> |Erstellt ein neues Formular, das auf einem vorhandenen Formular basiert.  <br/> |
|[NewFromSolution-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx)  <br/> |Erstellt ein neues Formular, das auf einer vorhandenen Formularvorlage basiert.  <br/> |
|[NewFromSolutionWithData-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Erstellt ein neues InfoPath-Formular mithilfe der angegebenen XML-Daten und der Formularvorlage.  <br/> |
|[Open-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx)  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **XDocument**-Objekte zurück, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **XDocument**-Objekt zurück.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Übersicht über die XDocument-Schnittstelle

Die **XDocument**-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, die Entwickler für die Interaktion mit dem einem Formular zugrunde liegenden XML-Dokument und für die Ausführung von Aktionen in diesem Dokument verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[GetDataVariable-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Gibt den Zeichenfolgenwert einer angegebenen Datenvariablen zurück.  <br/> |
|[GetDOM-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Gibt einen Verweis auf das XML-DOM (Document Object Model) zurück, das dem angegebenen **DataObject**-Objekt zugeordnet ist.  <br/> |
|[ImportFile-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx)  <br/> |Importiert das angegebene Formular in das derzeit geöffnete Formular (oder führt es mit diesem zusammen).  <br/> |
|[PrintOut-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx)  <br/> |Druckt die aktuelle Ansicht eines Formulars.  <br/> |
|[Abfragemethode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx)  <br/> |Ruft Daten von dem einem Formular zugeordneten Datenadapter ab.  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)-Methode  <br/> |Speichert das derzeit geöffnete Formular.  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)-Methode  <br/> |Speichert das derzeit geöffnete Formular unter dem angegebenen Namen.  <br/> |
|[SetDataVariable-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Legt den Wert einer angegebenen Datenvariablen fest.  <br/> |
|[Submit-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx)  <br/> |Sendet ein Formular gemäß des Sendevorgangs, die im Entwurfsmodus festgelegt wurde.  <br/> |
|[DataObjects-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx)  <br/> |Gibt einen Verweis auf die **DataObjects**-Auflistung zurück.  <br/> |
|[DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Gibt einen Verweis auf das XML-DOM zurück, das mit den XML-Quelldaten eines Formulars aufgefüllt wird.  <br/> |
|[Errors-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx)  <br/> |Gibt einen Verweis auf die **Errors**-Auflistung zurück.  <br/> |
|[Extension-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx)  <br/> |Gibt einen Verweis auf ein Objekt zurück, das alle Funktionen und Variablen darstellt, die in der Codedatei eines Formulars enthalten sind.  <br/> |
|[IsDirty-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx)  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob die Daten im Formular geändert wurden.  <br/> |
|[IsDOMReadOnly-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx)  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob das XML-DOM schreibgeschützt ist.  <br/> |
|[IsNew-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx)  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob das Formular nach dem Erstellen gespeichert wurde.  <br/> |
|[IsReadOnly-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx)  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob sich das Formular im schreibgeschützten Modus befindet.  <br/> |
|[IsSigned-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx)  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob ein Formular digital signiert ist.  <br/> |
|[Language-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx)  <br/> |Gibt den Zeichenfolgenwert der für das Formular verwendeten Sprache an oder zurück.  <br/> |
|[QueryAdapter-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx)  <br/> |Gibt einen Verweis auf das Datenadapterobjekt zurück.  <br/> |
|[Solution-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx)  <br/> |Gibt einen Verweis auf das **Solution**-Objekt zurück.  <br/> |
|[UI-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)  <br/> |Gibt einen Verweis auf das **UI**-Objekt zurück.  <br/> |
|[URI-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx)  <br/> |Gibt einen Zeichenfolgenwert zurück, der den URI (Uniform Resource Identifier) des Formulars enthält.  <br/> |
|[View-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx)  <br/> |Gibt einen Verweis auf das **View**-Objekt zurück.  <br/> |
|[ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx)  <br/> |Gibt einen Verweis auf die **ViewInfos**-Auflistung zurück.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Verwenden der XDocuments-Auflistung und der XDocument-Schnittstellen

Der Zugriff auf die **XDocumentsCollection-Schnittstelle** erfolgt über die [XDocuments-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) der [Application-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) In einem Projekt mit verwaltetem Code, das mit dem InfoPath 2003-kompatiblen Objektmodell erstellt wurde, können Sie auf die **XDocumentsCollection-Schnittstelle** zugreifen, indem Sie die  `thisApplication` Variable verwenden, die in der Methode des Formularcodes Ihres Projekts instanziiert  `_StartUp` wird. Über die folgenden Codezeilen wird eine Variable erstellt, die auf die **XDocumentsCollection**-Schnittstelle des aktuellen Projekts verweist. 
  
```cs
XDocumentsCollection xdocs;
xdocs = thisApplication.XDocuments;
// Write code here to work with the XDocumentsCollection.
```

```vb
Dim xdocs As XDocumentsCollection
xdocs = thisApplication.XDocuments
' Write code here to work with the XDocumentsCollection.
```

In einem Projekt mit verwaltetem Code, das mit dem InfoPath 2003-kompatiblen Objektmodell erstellt wurde, können Sie auf die **XDocument-Schnittstelle** zugreifen, indem Sie die  `thisXDocument` Variable verwenden, die in der Methode des Formularcodes des Projekts instanziiert  `StartUp` wird. In der folgenden Codezeile wird die  `thisXDocument` Variable verwendet, um auf die **XDocument-Schnittstelle** des aktuellen Projekts zuzugreifen, um den URI des aktuell geöffneten Formulars in einer Warnmeldung anzuzeigen. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Wenn Sie das **XDocument**-Objekt verwenden, um auf das einem Formular zugrunde liegende XML-Dokument zuzugreifen, greifen Sie auf das XML-Dokument zu, das dem derzeit geöffneten Formular zugeordnet ist. 
  
Eine Schlüsseleigenschaft der **XDocument**-Schnittstelle ist die **DOM**-Eigenschaft. Diese Eigenschaft gibt einen Verweis auf das XML-DOM zurück, das mit den XML-Quelldaten eines Formulars aufgefüllt wird. Wenn Sie die **DOM**-Eigenschaft verwenden, können Sie jede der Eigenschaften und Methoden verwenden, die vom XML-DOM unterstützt werden. Der folgende Code verwendet beispielsweise die **XML-Eigenschaft** des XML-DOM, um den gesamten Inhalt des einem Formular zugrunde liegenden XML-Dokuments zurückzugeben und anzuzeigen. 
  
```cs
string xmldoc;
xmldoc = thisXDocument.DOM.xml;
// Display xml.
thisXDocument.UI.Alert(xmldoc);
```

```vb
Dim xmldoc As String
xmldoc = thisXDocument.DOM.xml
' Display xml.
thisXDocument.UI.Alert(xmldoc)
```

> [!NOTE]
> Weitere Informationen zum XML-DOM und allen unterstützten Eigenschaften und Methoden finden Sie im MSXML SDK auf MSDN. 
  

