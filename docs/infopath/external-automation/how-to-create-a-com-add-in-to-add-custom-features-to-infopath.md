---
title: Erstellen eines COM-Add-Ins zum Hinzufügen benutzerdefinierter Features zu InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, Erstellen von Com-Add-Ins,InfoPath 2007, Hinzufügen benutzerdefinierter Features,COM-Add-Ins [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath unterstützt COM-Add-Ins für die Erweiterung der Benutzerumgebung zum Bearbeiten von Formularen. Obwohl die Unterstützung für COM-Add-Ins zuerst in InfoPath hinzugefügt wurde, unterstützen andere Office-Anwendungen wie Microsoft Office Word und Microsoft Office Excel com-Add-Ins seit Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303787"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Erstellen eines COM-Add-Ins zum Hinzufügen benutzerdefinierter Features zu InfoPath

Microsoft InfoPath unterstützt COM-Add-Ins für die Erweiterung der Benutzerumgebung zum Bearbeiten von Formularen. Obwohl die Unterstützung für COM-Add-Ins zuerst in InfoPath hinzugefügt wurde, unterstützen andere Office-Anwendungen wie Microsoft Office Word und Microsoft Office Excel com-Add-Ins seit Office 2000.
  
Com-Add-In-Unterstützung in InfoPath ist für die Formularbearbeitungsumgebung verfügbar. Die Formularentwurfsumgebung kann nicht mithilfe von COM-Add-Ins erweitert werden.
  
## <a name="the-idtextensibility2-interface"></a>Die IDTExtensibility2-Schnittstelle

Die InfoPath-Bearbeitungsumgebung bietet Unterstützung für die **IDTExtensibility2-Schnittstelle,** die von Entwicklern von COM-Add-Ins implementiert werden muss. **IDTExtensibility2** ist ein Objekt mit zwei Schnittstellen, das fünf Methoden zur Verfügung stellt, die in der Bearbeitungsumgebung als Ereignisse fungieren. Mit diesen Methoden kann das COM-Add-In auf Start- und Herunterfahrensbedingungen der Umgebung reagieren, die in der folgenden Tabelle aufgeführt sind. 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Tritt auf, wenn ein Add-In in der Umgebung geladen oder entladen wird.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Tritt auf, wenn die Umgebung heruntergefahren wird.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Tritt auf, wenn ein Add-In in der Umgebung geladen wird.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Tritt auf, wenn ein Add-In aus der Umgebung entladen wird.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Tritt auf, wenn die Umgebung gestartet wurde.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrieren von COM-Add-Ins

Alle Office, einschließlich InfoPath, verwenden die Registrierung, um Add-Ins in der COM Add-Ins-Auflistung auflisten, den Verbindungsstatus zu speichern und die Start- oder Anforderungsladeinformationen zu speichern. Für InfoPath COM-Add-Ins wird der Name der einzelnen Add-Ins unter dem folgenden Schlüssel angezeigt:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Für COM-Add-Ins, die für die Verwendung durch jeden Benutzer des Clientcomputers installiert sind, befindet sich der Registrierungsschlüssel im HKLM-Registrierungsstruktur:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Der Registrierungsschlüsselname entspricht dem **ProgIdAttribute** des Add-Ins und enthält die folgenden Werte. 
  
|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Der Name, der im Dialogfeld **COM-Add-Ins** angezeigt und auf der **Seite Add-Ins** im **Trust Center aufgeführt ist.**  <br/> |
|**Beschreibung** <br/> |**String** <br/> |Die Zeichenfolge, die angezeigt wird, wenn das Add-In im **Trust Center ausgewählt ist.**  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Gibt an, wie das COM-Add-In geladen wird. Der Wert kann eine Kombination aus 0, 1, 2, 8 und 16 sein. Weitere Informationen finden Sie in der folgenden Tabelle.  <br/> |
   
Der **DWORD-Wert** für **LoadBehavior** sollte einen Wert enthalten, der beschreibt, wie das COM-Add-In in der Bearbeitungsumgebung geladen wird. Der Wert kann aus der folgenden Tabelle oder einer Kombination von Werten aus der Tabelle sein. Ein com-Add-In, das in Visual Studio 2005 erstellt wurde, wird beispielsweise beim Starten der Anwendung mit dem **LoadBehavior** "3" geladen und verbunden. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Getrennt. Das Add-In wird im Dialogfeld **COM-Add-In** als inaktiv angezeigt.  <br/> |
|1  <br/> |Verbunden. Das Add-In wird im Dialogfeld **COM-Add-In** als aktiv angezeigt.  <br/> |
|2  <br/> |Beim Start laden. Das Add-In wird geladen und verbunden, wenn die Hostanwendung gestartet wird.  <br/> |
|8   <br/> |Load on Demand. Das Add-In wird geladen und verbunden, wenn die Hostanwendung dies erfordert, z. B. wenn ein Benutzer auf eine Schaltfläche klickt, die Funktionen im Add-In verwendet.  <br/> |
|16   <br/> |Verbindung bei der ersten Ausführung. Das Add-In wird geladen und verbunden, wenn der Benutzer die Hostanwendung nach der Registrierung des Add-Ins zum ersten Mal ausgeführt hat.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Erstellen eines verwalteten COM-Add-Ins mit Visual Studio 2005 oder Visual Studio 2008

Um ein verwaltetes COM-Add-In mithilfe von Microsoft Visual Studio 2005 oder Visual Studio 2008 zu erstellen, erstellen Sie ein freigegebenes Add-In-Projekt wie folgt: 
  
1. Starten Sie Visual Studio.
    
2. Klicken Sie im Menü **Datei** auf **Neues Projekt**.
    
3. Klicken Sie Project **im** Dialogfeld Neue **Project** auf den Ordner  Andere Projekttypen, und klicken Sie dann auf **Erweiterbarkeit**.
    
4. Klicken Sie **im Bereich** Vorlagen auf **Freigegebenes Add-In**.
    
5. Geben Sie **im Feld Name** einen Namen für das Projekt ein. 
    
6. Geben Sie **im Feld Speicherort** einen Ordnerpfad ein, oder klicken Sie auf **Durchsuchen,** und wählen Sie einen Ordnerpfad aus, und klicken Sie dann auf **OK**. Der **Assistent für freigegebene Add-Ins** wird angezeigt. 
    
7. Klicken **Sie im** Assistenten für **freigegebene Add-Ins** auf Weiter. Die **Seite Programmiersprache auswählen** wird angezeigt. 
    
8. Klicken **Sie auf Add-In mithilfe von Visual Basic** erstellen, und klicken Sie dann auf **Weiter**. Die **Seite Anwendungshost auswählen** wird angezeigt. 
    
9. Deaktivieren Sie die Kontrollkästchen neben jeder Anwendung mit Ausnahme **von Microsoft InfoPath,** und klicken Sie dann auf **Weiter**. Die **Seite Name und Beschreibung eingeben** wird angezeigt. 
    
10. Geben Sie **in das Feld Was ist der Name Ihres Add-Ins** ein, den Namen Ihres COM-Add-Ins ein. 
    
11. Geben Sie im Feld Was ist die Beschreibung Ihres Add-Ins ein, die Beschreibung für Ihr **COM-Add-In** ein, und klicken Sie auf **Weiter**. Die **Seite Add-In Optionen** auswählen wird angezeigt. 
    
12. Überprüfen Sie, ob mein **Add-In** geladen werden soll, wenn die Hostanwendung geladen wird, und **Mein Add-In** sollte für alle Benutzer des Computers verfügbar sein, auf dem es installiert wurde, nicht nur für die Person, die es installiert hat. 
    
13. Klicken **Sie auf Weiter,** um die **Seite Zusammenfassung** zu überprüfen, und klicken Sie dann auf Fertig **stellen**.
    
Nachdem das Projekt von Visual Studio erstellt wurde, werden zwei Projekte im Fenster Projektmappen-Explorer angezeigt. Das erste Projekt ist das Projekt für das COM-Add-In. Das zweite Projekt ist ein Setupprojekt für die Bereitstellung des COM-Add-Ins. Der Assistent für freigegebene **Add-Ins** fügt nur einen Verweis auf die **Microsoft Office 14.0-Objektbibliothek** ein. Daher muss mithilfe der folgenden Schritte ein Verweis auf die InfoPath-Objektbibliothek eingefügt werden:
  
1. Doppelklicken Sie auf **Meine Project,** um die Add-In-Projekteigenschaften anzeigen zu können. Klicken Sie auf **die** Registerkarte Verweise, um die Dem Projekt automatisch hinzugefügten Verweise anzeigen zu können. 
    
2. Klicken Sie auf **die** Schaltfläche Hinzufügen, um das **Dialogfeld Verweis** hinzufügen anzuzeigen. 
    
3. **Doppelklicken** Sie auf der Registerkarte COM auf **Microsoft.InfoPath 2.0 Type Library,** und klicken Sie auf **OK**.
    
4. Durch hinzufügen eines Verweises auf die **Microsoft InfoPath 3.0-Typbibliothek** werden auch Verweise auf drei Assemblys hinzugefügt, die entfernt werden müssen: **ADODB**, **MSHTML** und **MSXML2**. Klicken **Sie im** Projektmappen-Explorer unter **Verweise** mit der rechten Maustaste auf jeden dieser Verweise, und klicken Sie dann auf **Entfernen**.
    
## <a name="viewing-the-registry-settings"></a>Anzeigen der Registrierungseinstellungen Einstellungen

Führen Sie die folgenden Schritte aus, um die Registrierungseinstellungen anzeigen zu können, die bei der Installation des COM-Add-Ins erstellt werden:
  
1. Klicken Sie mit der rechten Maustaste auf den Stammknoten des Setupprojekts im **Projektmappen-Explorer,** klicken Sie auf **Ansicht,** dann **Editor** und dann auf **Registrierung**.
    
2. Klicken Sie im linken Bereich auf das Plus, um **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath** und **dann AddIns zu erweitern.**
    
3. Klicken Sie auf den Namen, der der **ProgID** Ihres freigegebenen Add-In-Projekts entspricht.
    
Klicken Sie zum Ändern dieser Eigenschaften mit der rechten Maustaste auf die Eigenschaft, klicken Sie auf Eigenschaftenfenster, und ändern Sie das Feld **Wert** im **Eigenschaftenfenster**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Kompilieren und Verteilen der freigegebenen Add-In

Klicken Sie zum Kompilieren des verwalteten COM-Add-Ins zu Testzwecken auf dem Computer, auf dem das Shared Add-In-Projekt entwickelt wurde, mit der rechten Maustaste auf den Stammknoten des Projekts Shared Add-In im Projektmappen-Explorer, und klicken Sie auf Erstellen. Wenn das Projekt ohne Fehler erstellt wird, können Sie die InfoPath-Bearbeitungsumgebung starten und mit der Verwendung des verwalteten COM-Add-Ins beginnen. Wenn eine Instanz von InfoPath ausgeführt wird, schließen Sie sie, bevor Sie das Projekt erstellen. Es kann auch erforderlich sein, das Dialogfeld COM-Add-Ins zu öffnen, um zu überprüfen, ob das COM-Add-In registriert ist. Führen Sie die folgenden Schritte aus, um das Dialogfeld COM-Add-Ins zu öffnen:
  
1. Öffnen Sie die InfoPath-Bearbeitungsumgebung. Die einfachste Möglichkeit dazu ist das Öffnen einer vorhandenen Formularvorlage, die ein neues Formular basierend auf dieser Formularvorlage erstellt.
    
2. Klicken **Sie im** Menü **Extras** auf Vertrauensstellungscenter. 
    
3. Klicken Sie auf der linken Seite auf die Kategorie **Add-Ins.** 
    
4. Wählen Sie **im Abschnitt** Verwalten am unteren Rand des Dialogfelds **Vertrauensstellungscenter** die Option **COM-Add-Ins aus** der Liste aus, und klicken Sie auf die Schaltfläche **Los.** 
    
5. Im Dialogfeld **COM-Add-Ins** wird der Name Des kürzlich erstellten Add-Ins angezeigt, und daneben sollte ein Kontrollkästchen angezeigt werden. Wenn kein Kontrollkästchen daneben ist, konnte das COM-Add-In aufgrund eines Fehlers nicht geladen werden, der im Abschnitt **Load Behavior** des Dialogfelds aufgeführt wird. 
    
Zum Kompilieren des verwalteten COM-Add-Ins für die Verwendung auf einem anderen Computer als dem Computer, auf dem das Shared Add-In-Projekt entwickelt wurde, müssen Sie zusätzliche Schritte ausführen, um Den Code zu sichern. Informationen zum Sichern freigegebener Add-In für die Verwendung auf anderen Computern finden Sie in den folgenden drei Artikeln:
  
- [Bereitstellung von verwalteten COM-Add-Ins in Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Verwenden der COM-Add-In-Shim-Lösung zum Bereitstellen verwalteter COM-Add-Ins in Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolieren Office Erweiterungen mit dem COM Shim-Assistenten](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Die Nichtisolierung des COM-Add-Ins kann zu Speicherverlusten und Anwendungsinstabilität führen. 
  
> [!NOTE]
> Wenn die .NET Framework oder andere erforderliche Assemblys aus dem Setupprojekt nicht bereits auf Zielcomputern installiert sind, wird die .msi möglicherweise nicht ordnungsgemäß installiert. Außerdem können Sie die Datei nicht .msi verteilen und dann versuchen, die Datei .msi installieren. Sie müssen auch die anderen Supportdateien im gleichen Ordner wie die ursprüngliche .msi verteilen, die von Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codieren im COM-Add-In

Anwendungsereignisse, die in der InfoPath-Formularbearbeitungsumgebung auftreten, können von einem COM-Add-In erfasst werden. Die folgenden Ereignisse des [ApplicationEvents-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) können vom COM-Add-In verwendet werden, um auf Benutzeraktionen zu reagieren: 
  
|**Event**|**Beschreibung**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Ereignis  <br/> |Tritt ein, wenn ein neues Formular erstellt wird.  <br/> |
|[Beenden](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Ereignis  <br/> |Tritt ein, wenn der Benutzer InfoPath beendet.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Ereignis  <br/> |Tritt ein, wenn ein Dokumentfenster aktiviert wird.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Ereignis  <br/> |Tritt ein, wenn ein Dokumentfenster deaktiviert wird.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Ereignis  <br/> |Tritt ein, wenn die Größe eines Dokumentfensters geändert wird oder das Dokumentfenster verschoben wird.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Ereignis  <br/> |Tritt unmittelbar vor dem Schließen eines Dokuments ein.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Ereignis  <br/> |Tritt unmittelbar vor dem Drucken eines geöffneten Dokuments auf.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Ereignis  <br/> |Tritt unmittelbar vor dem Speichern eines geöffneten Dokuments auf.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Ereignis  <br/> |Tritt ein, wenn ein neues Formular erstellt wird, wenn ein vorhandenes Formular geöffnet wird oder wenn ein anderes Formular als aktives Formular festgelegt wird.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Ereignis  <br/> |Tritt ein, wenn ein Dokument geöffnet wird.  <br/> |
   
Um diese Ereignisse im COM-Add-In **zu** erfassen, müssen Sie die folgenden Variablen auf Klassenebene in Ihrer Verbinden deklarieren: 
  
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

In der ersten Zeile wird die generische Anwendung **Object,** die vom Add-In empfangen wird, in das [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) werden. In der zweiten Zeile wird die [Events-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) des **_Application3** -Objekts (dargestellt durch die **InfoPathApplication-Variable)** in das [ApplicationEvents-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) um. 
  
Zum Erstellen von Ereignishandlern wählen Sie **infoPathApplicationEvents** im Dropdownfeld Klassenname oben im Visual Studio-Fenster aus, und wählen  Sie dann das Ereignis aus, das Sie behandeln möchten, im Dropdownfeld Methodenname oben im Visual Studio-Fenster.  Wenn Sie beispielsweise steuern müssen, wann ein Formular gespeichert wird, behandeln Sie das **XDocumentBeforeSave-Ereignis.** Wenn **Sie XDocumentBeforeSave aus** der Dropdownliste Methodenname auswählen, wird automatisch das folgende Verfahren eingefügt:  
  
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

Alle Ereignisse des **ApplicationEvents-Objekts** können vom COM-Add-In mit derselben Methode behandelt werden. 
  
## <a name="see-also"></a>Siehe auch

- [Erstellen eines Microsoft Office 2000 COM-Add-Ins](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Erstellen Office verwalteter COM-Add-Ins mit Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Arbeiten mit den IDTExtensibility2-Ereignisprozeduren](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Erstellen eines Office COM-Add-Ins mit Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Erstellen eines Office COM-Add-Ins mithilfe von Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Erstellen von InfoPath 2007 Add-Ins mithilfe Visual Studio 2005-Tools für Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

