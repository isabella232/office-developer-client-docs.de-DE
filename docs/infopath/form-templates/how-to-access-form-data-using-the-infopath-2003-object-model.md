---
title: Zugreifen auf Formulardaten mithilfe des InfoPath-Objektmodells 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- XDocument-Schnittstelle [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, Zugriff auf Formulardaten, XDocumentsCollection-Schnittstelle [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und das Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments durch die Verwendung der XDocument-Schnittstelle in Verbindung mit der XDocumentsCollection-Schnittstelle.
ms.openlocfilehash: 803122c6c377686a85f11cf48b76876c056f2ec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303675"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Zugreifen auf Formulardaten mithilfe des InfoPath-Objektmodells 2003

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und das Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments durch die Verwendung der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle in Verbindung mit der [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) -Schnittstelle. 
  
Die **XDocument**-Schnittstelle gehört zu den nützlichsten Typen innerhalb des InfoPath-Objektmodells, da sie eine Vielzahl von Eigenschaften, Methoden und Ereignissen bereitstellt, die nicht nur mit dem einem Formular zugrunde liegenden XML-Dokument zusammenarbeiten, sondern auch viele der Aktionen ausführen, die über die InfoPath-Benutzeroberfläche verfügbar sind. In einem Projekt mit verwaltetem Code, das mit dem InfoPath 2003-kompatiblen Objektmodell erstellt wurde, **** wird eine Variable vom `thisXDocument` Typ XDocument, die den `_StartUp` Namen hat, automatisch in der Methode der Klasse definiert, die Ereignishandler im Formularcode des Projekts enthält. . Sie können die `thisXDocument` Variable im Code des Formulars verwenden, um auf die **XDocument** -Schnittstelle und ihre Member zuzugreifen. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Übersicht über die XDocumentsCollection-Schnittstelle

Die **XDocumentsCollection**-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, mit deren Hilfe Entwickler die in der Auflistung enthaltenen **XDocument**-Objekte verwalten können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)-Methode  <br/> |Schließt das angegebene Formular.  <br/> |
|[Neue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) Methode  <br/> |Erstellt ein neues Formular, das auf einem vorhandenen Formular basiert.  <br/> |
|[NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx) -Methode  <br/> |Erstellt ein neues Formular, das auf einer vorhandenen Formularvorlage basiert.  <br/> |
|[NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx) -Methode  <br/> |Erstellt ein neues InfoPath-Formular mithilfe der angegebenen XML-Daten und der Formularvorlage.  <br/> |
|[Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx) -Methode  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **XDocument**-Objekte zurück, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **XDocument**-Objekt zurück.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Übersicht über die XDocument-Schnittstelle

Die **XDocument**-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, die Entwickler für die Interaktion mit dem einem Formular zugrunde liegenden XML-Dokument und für die Ausführung von Aktionen in diesem Dokument verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx) -Methode  <br/> |Gibt den Zeichenfolgenwert einer angegebenen Datenvariablen zurück.  <br/> |
|[GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx) -Methode  <br/> |Gibt einen Verweis auf das XML-DOM (Document Object Model) zurück, das dem angegebenen **DataObject**-Objekt zugeordnet ist.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx) Importierungs-Methode  <br/> |Importiert das angegebene Formular in das derzeit geöffnete Formular (oder führt es mit diesem zusammen).  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx) Print-Methode  <br/> |Druckt die aktuelle Ansicht eines Formulars.  <br/> |
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx) -Methode  <br/> |Ruft Daten von dem einem Formular zugeordneten Datenadapter ab.  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)-Methode  <br/> |Speichert das derzeit geöffnete Formular.  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)-Methode  <br/> |Speichert das derzeit geöffnete Formular unter dem angegebenen Namen.  <br/> |
|[SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx) -Methode  <br/> |Legt den Wert einer angegebenen Datenvariablen fest.  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx) -Methode  <br/> |Sendet ein Formular gemäß des Sendevorgangs, die im Entwurfsmodus festgelegt wurde.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) DataObjects-Eigenschaft  <br/> |Gibt einen Verweis auf die **DataObjects**-Auflistung zurück.  <br/> |
|[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das XML-DOM zurück, das mit den XML-Quelldaten eines Formulars aufgefüllt wird.  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die **Errors**-Auflistung zurück.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf ein Objekt zurück, das alle Funktionen und Variablen darstellt, die in der Codedatei eines Formulars enthalten sind.  <br/> |
|[IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) -Eigenschaft  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob die Daten im Formular geändert wurden.  <br/> |
|[IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx) -Eigenschaft  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob das XML-DOM schreibgeschützt ist.  <br/> |
|[IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx) -Eigenschaft  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob das Formular nach dem Erstellen gespeichert wurde.  <br/> |
|[IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx) -Eigenschaft  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob sich das Formular im schreibgeschützten Modus befindet.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) IsSigned-Eigenschaft  <br/> |Gibt einen Wert vom Typ **Boolean** zurück, der angibt, ob ein Formular digital signiert ist.  <br/> |
|[Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx) -Eigenschaft  <br/> |Gibt den Zeichenfolgenwert der für das Formular verwendeten Sprache an oder zurück.  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das Datenadapterobjekt zurück.  <br/> |
|[Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **Solution**-Objekt zurück.  <br/> |
|[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **UI**-Objekt zurück.  <br/> |
|[URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx) -Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den URI (Uniform Resource Identifier) des Formulars enthält.  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **View**-Objekt zurück.  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die **ViewInfos**-Auflistung zurück.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Verwenden der XDocuments-Auflistung und der XDocument-Schnittstellen

Der Zugriff auf die **XDocumentsCollection** -Schnittstelle erfolgt über die [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) -Eigenschaft der [Anwendungs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Schnittstelle. In einem Projekt mit verwaltetem Code, das mit dem InfoPath 2003-kompatiblen Objektmodell erstellt wurde, **** können Sie mithilfe der `thisApplication` Variablen, die in der `_StartUp` Methode des Formularcodes des Projekts instanziiert wird, auf die XDocumentsCollection-Schnittstelle zugreifen. Über die folgenden Codezeilen wird eine Variable erstellt, die auf die **XDocumentsCollection**-Schnittstelle des aktuellen Projekts verweist. 
  
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

In einem Projekt mit verwaltetem Code, das mit dem InfoPath 2003-kompatiblen Objektmodell erstellt wurde, **** können Sie mithilfe der `thisXDocument` Variablen, die in der `StartUp` Methode des Formularcodes des Projekts instanziiert wird, auf die XDocument-Schnittstelle zugreifen. Die folgende Codezeile verwendet die `thisXDocument` Variable für den Zugriff auf die **XDocument** -Schnittstelle des aktuellen Projekts, um den URI des derzeit geöffneten Formulars in einer Warnmeldung anzuzeigen. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Wenn Sie das **XDocument**-Objekt verwenden, um auf das einem Formular zugrunde liegende XML-Dokument zuzugreifen, greifen Sie auf das XML-Dokument zu, das dem derzeit geöffneten Formular zugeordnet ist. 
  
Eine Schlüsseleigenschaft der **XDocument**-Schnittstelle ist die **DOM**-Eigenschaft. Diese Eigenschaft gibt einen Verweis auf das XML-DOM zurück, das mit den XML-Quelldaten eines Formulars aufgefüllt wird. Wenn Sie die **DOM**-Eigenschaft verwenden, können Sie jede der Eigenschaften und Methoden verwenden, die vom XML-DOM unterstützt werden. Im folgenden Code wird beispielsweise die **XML** -Eigenschaft des XML-DOM verwendet, um den gesamten Inhalt des einem Formular zugrunde LIEGENden XML-Dokuments zurückzugeben und anzuzeigen. 
  
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
> Weitere Informationen zum XML-DOM und zu allen unterstützten Eigenschaften und Methoden finden Sie im MSXML-SDK auf MSDN. 
  

