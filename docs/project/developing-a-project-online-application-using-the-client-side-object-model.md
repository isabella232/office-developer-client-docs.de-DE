---
title: Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: In diesem Artikel wird beschrieben, Microsoft Project Online Anwendungsentwicklung für desktopanwendungen mit .NET Framework 4.0. Die Anwendung, die in diesem Artikel beschriebenen Ruft Informationen aus dem Hostserver.
ms.openlocfilehash: b6e7260fd2337d2b156f97605fdd201f5e0d4edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385263"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell

In diesem Artikel wird beschrieben, Microsoft Project Online Anwendungsentwicklung für desktopanwendungen mit .NET Framework 4.0. Die Anwendung, die in diesem Artikel beschriebenen Ruft Informationen aus dem Hostserver. 
  
## <a name="background"></a>Hintergrund

Microsoft Project als desktop-Anwendung in der frühen 1990er gestartet. Heute ist Project vieles Weitere abschließen, die mehrere Varianten:
  
- Project standard Edition ist eine desktop-Anwendung, die als eigenständige Anwendung ausgeführt wird.
    
- Project professional Edition ist eine desktop-Anwendung, die kann interagieren und Daten gemeinsam mit einem Server in einem größeren Ausmaß als auch die Funktionalität in Project standard Edition ausführen.
    
- Project Online ist ein Microsoft-gehosteten Dienst, der bietet Unternehmen eine Lösung auf Dokumentebene PMO koordinieren und Verwalten von Projekten, Programme und Portfolios. Eine andere besser als desktop-Editionen, Project Online warten und Nachverfolgen von Projektdetails im Lebenszyklus eines Projekts kann. 
    
- Projektserver ist eine Enterprise-gehosteten Dienst in dem Unternehmen verwaltet und sichert den Server, Project, Anwendung und Portfolio Informationen enthält. Projektserver nach der Sicherung des Servers internes bietet Projekt-, Anwendung und Portfolio orientierten Features von extern gehosteten Project Online mit eine höhere Kapazität für die Anpassung.
    
Project Online hat drei online API-Sätze: mithilfe der clientseitigen Objekt Objektmodell (CSOM), JavaScript-Objektmodell (JSOM) und Representational State Transfer (REST). 
  
- Die .NET CSOM-Implementierung ist die bevorzugte Schnittstelle beim Entwickeln von Windows-Anwendungen, die interagieren mit Project Online-Mandanten. Typische Umgebung für die Benutzer-centric Applications gehören Desktops unter Windows und Microsoft Surface Geräte. Back-End-Clientanwendungen mit .NET CSOM geschrieben können mit anderen Servern für Business Logic und Datenquellen eine Verbindung herstellen, die externe mit Project Online sind. Abruf Anfragen zu Project Online verwenden Sie ein LINQ-ähnliche Abfrage, die mehrere Verbesserungen über grundlegende Retrieval Funktionen bietet.
    
- Die JavaScript-Objektmodell (JSOM)-Schnittstelle bietet Browserübergreifende Unterstützung für Project Online-Add-ins. Ein Add-in ist eine Anwendung, die in Project Online-Mandanten gespeichert ist. Wenn ein Benutzer ein Add-in ausführen möchte, wird der Code für das Add-in-downloads und im Browser auf dem Computer des Benutzers ausgeführt wird. 
    
- Details des Modells REST/Odata-HTTP-basierte Kommunikation bereitstellt, wird diese Schnittstelle für Applikationen in nicht-Windows-Umgebungen empfohlen. Kommunikationsendpunkten sind die Objekte in der Website für die Project Web Application (PWA). Ergebnisse liefern normalen HTTP-Statuscodes.
    
Dieser Artikel befasst sich eine Anwendung, die die .NET CSOM-Schnittstelle verwendet.
  
## <a name="prerequisites"></a>Voraussetzungen

Starten Sie mit einem Basis-System mit Windows 10, und fügen Sie die folgenden Elemente:
  
- .NET Framework 4.0 oder höher – verwenden Sie das vollständige Framework. Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- Visual Studio 2013 oder höher--Edition ist zulässig. Die Community-Edition von Visual Studio 2015 wurde verwendet, um die beispielanwendung aus zu entwickeln. Die Community Edition steht unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- SharePoint-Clientkomponenten SDK – Project Online und Project Server sit auf der Basis SharePoint und SharePoint-Assemblys. Die SharePoint-Clientkomponenten sind in Visual Studio Professional und Enterprise Edition enthalten. Wenn Sie Visual Studio-Community Edition verwenden, die neueste Version des Office Developer Tools SDK steht auf der folgenden Website: https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Ein Konto Project Online – bietet dies Zugriff auf die Website gehostet. Weitere Informationen dazu, wie Sie ein Konto mit Project Online erhalten, finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Projekte auf der hosting-Website, die mit Daten aufgefüllt werden
    
> [!NOTE]
> Der Standard ist .NET Framework (4.0 oder höher) die richtigen Framework verwendet werden. Verwenden Sie die .NET Framework 4 Client Profile nicht. 
  
## <a name="develop-the-application"></a>Entwickeln der Anwendung

Bei der Entwicklung von einer desktop-Anwendung für SharePoint, ist die bevorzugte Schnittstelle des Project-Seite-Clientobjektmodells (CSOM). 
  
Sie können das vollständige Beispiel unter herunterladen https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.
  
Die ersten beiden Themen enthalten grundlegende Probleme: Erstellen eines Visual Studio-Projekts mit den entsprechenden Namespaces und Assemblys und den Zugriff auf den Hostserver. Abrufen von Informationen über die CSOM aus einem und viele Objekte dienen in den übrigen Themen. 
  
Abrufen von Informationen aus der Host ist ein Vorgang zwei-Aktion von Clientanwendungen. Zunächst wird die Anwendung gibt an, und sendet eine oder mehrere Retrieval Anforderungen an den Server. Zweitens gibt die Anwendung eine Benachrichtigung an den Server die übermittelten Abfragen ausgeführt werden. Der Server antwortet, indem die Ergebnisse der Abfrage an den Client gesendet.
  
### <a name="set-up-the-visual-studio-project"></a>Einrichten des Visual Studio-Projekts

Erstellen eines neuen Projekts, verknüpfen die entsprechenden Assemblys und die erforderlichen Namespaces deklarieren besteht der Installation der Anwendung aus. Visual Studio stellt verschiedene Arten von Entwicklungsprojekten. 
  
#### <a name="select-a-visual-studio-project"></a>Wählen Sie ein Visual Studio-Projekt

1. Starten Sie Visual Studio, und wählen Sie **Neues Projekt starten Sie** auf der Startseite. 
    
   Das Dialogfeld Neues Projekt verfügbar Anwendungsvorlagen und Datenfelder für jede ausgewählte Vorlage angezeigt. 
    
2. Geben Sie für diese Anwendung die folgenden Elemente an. Schlüsselwörter aufgetreten ist, auf dem Bildschirm aufweisen eine fett Attribut:
    
   1. Wählen Sie im linken Bereich die installierte Vorlagen ein **C#-** => **Windows** => **klassischen Desktop**. 
    
   2. Wählen Sie am oberen Rand der mittleren Bereich **.NET Framework 4**. 
    
   3. Wählen Sie im mittleren Bereich Anwendungstypen **Konsolenanwendung**aus. 
    
   4. Geben Sie im unteren Bereich einen Namen und Speicherort für das Projekt, und einen Lösungsnamen. 
    
   5. Auch im unteren Bereich das Kontrollkästchen Sie **Projektmappenverzeichnis erstellen** . 
    
3. Klicken Sie auf **OK** , um das ursprüngliche Projekt zu erstellen. 
    
#### <a name="add-assemblies"></a>Hinzufügen von Assemblys

Die VS-Lösung benötigt die Assembly ProjectServerClient aus Project 2103 SDK, eine Reihe von Assemblys aus dem SharePoint-SDK und die System.Security für .NET Framework-Assembly.
  
1. In VS Projektmappen-Explorer mit der rechten Maustaste in des Eintrags Verweise, und wählen Sie **Verweis hinzufügen** Klicken Sie im Kontextmenü. 
    
2. Überprüfen Sie die **Microsoft.ProjectServer.Client.dll**. 
    
   Falls erforderlich, klicken Sie auf die **Durchsuchen...** Navigieren Sie zu dem Installationsverzeichnis Project 2013-SDK zum Suchen der Assembly, und klicken Sie unten im Dialogfeld. 
    
3. Klicken Sie auf **OK**. 
    
4. Fügen Sie den Namespace PrjoctServer Client, um die CS-Datei.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Fügen Sie die SharePoint 2013 SDK-Assemblys, die mit der NuGet Package Manager-Konsole hinzu. 
  
1. Klicken Sie im Menü Extras VS auf die folgenden Menüs: **Tools =\> NuGet Package Manager =\> Paket-Manager-Konsole**. 
    
2. Geben Sie in der Paket-Manager-Konsole den folgenden Befehl und drücken Sie \<EINGABETASTE\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   Die **Paket-Manager-Konsole** enthält eine Beschreibung der Befehlsergebnisse; und VS Projektmappen-Explorer angezeigt, die SharePoint-Assemblys in den Projektverweisen. 
    
3. Fügen Sie die Namespaces in die CS-Datei:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

Die System.Security Assembly ist Teil von .NET Framework und mit Framework installiert wurde. Die beispielanwendung benötigt eine weitere Namespace, der eine verschlüsselte Zeichenfolge, die das Hostsystem für die Authentifizierung ermöglicht. Nach der Authentifizierung kann die Anwendung auf das Hostsystem Projekte zugreifen. CS-Datei auf diese Weise System.Security-Namespace hinzugefügt:
  
1. In VS Projektmappen-Explorer mit der rechten Maustaste in des Eintrags Verweise, und wählen Sie **Verweis hinzufügen** Klicken Sie im Kontextmenü. 
    
2. Wählen Sie **Assemblys =\> Framework** im linken Bereich des Dialogfelds Verweise Manager **System.Security**überprüfen. 
    
3. Klicken Sie auf **OK**. 
    
4. CS-Datei System.Security-Namespace hinzugefügt:
    
   ```cs
    using System.Security;
   ```

Der Anfang des CS-Datei sollte die folgenden Namespaces enthalten:
  
- System
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>Verbinden Sie mit dem Hostsystem

Project Online ist eine SharePoint-Anwendung mithilfe der SharePoint-Authentifizierung die richtige Vorgehensweise. Im folgenden Codefragment bereitet gehostete Umgebung zugreifen.
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

Vorbereitung die gehostete Umgebung Zugriff auf gehören die folgenden Elemente:
  
1. Ein Context-Objekt für die Projekte erstellen – dies in den folgenden Code, der im vorherigen Codefragment enthalten ist. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   Im Kontext wird von anderen Komponenten, die das System im Kontext des Project-Objektmodell verwalten geerbt.
    
2. Identifizieren der Hostwebsite – dies geschieht in den folgenden Code aus dem vorherigen Codefragment.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   Wenn Projekte Kontext zu instanziieren, muss die Anwendung den Stamm der Websitesammlung Projekte bereitstellen. Die Anwendung verwendet eine Teilzeichenfolge der URL des Stammverzeichnisses der Projekte. Ein rotes Rechteck in der folgenden Abbildung ist eine Momentaufnahme der von diesem Speicherort hervorgehoben. Die Authentifizierung benötigt die Zeichenfolge aus dem Start über die Teilzeichenfolge "pwa". Im Codebeispiel, die Anwendung verwendet die Zeichenfolge "https://XXXXXXXX.sharepoint.com/sites/pwa".
        
   ![Screenshot der URL der Websitesammlung Projekte innerhalb einer rote Rahmenlinie.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screenshot der URL der Projekte Websitesammlung innerhalb einer rote Rahmenlinie")
  
3. Setzen Sie das Kennwort in eine sichere Zeichenfolge – Dies geschieht in den folgenden Code aus dem vorherigen Codefragment.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   Das Kennwort und die Benutzer sind die Anmeldeinformationen zum Zugriff auf die Hostwebsite. 
    
4. Fügen Sie das Benutzerkonto und das Kennwort zum Bereich Anmeldeinformationen des Kontextobjekts – dies geschieht in den folgenden Code aus dem vorherigen Codefragment.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

Der Projektkontext instanziierte ist einsatzbereit.
  
### <a name="list-all-published-projects"></a>Listen Sie alle veröffentlichten Projekte

Project Online und ProjectServer verwenden Proxys für die Kommunikation mit dem Server zu erstellen, Bericht, Update und delete-Operationen (CRUD). Der Hostserver behandelt Anforderungen effizient und hat der Client die folgenden Aktionen ausführen, bei der Kommunikation mit dem Server:
  
1. Richten Sie einen Kontext für die Kommunikation. 
    
   Der Kontext wird von der Projects-Auflistung als auch andere Objekte und Auflistungen durch Vererbung, einschließlich der Tasks-Auflistung, Assignments-Auflistung, die Stage-Objekts und benutzerdefinierte Felder verwendet. 
    
2. Verwenden des Objektmodells auf ein Objekt, Auflistung oder abzurufenden Daten angeben.
    
   Dieser Schritt wird LINQ verwendet, als eine Abfrage oder eine Methode. Die Spezifikation steuert, was Sie erhalten. Dieser Schritt ist häufig als Hauptteil der Load-Methode (Schritt 3) eingebettet. 
    
3. Laden der Abruf aus dem vorherigen Schritt die Load() oder LoadQuery()-Methode verwenden.
    
   Verwenden Sie zum Laden von Auflistungen und Objekte, Load(). Für Abfragen mit Klauseln wie "Where" und "group" LoadQuery() verwenden. 
    
4. Führen Sie die Anforderung mithilfe der ExecuteQuery()-Methode.
    
   Die Methode ExecuteQuery() benachrichtigt den Host, dass die Abfrage oder Abfragen ausführen können. Nachdem der Host-Benachrichtigung erhält, führt die Abfragen und sendet die Ergebnisse an den Client. 
    
Sie mit den Informationen auf dem Client können die Anwendung verwenden. Im folgenden Codefragment durch die veröffentlichten Projekte und druckt die Id und Name für jedes veröffentlichte Projekt auf dem Host.
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

Ausgabe:
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>Stellen Sie eine Anforderung

Verwenden die Aktionen aus dem vorherigen Codefragment, ruft die Anwendung die Liste der Projekte in das angegebene Konto auf der Website hosten. 
  
1. Die ProjectContext wird für die Projekte in der Liste angegeben. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Geben Sie das Element abrufen. 
    
   ```cs
    projContext.Load(projects);
   ```

   Durch nur unter Angabe der Auflistung, ruft der Server Auffüllen jedes Projekt mit Werten für die Standardgruppe von Eigenschaften der Project-Auflistung ab. Zugreifen auf Eigenschaften, die Teil der standardeigenschaftensatz sind bietet erfolgreiche Ergebnisse. Zugreifen auf Eigenschaften, die nicht Teil der standardmäßigen sind festzulegen, führt zu einer Ausnahme "Nicht initialisiert".
    
3. Laden Sie die Anforderung (projContext.Load).
    
   Dies ist Teil der im vorherigen Schritt.
    
4. Ausführen der Abfrage (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Abrufen von allgemeinen Projektinformationen

Eigenschaften, die nicht standardmäßigen Eigenschaften in der Anforderung an den Server müssen angegeben werden. Im nächste Codefragment lädt den Projects-Auflistung Kontext wie im vorherigen Beispiel. Die Spezifikation angefordert zusätzliche nicht standardmäßigen Eigenschaften in das Ergebnis einbezogen. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

Die Load-Anweisung gibt den Kontext der Projects-Auflistung und fügt die StartDate, Phase und Stufe Abfrageergebnis hinzu. Die zusätzlichen Eigenschaften können skalare, werden Objekte und Auflistungen. Skalare Elemente können direkt zugegriffen werden. Objekte und Auflistungen benötigen weitere Verarbeitung weiterleitet, wie im folgenden Codefragment dargestellt.
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

Ausgabe der ersten drei Projekte:
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a>Rufen Sie aller Vorgänge in einem Projekt ab

Jedes Projekt verfügt über viele Aufgaben. Also umfasst die Aufgaben für ein einzelnes Projekt abrufen Folgendes:
  
1. Richten Sie im Kontext der Projects-Auflistung.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Rufen Sie die Projektinformationen, einschließlich der Task-Eigenschaften ab.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Beachten Sie, dass die Anwendung veröffentlichte Projekte Adressierung ist. Der Kontext für das aktuelle veröffentlichten Projekt ist PubProj. 
    
3. Richten Sie im Kontext der Tasks-Auflistung.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   Die `pubProj.Tasks` Eigenschaft verweist auf die Aufgaben des aktuellen Projekts veröffentlichte. 
    
4. Laden Sie die Spezifikation zum Abrufen der Auflistung von Workflowaufgaben, einschließlich der entsprechenden nicht standardmäßigen Eigenschaften.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Führen Sie die Abfrage zum Abrufen der Aufgabe-Auflistung mit den entsprechenden Eigenschaften an.
    
   ```cs
    projContext.ExecuteQuery();
   ```

Die Informationen sind jetzt lokalen. Im folgenden Codefragment verarbeitet die veröffentlichten Tasks-Auflistung durch Schreiben die Informationen in der Konsole angezeigt.
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

Ausgabe von Aufgaben für ein Projekt:
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a>Zugriff auf Informationen auf mehreren Ebenen

Jede Aufgabe kann eine oder mehrere Personen (auch bekannt als verfügen. Ressource) beiträgt, dessen Abschluss. Die Aufgaben und Ressourcen Auflistungen enthält diese Informationen für jeden Vorgang. 
  
Die Verarbeitung umfasst Folgendes:
  
1. Abrufen von einen Kontext für den Projektvorgang.
    
2. Erstellen Sie eine Anforderung, und Laden Sie die Anforderung für die Zuweisung der Aufgabe gebunden. 
    
3. Führen Sie die Abfrage für die Zuordnungen.
    
4. Erstellen Sie eine Anforderung, und Laden Sie die Anforderung für die Ressource eine einzelne Zuordnung zugeordnet. 
    
5. Führen Sie die Abfrage für die Ressource.
    
> [!NOTE] 
> - Assignments-Auflistung ist explizit in die Informationen vom Server angefordert, da es sich nicht um eine Standardeigenschaft der Tasks-Auflistung darstellt. Als Sammlung erfolgt eine nachfolgende Abfrage zum Abrufen der Auflistung vom Server. 
> - Die Ressource ist ein Objekt. Die Abfrage für eine Zuordnung enthält den Ressourcennamen der Zuordnung zugeordnet.
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

Die Ausgabe für Aufgaben 52, 75 und 76 eines Projekts:
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a>Access benutzerdefinierte Unternehmensebene Felder

Benutzerdefinierte Felder für Project Online vorhanden sein. Dies sind Unternehmensebene Felder, die einzelne Project zugeordnet werden können. In diesem Abschnitt wird beschrieben, wie diese Felder Zugriff auf. 
  
Benutzerdefinierte Felder sind nicht in die Standardgruppe von Eigenschaften, die einem Projekt zugeordnete enthalten. Ja, benötigen sie explizite Identifikation in der Spezifikation abrufen. Allgemeine Ansicht über den Prozess umfasst die folgenden Elemente:
  
1. Tunnelmodus an das benutzerdefinierte Feld mit den allgemeinen Namen.
    
2. Rufen Sie den internen Namen des benutzerdefinierten Felds ab.
    
3. Zurück zu globalen Kontext und Abfragen des Systems mit den internen Namen des benutzerdefinierten Felds.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>An das benutzerdefinierte Feld Tunnel, seinen internen Namen abrufen und es für das System die Abfrage verwendet

Für diese Aufgabe gibt eine abrufen, die eine Standardeigenschaft mit ein hinzugefügte Detail verwendet.
  
1. Beginnen Sie mit dem Kontext Projekte wie am Anfang dieses Artikels beschrieben.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Projects-Auflistung abrufen Anforderung zusätzlich zu anderen nicht standardmäßige-Eigenschaften zum Abrufen zwei Elemente hinzugefügt:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   Die `p => p.IncludeCustomFields` Klausel erkennt die muss ein Project-Objekt verwenden, benutzerdefinierte Felder unterstützt. 
    
   Die `p => p.IncludeCustomFields.CustomFields` Klausel fordert die Aufnahme der Daten im Abfrageergebnis benutzerdefinierter Felder. Diese Informationen werden verwendet, nachdem der interne Name des benutzerdefinierten Felds abgerufen wird. 
    
3. Laden Sie die Anforderung.
    
   Dies ist Teil der im vorherigen Schritt.
    
4. Ausführen der Abfrage.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Erstellen Sie mithilfe dieser Informationen auf dem Client eine Anforderung an die benutzerdefinierten Feldern, die dem aktuellen Projekt zugeordnete abrufen.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Suchen Sie die entsprechenden benutzerdefinierten Felds, und rufen Sie den internen Namen des Felds. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   Der interne Name des benutzerdefinierten Felds wird abgerufen. Elemente auf oberster Ebene 1 und 2 sind jetzt abgeschlossen.
    
7. Die Projekt-Kontext zurück, und rufen Sie den Wert des benutzerdefinierten Felds.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > Der Wert des benutzerdefinierten Felds ist mit den internen Namen als Index abgerufen. 
  
Ausgabe des Project-ID, Name des Projekts, Name des benutzerdefinierten Felds, interne Name des benutzerdefinierten Felds und der Wert des benutzerdefinierten Felds bestehend aus drei Projekte.
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele im Zusammenhang mit Project Online und die Anwendungsentwicklung mithilfe von CSOM finden Sie im [Projekt Development Portal](https://developer.microsoft.com/en-us/project).
    

