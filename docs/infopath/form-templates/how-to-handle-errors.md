---
title: Behandeln von Fehlern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Fehler [Infopath 2007], Behandlung, FormErrorCollection [InfoPath 2007], InfoPath 2007, Fehlerbehandlung, FormError [InfoPath 2007], Fehlerbehandlung [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Beim Erstellen von benutzerdefinierter Anwendungen müssen Entwickler häufig Fehlerbehandlung ausführen, die Programmierung Schreiben von Code zum Prüfen, ob Fehler, die von der Anwendung ausgelöst oder zum Erstellen und benutzerdefinierte Fehlermeldungen auslösen beinhaltet. Das InfoPath-Objektmodell von Microsoft.Office.InfoPath-Namespace unterstützt die Fehlerbehandlung durch Verwendung der FormError-Klasse in Verbindung mit der FormErrorCollection-Klasse bereitgestellt.
ms.openlocfilehash: 3bfad103c31d0b5364d1c75acfbb2f590f7658bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790755"
---
# <a name="handle-errors"></a>Behandeln von Fehlern

Beim Erstellen von benutzerdefinierter Anwendungen müssen Entwickler häufig Fehlerbehandlung ausführen, die Programmierung Schreiben von Code zum Prüfen, ob Fehler, die von der Anwendung ausgelöst oder zum Erstellen und benutzerdefinierte Fehlermeldungen auslösen beinhaltet. Das InfoPath-Objektmodell von [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace unterstützt die Fehlerbehandlung durch Verwendung der [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Klasse in Verbindung mit der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse bereitgestellt. 
  
Fehler in InfoPath können aus den folgenden Gründen auftreten:
  
- Wenn Daten, die in ein Formular eingegeben werden, bei der XML-Schemavalidierung Fehler aufweisen.
    
- Wenn eine benutzerdefinierte Validierungseinschränkung Fehler aufweist.
    
- Wenn von der [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methode der [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) -Event-Objekts ein Fehler generiert wird. 
    
- Wenn ein benutzerdefinierter Fehler erstellt wird mithilfe der [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methode der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse. 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Übersicht über die FormErrorCollection-Klasse

[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Objekte zu verwalten, die die Auflistung enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methode (+ 3 Überladungen)  <br/> |Erstellt ein **FormError** -Objekt und fügt es der Auflistung hinzu.  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) -Methode (+ 1 Überladung)  <br/> |Löscht den angegebenen benutzerdefinierten Fehler aus der Auflistung.   <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) -Methode  <br/> |Löscht alle **FormError** -Objekte, die in der Auflistung enthalten sind.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+ 1 Überladung)  <br/> |Alle **FormError** -Objekte des angegebenen Namens oder Typs zurückgegeben aus der Auflistung.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **FormError** -Objekte in der Auflistung ab.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf ein **FormError** -Objekt basierend auf der angegebenen Indexnummer ab.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Übersicht über die FormError-Klasse

Die [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Klasse stellt die folgenden Eigenschaften, die Formularentwickler Informationen zu dem Fehler ausgelösten zugreifen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen der detaillierten Fehlermeldung des **FormError** -Objekts.  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) -Eigenschaft  <br/> |Ruft ab oder legt den Fehlercode des **FormError** -Objekts fest.  <br/> |
|[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) -Eigenschaft  <br/> |Ruft ein **XPathNavigator** -Objekt, das auf dem **FormError** -Objekt zugeordneten Knoten positioniert ist.  <br/> |
|[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen der kurzen Fehlermeldung des **FormError** -Objekts.  <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) -Eigenschaft  <br/> |Ruft den Typ des **FormError** -Objekts ab.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Verwenden der Klassen "FormErrorCollection" und "FormError"

Der Zugriff auf das einem Formular zugeordnete **FormErrorCollection** -Objekt erfolgt über die [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) -Eigenschaft des [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Objekt. **FormErrorCollection** -Objekt ist mit einem Formular zugrunde liegenden XML-Dokument verknüpft, sodass tritt ein Fehler auf, es und anderen Fehlern zugegriffen und verwaltet werden können innerhalb des aktuellen XML-Dokuments. Im folgenden Beispiel wird veranschaulicht, wie eine Schleife verwendet werden kann, um den Fehler zu überprüfen, die in einem Formular zugrunde liegenden XML-Dokument enthalten sein könnten. Wenn Fehler aufgetreten sind, die Funktion durchläuft jede von ihnen und, mithilfe der **Message** -Eigenschaft des **FormError** -Objekts ein Meldungsfeld für den Benutzer angezeigt. 
  
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

Von einem Ereignishandler für das Formular Daten Validierung konnte die vorstehende-Funktion aufgerufen werden. Beispielsweise würde, wenn in den Ereignisdetails Ereignishandler für das [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) -Ereignis eines Felds im Formular verwendet wird, der Aufruf der Funktion das XML-Knoten-Argument mit der [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) -Eigenschaft des Event-Objekts [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) wie folgt übergeben. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Neben der Behandlung von InfoPath generierten Fehler, können Formularentwickler auch benutzerdefinierte Fehler mithilfe der [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methode der [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) -Event-Objekts oder mithilfe der [Hinzufügen generieren ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)-Methode der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse. Informationen zur Verwendung der Methods [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) oder [Hinzufügen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) klicken Sie auf die Links für diese Methoden am Anfang dieses Themas. 
  
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
    
2. Klicken Sie auf **Optionen**, und klicken Sie dann unter der Kategorie **Allgemein** auf **InfoPath-Optionen** . 
    
3. Wählen Sie auf der Registerkarte **Erweitert** das Kontrollkästchen **Benachrichtigung für Fehler in Visual Basic und C#-Code anzeigen** . 
    

