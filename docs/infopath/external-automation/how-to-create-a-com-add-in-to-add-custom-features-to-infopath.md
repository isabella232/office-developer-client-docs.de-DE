---
title: Erstellen eines COM-Add-Ins zum Hinzufügen von benutzerdefinierten Features zu InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, Erstellen von COM-Add-Ins, InfoPath 2007, Hinzufügen von benutzerdefinierten Features, COM-Add-Ins [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath unterstützt COM-Add-Ins für die Erweiterung der Benutzerumgebung zum Bearbeiten von Formularen. Obwohl die Unterstützung für COM-Add-ins erstmals in InfoPath hinzugefügt wurde, haben andere Office-Anwendungen wie Microsoft Office Word und Microsoft Office Excel seit Office 2000 COM-Add-Ins unterstützt.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303787"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Erstellen eines COM-Add-Ins zum Hinzufügen von benutzerdefinierten Features zu InfoPath

Microsoft InfoPath unterstützt COM-Add-Ins für die Erweiterung der Benutzerumgebung zum Bearbeiten von Formularen. Obwohl die Unterstützung für COM-Add-ins erstmals in InfoPath hinzugefügt wurde, haben andere Office-Anwendungen wie Microsoft Office Word und Microsoft Office Excel seit Office 2000 COM-Add-Ins unterstützt.
  
Die COM-Add-in-Unterstützung in InfoPath ist für die Formularbearbeitungsumgebung verfügbar. Die Formularentwurfsumgebung kann nicht mithilfe von COM-Add-Ins erweitert werden.
  
## <a name="the-idtextensibility2-interface"></a>Die IDTExtensibility2-Schnittstelle

Die InfoPath-Bearbeitungsumgebung bietet Unterstützung für die **IDTExtensibility2** -Schnittstelle, die von Entwicklern von COM-Add-Ins implementiert werden muss. **IDTExtensibility2** ist ein Dual-Interface-Objekt, das fünf Methoden bereitstellt, die als Ereignisse fungieren. innerhalb der Bearbeitungsumgebung. Diese Methoden ermöglichen es dem COM-Add-in, auf Umgebungsstart-und-herunter fahrenbedingungen zu reagieren, die in der folgenden Tabelle aufgeführt sind. 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal Custom () As Variant)** <br/> |Tritt ein, wenn ein Add-in in der Umgebung geladen oder entladen wird.  <br/> |
|**OnBeginShutdown (ByVal Custom () As Variant)** <br/> |Tritt ein, wenn die Umgebung heruntergefahren wird.  <br/> |
|**OnConnection (ByVal Application as Object, ByVal ConnectMode as ext_ConnectMode, ByVal AddInInst as Object, ByVal Custom () As Variant)** <br/> |Tritt auf, wenn ein Add-in in der Umgebung geladen wird.  <br/> |
|**Disconnection (ByVal RemoveMode as ext_DisconnectMode, ByVal Custom () As Variant)** <br/> |Tritt auf, wenn ein Add-in aus der Umgebung entladen wird.  <br/> |
|**OnStartupComplete (ByVal Custom () As Variant)** <br/> |Tritt ein, wenn die Umgebung gestartet wurde.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrieren von COM-Add-ins

Alle Office-Anwendungen, einschließlich InfoPath, verwenden die Registrierung, um Add-Ins in der COM-Add-Ins-Auflistung aufzulisten, den Verbindungsstatus zu speichern und die Start-oder Demand-Lade Informationen zu speichern. Bei InfoPath-COM-Add-Ins wird der Name der einzelnen Add-Ins unter dem folgenden Schlüssel angezeigt:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Für COM-Add-Ins, die von jedem Benutzer des Clientcomputers installiert werden, befindet sich der Registrierungsschlüssel in der Registrierungsstruktur HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Der Registrierungsschlüsselname entspricht dem **ProgIdAttribute** des Add-Ins und enthält die folgenden Werte. 
  
|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Der Name, der im Dialogfeld **com-Add-ins** angezeigt wird und auf der Seite **Add-ins** des **Trust Centers**aufgeführt wird.  <br/> |
|**Beschreibung** <br/> |**String** <br/> |Die Zeichenfolge, die angezeigt wird, wenn das Add-in im **Vertrauensstellungs Center**ausgewählt wird.  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Gibt an, wie das COM-Add-in geladen wird. Der Wert kann eine Kombination aus 0, 1, 2, 8 und 16 sein. Weitere Informationen finden Sie in der Tabelle unten.  <br/> |
   
Der **DWORD** -Wert für **LoadBehavior** sollte einen Wert enthalten, der beschreibt, wie das COM-Add-in in der Bearbeitungsumgebung geladen wird. Der Wert kann aus der folgenden Tabelle oder aus einer Kombination von Werten aus der Tabelle sein. Ein COM-Add-in, das in Visual Studio 2005 erstellt wurde, hat beispielsweise eine **LoadBehavior** von "3", die beim Anwendungsstart geladen und verbunden werden kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Getrennt. Das Add-in wird im Dialogfeld **com-Add-in** als inaktiv angezeigt.  <br/> |
|1  <br/> |Verbunden. Das Add-in wird im Dialogfeld **com-Add-in** als aktiv angezeigt.  <br/> |
|2  <br/> |Laden beim Start. Das Add-in wird geladen und verbunden, wenn die Hostanwendung gestartet wird.  <br/> |
|8  <br/> |Bei Bedarf laden. Das Add-in wird geladen und verbunden, wenn die Hostanwendung es benötigt, beispielsweise wenn ein Benutzer auf eine Schaltfläche klickt, die Funktionalität im Add-in verwendet.  <br/> |
|16  <br/> |Verbindung bei der ersten Ausführung. Das Add-in wird geladen und verbunden, wenn der Benutzer die Hostanwendung zum ersten Mal ausführt, nachdem das Add-in registriert wurde.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Erstellen eines verwalteten COM-Add-Ins mit Visual Studio 2005 oder Visual Studio 2008

Erstellen Sie ein FreigeGebenes Add-in-Projekt wie folgt, um ein verwaltetes COM-Add-in mithilfe von Microsoft Visual Studio 2005 oder Visual Studio 2008 zu erstellen: 
  
1. Starten Sie Visual Studio.
    
2. Klicken Sie im Menü **Datei** auf **Neues Projekt**.
    
3. Klicken Sie im Dialogfeld **Neues Projekt** im Bereich **Projekttypen** auf den Ordner **andere Projekttypen** , und klicken Sie dann **** auf Erweiterbarkeit.
    
4. Klicken Sie im Bereich **Vorlagen** auf **freigegebenes Add-in**.
    
5. Geben Sie im Feld **Name** einen Namen für das Projekt ein. 
    
6. Geben Sie im Feld **Speicherort** einen Ordnerpfad ein, oder klicken Sie auf **Durchsuchen** , und wählen Sie einen Ordnerpfad aus, und klicken Sie dann auf **OK**. Der **Assistent für gemeinsame Add-ins** wird angezeigt. 
    
7. Klicken Sie im **Assistenten für freiGegebene Add-ins**auf **weiter** . Die Seite **Programmiersprache auswählen** wird angezeigt. 
    
8. Klicken Sie auf **Add-in mit Visual Basic erstellen**, und klicken Sie dann auf **weiter**. Die Seite **Anwendungs Host auswählen** wird angezeigt. 
    
9. Deaktivieren Sie die Kontrollkästchen neben den einzelnen Anwendungen, außer **Microsoft InfoPath**, und klicken Sie dann auf **weiter**. Die Seite **Name und Beschreibung eingeben** wird angezeigt. 
    
10. Geben Sie im Feld **wie lautet der Name Ihres Add-ins** den Namen des COM-Add-Ins ein. 
    
11. Geben Sie im Feld **wie lautet die Beschreibung Ihres Add-ins** ein, und klicken Sie auf **weiter**. Die Seite **Add-in-Optionen auswählen** wird angezeigt. 
    
12. Aktivieren Sie das Kontrollkästchen Ich möchte, dass das **Add-in geladen wird, wenn die Hostanwendung** geladen **wird und mein Add-in für alle Benutzer des Computers, auf dem Sie installiert wurde, verfügbar sein soll, nicht nur für die Person, die die IT** -Box installiert. 
    
13. Klicken Sie auf **weiter** , um die Seite **Zusammenfassung** zu überarbeiten, und klicken Sie auf **Fertig stellen**.
    
Nachdem das Projekt von Visual Studio erstellt wurde, werden zwei Projekte im Projektmappen-Explorer angezeigt. Das erste Projekt ist das Projekt für das COM-Add-in; Das zweite Projekt ist ein Setupprojekt für die Bereitstellung des COM-Add-Ins. Der **Assistent für freiGegebene Add-ins** fügt nur einen Verweis auf die **Microsoft Office 14,0-Objektbibliothek**ein, daher muss mithilfe der folgenden Schritte ein Verweis auf die InfoPath-Objektbibliothek eingefügt werden:
  
1. Doppelklicken Sie auf **mein Projekt** , um die Eigenschaften des Add-in-Projekts anzuzeigen. Klicken Sie auf die Registerkarte **Verweise** , um die Verweise anzuzeigen, die dem Projekt automatisch hinzugefügt werden. 
    
2. Klicken Sie auf die Schaltfläche **Hinzufügen** , um das Dialogfeld **Verweis hinzufügen** anzuzeigen. 
    
3. Doppelklicken Sie auf der Registerkarte **com** auf **Microsoft. InfoPath 2,0**-Typbibliothek, und klicken Sie dann auf **OK**.
    
4. Wenn Sie einen Verweis auf die **Microsoft InfoPath 3,0** -Typbibliothek hinzufügen, werden auch Verweise auf drei Assemblys hinzugefügt, die entfernt werden müssen: **ADODB**, **MSHTML**und **msxml2**. Klicken Sie im **Projektmappen-Explorer** unter **Verweise**mit der rechten Maustaste auf jeden dieser Verweise, und klicken Sie dann auf **Entfernen**.
    
## <a name="viewing-the-registry-settings"></a>Anzeigen der Registrierungseinstellungen

Führen Sie die folgenden Schritte aus, um die Registrierungseinstellungen anzuzeigen, die bei der Installation des COM-Add-Ins erstellt werden:
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Stammknoten des Setup-Projekts, klicken Sie auf **Ansicht**, dann auf **Editor**, und klicken Sie dann auf **Registrierung**.
    
2. Klicken Sie im linken Bereich auf das Plus, um **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath**und dann AddIns **** zu erweitern.
    
3. Klicken Sie auf den Namen, der der **ProgID**des freigegebenen Add-in-Projekts entspricht.
    
Um diese Eigenschaften zu ändern, klicken Sie mit der rechten Maustaste auf die Eigenschaft, klicken Sie auf **Eigenschaftenfenster**, und ändern Sie das Feld **Wert** im **Fenster Eigenschaften**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Kompilieren und Verteilen des freigegebenen Add-ins

Zum Kompilieren des verwalteten COM-Add-Ins zu Testzwecken auf dem Computer, auf dem das FreigeGebene Add-in-Projekt entwickelt wurde, klicken Sie im projektMappen-Explorer mit der rechten Maustaste auf den Stammknoten des freigegebenen Add-in-Projekts, und klicken Sie auf erstellen. Wenn das Projekt ohne Fehler erstellt wird, können Sie die InfoPath-Bearbeitungsumgebung starten und mit der Verwendung des verwalteten COM-Add-ins beginnen. Wenn Sie eine Instanz von InfoPath haben, schließen Sie Sie, bevor Sie das Projekt erstellen. Möglicherweise muss auch das Dialogfeld COM-Add-Ins geöffnet werden, um zu überprüfen, ob das COM-Add-in registriert ist. Gehen Sie folgendermaßen vor, um das Dialogfeld COM-Add-Ins zu öffnen:
  
1. Öffnen Sie die InfoPath-Bearbeitungsumgebung. Die einfachste Möglichkeit hierzu ist das Öffnen einer vorhandenen Formularvorlage, mit der ein neues Formular erstellt wird, das auf dieser Formularvorlage basiert.
    
2. Klicken Sie im Menü **Extras** auf **Vertrauensstellungs Center** . 
    
3. Klicken Sie Links auf die Kategorie **Add-ins** . 
    
4. Wählen Sie im Abschnitt **Verwalten** am unteren Rand des Dialogfelds **Vertrauensstellungs Center** die Option **com-Add-ins** aus der Liste aus, und klicken Sie auf die Schaltfläche **Gehe** zu. 
    
5. Im Dialogfeld **com-Add-ins** wird der Name des kürzlich erstellten Add-Ins angezeigt, und daneben sollte ein Kontrollkästchen vorhanden sein. Wenn kein Kontrollkästchen angezeigt wird, konnte das COM-Add-in aufgrund eines Fehlers nicht geladen werden, der im Abschnitt **Ladeverhalten** des Dialogfelds aufgeführt wird. 
    
Zum Kompilieren des verwalteten COM-Add-Ins zur Verwendung auf einem anderen Computer als dem Computer, auf dem das FreigeGebene Add-in-Projekt entwickelt wurde, müssen Sie zusätzliche Schritte ausführen, um den Code zu sichern. Informationen zum Sichern von Projekten für FreigeGebene Add-Ins zur Verwendung auf anderen Computern finden Sie in den folgenden drei Artikeln:
  
- [Bereitstellung von verwalteten COM-Add-Ins in Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Verwenden der COM-Add-in-Shimlösung zum Bereitstellen von verwalteten COM-Add-Ins in Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolieren von Office-Erweiterungen mit dem COM-Shim-Assistenten](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Das nicht isolieren des COM-Add-Ins kann zu Speicherlecks und Anwendungsinstabilität führen. 
  
> [!NOTE]
> Wenn .NET Framework oder andere erforderliche Assemblys aus dem Setup-Projekt nicht bereits auf den Zielcomputern installiert sind, wird die MSI-Datei möglicherweise nicht richtig installiert. Außerdem können Sie die MSI-Datei nicht verteilen und dann versuchen, die MSI-Datei zu installieren. Außerdem müssen Sie die anderen Supportdateien im selben Ordner wie die von Visual Studio generierte Original-MSI-Datei verteilen. 
  
## <a name="coding-in-the-com-add-in"></a>Codieren im COM-Add-in

Anwendungsereignisse, die in der InfoPath-Formularbearbeitungsumgebung auftreten, können von einem COM-Add-in erfasst werden. Die folgenden Ereignisse des [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) -Objekts können vom COM-Add-in verwendet werden, um auf Benutzeraktionen zu reagieren: 
  
|**Event**|**Beschreibung**|
|:-----|:-----|
|[Neuxdocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Ereignis  <br/> |Tritt ein, wenn ein neues Formular erstellt wird.  <br/> |
|[Beenden](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Ereignis  <br/> |Tritt ein, wenn der Benutzer InfoPath beendet.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Ereignis  <br/> |Tritt ein, wenn ein Dokumentfenster aktiviert wird.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Ereignis  <br/> |Tritt ein, wenn ein Dokumentfenster deaktiviert wird.  <br/> |
|[Windowsisieren](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Ereignis  <br/> |Tritt ein, wenn die Größe eines Dokumentfensters geändert wird oder das Dokumentfenster verschoben wird.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Ereignis  <br/> |Tritt unmittelbar vor dem Schließen eines Dokuments ein.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Ereignis  <br/> |Tritt unmittelbar vor dem Drucken eines geöffneten Dokuments auf.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Ereignis  <br/> |Tritt unmittelbar vor dem Speichern eines geöffneten Dokuments auf.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Ereignis  <br/> |Tritt ein, wenn ein neues Formular erstellt wird, wenn ein vorhandenes Formular geöffnet wird oder wenn ein anderes Formular als aktives Formular festgelegt wird.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Ereignis  <br/> |Tritt ein, wenn ein Dokument geöffnet wird.  <br/> |
   
Um diese Ereignisse im COM-Add-in aufzuzeichnen, müssen Sie die folgenden Variablen auf Klassenebene in der **Connect** -Klasse deklarieren: 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

Die erste Codezeile wandelt das generische Application- **Objekt** , das vom Add-in empfangen wird, in das [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) -Objekt um. Die zweite Leitung wandelt die [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) -Eigenschaft des **_Application3** -Objekts (dargestellt durch die **InfoPathApplication** -Variable) in das [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) -Objekt um. 
  
Zum Erstellen von Ereignishandlern wählen Sie im Dropdownfeld **Klassenname** oben im Visual Studio-Fenster **InfoPathApplicationEvents** aus, und wählen Sie dann das zu behandelnde Ereignis im Dropdownfeld **methodenName** am oberen Rand des visuellen Studio-Fenster. Wenn Sie beispielsweise steuern möchten, wann ein Formular gespeichert wird, behandeln Sie das **XDocumentBeforeSave** -Ereignis. Durch Auswählen von **XDocumentBeforeSave** aus der Dropdownliste **Methoden Name** wird automatisch das folgende Verfahren eingefügt: 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

Ereignisse des **ApplicationEvents** -Objekts können vom COM-Add-in mit derselben Methode verarbeitet werden. 
  
## <a name="see-also"></a>Siehe auch

- [Erstellen eines Microsoft Office 2000-COM-Add-ins](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Erstellen von Office-verwalteten COM-Add-Ins mit Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Arbeiten mit den IDTExtensibility2-Ereignisprozeduren](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Erstellen eines Office-COM-Add-Ins mit Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Erstellen eines Office-COM-Add-Ins mithilfe von Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Erstellen von InfoPath 2007-Add-Ins mithilfe von Visual Studio 2005 Tools für Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

