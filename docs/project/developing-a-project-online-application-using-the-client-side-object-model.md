---
title: Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell
manager: lindalu
ms.date: 12/18/2019
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: 'Dieser Artikel beschreibt die Entwicklung von Microsoft Project Online-Anwendungen mit dem .NET Framework 4.0 und CSOM. '
localization_priority: Priority
ms.openlocfilehash: d48cf50b95ecea664cd9eae1b0e642fc2551d5be
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102968"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model-csom"></a>Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell (CSOM)

>[!NOTE] 
>Dieser Artikel beschreibt die Entwicklung von Microsoft Project Online-Anwendungen zur Verwendung von CSOM. Wir empfehlen Ihnen, die Entwicklung von Anwendungen mit dem [neuen Project für das Web](https://developer.microsoft.com/de-DE/office/blogs/developing-applications-and-reports-using-the-new-project/) zu erforschen.
  
## <a name="background"></a>Hintergrund

Microsoft Project kam in den frühen 1990er Jahren als Desktopanwendung auf den Markt. Heute ist Project viel mehr, wie seine verschiedenen Varianten belegen:
  
- Die Project Standard-Edition ist eine Desktopanwendung, die als eigenständige Anwendung ausgeführt wird.
    
- Die Project Professional-Edition ist eine Desktopanwendung, die in größerem Maßstab mit einem Server interagieren und Daten austauschen kann und die in der Lage ist, die von der Project Standard-Edition bereitgestellte Funktionalität auszuführen.
    
- Project Online ist ein von Microsoft gehosteter Dienst, der Unternehmen eine auf PMO-Ebene angesiedelte Lösung zur Koordinierung und Verwaltung von Projekten, Programmen und Portfolios bietet. Als Angebot, das sich von den Desktop-Editionen unterscheidet, kann Project Online Projektdetails während der gesamten Laufzeit eines Projekts verwalten und nachverfolgen. 
    
- Project Server ist ein von einem Unternehmen gehosteter Dienst, in dem das Unternehmen den Server verwaltet und schützt, auf dem sich Projekt-, Programm- und Portfolioinformationen befinden. Project Server bietet, insbesondere durch Schützen des Servers im eigenen Haus, die projekt-, programm- und portfolioorientierten Funktionen von extern gehostetem Project Online mit einer größeren Anpassungsfähigkeit.
    
Project Online hat drei Online-API-Sätze: clientseitiges Objektmodell (CSOM), JavaScript-Objektmodell (JSOM) und Representational State Transfer (REST). 
  
- Die .NET CSOM-Implementierung ist die bevorzugte Schnittstelle bei der Entwicklung von Windows-Anwendungen, die mit Project Online-Mandanten interagieren. Typische Umgebungen für benutzerorientierte Anwendungen sind Windows-Desktops und Microsoft Surface-Geräte. Back-End-Anwendung, die mit .NET CSOM geschrieben wurden, können mit anderen Servern für Geschäftslogik und Datenquellen verbunden werden, die sich außerhalb von Project Online befinden. Abrufanforderungen an Project Online verwenden ein LINQ-ähnliches Abfragesystem, das mehrere Verbesserungen gegenüber den einfachen Abruffunktionen bietet.
    
- Die JavaScript-Objektmodell-Schnittstelle (JSOM-Schnittstelle) bietet browserübergreifende Unterstützung für Project Online-Add-Ins. Ein Add-In ist eine Webanwendung, die im Project Online-Mandanten gespeichert ist. Wenn ein Benutzer ein Add-In ausführen möchte, wird der Code für das Add-In heruntergeladen und im Browser auf dem Benutzercomputer ausgeführt. 
    
- Das REST/OData-Modell stellt HTTP-basierte Kommunikation bereit. Diese Schnittstelle wird für Anwendungen in Nicht-Windows-Umgebungen empfohlen. Kommunikationsendpunkte sind die Objekte in der PWA-Website (Project Web Application). Ergebnisse stellen normale HTTP-Statuscodes bereit.
    
Dieser Artikel konzentriert sich auf eine Anwendung, in der die .NET CSOM-Schnittstelle verwendet wird.
  
## <a name="prerequisites"></a>Voraussetzungen

Beginnen Sie mit einem Basissystem unter Windows 10, und fügen Sie die folgenden Elemente hinzu:
  
- .NET Framework 4.0 oder höher: Verwenden Sie das vollständige Framework. Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- Visual Studio 2013 oder höher: Es kann jede Edition verwendet werden. Die Community-Edition von Visual Studio 2015 wurde verwendet, um die Beispielanwendung zu entwickeln. Die Community-Edition steht unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx zur Verfügung.
    
- SharePoint Client Components SDK: Project Online und Project Server setzen auf SharePoint und SharePoint-Assemblys auf. Die SharePoint Client Components sind in den Visual Studio-Editionen Professional und Enterprise enthalten. Wenn Sie Visual Studio Community verwenden, ist die neueste Version des Office Developer Tools SDKs auf der folgenden Website verfügbar: https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Ein Project Online-Konto: Dies ermöglicht den Zugriff auf die hostende Website. Weitere Informationen zum Einrichten eines Project Online-Kontos finden Sie unter https://products.office.com/en-gb/project/project-portfolio-management.
    
- Projekte auf der hostenden Website, die mit Informationen ausgefüllt sind
    
> [!NOTE]
> Das standardmäßige .NET Framework (4.0 oder höher) ist das zu verwendende Framework. Verwenden Sie nicht .NET Framework 4 Client Profile. 
  
## <a name="develop-the-application"></a>Entwickeln der Anwendung

Beim Entwickeln einer Desktopanwendung für SharePoint ist das clientseitige Objektmodell (CSOM) für Project die bevorzugte Schnittstelle. 
  
Sie können die [CSOM-Beispiele für Project](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) aus dem Project Developer-Ressourcenkatalog im Office Dev Center herunterladen.
  
Die ersten beiden Themen behandeln grundlegende Aspekte: Erstellen eines Visual Studio-Projekts mit geeigneten Namespaces und Assemblys und Zugreifen auf den hostenden Server. Die übrigen Themen befassen sich mit dem Abrufen von Informationen über das CSOM aus einem und aus vielen Objekten. 
  
Das Abrufen von Informationen vom Host ist ein Zwei-Aktionen-Vorgang aus Client-Anwendungen. Als Erstes gibt die Anwendung Abrufanforderungen an und sendet diese an den Server. Als Zweites sendet die Anwendung eine Benachrichtigung an den Server, damit die übermittelten Abfragen ausgeführt werden. Der Server antwortet, indem er die Abfrageergebnisse an den Client sendet.
  
### <a name="set-up-the-visual-studio-project"></a>Einrichten des Visual Studio-Projekts

Das Einrichten der Anwendung besteht aus dem Erstellen eines neuen Projekts, dem Verknüpfen der entsprechenden Assemblys und dem Deklarieren der benötigten Namespaces. Visual Studio bietet verschiedene Typen von Entwicklungsprojekten. 
  
#### <a name="select-a-visual-studio-project"></a>Auswählen eines Visual Studio-Projekts

1. Starten Sie Visual Studio, und wählen Sie **Neues Projekt starten** auf der Startseite aus. 
    
   Im Dialogfeld "Neues Projekt" werden verfügbare Anwendungsvorlagen und Datenfelder für die jeweils ausgewählte Vorlage angezeigt. 
    
2. Geben Sie für diese Anwendung die folgenden Elemente an. Schlüsselwörter, die auf dem Bildschirm zu finden sind, sind fett ausgezeichnet:
    
   1. Wählen Sie aus den installierten Vorlagen im linken Bereich die Vorlage ** C# **  =>  **Windows** => **Klassischer Desktop** aus. 
    
   2. Wählen Sie oben im zentralen Bereich die Option **.NET Framework 4** aus. 
    
   3. Wählen Sie aus den Anwendungstypen im zentralen Bereich den Typ **Konsolenanwendung** aus. 
    
   4. Geben Sie im unteren Abschnitt einen Namen und Speicherort für das Projekt und einen Projektmappennamen an. 
    
   5. Aktivieren Sie außerdem im unteren Abschnitt das Kontrollkästchen **Projektmappenverzeichnis erstellen**. 
    
3. Klicken Sie auf **OK**, um das Ausgangsprojekt zu erstellen. 
    
#### <a name="add-assemblies"></a>Hinzufügen von Assemblys

Für die VS-Projektmappe sind die Assembly "ProjectServerClient" aus dem Project 2013 SDK, einige Assemblys aus dem SharePoint SDK und die .NET Framework-Assembly "System.Security" erforderlich.
  
1. Klicken Sie im Projektmappen-Explorer von VS mit der rechten Maustaste auf den Eintrag "Verweise", und wählen Sie **Verweis hinzufügen...** im Kontextmenü aus. 
    
2. Aktivieren Sie den Verweis **Microsoft.ProjectServer.Client.dll**. 
    
   Klicken Sie ggf. auf die Schaltfläche **Durchsuchen...** unten im Dialogfeld, und navigieren Sie zum Installationsverzeichnis des Project 2013 SDKs, um die Assembly zu finden. 
    
3. Klicken Sie auf **OK**. 
    
4. Fügen Sie den Namespace "ProjectServer.Client" zur CS-Datei hinzu.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Fügen Sie die SharePoint 2013 SDK-Assemblys über die NuGet-Paket-Manager-Konsole hinzu. 
  
1. Klicken Sie über das VS-Menü "Extras" auf die folgenden Menüs: **Extras =\> NuGet-Paket-Manager =\> Paket-Manager-Konsole**. 
    
2. Geben Sie in der Paket-Manager-Konsole den folgenden Befehl ein, und drücken Sie die \<EINGABETASTE\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   Die **Paket-Manager-Konsole** stellt eine Beschreibung der Befehlsergebnisse bereit, und im Projektmappen-Explorer von VS werden die SharePoint-Assemblys in den Projektverweisen angezeigt. 
    
3. Fügen Sie die Namespaces zur CS-Datei hinzu:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

Die Assembly "System.Security" gehört zu .NET Framework und wurde mit dem Framework installiert. Für die Beispielanwendung ist ein weiterer Namespace erforderlich, der dem hostenden System eine verschlüsselte Zeichenfolge für die Authentifizierung bereitstellt. Sobald die Anwendung authentifiziert ist, kann sie auf Projekte auf dem hostenden System zugreifen. Fügen Sie den Namespace "System.Security" wie folgt zur CS-Datei hinzu:
  
1. Klicken Sie im Projektmappen-Explorer von VS mit der rechten Maustaste auf den Eintrag "Verweise", und wählen Sie **Verweis hinzufügen...** im Kontextmenü aus. 
    
2. Wählen Sie **Assemblys =\> Framework** im linken Bereich des Dialogfelds für den Verweis-Manager aus, und aktivieren Sie dann **System.Security**. 
    
3. Klicken Sie auf **OK**. 
    
4. Fügen Sie den Namespace "System.Security" zur CS-Datei hinzu:
    
   ```cs
    using System.Security;
   ```

Der Anfang der CS-Datei sollte die folgenden Namespaces enthalten:
  
- System
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>Verbinden mit dem Hostsystem

Project Online ist eine SharePoint-Anwendung, sodass die Verwendung der SharePoint-Authentifizierung der richtige Ansatz ist. Im folgenden Codefragment wird das Zugreifen auf die gehostete Umgebung vorbereitet.
  
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

Die Vorbereitungen für das Zugreifen auf die gehostete Umgebung umfassen die folgenden Schritte:
  
1. Erstellen Sie ein Kontextobjekt für die Projekte: Dieses Objekt ist im folgenden Code aus dem vorherigen Codefragment enthalten. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   Der Kontext wird an andere Komponenten vererbt, wodurch es dem System ermöglicht wird, den Kontext des Project-Objektmodells zu verwalten.
    
2. Geben Sie die Hostwebsite an. Dies erfolgt im folgenden Code aus dem vorherigen Codefragment.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   Wenn der Projektkontext instanziiert wird, muss die Anwendung den Stamm der Websitesammlung für Projekte bereitstellen. Die Anwendung verwendet eine Teilzeichenfolge der URL des Stamms der Projekte. Ein Momentaufnahme dieser Position ist in der folgenden Abbildung mit einem roten Rechteck hervorgehoben. Für die Authentifizierung wird die Zeichenfolge ab deren Anfang bis einschließlich der Teilzeichenfolge "pwa" benötigt. Im Codeeintrag wird für die Anwendung die Zeichenfolge "https://XXXXXXXX.sharepoint.com/sites/pwa" verwendet.
        
   ![Screenshot der URL für die Projekte-Websitesammlung in einem roten Rahmen.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screenshot der URL für die Projekte-Websitesammlung in einem roten Rahmen")
  
3. Geben Sie das Kennwort in einer sicheren Zeichenfolge an. Dies erfolgt im folgenden Code aus dem vorherigen Codefragment.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   Das Kennwort und das Benutzerkonto sind die Anmeldeinformationen für den Zugriff auf die Hostwebsite. 
    
4. Fügen Sie das Benutzerkonto und das Kennwort zur Anmeldeinformationen-Komponente des Kontextobjekts hinzu. Dies erfolgt im folgenden Code aus dem vorherigen Codefragment.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

Der instanziierte Projektkontext kann nun verwendet werden.
  
### <a name="list-all-published-projects"></a>Auflisten aller veröffentlichten Projekte

Project Online und ProjectServer verwenden Proxys, um mit dem Server zum Ausführen von Erstell-, Berichts-, Aktualisier- und Löschvorgängen zu kommunizieren. Der Host/Server verarbeitet Anfragen auf effiziente Weise und lässt den Client die folgenden Aktionen in der Kommunikation mit dem Server ausführen:
  
1. Richten Sie einen Kontext für Kommunikation ein. 
    
   Der Kontext wird von der Projektesammlung sowie anderen Objekten und Sammlungen (Collections) durch Vererbung verwendet, einschließlich der Aufgabensammlung, der Zuweisungensammlung, des Stufenobjekts und benutzerdefinierter Felder. 
    
2. Geben Sie mit dem Objektmodell ein Objekt, eine Sammlung oder Daten an, die abgerufen werden sollen.
    
   In diesem Schritt wird LINQ als Abfrage oder Methode verwendet. Die Spezifikation steuert, was Sie erhalten. Dieser Schritt wird häufig als Kern der Load-Methode (Schritt 3) eingebettet. 
    
3. Laden Sie die Spezifikation aus dem vorherigen Schritt mit der Load()- oder LoadQuery()-Methode.
    
   Verwenden Sie für das Laden von Sammlungen und Objekten Load(). Verwenden Sie für Abfragen mit Klauseln wie "where" und "group" LoadQuery(). 
    
4. Führen Sie die Anforderung mit der ExecuteQuery()-Methode aus.
    
   Die ExecuteQuery()-Methode benachrichtigt den Host, dass die Abfrage oder Abfragen ausgeführt werden können. Sobald der Host die Benachrichtigung erhalten hat, führt er die Abfragen aus und sendet die Ergebnisse an den Client. 
    
Sobald die Informationen beim Client eingetroffen sind, kann die Anwendung diese verwenden. Im folgenden Codefragment werden die veröffentlichten Projekte durchlaufen und werden die ID und der Name für jedes der auf dem Host veröffentlichten Projekte ausgegeben.
  
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

### <a name="make-a-request"></a>Stellen einer Anforderung

Über Verwenden der Aktionen aus dem vorherigen Codefragment ruft die Anwendung die Liste der Projekte im angegebenen Konto auf der hostenden Website ab. 
  
1. Die Projektkontext wird für die aufzulistenden Projekte angegeben. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Geben Sie das abzurufende Element an. 
    
   ```cs
    projContext.Load(projects);
   ```

   Weil nur die Sammlung angegeben ist, ruft der Server die Projektsammlung ab, wobei jedes Projekt mit den Werten für den Standardsatz der Eigenschaften aufgefüllt wird. Zugreifen auf Eigenschaften, die zum Standardeigenschaftensatz gehören, bringt erfolgreiche Ergebnisse. Zugreifen auf Eigenschaften, die nicht zum Standardeigenschaftensatz gehören, führt zu einer "Nicht initialisiert"-Ausnahme.
    
3. Laden Sie die Anforderung (projContext.Load).
    
   Dies gehört zum vorherigen Schritt.
    
4. Führen Sie die Abfrage aus (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Abrufen von allgemeinen Projektinformationen

Eigenschaften, die keine Standardeigenschaften sind, müssen in der Anforderung an den Server angegeben werden. Im nächsten Codefragment wird der Kontext der Projektesammlung so wie im vorherigen Beispiel geladen. Anschließend werden in der Spezifikation Nicht-Standardeigenschaften angefordert, die im Ergebnis enthalten sein sollen. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

In der Load-Anweisung wird der Kontext der Projektesammlung angegeben und werden das Startdatum (StartDate), die Phase und die Stufe (Stage) hinzugefügt. Die zusätzlichen Eigenschaften skalar, Objekte oder Sammlungen sein. Auf skalare Elemente kann direkt zugegriffen werden. Objekte und Sammlungen erfordern zusätzliche Verarbeitungsschritte, wie im folgenden Codefragment.
  
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

Ausgabe für die ersten drei Projekte:
  
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

### <a name="retrieve-all-tasks-in-a-project"></a>Abrufen aller Aufgaben in einem Projekt

Jedes Projekt hat viele Aufgaben. Somit besteht das Abrufen der Aufgaben für ein einzelnes Projekt aus folgenden Schritten:
  
1. Richten Sie den Kontext der Projektesammlung ein.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Rufen Sie die Projektinformationen ab, einschließlich der Aufgabeneigenschaften.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Beachten Sie, dass die Anwendung für veröffentlichte Projekte vorgesehen ist. Der Kontext für das aktuelle veröffentlichte Projekt ist "pubProj". 
    
3. Richten Sie den Kontext für die Aufgabensammlung (Tasks) ein.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   Die `pubProj.Tasks`-Eigenschaft verweist auf die Aufgaben des aktuellen veröffentlichten Projekts. 
    
4. Laden Sie die Spezifikation zum Abrufen der Aufgabensammlung (Task collection), einschließlich der entsprechenden Nicht-Standardeigenschaften.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Führen Sie die Abfrage aus, um die Aufgabensammlung mit den entsprechenden Eigenschaften abzurufen.
    
   ```cs
    projContext.ExecuteQuery();
   ```

Die Informationen liegen nun lokal vor. Im folgenden Codefragment wird die veröffentlichte Aufgabensammlung verarbeitet, indem die Informationen in die Konsole geschrieben werden.
  
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

Ausgabe der Aufgaben für ein Projekt:
  
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

### <a name="access-information-at-multiple-levels"></a>Zugreifen auf Informationen auf mehreren Ebenen

Für jede Aufgabe können eine oder mehrere Personen (auch als Ressourcen bezeichnet) an der Erledigung der Aufgabe beteiligt sein. Die Zuweisungen- (Assignments) und die Ressourcensammlung enthalten diese Informationen für jede Aufgabe. 
  
Die Verarbeitung besteht aus den folgenden Schritten:
  
1. Rufen Sie einen Kontext für die Projektaufgabe ab.
    
2. Erstellen Sie eine Anforderung, und laden Sie die Anforderung für die Zuweisungen, die mit der Aufgabe verknüpft sind. 
    
3. Führen Sie die Abfrage für die Zuweisungen aus.
    
4. Erstellen Sie eine Anforderung, und laden Sie die Anforderung für die Ressource, die mit einer einzelnen Zuweisung verknüpft ist. 
    
5. Führen Sie die Abfrage für die Ressource aus.
    
> [!NOTE] 
> - Die Zuweisungensammlung wird explizit in den Informationen vom Server angefordert, weil sie keine Standardeigenschaft der Aufgabensammlung ist. Als Sammlung wird anschließend eine Abfrage ausgeführt, um die Sammlung vom Server abzurufen. 
> - Die Ressource ist ein Objekt. Die Abfrage für eine Zuweisung enthält den Namen der Ressource, die mit der Zuweisung verknüpft ist.
    
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

Ausgabe für Aufgaben 52, 75 und 76 eines Projekts:
  
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

### <a name="access-custom-enterprise-level-fields"></a>Zugreifen auf benutzerdefinierte Felder auf Unternehmensebene

Für Project Online gibt es benutzerdefinierte Felder. Diese Felder sind Felder auf Unternehmensebene, die mit einzelnen Projekten verknüpft werden können. In diesem Abschnitt ist beschrieben, wie auf diese Felder zugegriffen wird. 
  
Benutzerdefinierte Felder sind nicht in den Standardeigenschaften enthalten, die mit einem Projekt verknüpft sind. Daher müssen sie in der Abrufspezifikation explizit angegeben werden. Die grundsätzliche Sicht auf den Vorgang besteht aus den folgenden Schritten:
  
1. Erstellen Sie einen Tunnel zum benutzerdefinierten Feld über dessen allgemeinen Namen.
    
2. Rufen Sie den internen Namen des benutzerdefinierten Felds ab.
    
3. Kehren Sie zum globalen Kontext zurück, und fragen Sie das System mit dem internen Namen des benutzerdefinierten Felds ab.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Erstellen eines Tunnels zum benutzerdefinierten Feld, Abrufen dessen internen Namens und Abfragen des Systems mit dem Namen

In dieser Aufgabe ist ein Abruf angegeben, in dem eine Nicht-Standardeigenschaft mit einem zusätzlichen Detail verwendet wird.
  
1. Beginnen Sie durch Verwenden Projektekontexts, wie dies am Anfang dieses Artikels beschrieben ist.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Fügen Sie zwei Elemente zur Abrufanforderung der Projektesammlung hinzu, zusätzlich zu allen anderen Nicht-Standardeigenschaften, die abgerufen werden sollen:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   Die `p => p.IncludeCustomFields`-Klausel kennzeichnet die Notwendigkeit, ein Projektobjekt zu verwenden, das benutzerdefinierte Felder unterstützt. 
    
   In der `p => p.IncludeCustomFields.CustomFields`-Klausel wird die Einbeziehung von Daten aus benutzerdefinierten Feldern in das Abfrageergebnis angefordert. Diese Informationen werden verwendet, nachdem der interne Name des benutzerdefinierten Felds abgerufen wurde. 
    
3. Laden Sie die Anforderung.
    
   Dies gehört zum vorherigen Schritt.
    
4. Führen Sie die Abfrage aus.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Mit diesen Informationen erstellen Sie auf dem Client eine Anforderung, um die benutzerdefinierten Felder abzurufen, die mit dem aktuellen Projekt verknüpft sind.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Suchen Sie das entsprechende benutzerdefinierte Feld, und rufen Sie den internen Namen des Felds ab. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   Der interne Name des benutzerdefinierten Felds wird abgerufen. Die grundsätzlichen Schritte 1 und 2 sind jetzt abgeschlossen.
    
7. Kehren Sie zum Projektkontext zurück, und rufen Sie den Wert des benutzerdefinierten Felds ab.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > Der Wert des benutzerdefinierten Felds wird abgerufen, indem der interne Name als Index verwendet wird. 
  
Die Ausgabe für drei Projekte, bestehend aus Projekt-ID, Projektname, Name des benutzerdefinierten Felds, interner Name des benutzerdefinierten Felds und Wert des benutzerdefinierten Felds.
  
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

## <a name="see-also"></a>Weitere Artikel

Dokumentation und Beispiele zu Project Online und zur Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/project) im Office Dev Center.
    

