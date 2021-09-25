---
title: Behandeln von Fehlern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- errors [infopath 2007], handling,FormErrorCollection [InfoPath 2007],InfoPath 2007, error handling,FormError [InfoPath 2007],error handling [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das von Microsoft bereitgestellte InfoPath-Objektmodell. Office. Der InfoPath-Namespace unterstützt die Fehlerbehandlung durch die Verwendung der FormError-Klasse in Verbindung mit der FormErrorCollection-Klasse.
ms.openlocfilehash: 7697a2a40be1f2dda76a6a9f1f218192acad9453
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557470"
---
# <a name="handle-errors"></a>Behandeln von Fehlern

Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das von Microsoft.Office bereitgestellte InfoPath-Objektmodell. [ Der InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) unterstützt die Fehlerbehandlung durch die Verwendung der [FormError-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) in Verbindung mit der [FormErrorCollection-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) 
  
Fehler in InfoPath können aus den folgenden Gründen auftreten:
  
- Wenn Daten, die in ein Formular eingegeben werden, bei der XML-Schemavalidierung Fehler aufweisen.
    
- Wenn eine benutzerdefinierte Validierungseinschränkung Fehler aufweist.
    
- Wenn ein Fehler von der [ReportError-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) des [XmlValidatingEventArgs-Ereignisobjekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) generiert wird. 
    
- Wenn ein benutzerdefinierter Fehler mithilfe der [Add-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) der [FormErrorCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) erstellt wird. 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Übersicht über die FormErrorCollection-Klasse

Die [FormErrorCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) stellt die folgenden Methoden und Eigenschaften bereit, mit denen Formularentwickler die [FormError-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) verwalten können, die die Auflistung enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) (+3 Überladungen)  <br/> |Erstellt ein **FormError**-Objekt und fügt es der Auflistung hinzu.  <br/> |
|[Delete-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) (+1 Überladung)  <br/> |Löscht den angegebenen benutzerdefinierten Fehler aus der Auflistung.  <br/> |
|[DeleteAll-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx)  <br/> |Löscht alle **FormError**-Objekte, die in der Auflistung enthalten sind.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+1 Überladung)  <br/> |Gibt alle **FormError**-Objekte mit dem angegebenen Namen oder Typ aus der Auflistung zurück.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **FormError**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf ein **FormError**-Objekt basierend auf der angegebenen Indexnummer ab.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Übersicht über die FormError-Klasse

Die [FormError-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) stellt die folgenden Eigenschaften bereit, mit denen Formularentwickler auf Informationen zu dem ausgelösten Fehler zugreifen können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DetailedMessage-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx)  <br/> |Ruft die ausführliche Fehlermeldung des **FormError**-Objekts ab oder legt sie fest.  <br/> |
|[ErrorCode-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx)  <br/> |Ruft den Fehlercode des **FormError**-Objekts ab oder legt ihn fest.  <br/> |
|[Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Ruft ein **XPathNavigator**-Objekt ab, das am Knoten positioniert ist, der dem **FormError**-Objekt zugeordnet ist.  <br/> |
|[Message-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx)  <br/> |Ruft die kurze Fehlermeldung des **FormError**-Objekts ab oder legt sie fest.  <br/> |
|[FormErrorType-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx)  <br/> |Ruft den Typ des **FormError**-Objekts ab.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Verwenden der Klassen "FormErrorCollection" und "FormError"

Der Zugriff auf das einem Formular zugeordnete **FormErrorCollection-Objekt** erfolgt über die [Errors-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) des [XmlForm-Objekts.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Das **FormErrorCollection-Objekt** ist dem einem Formular zugrunde liegenden XML-Dokument zugeordnet, sodass beim Auftreten eines Fehlers auf dieses und alle zusätzlichen Fehler im aktuellen XML-Dokument zugegriffen und verwaltet werden kann. Im folgenden Beispiel wird veranschaulicht, wie eine Schleife verwendet werden kann, um die Fehler zu überprüfen, die möglicherweise im einem Formular zugrunde liegenden XML-Dokument vorhanden sind. Wenn Fehler auftreten, durchläuft die Funktion die einzelnen Fehler und zeigt dem Benutzer mithilfe der **Message-Eigenschaft** des **FormError-Objekts** ein Meldungsfeld an. 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

Die vorangegangene Funktion kann von einem der Datenüberprüfungs-Ereignishandler des Formulars aufgerufen werden. Wenn beispielsweise im Ereignishandler für das [Changed-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) eines Felds im Formular verwendet wird, würde der Aufruf der Funktion das XML-Knotenargument mithilfe der [Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) des [XmlEventArgs-Ereignisobjekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) wie folgt übergeben. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Zusätzlich zur Behandlung von Fehlern, die von InfoPath generiert werden, können Formularentwickler auch benutzerdefinierte Fehler mithilfe der [ReportError(XPathNavigator, Boolean, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) des [XmlValidatingEventArgs-Ereignisobjekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) oder mithilfe der [Add-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) der [FormErrorCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) generieren. Wenn Sie Informationen zur Verwendung der Methoden [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) oder [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) erhalten möchten, klicken Sie am Anfang dieses Themas auf die Links für diese Methoden. 
  
## <a name="handling-managed-code-exceptions"></a>Behandlung von Ausnahmen im verwalteten Code

Sie können die try-catch-Ausnahmebehandlung zum Behandeln von Ausnahmen verwenden, die in Formularvorlagen mit verwaltetem Code ausgelöst wurden. Dies wird im folgenden Codebeispiel gezeigt.
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

Wenn Sie im Formularcode keine try-catch-Ausnahmebehandlung verwenden, zeigt InfoPath beim Debuggen und Anzeigen der Vorschau Informationen zu unbehandelten Ausnahmen im Dialogfeld für InfoPath-Fehler an. Außerdem werden unbehandelte Ausnahmen im Dialogfeld für InfoPath-Fehler zur Laufzeit standardmäßig nicht angezeigt, wenn Sie die Formularvorlage mit verwaltetem Code bereitstellen. Verwenden Sie das folgende Verfahren, um Informationen zu unbehandelten Ausnahmen zur Laufzeit anzuzeigen.
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Aktivieren von Benachrichtigungen zu unbehandelten Ausnahmen im verwalteten Code zur Laufzeit

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf die Registerkarte **"Datei".** 
    
2. Klicken Sie auf **Optionen**, und klicken Sie dann in der Kategorie **Allgemein** auf **InfoPath-Optionen**. 
    
3. Aktivieren Sie auf der Registerkarte **Erweitert** das Kontrollkästchen **Benachrichtigung für Fehler in Visual Basic- oder C#-Code anzeigen**. 
    

