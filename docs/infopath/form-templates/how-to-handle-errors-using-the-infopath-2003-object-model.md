---
title: Behandeln von Fehlern mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Behandeln von Fehlern, InfoPath 2003-kompatible Formularvorlagen, Fehlerbehandlung, Formularvorlagen [InfoPath 2007], Fehlerbehandlung,Fehlerbehandlung [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
ms.localizationpriority: medium
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das InfoPath 2003-kompatible Objektmodell unterstützt die Fehlerbehandlung durch die Verwendung des ErrorObject-Objekts in Verbindung mit der ErrorsCollection-Auflistung.
ms.openlocfilehash: 0f2e4e527d9f1599428e926bf278720b3aa2a22c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584892"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Behandeln von Fehlern mithilfe des InfoPath 2003-Objektmodells

Beim Erstellen von benutzerdefinierten Anwendungen müssen Entwickler häufig Fehler behandeln, wobei auch Programmiercode geschrieben werden muss, um nach Fehlern zu suchen, die von der Anwendung ausgelöst wurden, oder um benutzerdefinierte Fehler zu erstellen und auszulösen. Das InfoPath 2003-kompatible Objektmodell unterstützt die Fehlerbehandlung durch die Verwendung des [ErrorObject-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) in Verbindung mit der [ErrorsCollection-Auflistung.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) 
  
In InfoPath können Fehler auftreten, wenn in ein Formular eingegebene Daten die XML-Schemaüberprüfung nicht bestehen, wenn eine benutzerdefinierte Gültigkeitsprüfungseinschränkung fehlschlägt, wenn ein Fehler von der [ReportError-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) des [DataDOMEventObject-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) generiert wird oder wenn ein Fehler mithilfe der [Add-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) der [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) -Auflistung erstellt wird. 
  
## <a name="overview-of-the-errorscollection-collection"></a>Übersicht über die ErrorsCollection-Auflistung

Die **ErrorsCollection**-Auflistung stellt die folgenden Methoden und Eigenschaften bereit, mit deren Hilfe Entwickler die in der Auflistung enthaltenen **ErrorObject**-Objekte verwalten können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)-Methode  <br/> |Erstellt ein **ErrorObject**-Objekt und fügt es der Auflistung hinzu.  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)-Methode  <br/> |Löscht alle **ErrorObject**-Objekte, die dem angegebenen XML-Knoten und Bedingungsnamen zugeordnet sind, mit Ausnahme von benutzerdefinierten Fehlern, die mithilfe der **ReportError**-Methode hinzugefügt wurden.  <br/> |
|[DeleteAll-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx)  <br/> |Löscht alle **ErrorObject**-Objekte, die in der Auflistung enthalten sind.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **ErrorObject**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf ein **ErrorObject**-Objekt basierend auf der angegebenen Indexnummer ab.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Übersicht über das ErrorObject-Objekt

Das **ErrorObject**-Objekt stellt die folgenden Eigenschaften bereit, über die Formularentwickler auf Informationen zu dem ausgelösten Fehler zugreifen können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ConditionName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx)  <br/> |Ruft in Abhängigkeit vom Typ des **ErrorObject**-Objekts den Namen der Fehlerbedingung ab oder gibt **null** zurück.  <br/> |
|[DetailedErrorMessage-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx)  <br/> |Ruft die ausführliche Fehlermeldung des **ErrorObject**-Objekts ab oder legt sie fest.  <br/> |
|[ErrorCode-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx)  <br/> |Ruft den Fehlercode des **ErrorObject**-Objekts ab oder legt ihn fest.  <br/> |
|[Node-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx)  <br/> |Ruft einen Verweis auf den XML-Knoten ab, der dem **ErrorObject**-Objekt zugeordnet ist.  <br/> |
|[ShortErrorMessage-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx)  <br/> |Ruft die kurze Fehlermeldung des **ErrorObject**-Objekts ab oder legt sie fest.  <br/> |
|[ErrorType-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx)  <br/> |Ruft den Typ des **ErrorObject**-Objekts ab.  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Verwenden der ErrorsCollection-Auflistung und des ErrorObject-Objekts

Der Zugriff auf die **ErrorsCollection-Auflistung** erfolgt über die [Errors-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) des [XDocument-Objekts.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) Die **ErrorsCollection**-Auflistung ist dem einem Formular zugrunde liegenden XML-Dokument zugeordnet; falls ein Fehler auftritt, tritt er daher innerhalb des XML-Dokuments auf. Das folgende Beispiel zeigt, wie eine in Visual C# geschriebene **foreach**-Schleife verwendet werden kann, um die Fehler zu überprüfen, die in dem einem Formular zugrunde liegenden XML-Dokument vorhanden sein könnten. Falls Fehler gefunden werden, durchläuft die Funktion jeden dieser Fehler und zeigt mithilfe der **ShortErrorMessage**-Eigenschaft des **ErrorObject**-Objekts ein Meldungsfeld für den Benutzer an. 
  
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

Die vorangegangene Funktion kann von einem der Datenüberprüfungs-Ereignishandler des Formulars aufgerufen werden. Wenn beispielsweise im [OnAfterChange-Ereignishandler](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) für ein Feld im Formular verwendet wird, würde der Aufruf der Funktion das XML-Knotenargument mithilfe der [Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) des [DataDOMEventObject-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) wie folgt übergeben. 
  
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
  

