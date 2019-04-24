---
title: Behandeln von Fehlern mithilfe des InfoPath-2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, behandeln von Fehlern, InfoPath 2003-kompatible Formularvorlagen, Fehlerbehandlung, Formularvorlagen [InfoPath 2007], Fehlerbehandlung, Fehlerbehandlung [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das InfoPath 2003-kompatible Objektmodell unterstützt die Fehlerbehandlung durch die Verwendung des ErrorObject-Objekts in Verbindung mit der ErrorsCollection-Auflistung.
ms.openlocfilehash: 93991e33d8867f89454bec08b41ba83e98ab0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300126"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Behandeln von Fehlern mithilfe des InfoPath-2003-Objektmodells

Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das InfoPath 2003-kompatible Objektmodell unterstützt die Fehlerbehandlung durch die Verwendung des [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) -Objekts in Verbindung mit der [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) -Auflistung. 
  
In InfoPath können Fehler auftreten, wenn bei Daten, die in ein Formular eingegeben werden, die XML-Schemaüberprüfung fehlschlägt, wenn eine benutzerdefinierte Validierungs Einschränkung fehlschlägt, wenn ein Fehler durch die [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) -Methode des [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) -Objekts generiert wird oder wenn ein Fehler erstellt wird. Verwenden der [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) -Methode der [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) -Auflistung. 
  
## <a name="overview-of-the-errorscollection-collection"></a>Übersicht über die ErrorsCollection-Auflistung

Die **ErrorsCollection**-Auflistung stellt die folgenden Methoden und Eigenschaften bereit, mit deren Hilfe Entwickler die in der Auflistung enthaltenen **ErrorObject**-Objekte verwalten können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)-Methode  <br/> |Erstellt ein **ErrorObject**-Objekt und fügt es der Auflistung hinzu.  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)-Methode  <br/> |Löscht alle **ErrorObject**-Objekte, die dem angegebenen XML-Knoten und Bedingungsnamen zugeordnet sind, mit Ausnahme von benutzerdefinierten Fehlern, die mithilfe der **ReportError**-Methode hinzugefügt wurden.  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx) -Methode  <br/> |Löscht alle **ErrorObject**-Objekte, die in der Auflistung enthalten sind.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **ErrorObject**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf ein **ErrorObject**-Objekt basierend auf der angegebenen Indexnummer ab.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Übersicht über das ErrorObject-Objekt

Das **ErrorObject**-Objekt stellt die folgenden Eigenschaften bereit, über die Formularentwickler auf Informationen zu dem ausgelösten Fehler zugreifen können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx) -Eigenschaft  <br/> |Ruft in Abhängigkeit vom Typ des **ErrorObject**-Objekts den Namen der Fehlerbedingung ab oder gibt **null** zurück.  <br/> |
|[DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx) -Eigenschaft  <br/> |Ruft die ausführliche Fehlermeldung des **ErrorObject**-Objekts ab oder legt sie fest.  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx) -Eigenschaft  <br/> |Ruft den Fehlercode des **ErrorObject**-Objekts ab oder legt ihn fest.  <br/> |
|[Node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf den XML-Knoten ab, der dem **ErrorObject**-Objekt zugeordnet ist.  <br/> |
|[ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx) -Eigenschaft  <br/> |Ruft die kurze Fehlermeldung des **ErrorObject**-Objekts ab oder legt sie fest.  <br/> |
|[ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx) -Eigenschaft  <br/> |Ruft den Typ des **ErrorObject**-Objekts ab.  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Verwenden der ErrorsCollection-Auflistung und des ErrorObject-Objekts

Der **** Zugriff auf die ErrorsCollection-Auflistung erfolgt über die [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Objekts. Die **ErrorsCollection**-Auflistung ist dem einem Formular zugrunde liegenden XML-Dokument zugeordnet; falls ein Fehler auftritt, tritt er daher innerhalb des XML-Dokuments auf. Das folgende Beispiel zeigt, wie eine in Visual C# geschriebene **foreach**-Schleife verwendet werden kann, um die Fehler zu überprüfen, die in dem einem Formular zugrunde liegenden XML-Dokument vorhanden sein könnten. Falls Fehler gefunden werden, durchläuft die Funktion jeden dieser Fehler und zeigt mithilfe der **ShortErrorMessage**-Eigenschaft des **ErrorObject**-Objekts ein Meldungsfeld für den Benutzer an. 
  
```cs
public void CheckErrors(IXMLDOMNode xmlNode)
{
   foreach(ErrorObject err in thisXDocument.Errors)
   {
      if(xmlNode==err.Node)
         thisXDocument.UI.Alert("The following error has occured: "
             + err.ShortErrorMessage + ".");
   }
}
```

Die vorangegangene Funktion kann von einem der Datenüberprüfungs-Ereignishandler des Formulars aufgerufen werden. Wenn beispielsweise im [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) -Ereignishandler für ein Feld im Formular verwendet wird, würde der Aufruf der Funktion das XML-Knoten Argument mithilfe der [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) -Eigenschaft des [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) -Objekts wie folgt übergeben. 
  
```cs
CheckErrors(e.Site);
```

Neben der Behandlung von Fehlern, die durch InfoPath generiert werden, können Formularentwickler mithilfe der **ReportError**-Methode des **DataDOMEventObject**-Objekts oder mithilfe der **Add**-Methode der **ErrorsCollection**-Auflistung auch benutzerdefinierte Fehler generieren. Informationen zur Verwendung der Methoden **ReportError** und **Add** erhalten Sie, indem Sie am Anfang des Themas auf die entsprechende Methode klicken. 
  
## <a name="handling-managed-code-exceptions"></a>Behandlung von Ausnahmen im verwalteten Code

Sie können die try-catch-Ausnahmebehandlung zum Behandeln von Ausnahmen verwenden, die in Formularvorlagen mit verwaltetem Code ausgelöst wurden. Dies wird im folgenden Codebeispiel gezeigt.
  
```cs
DataAdapters dataAdapters;
dataAdapters = thisXDocument.DataAdapters; 
XMLFileAdapterObject queryXMLFile = 
   (XMLFileAdapterObject)dataAdapters["form1"];
// Perform the query.
try
{
   queryXMLFile.Query();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to query.\n\n" + ex.Message);
}
// Perform the submit.
try
{
   queryXMLFile.Submit();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to submit.\n\n" + ex.Message);
}
```

Wenn Sie im Formularcode keine try-catch-Ausnahmebehandlung verwenden, zeigt InfoPath beim Debuggen und Anzeigen der Vorschau Informationen zu unbehandelten Ausnahmen im Dialogfeld für InfoPath-Fehler an. 
  

