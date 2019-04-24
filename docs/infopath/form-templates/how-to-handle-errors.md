---
title: Behandeln von Fehlern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Fehler [InfoPath 2007], Handling, FormErrorCollection [InfoPath 2007], InfoPath 2007, Fehlerbehandlung, FormError [InfoPath 2007], Fehlerbehandlung [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das vom Microsoft. Office. InfoPath-Namespace bereitgestellte InfoPath-Objektmodell unterstützt die Fehlerbehandlung durch die Verwendung der FormError-Klasse in Verbindung mit der FormErrorCollection-Klasse.
ms.openlocfilehash: 30cf649188b7e4cbc35469d2a50540bb13ecb38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303605"
---
# <a name="handle-errors"></a>Behandeln von Fehlern

Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte InfoPath-Objektmodell unterstützt die Fehlerbehandlung durch die Verwendung der FormError-Klasse in Verbindung mit der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) 
  
Fehler in InfoPath können aus den folgenden Gründen auftreten:
  
- Wenn Daten, die in ein Formular eingegeben werden, bei der XML-Schemavalidierung Fehler aufweisen.
    
- Wenn eine benutzerdefinierte Validierungseinschränkung Fehler aufweist.
    
- Wenn durch die [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methode des [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) -Ereignisobjekts ein Fehler generiert wird. 
    
- Wenn ein benutzerdefinierter Fehler mithilfe der [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methode der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse erstellt wird. 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Übersicht über die FormErrorCollection-Klasse

Die [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler zum Verwalten der [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Objekte verwenden können, die in der Auflistung enthalten sind. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methode (+ 3 Überladungen)  <br/> |Erstellt ein **FormError**-Objekt und fügt es der Auflistung hinzu.  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) -Methode (+ 1-Überladung)  <br/> |Löscht den angegebenen benutzerdefinierten Fehler aus der Auflistung.  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) -Methode  <br/> |Löscht alle **FormError**-Objekte, die in der Auflistung enthalten sind.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+ 1 Überladung)  <br/> |Gibt alle **FormError**-Objekte mit dem angegebenen Namen oder Typ aus der Auflistung zurück.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **FormError**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf ein **FormError**-Objekt basierend auf der angegebenen Indexnummer ab.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Übersicht über die FormError-Klasse

Die [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Klasse stellt die folgenden Eigenschaften bereit, mit denen Formularentwickler auf Informationen zu dem ausgelösten Fehler zugreifen können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) -Eigenschaft  <br/> |Ruft die ausführliche Fehlermeldung des **FormError**-Objekts ab oder legt sie fest.  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) -Eigenschaft  <br/> |Ruft den Fehlercode des **FormError**-Objekts ab oder legt ihn fest.  <br/> |
|[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) -Eigenschaft  <br/> |Ruft ein **XPathNavigator**-Objekt ab, das am Knoten positioniert ist, der dem **FormError**-Objekt zugeordnet ist.  <br/> |
|[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) -Eigenschaft  <br/> |Ruft die kurze Fehlermeldung des **FormError**-Objekts ab oder legt sie fest.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) FormErrorType-Eigenschaft  <br/> |Ruft den Typ des **FormError**-Objekts ab.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Verwenden der Klassen "FormErrorCollection" und "FormError"

Der Zugriff auf das **FormErrorCollection** -Objekt, das einem Formular zugeordnet ist, erfolgt über die [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) -Eigenschaft des [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Objekts. Das **FORMERRORCOLLECTION** -Objekt ist dem einem Formular zugrunde liegenden XML-Dokument zugeordnet, sodass beim Auftreten eines Fehlers der Zugriff auf und alle zusätzlichen Fehler innerhalb des aktuellen XML-Dokuments möglich ist. Das folgende Beispiel veranschaulicht, wie eine Schleife verwendet werden kann, um die Fehler zu überprüfen, die im einem Formular zugrunde liegenden XML-Dokument möglicherweise vorhanden sind. Wenn Fehler vorhanden sind, durchläuft die Funktion die einzelnen Objekte, und der Benutzer wird mithilfe der **Message** -Eigenschaft des FormError-Objekts ein Meldungsfeld angezeigt. **** 
  
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

Die vorangegangene Funktion kann von einem der Datenüberprüfungs-Ereignishandler des Formulars aufgerufen werden. Wenn Sie beispielsweise im Ereignishandler für das [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) -Ereignis eines Felds im Formular verwendet wird, würde der Aufruf der Funktion das XML-Knoten Argument mithilfe der [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) -Eigenschaft des XmlEventArgs [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) -Ereignisobjekts wie folgt übergeben. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Neben Fehlern, die von InfoPath generiert werden, können Formularentwickler auch benutzerdefinierte Fehler mithilfe der [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methode des [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) -Ereignisobjekts oder mithilfe des [Add ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)Methode der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse. Weitere Informationen zur Verwendung der [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -oder [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methoden finden Sie in den Links für diese Methoden am Anfang dieses Themas. 
  
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

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf die Registerkarte **Datei** . 
    
2. Klicken Sie auf **Optionen**, und klicken Sie dann in der Kategorie **Allgemein** auf **InfoPath-Optionen**. 
    
3. Aktivieren Sie auf der Registerkarte **Erweitert** das Kontrollkästchen **Benachrichtigung für Fehler in Visual Basic- oder C#-Code anzeigen**. 
    

