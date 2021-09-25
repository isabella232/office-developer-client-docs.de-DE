---
title: Erstellen eines COM-Add-Ins zum Hinzufügen von benutzerdefinierten Features zu InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, creating com add-ins,InfoPath 2007, adding custom features,COM add-ins [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath unterstützt COM-Add-Ins für die Erweiterung der Benutzerumgebung zum Bearbeiten von Formularen. Obwohl die Unterstützung für COM-Add-Ins zuerst in InfoPath hinzugefügt wurde, unterstützen andere Office-Anwendungen wie Microsoft Office Word und Microsoft Office Excel seit Office 2000 COM-Add-Ins.
ms.openlocfilehash: b53d14f637b8f2bd6b8accdf45a331f674a7d91a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552115"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Erstellen eines COM-Add-Ins zum Hinzufügen von benutzerdefinierten Features zu InfoPath

Microsoft InfoPath unterstützt COM-Add-Ins für die Erweiterung der Benutzerumgebung zum Bearbeiten von Formularen. Obwohl die Unterstützung für COM-Add-Ins zuerst in InfoPath hinzugefügt wurde, unterstützen andere Office-Anwendungen wie Microsoft Office Word und Microsoft Office Excel seit Office 2000 COM-Add-Ins.
  
Die COM-Add-In-Unterstützung in InfoPath ist für die Formularbearbeitungsumgebung verfügbar. Die Formularentwurfsumgebung kann nicht mithilfe von COM-Add-Ins erweitert werden.
  
## <a name="the-idtextensibility2-interface"></a>Die IDTExtensibility2-Schnittstelle

Die InfoPath-Bearbeitungsumgebung bietet Unterstützung für die **IDTExtensibility2-Schnittstelle,** die von Entwicklern von COM-Add-Ins implementiert werden muss. **IDTExtensibility2** ist ein Objekt mit zwei Schnittstellen, das fünf Methoden bereitstellt, die als Ereignisse innerhalb der Bearbeitungsumgebung fungieren. Diese Methoden ermöglichen es dem COM-Add-In, auf start- und herunterfahrende Umgebungsbedingungen zu reagieren, die in der folgenden Tabelle aufgeführt sind. 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Tritt auf, wenn ein Add-In in der Umgebung geladen oder entladen wird.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Tritt auf, wenn die Umgebung heruntergefahren wird.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Tritt auf, wenn ein Add-In in der Umgebung geladen wird.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Tritt auf, wenn ein Add-In aus der Umgebung entladen wird.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Tritt auf, wenn der Start der Umgebung abgeschlossen ist.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrieren von COM-Add-Ins

Alle Office-Anwendungen, einschließlich InfoPath, verwenden die Registrierung zum Auflisten von Add-Ins in der COM-Add-Ins-Auflistung, zum Speichern des Verbindungsstatus und zum Speichern der Start- oder Anforderungsladeinformationen. Bei InfoPath-COM-Add-Ins wird der Name jedes Add-Ins unter dem folgenden Schlüssel angezeigt:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Für COM-Add-Ins, die zur Verwendung durch jeden Benutzer des Clientcomputers installiert sind, befindet sich der Registrierungsschlüssel in der HKLM-Registrierungsstruktur:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Der Name des Registrierungsschlüssels entspricht dem **ProgIdAttribute** des Add-Ins und enthält die folgenden Werte. 
  
|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Der Name, der im Dialogfeld **COM-Add-Ins** angezeigt und auf der **Add-Ins-Seite** des **Sicherheitscenters** aufgeführt wird.  <br/> |
|**Beschreibung** <br/> |**String** <br/> |Die Zeichenfolge, die angezeigt wird, wenn das Add-In im **Sicherheitscenter** ausgewählt wird.  <br/> |
|**Loadbehavior** <br/> |**DWORD** <br/> |Gibt an, wie das COM-Add-In geladen wird. Der Wert kann eine Kombination aus 0, 1, 2, 8 und 16 sein. Weitere Informationen finden Sie in der folgenden Tabelle.  <br/> |
   
Der **DWORD-Wert** für **LoadBehavior** sollte einen Wert enthalten, der beschreibt, wie das COM-Add-In in der Bearbeitungsumgebung geladen wird. Der Wert kann aus der folgenden Tabelle oder einer Kombination von Werten aus der Tabelle stammen. Beispielsweise wird für ein com-Add-In, das in Visual Studio 2005 erstellt wurde, der **LoadBehavior** "3" beim Starten der Anwendung geladen und verbunden. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Getrennt. Das Add-In wird im Dialogfeld **COM-Add-In** als inaktiv angezeigt.  <br/> |
|1  <br/> |Verbunden. Das Add-In wird im Dialogfeld **COM-Add-In** als aktiv angezeigt.  <br/> |
|2  <br/> |Beim Start laden. Das Add-In wird geladen und verbunden, wenn die Hostanwendung gestartet wird.  <br/> |
|8   <br/> |Laden bei Bedarf. Das Add-In wird geladen und verbunden, wenn es von der Hostanwendung benötigt wird, z. B. wenn ein Benutzer auf eine Schaltfläche klickt, die Funktionen im Add-In verwendet.  <br/> |
|16   <br/> |Verbindung bei der ersten Ausführung. Das Add-In wird geladen und verbunden, wenn der Benutzer die Hostanwendung nach der Registrierung des Add-Ins zum ersten Mal ausführt.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Erstellen eines verwalteten COM-Add-Ins mit Visual Studio 2005 oder Visual Studio 2008

Um ein verwaltetes COM-Add-In mit Microsoft Visual Studio 2005 oder Visual Studio 2008 zu erstellen, erstellen Sie wie folgt ein freigegebenes Add-In Projekt: 
  
1. Starten Sie Visual Studio.
    
2. Klicken Sie im Menü **Datei** auf **Neues Projekt**.
    
3. Klicken Sie im Dialogfeld **Neue** Project im Bereich Project **Typen** auf den Ordner **Andere** Projekttypen und anschließend auf Erweiterbarkeit. 
    
4. Klicken Sie im Bereich **"Vorlagen"** auf **"Freigegebenes Add-In".**
    
5. Geben Sie im **Feld "Name"** einen Namen für das Projekt ein. 
    
6. Geben Sie im **Feld "Speicherort"** einen Ordnerpfad ein, oder klicken Sie auf **"Durchsuchen",** wählen Sie einen Ordnerpfad aus, und klicken Sie dann auf **"OK".** Der **Assistent für freigegebene Add-Ins** wird angezeigt. 
    
7. Klicken Sie im **Assistenten für freigegebene Add-Ins** auf **"Weiter".** Die Seite **"Programmiersprache auswählen"** wird angezeigt. 
    
8. Klicken Sie auf **"Add-In erstellen" mit Visual Basic,** und klicken Sie dann auf **"Weiter".** Die Seite **"Anwendungshost auswählen"** wird angezeigt. 
    
9. Deaktivieren Sie die Kontrollkästchen neben jeder Anwendung außer **Microsoft InfoPath,** und klicken Sie dann auf **"Weiter".** Die Seite **"Name und Beschreibung eingeben"** wird angezeigt. 
    
10. Geben Sie **im Feld "Was ist der Name des Add-Ins"** den Namen Ihres COM-Add-Ins ein. 
    
11. Geben Sie im **Feld "Was ist die Beschreibung ihres Add-Ins"** die Beschreibung für Ihr COM-Add-In ein, und klicken Sie auf **"Weiter".** Die Seite **"Add-In Optionen auswählen"** wird angezeigt. 
    
12. Überprüfen Sie, ob **mein Add-In geladen werden soll, wenn die Hostanwendung geladen** wird, und **"Mein Add-In" sollte für alle Benutzer des Computers verfügbar sein, auf dem es installiert wurde, nicht nur für die Person, die es installiert.** 
    
13. Klicken Sie auf **"Weiter",** um die Seite **"Zusammenfassung"** zu überprüfen, und klicken Sie dann auf **"Fertig stellen".**
    
Nachdem das Projekt von Visual Studio erstellt wurde, werden im Projektmappen-Explorer zwei Projekte angezeigt. Das erste Projekt ist das Projekt für das COM-Add-In. Das zweite Projekt ist ein Setupprojekt für die Bereitstellung des COM-Add-Ins. Der **Assistent für freigegebene Add-Ins** fügt nur einen Verweis auf die **Microsoft Office 14.0-Objektbibliothek** ein, daher muss mit den folgenden Schritten ein Verweis auf die InfoPath-Objektbibliothek eingefügt werden:
  
1. Doppelklicken Sie auf **"Meine Project",** um die Add-In-Projekteigenschaften anzuzeigen. Klicken Sie auf die Registerkarte **"Verweise",** um die Verweise anzuzeigen, die dem Projekt automatisch hinzugefügt werden. 
    
2. Klicken Sie auf die Schaltfläche **"Hinzufügen",** um das Dialogfeld **"Verweis hinzufügen"** anzuzeigen. 
    
3. Doppelklicken Sie auf der Registerkarte **COM** auf **die Typbibliothek von Microsoft.InfoPath 2.0,** und klicken Sie auf **"OK".**
    
4. Wenn Sie einen Verweis auf die **Microsoft InfoPath 3.0-Typbibliothek** hinzufügen, werden auch Verweise auf drei Assemblys hinzugefügt, die entfernt werden müssen: **ADODB**, **MSHTML** und **MSXML2**. Klicken Sie im **Projektmappen-Explorer** unter **"Verweise"** mit der rechten Maustaste auf jeden dieser Verweise, und klicken Sie dann auf **"Entfernen".**
    
## <a name="viewing-the-registry-settings"></a>Anzeigen des Registrierungs-Einstellungen

Führen Sie die folgenden Schritte aus, um die Registrierungseinstellungen anzuzeigen, die bei der Installation des COM-Add-Ins erstellt werden:
  
1. Klicken Sie im **Projektmappen-Explorer** mit der rechten Maustaste auf den Stammknoten des Setupprojekts, klicken Sie auf **"Anzeigen",** dann auf **"Editor"** und dann auf **"Registrierung".**
    
2. Klicken Sie im linken Bereich auf das Pluszeichen, um **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath** und dann **AddIns** zu erweitern.
    
3. Klicken Sie auf den Namen, der der ProgID Ihres freigegebenen Add-In-Projekts **entspricht.**
    
Klicken Sie zum Ändern dieser Eigenschaften mit der rechten Maustaste auf die Eigenschaft, klicken Sie auf **Eigenschaftenfenster,** und ändern Sie das **Feld Wert** im **Eigenschaftenfenster.**
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Kompilieren und Verteilen der freigegebenen Add-In

Um das verwaltete COM-Add-In zu Testzwecken auf dem Computer zu kompilieren, auf dem das Freigegebene Add-In-Projekt entwickelt wurde, klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den Stammknoten des Projekts "Freigegebenes Add-In", und klicken Sie auf "Erstellen". Wenn das Projekt fehlerfrei erstellt wird, können Sie die InfoPath-Bearbeitungsumgebung starten und mit der Verwendung des verwalteten COM-Add-Ins beginnen. Wenn Sie eine Instanz von InfoPath ausführen, schließen Sie sie, bevor Sie das Projekt erstellen. Es kann auch erforderlich sein, das Dialogfeld COM-Add-Ins zu öffnen, um zu überprüfen, ob das COM-Add-In registriert ist. Führen Sie die folgenden Schritte aus, um das Dialogfeld COM-Add-Ins zu öffnen:
  
1. Öffnen Sie die InfoPath-Bearbeitungsumgebung. Die einfachste Möglichkeit besteht darin, eine vorhandene Formularvorlage zu öffnen, die ein neues Formular basierend auf dieser Formularvorlage erstellt.
    
2. Klicken Sie im Menü **"Extras"** auf **"Sicherheitscenter".** 
    
3. Klicken Sie auf der linken Seite auf die Kategorie **"Add-Ins".** 
    
4. Wählen Sie im Abschnitt **"Verwalten"** am unteren Rand des Dialogfelds **"Sicherheitscenter"** in der Liste **COM-Add-Ins** aus, und klicken Sie auf die Schaltfläche **"Los".** 
    
5. Im Dialogfeld **COM-Add-Ins** wird der Name Ihres kürzlich erstellten Add-Ins angezeigt, und es sollte ein Kontrollkästchen daneben vorhanden sein. Wenn kein Kontrollkästchen daneben vorhanden ist, konnte das COM-Add-In aufgrund eines Fehlers nicht geladen werden, der im Abschnitt **"Ladeverhalten"** des Dialogfelds aufgeführt wird. 
    
Um das verwaltete COM-Add-In für die Verwendung auf einem anderen Computer als dem Computer zu kompilieren, auf dem das Freigegebene Add-In-Projekt entwickelt wurde, müssen Sie zusätzliche Schritte ausführen, um Ihren Code zu sichern. Informationen zum Sichern freigegebener Add-In Projekte für die Verwendung auf anderen Computern finden Sie in den folgenden drei Artikeln:
  
- [Bereitstellung von verwalteten COM-Add-Ins in Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Verwenden der COM-Add-In-Shim-Lösung zum Bereitstellen von verwalteten COM-Add-Ins in Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolieren von Office-Erweiterungen mit dem COM Shim-Assistenten](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Das Nicht isolieren des COM-Add-Ins kann zu Speicherverlusten und Anwendungsinstabilität führen. 
  
> [!NOTE]
> Wenn die .NET Framework oder andere erforderliche Assemblys aus dem Setupprojekt nicht bereits auf Zielcomputern installiert sind, wird die .msi Datei möglicherweise nicht ordnungsgemäß installiert. Außerdem können Sie die .msi Datei nicht verteilen und dann versuchen, die .msi-Datei zu installieren. Sie müssen auch die anderen Supportdateien im selben Ordner verteilen wie die ursprüngliche .msi datei, die von Visual Studio generiert wurde. 
  
## <a name="coding-in-the-com-add-in"></a>Codieren im COM-Add-In

Anwendungsereignisse, die in der InfoPath-Formularbearbeitungsumgebung auftreten, können von einem COM-Add-In erfasst werden. Die folgenden Ereignisse des [ApplicationEvents-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) können vom COM-Add-In verwendet werden, um auf Benutzeraktionen zu reagieren: 
  
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
   
Um diese Ereignisse im COM-Add-In zu erfassen, müssen Sie die folgenden Variablen auf Klassenebene in Ihrer **Verbinden** Klasse deklarieren: 
  
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

In der ersten Zeile wird das generische **Anwendungsobjekt,** das vom Add-In empfangen wird, in das [_Application3 Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) umgewandelt. In der zweiten Zeile wird die [Eigenschaft "Events"](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) des **_Application3** -Objekts (dargestellt durch die **InfoPathApplication-Variable)** in das [ApplicationEvents -Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) umgewandelt. 
  
Um Ereignishandler zu erstellen, wählen Sie **InfoPathApplicationEvents** aus dem Dropdownfeld **"Klassenname"** oben im fenster Visual Studio aus, und wählen Sie dann das Ereignis aus, das Sie behandeln möchten, im Dropdownfeld **"Methodenname"** am oberen Rand des Visual Studio Fensters. Wenn Sie beispielsweise steuern müssen, wann ein Formular gespeichert wird, behandeln Sie das **XDocumentBeforeSave-Ereignis.** Wenn Sie **XDocumentBeforeSave** aus der Dropdownliste **"Methodenname"** auswählen, wird automatisch die folgende Prozedur eingefügt: 
  
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
- [Erstellen Office verwalteten COM-Add-Ins mit Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Arbeiten mit den IDTExtensibility2-Ereignisprozeduren](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Erstellen eines Office COM-Add-Ins mit Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Erstellen eines Office COM-Add-Ins mit Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Erstellen von InfoPath 2007-Add-Ins mithilfe von Visual Studio 2005-Tools für das Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

