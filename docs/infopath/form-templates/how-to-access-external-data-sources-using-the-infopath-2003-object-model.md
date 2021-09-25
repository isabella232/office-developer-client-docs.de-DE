---
title: Zugreifen auf externe Datenquellen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Datenquellen [infopath 2007], Zugreifen mit infopath 2003-Objektmodell, InfoPath 2003-kompatible Formularvorlagen, Zugreifen auf externe Daten
ms.localizationpriority: medium
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Beim Arbeiten mit einer InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet, können Sie Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die darin enthaltenen Daten zu bearbeiten.
ms.openlocfilehash: f8cf9bf1d4f94fb2486dff6c436331a66842df67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592935"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Zugreifen auf externe Datenquellen mithilfe des InfoPath 2003-Objektmodells

Beim Arbeiten mit einer InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet, können Sie Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die darin enthaltenen Daten zu bearbeiten.
  
Jede sekundäre Datenquelle wird durch ein Mithilfe der [DataSourceObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) instanziiertes Objekt dargestellt und entspricht gespeicherten Daten, die aus einer externen Datenquelle wie einer Datenbank oder einer Webdienstabfrage abgerufen werden. Diese Datenquellen werden als sekundär bezeichnet, da der Benutzer beim Speichern eines InfoPath-Formulars die Daten nur in der Hauptdatenquelle und nicht in den sekundären Datenquellen speichert. Die Verbindung mit einer Datenquelle wird durch ein Objekt dargestellt, das mithilfe einer der Datenadapterschnittstellen instanziiert wird, z. B. der [WebServiceAdapterObject-Schnittstelle,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) die eine Datenverbindung mit einem XML-Webdienst darstellt. 
  
Das instanziierte [DataSourceObject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) stellt die Speicherung von XML-Daten dar, die von einer Datenverbindung (mit einer Datenbank- oder Webdienstabfrage) zurückgegeben werden, und der Datenadapter stellt die Datenverbindung selbst dar. 
  
Das InfoPath-Objektmodell unterstützt den Zugriff auf die sekundären Datenquellen eines Formulars durch die Verwendung der [DataSourceObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) in Verbindung mit der [DataObjectsCollection-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) 
  
Das InfoPath-Objektmodell stellt auch verschiedene Datenadapterobjekte mit Informationen über die vom Formular verwendeten Datenverbindungen bereit. 
  
Es gibt zwei Typen von Datenadaptern: Abfrageadapter und Absendeadapter. Abfrageadapter werden zum Abrufen der in einer sekundären Datenquelle gespeicherten Daten verwendet, während Absendeadapter zum Senden von Daten z. B. an eine Datenbank oder einen Webdienst verwendet werden. Die gesendeten Daten werden aus den Hauptdatenquellen oder den sekundären Datenquellen kopiert. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Übersicht über die DataObjectsCollection-Schnittstelle

Die [DataObjectsCollection-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) stellt die folgenden Eigenschaften und Methoden bereit, mit denen Formularentwickler die [DataSourceObject-Instanzen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) verwalten können, die das Formular enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **DataSourceObject**-Instanzen zurück, die in der Auflistung enthalten sind.  <br/> |
|[GetEnumerator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Gibt ein **IEnumerator**-Objekt zurück, das für die Iteration durch die Auflistung verwendet werden kann.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf die angegebene **DataSourceObject**-Instanz zurück.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Übersicht über die DataSourceObject-Schnittstelle

Die [DataSourceObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) stellt die folgende Methode und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer sekundären InfoPath-Datenquelle verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Abfragemethode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx)  <br/> |Führt die Abfrage des Datenadapters aus und fügt die zurückgegebenen Daten als XML in das XML-DOM (Document Object Model) ein, das der **DataSourceObject**-Schnittstelle zugeordnet ist.  <br/> |
|[DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Gibt einen Verweis auf das zum Speichern und Bearbeiten von Daten mithilfe der **DataSourceObject**-Schnittstelle verwendete XML-DOM zurück.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)-Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den Namen der **DataSourceObject**-Schnittstelle angibt.  <br/> |
|[QueryAdapter-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Gibt einen Verweis auf das zugeordnete Datenadapterobjekt zurück.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Übersicht über die Datenadapterschnittstellen

Die Schnittstellen für den Zugriff auf Datenadapter stellen unterschiedliche Eigenschaften und Methoden bereit, die Daten über Verbindungen zu externen Datenquellen abrufen und übermitteln. Der Datenadapter, der einem [DataSourceObject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) zugeordnet ist, hängt vom Typ der externen Datenverbindung ab. InfoPath implementiert die folgenden Schnittstellen für den Zugriff auf Datenadapter. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ADOAdapterObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Stellt eine Verbindung zu ADO/OLE DB-Datenquellen her; beschränkt auf Microsoft Access und Microsoft SQL Server™.  <br/> |
|[SharepointListAdapterObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Stellt eine Verbindung mit einer SharePoint-Liste oder einer Dokumentbibliothek her.  <br/> |
|[WebServiceAdapterObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Stellt eine Verbindung zu XML-Webdiensten her.  <br/> |
|[XMLFileAdapterObject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Stellt eine Verbindung zu einer XML-Datei her.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Verwenden der Schnittstellen "DataSourceObjects" und "DataSourceObject"

Der Zugriff auf die **DataSourceObjects-Auflistung** erfolgt über die [DataObjects-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) der [XDocument-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) Wenn Sie z. B. eine sekundäre Datenquelle namens "Personal" erstellen, die Daten aus der Tabelle "Personal" in der Microsoft Access-Datenbank "Nordwind" abruft, können Sie mithilfe der **DataSourceObjects**-Auflistung einen Verweis auf das **DataObject**-Objekt festlegen, das die abgefragten Daten darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft der **DataObjectsCollection**-Schnittstelle übergeben, die einen Verweis auf das **DataSourceObject**-Objekt zurückgibt. Die Daten aus der sekundären Datenquelle werden mithilfe der **DOM**-Eigenschaft der **DataSourceObject**-Schnittstelle in einem Nachrichtenfeld angezeigt, um auf die **xml**-Eigenschaft des XML-DOM zuzugreifen. 
  
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

Zur Bearbeitung der in einer sekundären Datenquelle enthaltenen Daten verwenden Sie die **DOM**-Eigenschaft der **DataSourceObject**-Schnittstelle, um einen Verweis auf das XML-DOM zurückzugeben, das die Daten enthält. Wenn der Verweis auf das XML-DOM vorliegt, können Sie beliebige seiner Eigenschaften und Methoden verwenden, um die enthaltenen Daten zu bearbeiten. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Verwenden der Schnittstellen "DataAdaptersCollection" und "DataAdapterObject"

Der Zugriff auf die [DataAdaptersCollection-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) erfolgt über die [DataAdapters-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) der **XDocument-Schnittstelle.** Wenn Sie beispielsweise eine sekundäre Datenquelle namens "Personal" erstellen, die Daten aus der Tabelle "Personal" in der Microsoft Access-Datenbank "Nordwind" abruft, können Sie mithilfe der **DataAdapterObjects**-Auflistung einen Verweis auf das **DataAdapterObject**-Objekt festlegen, das die Verbindung zur Datenbank darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft von **DataAdaptersCollection** übergeben, die in diesem Fall einen Verweis auf eine Instanz der **ADOAdapterObject**-Schnittstelle zurückgibt, die die Verbindung mit der Microsoft Access-Datenbank "Nordwind" darstellt. Dies funktioniert nur einwandfrei, wenn Sie das zurückgegebene Objekt explizit zu einer **ADOAdapterObject**-Schnittstelle umwandeln. Die [Connection-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) der **ADOAdapterObject-Schnittstelle** wird verwendet, um die ADO-Verbindungszeichenfolge in einem Meldungsfeld anzuzeigen. 
  
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


