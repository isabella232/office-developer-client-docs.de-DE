---
title: Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], reagieren auf Ereignisse, InfoPath 2003-kompatible Formularvorlagen, Reagieren auf Formularereignisse
ms.localizationpriority: medium
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Für die Bearbeitung von Ereignissen in InfoPath erstellen Sie im InfoPath-Designer Ereignishandler.
ms.openlocfilehash: bf3ad11e63cf975d40d0335d98767fa53876c61e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631307"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells

Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Für die Bearbeitung von Ereignissen in InfoPath erstellen Sie im InfoPath-Designer Ereignishandler.
  
InfoPath-Ereignishandler sollten im InfoPath-Designer erstellt werden, da InfoPath bei Verwendung des InfoPath 2003-kompatiblen Objektmodells automatisch die richtige Deklaration hinzufügt und ein Attribut ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) in der Codedatei eines Formulars (FormCode.cs oder FormCode.vb) anwendet, um den Ereignishandler zu identifizieren und zu senken. Nachdem Sie einen Ereignishandler erstellt haben, sollten Sie die zugehörige Deklaration und das Attribut in der Codedatei des Formulars nicht mehr ändern. 
  
Informationen zum Erstellen der InfoPath-Ereignishandler finden Sie unter [Hinzufügen eines Ereignishandlers mithilfe des InfoPath 2003-Objektmodells.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
## <a name="overview-of-the-event-objects"></a>Übersicht über die Ereignisobjekte

Das InfoPath 2003-kompatible Objektmodell implementiert neun Ereignisobjekte, die im [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) verfügbar gemacht werden. In der folgenden Tabelle sind alle InfoPath-Ereignisobjekte, die zugeordneten Ereignishandler sowie eine Beschreibung der durch sie bereitgestellten Funktionen aufgelistet. 
  
|**Name**|**Ereignishandler**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument, den Rückgabestatus sowie andere Eigenschaften, die Informationen zum XML-Knoten enthalten, zurück, während ein XML-DOM (Document Object Model) geändert wird. Schließt auch eine Methode zum Auslösen eines Fehlers ein.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument, den Rückgabestatus und den XML-Quellknoten zurück, während im Formularbereich auf eine Schaltfläche geklickt wird.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Gibt Informationen zum XML-DOM-Knoten (Document Object Model) zurück, bei dem es sich um den aktuellen Kontext des dem Formular zugrunde liegenden XML-Dokuments handelt.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument zurück, während die Ansicht gewechselt oder Formulare zusammengeführt werden.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument und den Rückgabestatus zurück, während ein Formular geladen oder gesendet wird.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[Onmergerequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Gibt Eigenschaften und Methoden zurück, die während eines **OnMergeRequest**-Ereignisses für die programmseitige Interaktion mit dem zugrunde liegenden XML-Dokument eines Formulars sowie für die Ermittlung von Zusammenführungseigenschaften, wie z. B. die Anzahl der zusammenzuführenden Dateien, verwendet werden können.  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Gibt eine Reihe von Eigenschaften und Methoden zurück, die während eines Speichervorgangs vom **OnSaveRequest**-Ereignishandler für die programmseitige Interaktion mit dem zugrunde liegenden XML-Dokument eines Formulars, die Festlegung der Speichereigenschaften und die Ausführung des Speichervorgangs verwendet werden können.  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[Onsign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Wird verwendet, um zusätzliche Daten zur digitalen Signatur hinzuzufügen.  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[Onversionupgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Gibt einen Verweis auf das einem Formular zugrunde liegende XML-Dokument, den Rückgabestatus sowie die Dokument- und Lösungsversionsnummern zurück, während ein Versionsupgrade durchgeführt wird.  <br/> |
   
## <a name="using-the-event-objects"></a>Verwenden der Ereignisobjekte

Beim Erstellen eines Ereignishandlers wird von InfoPath dessen Deklaration in der Formularcodedatei des Projekts ("FormCode.cs" oder "FormCode.vb") erstellt. In der Deklaration des Ereignishandlers wird von InfoPath **e** als Name der Parameter verwendet, der an den Ereignishandler übergeben wird. Dieser Parameter enthält das Ereignisobjekt, das dem Ereignishandler zugeordnet ist. 
  
Wenn Sie beispielsweise einen Ereignishandler für das **OnLoad**-Ereignis im Entwurfsmodus erstellen (klicken Sie auf der Registerkarte **Entwicklertools** auf **On Load-Ereignis**), wird von InfoPath die Deklaration für den Ereignishandler, der das **DocReturnEvent**-Objekt erhält, der Formularcodedatei hinzugefügt. Dann wird der Code-Editor geöffnet, damit Sie den Code der folgenden Ereignishandlerdeklaration hinzufügen können. 
  
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

Beim Schreiben von Code für einen Ereignishandler können Sie die Eigenschaften und Methoden verwenden, die vom Ereignisobjekt implementiert werden, das über den **e-Parameter** übergeben wird. Im folgenden **OnBeforeChange-Ereignishandler** wird beispielsweise die [NewValue-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) des **DataDOMEvent-Ereignisobjekts** verwendet, um den Wert des soeben geänderten Felds zu überprüfen. Wenn sie leer ist, wird die [ReturnMessage-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) des **DataDOMEvent-Ereignisobjekts** verwendet, um dem Benutzer in einem Dialogfeld einen Fehler anzuzeigen, und die [ReturnStatus-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) ist auf **"false"** festgelegt, was bedeutet, dass die vom Benutzer vorgenommenen Änderungen nicht akzeptiert werden sollen.
  
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
  

