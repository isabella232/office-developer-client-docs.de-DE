---
title: Zugreifen auf externe Datenquellen mit dem InfoPath-Objektmodell 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Datenquellen [InfoPath 2007], Zugriff mit InfoPath 2003-Objektmodell, InfoPath 2003-kompatible Formularvorlagen, Zugriff auf externe Daten
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Beim Arbeiten mit einer InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet, können Sie Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die darin enthaltenen Daten zu bearbeiten.
ms.openlocfilehash: 569f029b412328f4d49e3079eaf207dc1556fc4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431680"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Zugreifen auf externe Datenquellen mit dem InfoPath-Objektmodell 2003

Beim Arbeiten mit einer InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet, können Sie Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die darin enthaltenen Daten zu bearbeiten.
  
Jede sekundäre Datenquelle wird durch ein Objekt dargestellt, das mithilfe der [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) DataSourceObject-Schnittstelle instanziiert wird, und entspricht gespeicherten Daten, die von einer externen Datenquelle wie einer Datenbank oder einer Webdienstabfrage abgerufen werden. Diese Datenquellen werden als sekundär bezeichnet, da der Benutzer beim Speichern eines InfoPath-Formulars die Daten nur in der Hauptdatenquelle und nicht in den sekundären Datenquellen speichert. Die Verbindung zu einer Datenquelle wird durch ein Objekt dargestellt, das mit einer der Datenadapterschnittstellen instanziiert wird, wie beispielsweise der [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) -Schnittstelle, die eine Datenverbindung mit einem XML-Webdienst darstellt. 
  
Das instanziierte [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) DataSourceObject-Objekt stellt die Speicherung von XML-Daten dar, die von einer Datenverbindung (an eine Datenbank-oder Webdienstabfrage) zurückgegeben werden, und der Datenadapter stellt die Datenverbindung selbst dar. 
  
Das InfoPath-Objektmodell unterstützt den Zugriff auf die sekundären Datenquellen eines Formulars mithilfe [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) der DataSourceObject-Schnittstelle in Verbindung mit der DataObjectsCollection-Schnittstelle. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) 
  
Das InfoPath-Objektmodell stellt auch verschiedene Datenadapterobjekte mit Informationen über die vom Formular verwendeten Datenverbindungen bereit. 
  
Es gibt zwei Typen von Datenadaptern: Abfrageadapter und Absendeadapter. Abfrageadapter werden zum Abrufen der in einer sekundären Datenquelle gespeicherten Daten verwendet, während Absendeadapter zum Senden von Daten z. B. an eine Datenbank oder einen Webdienst verwendet werden. Die gesendeten Daten werden aus den Hauptdatenquellen oder den sekundären Datenquellen kopiert. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Übersicht über die DataObjectsCollection-Schnittstelle

Die [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) DataObjectsCollection-Schnittstelle stellt die folgenden Eigenschaften und Methoden bereit, mit denen Formularentwickler die vom Formular enthaltenen DataSourceObject-Instanzen verwalten können. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **DataSourceObject**-Instanzen zurück, die in der Auflistung enthalten sind.  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx) -Methode  <br/> |Gibt ein **IEnumerator**-Objekt zurück, das für die Iteration durch die Auflistung verwendet werden kann.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf die angegebene **DataSourceObject**-Instanz zurück.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Übersicht über die DataSourceObject-Schnittstelle

Die [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) DataSourceObject-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer sekundären InfoPath-Datenquelle verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) -Methode  <br/> |Führt die Abfrage des Datenadapters aus und fügt die zurückgegebenen Daten als XML in das XML-DOM (Document Object Model) ein, das der **DataSourceObject**-Schnittstelle zugeordnet ist.  <br/> |
|[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das zum Speichern und Bearbeiten von Daten mithilfe der **DataSourceObject**-Schnittstelle verwendete XML-DOM zurück.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)-Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den Namen der **DataSourceObject**-Schnittstelle angibt.  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das zugeordnete Datenadapterobjekt zurück.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Übersicht über die Datenadapterschnittstellen

Die Schnittstellen für den Zugriff auf Datenadapter bieten unterschiedliche Eigenschaften und Methoden zum Abrufen und Übermitteln von Daten über Verbindungen zu externen Datenquellen; der Datenadapter, der einem dataSourceobject-Objekt zugeordnet ist, hängt vom Typ der externen Datenverbindung ab. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) InfoPath implementiert die folgenden Schnittstellen für den Zugriff auf Datenadapter. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx) -Schnittstelle  <br/> |Stellt eine Verbindung zu ADO/OLE DB-Datenquellen her; beschränkt auf Microsoft Access und Microsoft SQL Server™.  <br/> |
|[SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx) -Schnittstelle  <br/> |Stellt eine Verbindung mit einer SharePoint-Liste oder einer Dokumentbibliothek her.  <br/> |
|[WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) -Schnittstelle  <br/> |Stellt eine Verbindung zu XML-Webdiensten her.  <br/> |
|[XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx) -Objekt  <br/> |Stellt eine Verbindung zu einer XML-Datei her.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Verwenden der Schnittstellen "DataSourceObjects" und "DataSourceObject"

Der Zugriff auf die **DataSourceObjects** -Auflistung erfolgt über die DataObjects-Eigenschaft der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) Wenn Sie z. B. eine sekundäre Datenquelle namens "Personal" erstellen, die Daten aus der Tabelle "Personal" in der Microsoft Access-Datenbank "Nordwind" abruft, können Sie mithilfe der **DataSourceObjects**-Auflistung einen Verweis auf das **DataObject**-Objekt festlegen, das die abgefragten Daten darstellt. 
  
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

Der [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) Zugriff auf die dataadaptercollection-Schnittstelle erfolgt über die DataAdapters-Eigenschaft der **XDocument** -Schnittstelle. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) Wenn Sie beispielsweise eine sekundäre Datenquelle namens "Personal" erstellen, die Daten aus der Tabelle "Personal" in der Microsoft Access-Datenbank "Nordwind" abruft, können Sie mithilfe der **DataAdapterObjects**-Auflistung einen Verweis auf das **DataAdapterObject**-Objekt festlegen, das die Verbindung zur Datenbank darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft von **DataAdaptersCollection** übergeben, die in diesem Fall einen Verweis auf eine Instanz der **ADOAdapterObject**-Schnittstelle zurückgibt, die die Verbindung mit der Microsoft Access-Datenbank "Nordwind" darstellt. Dies funktioniert nur einwandfrei, wenn Sie das zurückgegebene Objekt explizit zu einer **ADOAdapterObject**-Schnittstelle umwandeln. Die [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) -Eigenschaft der **ADOAdapterObject** -Schnittstelle wird verwendet, um die ADO-Verbindungszeichenfolge in einem Meldungsfeld anzuzeigen. 
  
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


