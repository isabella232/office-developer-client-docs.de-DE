---
title: Behandeln von Fehlern mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen Behandlung Fehler, InfoPath 2003-kompatible Formularvorlagen, Fehlerbehandlung, Formularvorlagen [InfoPath 2007], Fehlerbehandlung, Fehlerbehandlung [InfoPath 2007], des InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Beim Erstellen von benutzerdefinierter Anwendungen müssen Entwickler häufig Fehlerbehandlung ausführen, die Programmierung Schreiben von Code zum Prüfen, ob Fehler, die von der Anwendung ausgelöst oder zum Erstellen und benutzerdefinierte Fehlermeldungen auslösen beinhaltet. Das InfoPath 2003-kompatible Objektmodell unterstützt Fehlerbehandlung mithilfe des ErrorObject-Objekts im Zusammenhang mit der ErrorsCollection-Auflistung.
ms.openlocfilehash: 577e531d8943dc8fc3884cd81f68b11ca285c5d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790759"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Behandeln von Fehlern mit dem InfoPath 2003-Objektmodell

Beim Erstellen von benutzerdefinierter Anwendungen müssen Entwickler häufig Fehlerbehandlung ausführen, die Programmierung Schreiben von Code zum Prüfen, ob Fehler, die von der Anwendung ausgelöst oder zum Erstellen und benutzerdefinierte Fehlermeldungen auslösen beinhaltet. Das InfoPath 2003-kompatible Objektmodell unterstützt Fehlerbehandlung mithilfe des [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) -Objekts im Zusammenhang mit der [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) -Auflistung. 
  
In InfoPath können Fehler auftreten, wenn ein Formular eingegebene Daten XML-Schema-Validation, schlägt fehl, wenn eine benutzerdefinierte validierungseinschränkung Fehler, wenn von der [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) -Methode des [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) -Objekts ein Fehler generiert wird, oder wenn ein Fehler erstellt wird verwenden die [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) -Methode der [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) -Auflistung. 
  
## <a name="overview-of-the-errorscollection-collection"></a>Übersicht über die ErrorsCollection-Auflistung

Die **ErrorsCollection** -Auflistung enthält die folgenden Methoden und Eigenschaften, die Formularentwickler **ErrorObject** -Objekte zu verwalten, die die Auflistung enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) -Methode  <br/> |Erstellt ein **ErrorObject** -Objekt und fügt es der Auflistung hinzu.  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)-Methode  <br/> |Löscht alle **ErrorObject** -Objekte der angegebenen XML-Knoten und Bedingungsnamen, mit Ausnahme der benutzerdefinierte Fehler mit der **ReportError** -Methode hinzugefügt zugeordnet.  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx) -Methode  <br/> |Löscht alle **ErrorObject** -Objekte, die in der Auflistung enthalten sind.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **ErrorObject** -Objekte in der Auflistung ab.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf ein **ErrorObject** -Objekt basierend auf der angegebenen Indexnummer ab.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Übersicht über das ErrorObject-Objekt

Das **ErrorObject** -Objekt stellt die folgenden Eigenschaften, die Formularentwickler Informationen zu dem Fehler ausgelösten zugreifen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx) -Eigenschaft  <br/> |Ruft den Namen der fehlerbedingung ab, oder **null**, je nach den Typ des **ErrorObject** -Objekt zurückgibt.  <br/> |
|[DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen der detaillierten Fehlermeldung des **ErrorObject** -Objekts.  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx) -Eigenschaft  <br/> |Ruft ab oder legt den Fehlercode des **ErrorObject** -Objekts fest.  <br/> |
|[Node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf den XML-Knoten, der dem **ErrorObject** -Objekt zugeordnet.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen der kurzen Fehlermeldung des **ErrorObject** -Objekts.  <br/> |
|[ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx) -Eigenschaft  <br/> |Ruft den Typ des **ErrorObject** -Objekts ab.  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Verwenden der ErrorsCollection-Auflistung und des ErrorObject-Objekts

Der Zugriff auf die **ErrorsCollection** -Auflistung erfolgt über die [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Objekts. Die **ErrorsCollection** -Auflistung ist mit einem Formular zugrunde liegenden XML-Dokument zugeordnet, sodass tritt ein Fehler im XML-Dokument erfolgt. Im folgenden Beispiel wird veranschaulicht, wie eine Visual C#- **Foreach** -Schleife verwendet werden kann, um den Fehler zu überprüfen, die in einem Formular zugrunde liegenden XML-Dokument enthalten sein könnten. Wenn Fehler aufgetreten sind, die Funktion durchläuft jede von ihnen und, mithilfe der **Count** -Eigenschaft des **ErrorObject** -Objekts ein Meldungsfeld für den Benutzer angezeigt. 
  
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

Von einem Ereignishandler für das Formular Daten Validierung konnte die vorstehende-Funktion aufgerufen werden. Beispielsweise würde bei Verwendung in der [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) -Ereignishandler für ein Feld in der Form der Aufruf der Funktion das XML-Knoten-Argument mit der [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) -Eigenschaft des Objekts [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) wie folgt übergeben. 
  
```cs
CheckErrors(e.Site);
```

Neben der Behandlung von InfoPath generierten Fehler, können Formularentwickler auch benutzerdefinierte Fehler mithilfe der **ReportError** -Methode des **DataDOMEventObject** -Objekts oder mithilfe der **Add** -Methode, der die **ErrorsCollection** generieren Auflistung. Informationen zur Verwendung der Methods **ReportError** oder **Hinzufügen** klicken Sie auf die Methoden am Anfang dieses Themas. 
  
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
  

