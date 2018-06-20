---
title: Zugriff auf externe Datenquellen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- mit Infopath 2003-Objektmodells zugreifen InfoPath 2003-kompatible Formularvorlagen, zugreifen auf externe Daten Datenquellen [Infopath 2007]
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Beim Arbeiten mit einer InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet, können Sie Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die darin enthaltenen Daten zu bearbeiten.
ms.openlocfilehash: cf06cdc6a02eba855442cdab4c3c698ed3f4425f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790732"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Zugriff auf externe Datenquellen mithilfe des InfoPath 2003-Objektmodells

Beim Arbeiten mit einer InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet, können Sie Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die darin enthaltenen Daten zu bearbeiten.
  
Jede sekundäre Datenquelle wird durch ein Objekt mit der [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) -Schnittstelle instanziiert dargestellt und gespeicherten Daten, die von einer externen Quelle der Daten, wie etwa eine Datenbank oder einen Webdienst Abfrage abgerufen entspricht. Diese Datenquellen werden als sekundäre bezeichnet, da der Benutzer ein InfoPath-Formular speichert, der Benutzer die Daten nur in der Hauptdatenquelle nicht die Daten in der sekundären Datenquellen gespeichert wird. Die Verbindung mit einer Datenquelle wird durch ein Objekt mit einer der Schnittstellen "Datenadapter" beispielsweise die [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) -Schnittstelle eine Datenverbindung mit einem XML-Webdienst stellt instanziiert dargestellt. 
  
Das instanziierte [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) -Objekt stellt die Speicherung der (an eine Datenbank oder eine Webdienstabfrage) von einer Datenverbindung zurückgegebenen XML-Daten und der Datenadapter stellt die Datenverbindung selbst. 
  
Das InfoPath-Objektmodell unterstützt den Zugriff auf ein Formular sekundären Datenquellen mithilfe der [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) -Schnittstelle im Zusammenhang mit der [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) -Schnittstelle. 
  
Das InfoPath-Objektmodell stellt auch verschiedene Datenadapterobjekte mit Informationen über die vom Formular verwendeten Datenverbindungen bereit.  
  
Es gibt zwei Arten von Datenadaptern: Adapter Abfragen und Übermitteln von Adapter. Abfrage Adapter werden verwendet, um Daten abzurufen, die dann in eine sekundäre Datenquelle gespeichert sind, während die Submit-Adapter zum Senden von Daten an eine Datenbank oder einen Webdienst, beispielsweise verwendet werden. Die gesendeten Daten werden aus den Haupt- oder sekundären Datenquellen kopiert. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Übersicht über die DataObjectsCollection-Schnittstelle

Die [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) -Schnittstelle bietet die folgenden Eigenschaften und Methoden, die Formularentwickler [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) -Instanzen verwalten, die das Formular enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **DataSourceObject** -Instanzen, die in der Auflistung enthalten sind.  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx) -Methode  <br/> |Gibt ein **IEnumerator-Objekt** , das zum Durchlaufen der Auflistung verwendet werden kann.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf die angegebene **DataSourceObject** -Instanz zurück.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Übersicht über die DataSourceObject-Schnittstelle

Die [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) -Schnittstelle bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einer sekundären InfoPath-Datenquelle verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) -Methode  <br/> |Führt die Abfrage des Datenadapters aus und fügt die zurückgegebenen Daten wie die **DataSourceObject**XML in das XML-Objektmodell (DOM) zugeordnet.  <br/> |
|[DOM-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx) Eigenschaft  <br/> |Gibt einen Verweis auf das XML-DOM zum Speichern und Bearbeiten von Daten mithilfe der **DataSourceObject**verwendet.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)-Eigenschaft  <br/> |Gibt einen String-Wert zurück, der den Namen der **DataSourceObject**angibt.  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das zugeordnete Datenadapterobjekt zurück.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Übersicht über die Datenadapterschnittstellen

Die Schnittstellen für den Zugriff auf Datenadapter bieten verschiedene Eigenschaften und Methoden, die empfangen und Versenden von Daten über Verbindungen mit externen Datenquellen; der Datenadapter, der ein [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) -Objekt zugeordnet ist ist abhängig von der Art der Verbindung mit externen Daten. InfoPath implementiert die folgenden Schnittstellen für den Zugriff auf Datenadapter. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx) -Schnittstelle  <br/> |Stellt eine Verbindung zu ADO/OLE DB-Datenquellen her; beschränkt auf Microsoft Access und Microsoft SQL Server™.  <br/> |
|[SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx) -Schnittstelle  <br/> |Stellt eine Verbindung mit einer SharePoint-Liste oder einer Dokumentbibliothek her.  <br/> |
|[WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) -Schnittstelle  <br/> |Stellt eine Verbindung zu XML-Webdiensten her.  <br/> |
|[XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx) -Objekt  <br/> |Stellt eine Verbindung zu einer XML-Datei her.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Verwenden der Schnittstellen "DataSourceObjects" und "DataSourceObject"

Der Zugriff auf die **DataSourceObjects** -Auflistung erfolgt über die [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle. Angenommen, wenn Sie eine sekundäre Datenquelle mit der Bezeichnung Employees, die Daten aus der Employees-Tabelle in der Northwind Traders Microsoft Access-Datenbank abruft erstellen, können die **DataSourceObjects** -Auflistung Sie einen Verweis auf ein **DataObject** festgelegt Objekt, das die abgerufenen Daten darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle der Accessor-Eigenschaft über die **DataObjectsCollection** -Schnittstelle übergeben, die einen Verweis auf das **DataSourceObject** -Objekt zurückgibt. Die Daten aus der sekundären Datenquelle werden in einem Meldungsfeld angezeigt, mithilfe der **DOM** -Eigenschaft der **DataSourceObject** -Schnittstelle auf die **Xml** -Eigenschaft des XML-DOM. zugreifen 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataObjectsCollection of the form.
   // You must explicitly cast to the DataSourceObject type 
   // before you can access the data object.
   DataSourceObject myDataObject = 
      thisXDocument.DataObjects["Employees"] as DataSourceObject;
   // Display the data from the secondary data source using the 
   // XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object
   ' from the DataObjectsCollection of the form.
   Dim myDataObject As DataSourceObject = _
      thisXDocument.DataObjects("Employees")
   ' Display the data from the secondary data source using the 
   ' XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml)
End Sub
```

Um die Daten zu bearbeiten, die in eine sekundäre Datenquelle enthalten ist, verwenden Sie die **DOM** -Eigenschaft der **DataSourceObject** -Schnittstelle, um einen Verweis auf das XML-DOM mit den Daten zurückzugeben. Wenn Sie den Verweis auf das XML-DOM haben, können Sie alle Eigenschaften und Methoden des zum Bearbeiten der Daten, die er enthält. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Verwenden der Schnittstellen "DataAdaptersCollection" und "DataAdapterObject"

Der Zugriff auf die Schnittstelle [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) erfolgt über die [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) -Eigenschaft des **XDocument** -Schnittstelle. Angenommen, wenn Sie eine sekundäre Datenquelle mit der Bezeichnung Employees, die Daten aus der Employees-Tabelle in der Northwind Traders Microsoft Access-Datenbank abruft erstellen, können die **DataAdapterObjects** -Auflistung Sie einen Verweis auf die **festgelegt DataAdapterObject** , der die Verbindung mit der Datenbank darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft der **DataAdaptersCollection**übergeben, die in diesem Fall einen Verweis auf eine Instanz der **ADOAdapterObject** zurückgibt, die die Verbindung darstellt. um die Microsoft Access-Datenbank Northwind. Für diese ordnungsgemäß funktioniert müssen Sie das Objekt zurückgegeben wird, als ein **ADOAdapterObject**explizit umwandeln. Die [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) -Eigenschaft der **ADOAdapterObject** -Schnittstelle wird verwendet, um die ADO-Verbindungszeichenfolge in einem Meldungsfeld anzuzeigen. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataAdaptersCollection of the form. 
   // You must explicitly cast to the specific adapter type
   // (ADOAdapterObject) before you can access the data adapter.
   ADOAdapterObject myADOAdapter = 
      thisXDocument.DataAdapters["Employees"] as ADOAdapterObject;
   // Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object. 
   ' You must explicitly cast to the specific adapter type
   ' (ADOAdapterObject) before you can access the data adapter.
   Dim myADOAdapter As ADOAdapterObject = _
      thisXDocument.DataAdapters("Employees")
   ' Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection)
End Sub
```


