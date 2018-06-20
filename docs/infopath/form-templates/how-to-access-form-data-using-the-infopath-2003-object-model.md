---
title: Access-Formulardaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- XDocument-Schnittstelle [Infopath 2007] InfoPath 2003-kompatible Formularvorlagen, zugreifen auf Formulardaten, XDocumentsCollection-Schnittstelle [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es oft notwendig, den programmgesteuerten Zugriff auf Informationen zu dem Formular zugrunde liegenden XML-Dokument, Zugriff auf die Daten, die das XML-Dokument enthält oder Aktionen auf dem XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und Bearbeitung von einem Formular zugrunde liegenden XML-Dokument mithilfe der XDocument-Schnittstelle im Zusammenhang mit der XDocumentsCollection-Schnittstelle.
ms.openlocfilehash: 24e9abc8ce7327ab94b3608f1279c0f0d381ea83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790736"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Access-Formulardaten mithilfe des InfoPath 2003-Objektmodells

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es oft notwendig, den programmgesteuerten Zugriff auf Informationen zu dem Formular zugrunde liegenden XML-Dokument, Zugriff auf die Daten, die das XML-Dokument enthält oder Aktionen auf dem XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und Bearbeitung von einem Formular zugrunde liegenden XML-Dokument mithilfe der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle im Zusammenhang mit der [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) -Schnittstelle. 
  
Die **XDocument** -Schnittstelle ist eine der nützlichsten Typen innerhalb des InfoPath-Objektmodells, da es eine Vielzahl von Eigenschaften, Methoden bietet und Ereignisse, die nicht nur mit einem Formular zugrunde liegenden XML interagieren-Dokument, jedoch auch viele der Aktionen ausführen, stehen in der InfoPath-Benutzeroberfläche. Geben Sie in ein Projekt mit verwaltetem Code mit dem InfoPath 2003-kompatible Objektmodell erstellt, eine Variable vom **XDocument-Objekt** mit dem Namen `thisXDocument` wird automatisch in definiert die `_StartUp` -Methode der Klasse, die Ereignishandler in Ihrem Projekt Formularcode enthält . Sie können die `thisXDocument` Variablen in Code des Formulars auf die **XDocument** -Schnittstelle und deren Member zugreifen. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Übersicht über die XDocumentsCollection-Schnittstelle

Die **XDocumentsCollection** -Schnittstelle bietet die folgenden Methoden und Eigenschaften, die Formularentwickler verwenden können, die die Auflistung enthaltenen **XDocument** -Objekte verwalten. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)-Methode  <br/> |Schließt das angegebene Formular.  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) -Methode  <br/> |Erstellt ein neues Formular, das auf einem vorhandenen Formular basiert.  <br/> |
|[NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx) -Methode  <br/> |Erstellt ein neues Formular, das auf einer vorhandenen Formularvorlage basiert.  <br/> |
|[NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx) -Methode  <br/> |Erstellt ein neues InfoPath-Formular mithilfe der angegebenen XML-Daten und der Formularvorlage.   <br/> |
|[Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx) -Methode  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der in der Auflistung enthaltenen **XDocument** -Objekte zurück.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **XDocument** -Objekt zurück.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Übersicht über die XDocument-Schnittstelle

Die **XDocument** -Schnittstelle bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit und Ausführen von Aktionen für das einem Formular zugrunde liegenden XML-Dokument verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx) -Methode  <br/> |Gibt den Zeichenfolgenwert einer angegebenen Datenvariablen zurück.  <br/> |
|[GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx) -Methode  <br/> |Gibt einen Verweis auf das XML-Objektmodell DOM (Document Object) der angegebenen **DataObject** -Objekt zugeordnet.  <br/> |
|[ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx) -Methode  <br/> |Importiert das angegebene Formular in das derzeit geöffnete Formular (oder führt es mit diesem zusammen).  <br/> |
|[PrintOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx) -Methode  <br/> |Druckt die aktuelle Ansicht eines Formulars.  <br/> |
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx) -Methode  <br/> |Ruft Daten von dem einem Formular zugeordneten Datenadapter ab.  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)-Methode  <br/> |Speichert das derzeit geöffnete Formular.  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)-Methode  <br/> |Speichert das derzeit geöffnete Formular unter dem angegebenen Namen.  <br/> |
|[SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx) -Methode  <br/> |Legt den Wert einer angegebenen Datenvariablen fest.  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx) -Methode  <br/> |Sendet ein Formular gemäß des Sendevorgangs, die im Entwurfsmodus festgelegt wurde.  <br/> |
|[DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die **DataObjects** -Auflistung zurück.  <br/> |
|[DOM-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) Eigenschaft  <br/> |Gibt einen Verweis auf das XML-DOM zurück, das mit den XML-Quelldaten eines Formulars aufgefüllt wird.  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die **Errors** -Auflistung zurück.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf ein Objekt zurück, das alle Funktionen und Variablen darstellt, die in der Codedatei eines Formulars enthalten sind.  <br/> |
|[IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) -Eigenschaft  <br/> |Gibt einen **Boolean** -Wert zurück, der angibt, ob die Daten im Formular geändert wurden.  <br/> |
|[IsDOMReadOnly (](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx) Eigenschaft)  <br/> |Gibt einen **Boolean** -Wert zurück, der angibt, ob das XML-DOM schreibgeschützt festgelegt ist.  <br/> |
|[IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx) -Eigenschaft  <br/> |Gibt einen **Boolean** -Wert zurück, der angibt, ob das Formular gespeichert wurde, nachdem es erstellt wurde.  <br/> |
|[IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx) -Eigenschaft  <br/> |Gibt einen **Boolean** -Wert zurück, der angibt, ob das Formular im schreibgeschützten Modus befindet.  <br/> |
|[IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) -Eigenschaft  <br/> |Gibt einen **Boolean** -Wert zurück, der angibt, ob das Formular digital signiert ist.  <br/> |
|[Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx) -Eigenschaft  <br/> |Gibt den Zeichenfolgenwert der für das Formular verwendeten Sprache an oder zurück.  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das Datenadapterobjekt zurück.  <br/> |
|[Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **Solution** -Objekt zurück.  <br/> |
|[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **UI** -Objekt zurück.  <br/> |
|[URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx) -Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den URI (Uniform Resource Identifier) des Formulars enthält.  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **View** -Objekt zurück.  <br/> |
|[ViewInfos (](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx) Eigenschaft)  <br/> |Gibt einen Verweis auf die **ViewInfos** -Auflistung zurück.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Verwenden der XDocuments-Auflistung und der XDocument-Schnittstellen

Die **XDocumentsCollection** -Schnittstelle erfolgt über die [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Schnittstelle. In einem Projekt mit verwaltetem Code mit dem InfoPath 2003-kompatible Objektmodell erstellt haben, können Sie die **XDocumentsCollection** -Schnittstelle zugreifen, mithilfe der `thisApplication` Variable, die in instanziiert wird die `_StartUp` -Methode des Formularcode Ihres Projekts. Die folgenden Codezeilen erstellen Sie eine Variable, die die **XDocumentsCollection** -Schnittstelle des aktuellen Projekts verweist. 
  
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

In einem Projekt mit verwaltetem Code mit dem InfoPath 2003-kompatible Objektmodell erstellt haben, können Sie die **XDocument** -Schnittstelle zugreifen, mithilfe der `thisXDocument` Variable, die in instanziiert wird die `StartUp` -Methode des Formularcode Ihres Projekts. Die folgende Codezeile Code verwendet die `thisXDocument` Variable auf das **XDocument** -Schnittstelle des aktuellen Projekts in eine Benachrichtigung an den URI das derzeit geöffnete Formular angezeigt. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Wenn Sie die **XDocument** -Schnittstelle verwenden, um auf einem Formular zugrunde liegenden XML-Dokument zuzugreifen, greifen Sie das XML-Dokument, das dem derzeit geöffneten Formular zugeordnet ist. 
  
Eine zentrale Eigenschaft des **XDocument** -Schnittstelle ist die **DOM** -Eigenschaft. Diese Eigenschaft gibt einen Verweis auf das XML-DOM, die mit den XML-Quelldaten eines Formulars aufgefüllt wird. Wenn Sie die **DOM** -Eigenschaft verwenden, können Sie die Eigenschaften und Methoden, die vom XML-DOM. unterstützt werden Beispielsweise verwendet der folgende Code die **Xml** -Eigenschaft des XML-DOM zurückzugeben und alle Inhalte des einem Formular zugrunde liegenden XML-Dokument anzeigen. 
  
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
> Weitere Informationen zum XML-DOM und alle Eigenschaften und Methoden, die es unterstützt finden Sie unter MSXML SDK auf MSDN. 
  

