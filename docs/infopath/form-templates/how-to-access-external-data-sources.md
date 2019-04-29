---
title: Zugriff auf externe Datenquellen
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- Datenverbindungsklassen [InfoPath 2007], sekundäre Datenquellen [InfoPath 2007], Daten [InfoPath 2007], sekundäre, DataSource-Klasse [InfoPath 2007], Zugriff auf externe Datenquellen [InfoPath 2007], dataSourcecollection-Klasse [InfoPath 2007], DataConnectioncollection-Klasse [InfoPath 2007], DataConnection-Klasse [InfoPath 2007], InfoPath 2007, Zugriff auf externe Daten, Daten [InfoPath 2007], externe Quellen
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Sie können bei der Arbeit mit einer InfoPath-Formularvorlage Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die enthaltenen Daten zu bearbeiten.
ms.openlocfilehash: f6957c561231eef0e3e4df6deb09ae89f85afcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408313"
---
# <a name="access-external-data-sources"></a>Zugriff auf externe Datenquellen

Sie können bei der Arbeit mit einer InfoPath-Formularvorlage Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die enthaltenen Daten zu bearbeiten. 
  
Jede sekundäre Datenquelle wird durch ein Objekt dargestellt, das mithilfe der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse instanziiert wird, und entspricht gespeicherten Daten, die von einer externen Datenquelle wie einer Datenbank oder einer Webdienstabfrage abgerufen werden. Diese Datenquellen werden als sekundär bezeichnet, da der Benutzer beim Speichern eines InfoPath-Formulars die Daten nur in der Hauptdatenquelle (der primären Datenquelle) und nicht in den sekundären Datenquellen speichert. Die Verbindung zu einer Datenquelle wird durch ein Objekt dargestellt, das mit einer der Datenverbindungsklassen instanziiert wird, wie beispielsweise der [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) -Klasse, die eine Datenverbindung mit einem XML-Webdienst darstellt. 
  
Das instanziierte [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt stellt die Speicherung von XML-Daten dar, die von einer Datenverbindung (aus einer Datenbank-oder Webdienstabfrage) zurückgegeben werden, und die "Data Connection"-Klasse stellt die Datenverbindung selbst (wie definiert und benannt mithilfe der **Daten Connections** -Befehl auf der Registerkarte **Daten** ). 
  
Das InfoPath-Objektmodell unterstützt den Zugriff auf die sekundären Datenquellen eines Formulars mithilfe der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse in Verbindung mit der DataSourceCollection-Klasse. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) 
  
Das InfoPath-Objektmodell stellt auch verschiedene Datenverbindungsklassen mit Informationen über die vom Formular verwendeten Datenverbindungen bereit.
  
> [!NOTE]
> In Microsoft InfoPath 2003 wird eine Datenverbindung als Datenadapter bezeichnet.  
  
Es gibt zwei verschiedene Arten von Datenverbindungen: Abfrageverbindungen werden zum Abrufen der Daten verwendet, die dann in einer sekundären Datenquelle gespeichert werden. Sendeverbindungen werden zum Senden von Daten an beispielsweise eine Datenbank oder einen Webdienst verwendet. Die gesendeten Daten werden aus den Hauptdatenquellen oder den sekundären Datenquellen kopiert. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Übersicht über die DataSourceCollection-Klasse

Die [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) DataSourceCollection-Klasse stellt die folgenden Eigenschaften und Methoden bereit, die Formularentwickler zum Verwalten der [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) DataSourceCollection-Objektinstanzen verwenden können, die das Formular enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **DataSource**-Objektinstanzen zurück, die in der Auflistung enthalten sind.  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) -Methode  <br/> |Gibt ein **IEnumerator**-Objekt zurück, das für die Iteration durch die Auflistung verwendet werden kann.  <br/> |
|[Item [Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **DataSource**-Objekt nach Indexwert zurück.  <br/> |
|[Item [String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **DataSource**-Objekt nach Namen zurück.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Übersicht über die DataSource-Klasse

Die [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) DataSourceCollection-Klasse stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer sekundären InfoPath-Datenquelle verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode  <br/> |Gibt ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt für den Zugriff auf und die Bearbeitung der Datenquelle zurück.  <br/> |
|[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das zugeordnete Datenverbindungsobjekt ab.  <br/> Verwenden Sie die [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) -Methode des zugeordneten Datenverbindungsobjekts, um die Abfrage für die Datenverbindung auszuführen und die zurückgegebenen Daten als XML in den XML-Knoten einzufügen, der dem **DataSource** -Objekt zugeordnet ist.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)-Eigenschaft  <br/> |Ruft den Namen des **DataSource**-Objekts ab.  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob sich die Datenquelle im Schreibschutzmodus befindet.  <br/> |
|[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) -Methode  <br/> |Ruft den Wert einer benannten Eigenschaft für den angegebenen XML-Knoten ab, bei dem es sich um einen **nonattribute** (nicht attributierten) Knoten in der Hauptdatenquelle handeln muss.  <br/> |
|[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) -Methode  <br/> |Legt den Wert einer benannten Eigenschaft für den angegebenen XML-Knoten fest, bei dem es sich um einen **nonattribute**-Knoten in der Hauptdatenquelle handeln muss.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Übersicht über die Datenverbindungsklassen

Die Klassen für den Zugriff auf Datenverbindungen stellen unterschiedliche Eigenschaften und Methoden bereit, die Daten über Verbindungen zu externen Datenquellen abrufen und an diese senden; die Datenverbindung, die einem **DataSource**-Objekt zugeordnet ist, hängt vom Typ der externen Datenverbindung ab. InfoPath implementiert die folgenden Klassen für den Zugriff auf Datenverbindungen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage einer ADO/OLE DB-Datenquelle aus; beschränkt auf Microsoft Access und Microsoft SQL Server.  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) -Klasse  <br/> |Sendet an eine ADO/OLE DB-Datenquelle; beschränkt auf Microsoft Access und Microsoft SQL Server.  <br/> |
|[SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage einer SharePoint-Liste oder einer Dokumentbibliothek aus.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Sendet an eine SharePoint-Liste oder Dokumentbibliothek.  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) -Klasse  <br/> |Stellt eine Verbindung zu einem XML-Webdienst her.  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage einer XML-Datei aus.  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) -Klasse  <br/> |Sendet an eine XML-Datei.  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) -Klasse  <br/> |Sendet ein Formular als Anlage in einer e-Mail.  <br/> |
|[BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx) -Klasse  <br/> |Fragt eine externe Liste auf einem Server mit SharePoint Foundation 2010 oder SharePoint Server 2010 ab.  <br/> |
|[BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx) -Klasse  <br/> |Sendet an eine externe Liste auf einem Server mit SharePoint Foundation 2010 oder SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Verwenden der DataSourceCollection- und der DataSource-Klasse

Der **** Zugriff auf das DataSourceCollection-Objekt, das die Auflistung der einer Formularvorlage zugeordneten Datenquellen darstellt, erfolgt über die DataSources-Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) Wenn Sie beispielsweise eine sekundäre Datenquelle mit Namen Mitarbeiter erstellen, die Daten aus der Tabelle Mitarbeiter in der Nordwind-Datenbank abruft, können Sie das **DataSourceCollection**-Objekt zum Festlegen eines Verweises auf ein **DataSource**-Objekt verwenden, das die abgerufenen Daten darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessor-Eigenschaft der dataSourcecollection **** -Klasse übergeben, die einen Verweis auf das **DataSource** -Objekt zurückgibt, das die abgerufenen Employees-Tabellendaten darstellt. Der XML-Knoten, der die abgerufenen Daten der sekundären Datenquelle speichert, wird in einem Meldungsfeld mithilfe der **CreateNavigator**-Methode der **DataSource**-Klasse dargestellt, um auf die **InnerXml**-Eigenschaft der **XPathNavigator**-Klasse zuzugreifen. 
  
```cs
// Instantiate a variable to access the specified data source
// from the DataSourceCollection of the form.
DataSource myDataSource = 
   this.DataSources["Employees"];
// Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " +
   myDataSource.CreateNavigator().InnerXml.ToString());
```

```vb
' Instantiate a variable to access the specified data source
' from the DataSourceCollection of the form.
Dim myDataSource As DataSource = _
   Me.DataSources("Employees")
' Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " &amp; _
   myDataSource.CreateNavigator().InnerXml.ToString())
```

Verwenden Sie zum Bearbeiten der in einer sekundären Datenquelle enthaltenen Daten die **CreateNavigator**-Methode der **DataSource**-Klasse, um einen Verweis auf ein **XPathNavigator**-Objekt zurückzugeben, das an dem Knoten positioniert ist, an dem die sekundären Daten gespeichert sind. Sie können zum Bearbeiten der Daten die Eigenschaften oder Methoden der **XPathNavigator**-Klasse verwenden. Weitere Informationen finden Sie unter [Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Verwenden der DataConnectionCollection- und der DataConnection-Klasse

Der [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) Zugriff auf das DataConnectionCollection-Objekt, das die Auflistung der einer Formularvorlage zugeordneten Datenverbindungen darstellt, erfolgt über die DataConnections-Eigenschaft der **XmlForm** -Klasse. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) Wenn Sie beispielsweise eine sekundäre Datenquelle mit NamenMitarbeiter erstellen, die Daten aus der Tabelle Mitarbeiter in der Nordwind-Datenbank abruft, können Sie das der Formularvorlage zugeordnete **DataConnectionCollection**-Objekt verwenden, um einen Verweis auf die **DataConnection** festzulegen, die die Verbindung zur Datenbank darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft der **DataConnectionCollection**-Klasse übergeben, die in diesem Fall einen Verweis auf das **ADOQueryConnection**-Objekt zurückgibt, das die Verbindung mit der Nordwind-Datenbank darstellt. Dies funktioniert nur einwandfrei, wenn Sie das zurückgegebene Objekt explizit in den **ADOQueryConnection**-Typ umwandeln. Die [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) -Eigenschaft der **ADOAdapterObject** -Schnittstelle wird verwendet, um die ADO-Verbindungszeichenfolge in einem Meldungsfeld anzuzeigen. 
  
```cs
// Instantiate a variable to access the specified data connection
// from the DataConnectionCollection of the form. 
// You must cast to the specific data connection type
// (ADOQueryConnection) before you can access the data connection.
ADOQueryConnection myADOConnection = 
   (ADOQueryConnection)this.DataConnections["Employees"];
// Display the connection information for the data connection.
MessageBox.Show("Connection string: " + myADOConnection.Connection);
```

```vb
' Instantiate a variable to access the specified data connection
' from the DataConnectionCollection of the form. 
' You must cast to the specific data connection type
' (ADOQueryConnection) before you can access the data connection.
Dim myADOConnection As ADOQueryConnection = _
   DirectCast(Me.DataConnections("Employees"), ADOQueryConnection)
' Display the connection information for the data connection.
MessageBox.Show("Connection string: " &amp; myADOConnection.Connection)
```

## <a name="see-also"></a>Siehe auch



[Erstellen von InfoPath-Formularvorlagen, die mit InfoPath Forms Services verwendet werden](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

