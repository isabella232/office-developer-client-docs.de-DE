---
title: Zugriff auf externe Datenquellen
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- datenverbindungsklassen [Infopath 2007], sekundäre Datenquellen [InfoPath 2007], Daten [InfoPath 2007], sekundären, DataSource-Klasse [InfoPath 2007], zugreifen auf externe Datenquellen [InfoPath 2007], DataSourceCollection-Klasse [InfoPath 2007] DataConnectionCollection-Klasse [InfoPath 2007], DataConnection-Klasse [InfoPath 2007], InfoPath 2007, zugreifen auf externe Daten, Daten [InfoPath 2007], externen Quellen
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code zum Zugriff auf die sekundären Datenquellen des Formulars und bearbeiten die darin enthaltenen Daten schreiben.
ms.openlocfilehash: e26708e0033bbfe4110ac522dd1e0a0dd037c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790739"
---
# <a name="access-external-data-sources"></a>Zugriff auf externe Datenquellen

Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code zum Zugriff auf die sekundären Datenquellen des Formulars und bearbeiten die darin enthaltenen Daten schreiben. 
  
Jede sekundäre Datenquelle wird durch ein Objekt mit der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse instanziiert dargestellt und gespeicherten Daten, die von einer externen Quelle der Daten, wie etwa eine Datenbank oder einen Webdienst Abfrage abgerufen entspricht. Diese Datenquellen werden als sekundäre bezeichnet, da der Benutzer ein InfoPath-Formular speichert, der Benutzer die Daten nur in der main (oder primäre) Datenquelle, nicht die Daten in der sekundären Datenquellen gespeichert wird. Die Verbindung mit einer Datenquelle wird durch ein Objekt mit einer der Klassen "Data Connection" beispielsweise die [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) -Klasse, die stellt eine Datenverbindung mit einem XML-Webdienst instanziiert dargestellt. 
  
Das instanziierte [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt stellt die Speicherung der (aus einer Datenbank oder eine Webdienstabfrage) von einer Datenverbindung zurückgegebenen XML-Daten und die Klasse "Datenverbindung" stellt die Datenverbindung selbst (als definierte und benannten mithilfe der **Daten Verbindungen** Befehl auf der Registerkarte **Daten** ). 
  
Das InfoPath-Objektmodell unterstützt den Zugriff auf ein Formular sekundären Datenquellen mithilfe der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse im Zusammenhang mit der [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) -Klasse. 
  
Das InfoPath-Objektmodell stellt auch verschiedene Datenverbindungsklassen mit Informationen über die vom Formular verwendeten Datenverbindungen bereit.
  
> [!NOTE]
> In Microsoft InfoPath 2003 wird eine Datenverbindung als Datenadapter bezeichnet. 
  
Datenverbindungen werden zwei Arten: Abfrage Verbindungen werden verwendet, um die Daten abzurufen, die dann in eine sekundäre Datenquelle gespeichert ist. Senden von Verbindungen zum Senden von Daten, in eine Datenbank oder einen Webdienst, zum Beispiel verwendet werden. Die gesendeten Daten werden aus den Haupt- oder sekundären Datenquellen kopiert. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Übersicht über die DataSourceCollection-Klasse

Die [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) -Klasse bietet die folgenden Eigenschaften und Methoden, die Formularentwickler die [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) -Objektinstanzen verwalten, die das Formular enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **DataSource** -Objektinstanzen, die in der Auflistung enthalten sind.  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) -Methode  <br/> |Gibt ein **IEnumerator-Objekt** , das zum Durchlaufen der Auflistung verwendet werden kann.  <br/> |
|Elementeigenschaft [[Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Gibt einen Verweis auf das angegebene **DataSource** -Objekt anhand des Indexwertes zurück.  <br/> |
|Elementeigenschaft [[String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Gibt einen Verweis auf das angegebene **DataSource** -Objekt nach Namen zurück.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Übersicht über die DataSource-Klasse

Die [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einer sekundären InfoPath-Datenquelle verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode  <br/> |Gibt ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt für den Zugriff und zum Bearbeiten der Datenquelle  <br/> |
|[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das zugeordnete Datenverbindungsobjekt ab.   <br/> Zum Ausführen der Abfrage für die Datenverbindung und Einfügen der zurückgegebenen Daten als XML in den XML-Knoten mit das **DataSource** -Objekt verknüpft ist, verwenden Sie die [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) -Methode des Connection-Objekts zugehörigen Daten.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)-Eigenschaft  <br/> |Ruft den Namen des **DataSource** -Objekts ab.  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob sich die Datenquelle im Schreibschutzmodus befindet.  <br/> |
|[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) -Methode  <br/> |Ruft den Wert einer benannten Eigenschaft für den angegebenen XML-Knoten, der einem **Nonattribute** -Knoten in der Hauptdatenquelle handeln muss.  <br/> |
|[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) -Methode  <br/> |Legt den Wert einer benannten Eigenschaft für den angegebenen XML-Knoten, der einem **Nonattribute** -Knoten in der Hauptdatenquelle handeln muss.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Übersicht über die Datenverbindungsklassen

Die Klassen für den Zugriff auf datenverbindungen bieten verschiedene Eigenschaften und Methoden, die empfangen und Versenden von Daten über Verbindungen mit externen Datenquellen; die Datenverbindung, die ein **DataSource** -Objekt zugeordnet ist ist abhängig von der Art der Verbindung mit externen Daten. InfoPath implementiert die folgenden Klassen für den Zugriff auf datenverbindungen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage einer ADO/OLE DB-Datenquelle aus; beschränkt auf Microsoft Access und Microsoft SQL Server.  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) -Klasse  <br/> |Sendet an eine ADO/OLE DB-Datenquelle; beschränkt auf Microsoft Access und Microsoft SQL Server.  <br/> |
|[SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage einer SharePoint-Liste oder einer Dokumentbibliothek aus.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Sendet an eine SharePoint-Liste oder Dokumentbibliothek.  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) -Klasse  <br/> |Stellt eine Verbindung zu einem XML-Webdienst her.  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage einer XML-Datei aus.  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) -Klasse  <br/> |Sendet an eine XML-Datei.  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) -Klasse  <br/> |Sendet ein Formular als Anlage einer e-Mail an.  <br/> |
|[BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx) -Klasse  <br/> |Führt eine Abfrage eine externe Liste auf einem Server mit SharePoint Foundation 2010 oder SharePoint Server 2010.  <br/> |
|[BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx) -Klasse  <br/> |Sendet an eine externe Liste auf einem Server mit SharePoint Foundation 2010 oder SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Verwenden der DataSourceCollection- und der DataSource-Klasse

Das **DataSourceCollection** -Objekt, das die Auflistung der Datenquellen, die einer Formularvorlage zugeordneten darstellt, wird über die [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zugegriffen. Angenommen, wenn Sie eine sekundäre Datenquelle mit der Bezeichnung Employees, die Daten aus der Employees-Tabelle in der Nordwind-Datenbank abruft erstellen, können das **DataSourceCollection** -Objekt einen Verweis auf ein **DataSource** -Objekt festgelegt, darstellt der abgerufenen Daten. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle der Accessor-Eigenschaft der **DataSourceCollection** -Klasse, übergeben, die einen Verweis auf das **DataSource** -Objekt zurückgibt, die abgerufenen Daten der Employees-Tabelle darstellt. Der XML-Knoten, in dem die abgerufenen Daten aus der sekundären Datenquelle gespeichert wird in einem Meldungsfeld mit, dass die **CreateNavigator** -Methode der **DataSource** -Klasse die **InnerXml** -Eigenschaft der **XPathNavigator** -Klasse zugreifen angezeigt. 
  
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

Um die Daten zu bearbeiten, die in eine sekundäre Datenquelle enthalten ist, verwenden Sie die **CreateNavigator** -Methode der **DataSource** -Klasse zum Zurückgeben eines Verweises auf ein **XPathNavigator** -Objekt am Knoten, in die sekundären Daten gespeichert ist. Sie können die Eigenschaften oder Methoden der **XPathNavigator** -Klasse zum Bearbeiten der Daten verwenden. Weitere Informationen finden Sie unter [Arbeiten mit dem XPathNavigator und XPathNodeIterator-Klassen](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Verwenden der DataConnectionCollection- und der DataConnection-Klasse

Das [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) -Objekt, das die Auflistung von datenverbindungen einer Formularvorlage zugeordneten darstellt, wird über die [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) -Eigenschaft der **XmlForm** -Klasse zugegriffen. Angenommen, wenn Sie eine sekundäre Datenquelle mit der Bezeichnung Employees, die Daten aus der Employees-Tabelle in der Nordwind-Datenbank abruft erstellen, können das der Formularvorlage zugeordnete **DataConnectionCollection** -Objekt Sie einen Verweis auf die **festgelegt DataConnection** , der die Verbindung mit der Datenbank darstellt. 
  
Im folgenden Codebeispiel wird der Name der sekundären Datenquelle an die Accessoreigenschaft der **DataConnectionCollection** -Klasse, die in diesem Fall einen Verweis auf das **ADOQueryConnection** -Objekt zurückgibt, das darstellt übergeben der Verbindung mit der Nordwind-Datenbank. Für diese ordnungsgemäß funktioniert müssen Sie explizit das Objekt zurückgegeben wird, in der **ADOQueryConnection** -Typ umwandeln. Die [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) -Eigenschaft der **ADOAdapterObject** -Schnittstelle wird verwendet, um die ADO-Verbindungszeichenfolge in einem Meldungsfeld anzuzeigen. 
  
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



[Erstellen von InfoPath-Formularvorlagen, die Arbeit mit InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

