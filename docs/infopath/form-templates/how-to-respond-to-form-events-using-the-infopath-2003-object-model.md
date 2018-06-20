---
title: Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Formularvorlagen [Infopath 2007] reagieren auf Ereignisse, InfoPath 2003-kompatible Formularvorlagen, reagieren auf Formularereignisse
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Für die Bearbeitung von Ereignissen in InfoPath erstellen Sie im InfoPath-Designer Ereignishandler.
ms.openlocfilehash: dff7b4f1657b7d1450d8b345521a747c0594462b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790745"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells

Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Für die Bearbeitung von Ereignissen in InfoPath erstellen Sie im InfoPath-Designer Ereignishandler.
  
InfoPath-Ereignishandler sollte im InfoPath-Designer erstellt werden, da, wenn mit dem InfoPath 2003-kompatible Objektmodell, InfoPath automatisch und fügt die korrekte Deklaration wendet ein Attribut ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) in eine des Formulars Codedatei ("FormCode.cs" oder "FormCode.vb") zu identifizieren und Auffangen den Ereignishandler verwenden. Nachdem Sie einen Ereignishandler erstellt haben, sollten Sie nicht die Deklaration und -Attribut in der Formularcodedatei ändern. 
  
Informationen zum Erstellen von InfoPath-Ereignishandler finden Sie unter [Hinzufügen einer Event Handler mithilfe des InfoPath 2003-Objektmodells](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="overview-of-the-event-objects"></a>Übersicht über die Ereignisobjekte

Das InfoPath 2003-kompatible Objektmodell implementiert neun Ereignisobjekte, die verfügbar gemacht werden im [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace. Die folgende Tabelle enthält die einzelnen InfoPath-Ereignisobjekte, die Ereignishandler, denen sie zugeordnet sind, und eine Beschreibung der Funktionen, die sie bereitstellen. 
  
|**Name**|**Ereignishandler**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument, den Rückgabestatus sowie andere Eigenschaften, die Informationen zum XML-Knoten enthalten, zurück, während ein XML-DOM (Document Object Model) geändert wird. Schließt auch eine Methode zum Auslösen eines Fehlers ein.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument, den Rückgabestatus und den XML-Quellknoten zurück, während im Formularbereich auf eine Schaltfläche geklickt wird.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Gibt Informationen zum XML-DOM-Knoten (Document Object Model) zurück, bei dem es sich um den aktuellen Kontext des dem Formular zugrunde liegenden XML-Dokuments handelt.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument zurück, während die Ansicht gewechselt oder Formulare zusammengeführt werden.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument und den Rückgabestatus zurück, während ein Formular geladen oder gesendet wird.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Gibt Eigenschaften und Methoden, die während eines **OnMergeRequest** -Ereignisses zum programmgesteuerten verwendet werden können interagieren mit einem Formular zugrunde liegenden XML-Dokument und Merge-Eigenschaften, wie die Anzahl der zusammengeführten Dateien zu bestimmen.  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Gibt eine Anzahl von Eigenschaften und Methoden, die während eines Speichervorgangs verwendet werden können Operation vom **OnSaveRequest** -Ereignishandler für die programmgesteuerte Interaktion mit einem Formular zugrunde liegende XML-Dokument Bestimmen der Speichereigenschaften und Ausführen des Vorgangs.  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Wird verwendet, um zusätzliche Daten zur digitalen Signatur hinzuzufügen.  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument, den Rückgabestatus sowie die Dokument- und Lösungsversionsnummern zurück, während ein Versionsupgrade durchgeführt wird.  <br/> |
   
## <a name="using-the-event-objects"></a>Verwenden der Ereignisobjekte

Wenn Sie einen Ereignishandler erstellen, erstellt InfoPath den Ereignishandler Deklaration in das Projekt Formularcodedatei ("FormCode.cs" oder "FormCode.vb"). In der Deklaration der Ereignishandler verwendet InfoPath **e** als den Namen des Parameters, der an den Ereignishandler übergeben wird. Dieser Parameter enthält das Ereignisobjekt, das den Ereignishandler zugeordnet ist. 
  
Wenn Sie einen Ereignishandler für das **OnLoad** -Ereignis im Entwurfsmodus (durch Klicken auf **On Load-Ereignis** auf der Registerkarte **Entwicklertools** ) erstellen, wird InfoPath beispielsweise die Deklaration für den Ereignishandler, der empfängt das **DocReturnEvent** -Objekt das Formular code Datei und dann wird im Code-Editor geöffnet, damit Sie Ihr Code die folgende Deklaration der Ereignis-Handler hinzufügen können. 
  
```cs
// The following function handler is created by Microsoft Office 
// InfoPath. Do not modify the type or number of arguments.
[InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
public void FormEvents_OnLoad(DocReturnEvent e)
{
   // Write your code here.
}
```

```vb
' The following function handler is created by Microsoft Office 
' InfoPath. Do not modify the type or number of arguments.
<InfoPathEventHandler(EventType:=InfoPathEventType.OnLoad)> _
Public Sub FormEvents_OnLoad(ByVal e As DocReturnEvent)
   ' Write your code here.
End Sub
```

Wenn Code für einen Ereignishandler schreiben, können Sie die Eigenschaften und Methoden implementiert, durch das Event-Objekt, das über den **e** -Parameter übergeben wird. Beispielsweise wird in den folgenden **OnBeforeChange** -Ereignishandler die [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) -Eigenschaft des **DataDOMEvent** -Event-Objekts verwendet, um den Wert des Felds überprüfen, die gerade geändert wurde. Wenn es leer ist, die [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) -Eigenschaft des **DataDOMEvent** -Event-Objekts wird verwendet, um einen Fehler an den Benutzer in einem Dialogfeld angezeigt werden soll, und die [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) -Eigenschaft auf **false festgelegt**, das angibt, dass die Änderungen, die der Benutzer vorgenommenen sollte festgelegt ist nicht akzeptiert werden.
  
```cs
[InfoPathEventHandler(MatchPath="/my:myFields/my:field1", 
    EventType=InfoPathEventType.OnBeforeChange)]
public void field1_OnBeforeChange(DataDOMEvent e)
{
   // Determine whether there is a new value.
   if ((string)e.NewValue == "")
   {
      // The value is blank, so display an error message and roll
      // back the changes.
      e.ReturnMessage = "You must supply a value for this field.";
      e.ReturnStatus = false;
      return;
   }
}
```

```vb
<InfoPathEventHandler(MatchPath:="/my:myFields/my:field1", _ EventType:=InfoPathEventType.OnBeforeChange)> _
Public Sub field1_OnBeforeChange(ByVal e As DataDOMEvent)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message and roll back
      ' the changes.
      e.ReturnMessage = "You must supply a value for this field."
      e.ReturnStatus = False
      Return
   End If
End Sub
```

> [!NOTE]
> Von jedem der InfoPath-Ereignisobjekte im InfoPath 2003-kompatiblen Objektmodell werden unterschiedliche Eigenschaften und Methoden implementiert. Klicken Sie in der zuvor angezeigten Tabelle zu den Ereignisobjekten auf das entsprechende Objekt, um weitere Informationen zu einem bestimmten Ereignisobjekt zu erhalten. 
  

