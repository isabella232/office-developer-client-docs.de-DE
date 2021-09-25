---
title: Zugreifen auf externe Datenquellen
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- Data Connection Classes [infopath 2007],secondary data sources [InfoPath 2007],data [InfoPath 2007], secondary,DataSource class [InfoPath 2007],accessing external data sources [InfoPath 2007],DataSourceCollection-Klasse [InfoPath 2007],DataConnectionCollection-Klasse [InfoPath 2007],DataConnection-Klasse [InfoPath 2007],InfoPath 2007, zugreifen auf externe Daten,data [InfoPath 2007], externe Quellen
ms.localizationpriority: medium
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Sie können bei der Arbeit mit einer InfoPath-Formularvorlage Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die enthaltenen Daten zu bearbeiten.
ms.openlocfilehash: 2119564d31766e318434324fc553394c73d82f83
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564638"
---
# <a name="access-external-data-sources"></a>Zugreifen auf externe Datenquellen

Sie können bei der Arbeit mit einer InfoPath-Formularvorlage Code schreiben, um auf die sekundären Datenquellen des Formulars zuzugreifen und die enthaltenen Daten zu bearbeiten. 
  
Jede sekundäre Datenquelle wird durch ein Mithilfe der [DataSource-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) instanziiertes Objekt dargestellt und entspricht gespeicherten Daten, die aus einer externen Datenquelle wie einer Datenbank oder einer Webdienstabfrage abgerufen werden. Diese Datenquellen werden als sekundär bezeichnet, da der Benutzer beim Speichern eines InfoPath-Formulars die Daten nur in der Hauptdatenquelle (der primären Datenquelle) und nicht in den sekundären Datenquellen speichert. Die Verbindung mit einer Datenquelle wird durch ein Objekt dargestellt, das mithilfe einer der Datenverbindungsklassen instanziiert wird, z. B. der [WebServiceConnection-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) die eine Datenverbindung mit einem XML-Webdienst darstellt. 
  
Das instanziierte [DataSource-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) stellt die Speicherung von XML-Daten dar, die von einer Datenverbindung zurückgegeben werden (aus einer Datenbank- oder Webdienstabfrage), und die Datenverbindungsklasse stellt die Datenverbindung selbst dar (wie mithilfe des **Befehls "Datenverbindungen"** auf der Registerkarte **"Daten"** definiert und benannt). 
  
Das InfoPath-Objektmodell unterstützt den Zugriff auf die sekundären Datenquellen eines Formulars durch die Verwendung der [DataSource-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) in Verbindung mit der [DataSourceCollection-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) 
  
Das InfoPath-Objektmodell stellt auch verschiedene Datenverbindungsklassen mit Informationen über die vom Formular verwendeten Datenverbindungen bereit.
  
> [!NOTE]
> In Microsoft InfoPath 2003 wird eine Datenverbindung als Datenadapter bezeichnet.  
  
Es gibt zwei verschiedene Arten von Datenverbindungen: Abfrageverbindungen werden zum Abrufen der Daten verwendet, die dann in einer sekundären Datenquelle gespeichert werden. Sendeverbindungen werden zum Senden von Daten an beispielsweise eine Datenbank oder einen Webdienst verwendet. Die gesendeten Daten werden aus den Hauptdatenquellen oder den sekundären Datenquellen kopiert. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Übersicht über die DataSourceCollection-Klasse

Die [DataSourceCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) stellt die folgenden Eigenschaften und Methoden bereit, die Formularentwickler zum Verwalten der [DataSourceCollection-Objektinstanzen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) verwenden können, die das Formular enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **DataSource**-Objektinstanzen zurück, die in der Auflistung enthalten sind.  <br/> |
|[GetEnumerator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Gibt ein **IEnumerator**-Objekt zurück, das für die Iteration durch die Auflistung verwendet werden kann.  <br/> |
|[Item[Int32]-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Gibt einen Verweis auf das angegebene **DataSource**-Objekt nach Indexwert zurück.  <br/> |
|[Item[String]-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Gibt einen Verweis auf das angegebene **DataSource**-Objekt nach Namen zurück.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Übersicht über die DataSource-Klasse

Die [DataSourceCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) stellt die folgende Methode und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer sekundären InfoPath-Datenquelle verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Gibt ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt zum Zugreifen und Bearbeiten der Datenquelle zurück.  <br/> |
|[QueryConnection-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Ruft einen Verweis auf das zugeordnete Datenverbindungsobjekt ab.  <br/> Verwenden Sie die [Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) des zugeordneten Datenverbindungsobjekts, um die Abfrage für die Datenverbindung auszuführen und die zurückgegebenen Daten als XML in den XML-Knoten einzufügen, der dem **DataSource-Objekt** zugeordnet ist.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)-Eigenschaft  <br/> |Ruft den Namen des **DataSource**-Objekts ab.  <br/> |
|[ReadOnly-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob sich die Datenquelle im Schreibschutzmodus befindet.  <br/> |
|[GetNamedNodeProperty-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Ruft den Wert einer benannten Eigenschaft für den angegebenen XML-Knoten ab, bei dem es sich um einen **nonattribute** (nicht attributierten) Knoten in der Hauptdatenquelle handeln muss.  <br/> |
|[SetNamedNodeProperty-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Legt den Wert einer benannten Eigenschaft für den angegebenen XML-Knoten fest, bei dem es sich um einen **nonattribute**-Knoten in der Hauptdatenquelle handeln muss.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Übersicht über die Datenverbindungsklassen

Die Klassen für den Zugriff auf Datenverbindungen stellen unterschiedliche Eigenschaften und Methoden bereit, die Daten über Verbindungen zu externen Datenquellen abrufen und an diese senden; die Datenverbindung, die einem **DataSource**-Objekt zugeordnet ist, hängt vom Typ der externen Datenverbindung ab. InfoPath implementiert die folgenden Klassen für den Zugriff auf Datenverbindungen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[AdoQueryConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Führt eine Abfrage einer ADO/OLE DB-Datenquelle aus; beschränkt auf Microsoft Access und Microsoft SQL Server.  <br/> |
|[AdoSubmitConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Sendet an eine ADO/OLE DB-Datenquelle; beschränkt auf Microsoft Access und Microsoft SQL Server.  <br/> |
|[SharePointListRWQueryConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Führt eine Abfrage einer SharePoint-Liste oder einer Dokumentbibliothek aus.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Sendet an eine SharePoint-Liste oder Dokumentbibliothek.  <br/> |
|[WebServiceConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Stellt eine Verbindung zu einem XML-Webdienst her.  <br/> |
|[FileQueryConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Führt eine Abfrage einer XML-Datei aus.  <br/> |
|[FileSubmitConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Sendet an eine XML-Datei.  <br/> |
|[EmailSubmitConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Sendet ein Formular als Anlage in einer E-Mail.  <br/> |
|[BdcQueryConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Fragt eine externe Liste auf einem Server ab, auf dem SharePoint Foundation 2010 oder SharePoint Server 2010 ausgeführt wird.  <br/> |
|[BdcSubmitConnection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Sendet an eine externe Liste auf einem Server, auf dem SharePoint Foundation 2010 oder SharePoint Server 2010 ausgeführt wird.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Verwenden der DataSourceCollection- und der DataSource-Klasse

Auf das **DataSourceCollection-Objekt,** das die Auflistung von Datenquellen darstellt, die einer Formularvorlage zugeordnet sind, wird über die [DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zugegriffen. Wenn Sie beispielsweise eine sekundäre Datenquelle mit Namen Mitarbeiter erstellen, die Daten aus der Tabelle Mitarbeiter in der Nordwind-Datenbank abruft, können Sie das **DataSourceCollection**-Objekt zum Festlegen eines Verweises auf ein **DataSource**-Objekt verwenden, das die abgerufenen Daten darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft der **DataSourceCollection-Klasse** übergeben, die einen Verweis auf das **DataSource** -Objekt zurückgibt, das die abgerufenen Employees-Tabellendaten darstellt. Der XML-Knoten, der die abgerufenen Daten der sekundären Datenquelle speichert, wird in einem Meldungsfeld mithilfe der **CreateNavigator**-Methode der **DataSource**-Klasse dargestellt, um auf die **InnerXml**-Eigenschaft der **XPathNavigator**-Klasse zuzugreifen. 
  
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

Verwenden Sie zum Bearbeiten der in einer sekundären Datenquelle enthaltenen Daten die **CreateNavigator**-Methode der **DataSource**-Klasse, um einen Verweis auf ein **XPathNavigator**-Objekt zurückzugeben, das an dem Knoten positioniert ist, an dem die sekundären Daten gespeichert sind. Sie können zum Bearbeiten der Daten die Eigenschaften oder Methoden der **XPathNavigator**-Klasse verwenden. Weitere Informationen finden Sie unter [Arbeiten mit den Klassen XPathNavigator und XPathNodeIterator.](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Verwenden der DataConnectionCollection- und der DataConnection-Klasse

Auf das [DataConnectionCollection-Objekt,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) das die Auflistung von Datenverbindungen darstellt, die einer Formularvorlage zugeordnet sind, wird über die [DataConnections-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) der **XmlForm-Klasse** zugegriffen. Wenn Sie beispielsweise eine sekundäre Datenquelle mit NamenMitarbeiter erstellen, die Daten aus der Tabelle Mitarbeiter in der Nordwind-Datenbank abruft, können Sie das der Formularvorlage zugeordnete **DataConnectionCollection**-Objekt verwenden, um einen Verweis auf die **DataConnection** festzulegen, die die Verbindung zur Datenbank darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft der **DataConnectionCollection**-Klasse übergeben, die in diesem Fall einen Verweis auf das **ADOQueryConnection**-Objekt zurückgibt, das die Verbindung mit der Nordwind-Datenbank darstellt. Dies funktioniert nur einwandfrei, wenn Sie das zurückgegebene Objekt explizit in den **ADOQueryConnection**-Typ umwandeln. Die [Connection-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) der **ADOAdapterObject-Schnittstelle** wird verwendet, um die ADO-Verbindungszeichenfolge in einem Meldungsfeld anzuzeigen. 
  
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



[Erstellen von InfoPath-Formularvorlagen, die mit InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

