---
title: Erstellen eines COM-Add-Ins zum Hinzufügen von benutzerdefinierten Funktionen in InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, Erstellen von COM-add-ins und InfoPath 2007, Hinzufügen von benutzerdefinierten Funktionen, COM-add-ins [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath unterstützt COM-Add-ins zur Erweiterung des Formulars Benutzererlebnis bearbeiten. Obwohl die Unterstützung für COM-Add-ins in InfoPath, andere Office-Clientanwendungen zuerst hinzugefügt wurde, wie Microsoft Office Word und Microsoft Office Excel COM-add-ins seit Office 2000 unterstützt haben.
ms.openlocfilehash: 4c70dfb71cf7b15a0978b4567ffac02a8ba524c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790636"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Erstellen eines COM-Add-Ins zum Hinzufügen von benutzerdefinierten Funktionen in InfoPath

Microsoft InfoPath unterstützt COM-Add-ins zur Erweiterung des Formulars Benutzererlebnis bearbeiten. Obwohl die Unterstützung für COM-Add-ins in InfoPath, andere Office-Clientanwendungen zuerst hinzugefügt wurde, wie Microsoft Office Word und Microsoft Office Excel COM-add-ins seit Office 2000 unterstützt haben.
  
COM-Add-in-Unterstützung in InfoPath ist für das Formular bearbeiten einer Umgebung zur Verfügung. Die Formular-Design-Umgebung kann nicht mithilfe von COM-Add-ins erweitert werden.
  
## <a name="the-idtextensibility2-interface"></a>Der IDTExtensibility2-Schnittstelle

Die InfoPath-Umgebung zum Bearbeiten der **IDTExtensibility2** -Schnittstelle unterstützt die von Entwicklern von COM-Add-Ins **IDTExtensibility2** implementiert werden müssen, ist ein Dual-Schnittstelle-Objekt, das fünf Methoden bereitstellt, die als Ereignisse fungieren innerhalb der Umgebung bearbeiten. Diese Methoden ermöglichen das COM-add-in zur Beantwortung der Umgebung starten und Herunterfahren Situationen, in der folgenden Tabelle aufgeführt. 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() als Variant-Wert)** <br/> |Tritt auf, wenn ein Add-In geladen oder entladen wird in der Umgebung.  <br/> |
|**Geladen (ByVal custom() als Variant-Wert)** <br/> |Tritt auf, wenn die Umgebung heruntergefahren wird.  <br/> |
|**OnConnection (ByVal als Anwendungsobjekt, ByVal ConnectMode als Ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() als Variant)** <br/> |Tritt auf, wenn ein Add-in, in der Umgebung geladen wird.  <br/> |
|**OnDisconnection (ByVal RemoveMode als Ext_DisconnectMode, ByVal custom() als Variant)** <br/> |Tritt auf, wenn ein Add-in aus der Umgebung entladen wird.  <br/> |
|**OnStartupComplete (ByVal custom() als Variant-Wert)** <br/> |Tritt auf, wenn die Umgebung starten abgeschlossen ist.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrieren des COM-Add-ins

Alle Office-Clientanwendungen, InfoPath, einschließlich verwenden die Registrierung, um die Liste-add-ins in der Auflistung COM-Add-Ins Sie zum Speichern von des Verbindungsstatus und zum Speichern der Start- oder bei Bedarf laden Informationen. Für InfoPath-COM-Add-ins, wird der Name der einzelnen Add-Ins angezeigt, unter dem folgenden Schlüssel:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Für COM-Add-ins für die Verwendung von jedem Benutzer des Clientcomputers installiert, befindet sich der Registrierungsschlüssel in der Registrierungsstruktur HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Der Name des Registrierungsschlüssels entspricht **ProgIdAttribute** des Add-Ins und enthält die folgenden Werte. 
  
|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Der Name, der im Dialogfeld **COM-Add-ins** angezeigt und in die Seite **-Add-ins** im **Sicherheitscenter**aufgeführt ist.  <br/> |
|**Beschreibung** <br/> |**String** <br/> |Die Zeichenfolge, die angezeigt wird, wenn das Add-in im **Trust Center**ausgewählt ist.  <br/> |
|**LoadBehavior** <br/> |**EIN DWORD-WERT** <br/> |Gibt an, wie das COM-Add-in geladen ist. Der Wert kann eine Kombination von 0, 1, 2, 8 und 16 sein. Siehe Tabelle unten für Weitere Informationen.  <br/> |
   
Der **DWORD-** Wert für **LoadBehavior** sollte einen Wert in der Bearbeitung Umgebung wie das COM-Add-in geladen, beschreibt enthalten. Der Wert kann aus der folgenden Tabelle oder eine Kombination von Werten aus der Tabelle entsprechen. Zum Beispiel erstellt ein COM-Add-in in Visual Studio 2005 müssen beim Starten der Anwendung eine **LoadBehavior** "3" geladen und verbunden sein. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Getrennt. Das Add-in zeigt als inaktiv im Dialogfeld **COM-Add-in** .  <br/> |
|1  <br/> |Verbunden. Das Add-in zeigt als aktiv im Dialogfeld **COM-Add-in** .  <br/> |
|2  <br/> |Beim Start laden. Das Add-in ist geladen und beim Starten der hostanwendung verbunden.  <br/> |
|8  <br/> |Bei Bedarf laden. Das Add-In wird geladen und verbunden, wenn die Host-Anwendung ist, beispielsweise notwendig Wenn ein Benutzer auf eine Schaltfläche klickt, die in der Add-in-Funktionen verwendet.  <br/> |
|16  <br/> |Verbinden Sie beim ersten Mal. Das Add-In wird geladen und verbunden erstmalig der Benutzer die Host-Anwendung nach dem registrieren das Add-in ausgeführt wird.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Erstellen eines verwalteten COM-Add-Ins mit Visual Studio 2005 oder Visual Studio 2008

Um ein verwaltetes COM-add-Ins mithilfe von Microsoft Visual Studio 2005 oder Visual Studio 2008, erstellen Sie ein gemeinsames Add-In-Projekt wie folgt: 
  
1. Starten Sie Visual Studio.
    
2. Klicken Sie im Menü **Datei** auf **Neues Projekt**.
    
3. Klicken Sie im Bereich **Projekttypen** im Dialogfeld **Neues Projekt** auf den Ordner **Andere Projekttypen** , und klicken Sie dann auf **Erweiterbarkeit**.
    
4. Klicken Sie im Bereich **Vorlagen** auf **Gemeinsames Add-in**.
    
5. Geben Sie im Feld **Name** einen Namen für das Projekt ein. 
    
6. Geben Sie im Feld **Speicherort** einen Ordnerpfad oder klicken Sie auf **Durchsuchen** und wählen Sie einen Ordnerpfad und klicken Sie dann auf **OK**. Der **Assistent für gemeinsames Add-in** wird angezeigt. 
    
7. Klicken Sie auf **nächste** in der **Assistent für gemeinsames Add-in**. Die Seite **Wählen Sie eine Programmiersprache** wird angezeigt. 
    
8. Klicken Sie auf **ein Add-in mit Visual Basic**und dann auf **Weiter**. Die Seite **Wählen Sie einen Anwendungshost** wird angezeigt. 
    
9. Deaktivieren Sie die Kontrollkästchen neben jedem Anwendung außer **Microsoft InfoPath**, und klicken Sie dann auf **Weiter**. Die Seite **Geben Sie einen Namen und eine Beschreibung** wird angezeigt. 
    
10. Geben Sie im Feld **wie lautet der Name des Add-In** den Namen des Ihre COM-Add-Ins. 
    
11. Geben Sie im Feld **Beschreibung von Ihrem Add-in -** die Beschreibung für die COM-Add-in, und klicken Sie auf **Weiter**. Die Seite **Wählen Sie die Add-In-Optionen** wird angezeigt. 
    
12. Das Kontrollkästchen Sie **ich würde gerne Add-In laden, wenn die hostanwendung geladen wird** und Feldern **sollte Add-In für alle Benutzer des Computers an, die er nicht nur die Person installiert wurde, die sie installiert, verfügbar sein** . 
    
13. Klicken Sie auf **Weiter** , um der Seite **Zusammenfassung** der überprüfen und dann auf **Fertig stellen**.
    
Nachdem das Projekt von Visual Studio erstellt wurde, werden zwei Projekte im Projektmappen-Explorer-Fenster angezeigt. Das erste Projekt ist das Projekt für das COM-Add-in. Das zweite Projekt ist ein Setup-Projekt für das COM-Add-in bereitstellen. Den **Assistenten für gemeinsames Add-in -** fügt nur einen Verweis auf die **Microsoft Office 14.0-Objektbibliothek**, so dass es notwendig ist, fügen Sie einen Verweis auf die InfoPath-Objektbibliothek mit den folgenden Schritten:
  
1. Doppelklicken Sie auf **Mein Projekt** , um die Add-in-Projekteigenschaften anzuzeigen. Klicken Sie auf der Registerkarte **Referenzen** zum Anzeigen der Verweise automatisch dem Projekt hinzugefügt. 
    
2. Klicken Sie auf die Schaltfläche **Hinzufügen** , um das Dialogfeld **Verweis hinzufügen** angezeigt. 
    
3. Doppelklicken Sie auf **Microsoft.InfoPath 2.0-Typenbibliothek**auf der Registerkarte **COM** , und klicken Sie auf **OK**.
    
4. Hinzufügen eines Verweises auf die **Typbibliothek von Microsoft InfoPath 3.0** Verweise auf drei Assemblys, die entfernt werden, müssen auch hinzugefügt: **ADODB** **MSHTML**und **MSXML2**. Klicken Sie im **Projektmappen-Explorer** unter **Verweise**Maustaste auf jeden dieser Verweise, und klicken Sie dann auf **Entfernen**.
    
## <a name="viewing-the-registry-settings"></a>Anzeigen von Registrierungseinstellungen

Um die registrierungseinstellungen anzuzeigen, die erstellt werden, wenn das COM-Add-in installiert ist, gehen Sie folgendermaßen vor:
  
1. Klicken Sie auf den Stammknoten des Setup-Projekts im **Projektmappen-Explorer**, klicken Sie auf **Ansicht**, klicken Sie dann- **Editor**, und klicken Sie auf **Registrierung**.
    
2. Klicken Sie im linken Bereich auf das Pluszeichen, um **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath**und dann **Add-Ins**zu erweitern.
    
3. Klicken Sie auf den Namen Ihres freigegebenen Add-In-Projekts **ProgID**entspricht.
    
Um diese Eigenschaften zu ändern, mit der rechten Maustaste der-Eigenschaft, klicken Sie **Im Fenster Eigenschaften**auf, und ändern Sie den **Wert** im **Fenster Eigenschaften**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Kompilieren und Verteilen von gemeinsamem Add-in

Zum Kompilieren des verwalteten COM-Add-Ins zu Testzwecken auf dem Computer, auf dem das gemeinsames Add-In-Projekt entwickelt wurde, klicken Sie auf den Stammknoten des Shared-Add-In-Projekts im Projektmappen-Explorer, und klicken Sie auf erstellen. Wenn das Projekt ohne Fehler erstellt wird, können Sie die Bearbeitung InfoPath-Umgebung zu starten und Verwenden des verwalteten COM-Add-Ins. Wenn Sie eine Instanz von InfoPath ausgeführt haben, schließen sie vor dem Erstellen des Projekts. Es ist auch möglich, öffnen Sie das Dialogfeld COM-Add-ins, um sicherzustellen, dass das COM-Add-in registriert ist. Gehen Sie folgendermaßen vor, um das Dialogfeld COM-Add-ins zu öffnen:
  
1. Öffnen Sie die Bearbeitung InfoPath-Umgebung. Die einfachste Möglichkeit hierzu ist zum Öffnen einer vorhandenen Formularvorlage, die basierend auf dieser Formularvorlage ein neues Formular erstellt wird.
    
2. Klicken Sie im Menü **Extras** auf **Sicherheitscenter** . 
    
3. Klicken Sie auf die Kategorie **-Add-ins** auf der linken Seite. 
    
4. Wählen Sie im Abschnitt **Verwalten** im unteren Bereich des Dialogfelds **Sicherheitscenter** aus der Liste **COM-Add-ins** , und klicken Sie auf die Schaltfläche **Gehe zu** . 
    
5. Klicken Sie im Dialogfeld **COM-Add-ins** sehen Sie den Namen des Ihr Add-in vor kurzem erstellten und sollte ein Kontrollkästchen vorhanden sein. Wenn keine Kontrollkästchen vorhanden ist, konnte nicht das COM-Add-in aufgrund eines Fehlers zu laden, das im Abschnitt **Verhalten laden** des Dialogfelds aufgeführt wird. 
    
Um die verwalteten COM-add-in für die Verwendung auf einem anderen Computer als dem Computer zu kompilieren auf dem das gemeinsames Add-In-Projekt entwickelt wurde, müssen Sie zusätzliche Schritte zum Sichern des Codes ausführen. Informationen zum Sichern von gemeinsames Add-in-Projekte für die Verwendung auf anderen Computern finden Sie unter den folgenden drei Artikeln:
  
- [Bereitstellung von verwalteten COM-Add-Ins in Office XP](http://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Verwenden die COM-Add-in-Shim-Lösung zum Bereitstellen von verwalteten COM-Add-ins in Office XP](http://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolieren von Office-Erweiterungen mit COM Shim-Assistenten](http://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Isolieren von nicht das COM-Add-in kann Speicherverluste und Anwendung instabil führen. 
  
> [!NOTE]
> Wenn .NET Framework oder andere erforderliche Assemblys aus dem Setup-Projekt noch nicht auf den Zielcomputern installiert sind, wird die MSI-Datei möglicherweise nicht ordnungsgemäß installiert. Darüber hinaus nicht verteilen Sie die MSI-Datei und dann versuchen, die MSI-Datei installieren. Sie müssen auch die anderen Unterstützungsdateien im gleichen Ordner wie die ursprüngliche MSI-Datei, die von Visual Studio generierte verteilen. 
  
## <a name="coding-in-the-com-add-in"></a>Codieren im COM-Add-Ins

Anwendungsereignisse, die in der InfoPath-formularbearbeitungsumgebung auftreten können mithilfe eines COM-Add-Ins erfasst werden. Die folgenden Ereignisse des [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) -Objekts können mithilfe des COM-Add-Ins auf Benutzeraktionen reagieren verwendet werden: 
  
|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
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
   
Um diese Ereignisse in der COM-Add-in zu erfassen, müssen Sie in der **Connect** -Klasse die folgenden Variablen auf Klassenebene deklarieren: 
  
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

Die erste Zeile in der **durch das Add-in das Objekt [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) empfangene** allgemeine Anwendungsobjekt umwandelt. Die zweite Zeile wandelt die [Ereignisse](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) -Eigenschaft des Objekts **_Application3** (dargestellt durch die Variable **InfoPathApplication** ) auf das [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) -Objekt. 
  
So erstellen Sie Ereignishandler, wählen Sie **InfoPathApplicationEvents** aus dem Dropdown-Feld **Klassenname** , im oberen Bereich des Visual Studio-Fensters, und wählen Sie dann das Ereignis im Dropdown- **Methodenname** im oberen Bereich des visuellen behandeln möchten Studio-Fenster. Wenn Sie möchten steuern, wenn ein Formular gespeichert wird, behandeln Sie das **XDocumentBeforeSave** -Ereignis. Fügt ein **XDocumentBeforeSave** automatisch aus der Dropdownliste **Methodennamen** auswählen die folgende Schritte aus: 
  
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

Eines der Ereignisse des **ApplicationEvents** -Objekts kann mithilfe der COM-Add-in mit demselben Verfahren behandelt werden. 
  
## <a name="see-also"></a>Siehe auch

- [Erstellen eine Microsoft Office 2000 COM-Add-in](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [Erstellen von Office verwalteten COM-Add-Ins mit Visual Studio .NET](http://go.microsoft.com/fwlink/?LinkID=73470)
- [Arbeiten mit der IDTExtensibility2-Ereignisprozeduren](http://go.microsoft.com/fwlink/?LinkID=73471)
- [Erstellen eines Office COM-Add-Ins mit Visual Basic .NET](http://go.microsoft.com/fwlink/?LinkID=73469)
- [Erstellen eines Office COM-Add-Ins mit Visual c#](http://go.microsoft.com/fwlink/?LinkID=73472)
- [Erstellen von InfoPath 2007-Add-Ins mithilfe von Visual Studio 2005-Tools für Office System SE (engl.)](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)

