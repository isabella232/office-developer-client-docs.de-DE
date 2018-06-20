---
title: Erste Schritte mit dem Project Server-CSOM und .NET
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Sie können das Project Server 2013 mithilfe der clientseitigen Objektmodell (CSOM) zum Entwickeln von Project Online und lokale Lösungen mit .NET Framework 4 verwenden. Dieser Artikel beschreibt, wie Sie eine Konsolenanwendung erstellen, die das CSOM zum Erstellen und Veröffentlichen von Projekten verwendet. Nach der Veröffentlichung eines Projekts, die Anwendung wartet darauf, dass der Project Server-Warteschlangendienst auf Fertig stellen, mit der Veröffentlichungsaktion und zeigt dann die veröffentlichten Projekte.
ms.openlocfilehash: 1815122ce824fcd2f9b8c9119346ca02c720ae89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796196"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Erste Schritte mit dem Project Server-CSOM und .NET

Sie können das Project Server 2013 mithilfe der clientseitigen Objektmodell (CSOM) zum Entwickeln von Project Online und lokale Lösungen mit .NET Framework 4 verwenden. Dieser Artikel beschreibt, wie Sie eine Konsolenanwendung erstellen, die das CSOM zum Erstellen und Veröffentlichen von Projekten verwendet. Nach der Veröffentlichung eines Projekts, die Anwendung wartet darauf, dass der Project Server-Warteschlangendienst auf Fertig stellen, mit der Veröffentlichungsaktion und zeigt dann die veröffentlichten Projekte.
  
Eine allgemeine Einführung in die Project Server-CSOM finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). Referenzthemen im CSOM-Namespace finden Sie unter [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Erstellen eines CSOM-Projekts in Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Verwenden Sie Visual Studio 2010 oder Visual Studio 2012, zum Entwickeln von Lösungen, die die Project Server-CSOM verwenden. Die Project Server-CSOM umfasst drei Assemblys für die Entwicklung von Clientanwendungen, Microsoft Silverlight-Anwendungen und Windows Phone 8-Anwendungen mithilfe von .NET Framework 4. Das CSOM enthält auch eine JavaScript-Datei für die Entwicklung von Webanwendungen, wie in [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) beschrieben. 
  
Sie können die CSOM-Assembly, die Sie benötigen aus der Project Server-Computer oder aus der Project 2013-SDK-Download auf einem Computer remoteentwicklung kopieren. Die **QueueCreateProject** Konsolenanwendung, die in diesem Thema beschrieben wird ist keiner Silverlight-Anwendung oder einer Windows Phone 8-Anwendung benötigen Sie die Assembly Microsoft.ProjectServer.Client.dll. Da das CSOM unabhängig von der WCF-basierte oder ASMX-basierte Project Server Interface (PSI) ist, müssen Sie keinen zum Festlegen von Dienstverweise für die PSI, oder verwenden Sie den **Microsoft.Office.Project.Server.Library** -Namespace. 
  
Die Anwendung **QueueCreateProject** verwendet Befehlszeilenargumente für den Namen des Projekts, um das Erstellen und die Warteschlange Zeitlimit für. In Schritt 1 erstellen die standardkonsolenanwendung, eine Routine zum Analysieren der Befehlszeile hinzufügen und eine Hilfetext hinzufügen, treten Fehler in der Befehlszeile. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Verfahren 1: So erstellen Sie ein CSOM-Projekt in Visual Studio

1. Kopieren Sie die Assembly Microsoft.ProjectServer.Client.dll aus der `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` Ordner auf Ihrem Entwicklungscomputer. Kopieren Sie die Assembly in einen Ordner komfortable für andere Project Server und SharePoint-Verweisassemblys, die Sie, z. B. verwenden möchten `C:\Project\Assemblies`.
    
2. Kopieren Sie die Microsoft.SharePoint.Client.dll-Assembly und die Microsoft.SharePoint.Client.Runtime.dll-Assembly aus demselben Quellordner auf Ihren Entwicklungscomputer. Die Microsoft.ProjectServer.Client.dll-Assembly verfügt über Abhängigkeiten für die zugehörigen SharePoint-Assemblys.
    
3. Klicken Sie in Visual Studio erstellen Sie eine Windows, und legen Sie das Zielframework in .NET Framework 4. Nennen Sie beispielsweise die Anwendung QueueCreateProject.
    
   > [!NOTE]
   > Wenn Sie vergessen, das richtige Ziel, festzulegen, nachdem Visual Studio das Projekt erstellt haben, öffnen Sie im Menü **Projekt** **QueueCreateProject Eigenschaften** . Wählen Sie auf der Registerkarte **Anwendung** in der Dropdownliste **Zielframework** **.NET Framework 4**. Verwenden Sie das **.NET Framework 4 Client Profile**nicht. 
  
4. Legen Sie im Projektmappen-Explorer Verweise auf die folgenden Assemblys fest:
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. In der Datei Program.cs Bearbeiten der `using` Anweisungen, die wie folgt. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. Fügen Sie Methoden zum Analysieren der Befehlszeilenargumente für den Projektnamen und die Anzahl von Sekunden für das Warteschlangen-Zeitlimit, das Anzeigen von Verwendungsinformationen und das Beenden der Anwendung hinzu. Ersetzen Sie den Hauptteil des Codes in der Datei „Program.cs“ durch den folgenden Code.
    
   ```cs
    namespace QueueCreateProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                if (!ParseCommandLine(args))
                {
                    Usage();
                    ExitApp();
                }
                /* Add calls to methods here to get the project context and create a project. */
                ExitApp();
            }
            // Parse the command line. Return true if there are no errors.
            private static bool ParseCommandLine(string[] args)
            {
                bool error = false;
                int argsLen = args.Length;
                try
                {
                    for (int i = 0; i < argsLen; i++)
                    {
                        if (error) break;
                        if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                            args[i] = "*" + args[i].Substring(1).ToLower();
                        switch (args[i])
                        {
                            case "*projname":
                            case "*n":
                                if (++i >= argsLen) return false;
                                projName = args[i];
                                break;
                            case "*timeout":
                            case "*t":
                                if (++i >= argsLen) return false;
                                timeoutSeconds = Convert.ToInt32(args[i]);
                                break;
                            case "*?":
                            default:
                                error = true;
                                break;
                        }
                    }
                }
                catch (FormatException)
                {
                    error = true;
                }
                if (string.IsNullOrEmpty(projName)) error = true;
                return !error;
            }
            private static void Usage()
            {
                string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
                example += "\nExample: QueueCreateProject -n \"My new project\"";
                example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
                Console.WriteLine(example);
            }
            private static void ExitApp()
            {
                Console.Write("\nPress any key to exit... ");
                Console.ReadKey(true);
                Environment.Exit(0);
            }
        }
    }
   ```

## <a name="getting-the-project-context"></a>Abrufen des Projektkontexts
<a name="pj15_GettingStartedCSOM_GettingContext"> </a>

CSOM Entwicklung erfordert das **ProjectContext** -Objekt, das mit der Project Web App-URL nicht initialisiert werden. Der Code in Schritt 2 verwendet die **PwaPath** -Konstante. Wenn Sie die Anwendung für mehrere Instanzen von Project Web App verwenden möchten, können Sie **PwaPath** stellen Sie eine Variable und Hinzufügen einer anderen Befehlszeilenargument. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Verfahren 2: So rufen Sie den Projektkontext ab

1. Hinzufügen von **Programm** -Klasse Konstanten und Variablen, die die **QueueCreateProject** -Anwendung verwendet wird. Zusätzlich zu den Project Web App-URL verwendet die Anwendung den Namen der standardmäßige Enterprise-Projekttyp (EPT), den Namen des Projekts zu erstellen und eine maximale Warteschlangentimeout in Sekunden an. In diesem Fall kann die Variable **TimeoutSeconds** Sie testen, wie verschiedene Werte für das Timeout die Anwendung auswirken. Das **ProjectContext** -Objekt ist das primäre Objekt für den Zugriff auf die CSOM. 
    
   ```cs
    private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Ersetzen Sie die `/* Add calls to methods here to get the project context and create a project. */` Kommentar durch den folgenden Code. Das **Microsoft.ProjectServer.Client.ProjectContext** -Objekt wird mit der Project Web App-URL initialisiert. Die **CreateTestProject** -Methode und die **ListPublishedProjects** -Methode sind im Verfahren 4 und 5 Verfahren dargestellt. 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>Abrufen eines Enterprise-Projekttyps
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

Die beispielanwendung **QueueCreateProject** wählt explizit Enterprise Standardprojekt-EPT um anzuzeigen, wie eine Anwendung die EPT für ein Projekt auswählen kann. Wenn die Informationen zur Erstellung von Projekt nicht die EPT GUID angegeben wird, würde eine Anwendung der Standard-EPT verwenden. Die **GetEptUid** -Methode wird von der **CreateTestProject** -Methode verwendet, die im Verfahren 4 beschrieben wird. 
  
Die Methode **GetEptUid** fragt das **ProjectContext** -Objekt für die Auflistung der **EnterpriseProjectTypes** , in dem die EPT der Name der den angegebenen Namen entspricht. Nach dem Ausführen der Abfrage, wird die Variable **EptUid** auf die GUID des ersten Objekts in der Auflistung **EptList** **EnterpriseProjectType** festgelegt. Da EPT Namen eindeutig sind, besteht nur ein **EnterpriseProjectType** -Objekt, das dem angegebenen Namen ab. 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>Verfahren 3: So rufen Sie die GUID für den ETP eines neuen Projekts ab

- Fügen Sie die **GetEptUid** -Methode auf die **Programm** -Klasse. 
    
   ```cs
    // Get the GUID of the specified enterprise project type.
    private static Guid GetEptUid(string eptName)
    {
        Guid eptUid = Guid.Empty;
        try
        {
            // Get the list of EPTs that have the specified name. 
            // If the EPT name exists, the list will contain only one EPT.
            var eptList = projContext.LoadQuery(
                projContext.EnterpriseProjectTypes.Where(
                    ept => ept.Name == eptName));
            projContext.ExecuteQuery();
            eptUid = eptList.First().Id;
        }
        catch (Exception ex)
        {
            string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                eptName, ex.GetBaseException().ToString());
            throw new ArgumentException(msg);
        }
        return eptUid;
    }
   ```

Es gibt verschiedene Möglichkeiten, die EPT-GUID finden. Die Abfrage in der **GetEptUid** -Methode dargestellt ist effizient, da sie nur das einzige Objekt **EnterpriseProjectType** heruntergeladen, das mit dem Namen EPT übereinstimmt. Die folgenden alternative Routine ist weniger effizient, da sie die vollständige Liste der EPTs an die Clientanwendung downloads und und der Liste durchlaufen. 

```cs
foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
{
    if (ept.Name == eptName)
    {
        eptUid = ept.Id;
        break;
    }
}
```

Die folgende Routine mithilfe einen LINQ-Abfrage und Lambda-Ausdruck das EPT-Objekt ausgewählt, aber weiterhin alle Objekte **EnterpriseProjectType** downloads. 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Festlegen der Erstellungsinformationen und Veröffentlichen des Projekts
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

Die **CreateTestProject** -Methode erstellt ein **ProjectCreationInformation** -Objekt und gibt die Informationen, die zum Erstellen eines Projekts erforderlich ist. Die Projekt-GUID und Name sind erforderlich. Das Startdatum, die Beschreibung des Projekts und die EPT GUID sind optional. 
  
Nach dem Festlegen der neuen Projekteigenschaften, fügt die **Projects.Add** -Methode des Projekts zur **Projects** -Auflistung. Um zu speichern und veröffentlichen Sie das Projekt, müssen Sie die **Projects.Update** -Methode zum Senden einer Nachricht an die Project Server-Warteschlange, und erstellen Sie ein Projekt aufrufen. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>Verfahren 4: So legen Sie die neuen Projekteigenschaften fest, erstellen das Projekt und veröffentlichen das Projekt

1. Fügen Sie die **CreateTestProject** -Methode auf die **Programm** -Klasse. Der folgende Code erstellt und ein Projekt veröffentlicht, aber wartet für die Durchführung der Warteschlangenauftrag nicht. 
    
   ```cs
    // Create a project.
    private static bool CreateTestProject()
    {
        bool projCreated = false;
        try
        {
            Console.Write("\nCreating project: {0} ...", projName);
            ProjectCreationInformation newProj = new ProjectCreationInformation();
            newProj.Id = Guid.NewGuid();
            newProj.Name = projName;
            newProj.Description = "Test creating a project with CSOM";
            newProj.Start = DateTime.Today.Date;
            // Setting the EPT GUID is optional. If no EPT is specified, Project Server  
            // uses the default EPT. 
            newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
            PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
            QueueJob qJob = projContext.Projects.Update();
            /* Add code here to wait for the queue. */
        }
        catch(Exception ex)
        {
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("\nError: {0}", ex.Message);
            Console.ResetColor();
        }
        return projCreated;
    }
   ```

2. Ersetzen Sie die `/* Add code here to wait for the queue. */` Kommentar durch den folgenden Code für den Warteschlangenauftrag gewartet. Die Routine wartet, bis zu der angegebenen **TimeoutSeconds** Anzahl von Sekunden oder wird fortgesetzt, wenn vor dem Timeout der Warteschlangenauftrag beendet wurde. Mögliche Warteschlange Auftragsstatusangaben finden Sie unter [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) . 
    
   Das Aufrufen der **Load** -Methode und die **ExecuteQuery** -Methode für das Objekt **QueueJob** ist optional. Wenn das **QueueJob** -Objekt nicht initialisiert wird, wenn Sie die **WaitForQueue** -Methode aufrufen, Project Server wird initialisiert. 
    
   ```cs
    // Calling Load and ExecuteQuery for the queue job is optional.
    // projContext.Load(qJob);
    // projContext.ExecuteQuery();
    JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    if (jobState == JobState.Success)
    {
        projCreated = true;
    }
    else
    {
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
            timeoutSeconds);
        Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
        Console.ResetColor();
    }
    Console.WriteLine();
   ```

## <a name="listing-the-published-projects"></a>Auflisten der veröffentlichten Projekte
<a name="pj15_GettingStartedCSOM_ListingPublished"> </a>

Die **ListPublishedProjects** -Methode ruft die Auflistung aller Projekte, die in Project Web App veröffentlicht werden. Wenn der Warteschlangenauftrag erstellt, die in Verfahren 4 ein Projekt nicht erfolgreich abgeschlossen oder ein Timeout, das neue Projekt nicht in der **Projects** -Auflistung enthalten ist. 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Verfahren 5: So listen Sie die veröffentlichten Projekte auf

1. Fügen Sie die **ListPublishedProjects** -Methode auf die **Programm** -Klasse. 
    
   ```cs
    // List the published projects.
    private static void ListPublishedProjects()
    {
        // Get the list of projects on the server.
        projContext.Load(projContext.Projects);
        projContext.ExecuteQuery();
        Console.WriteLine("\nProject ID : Project name : Created date");
        foreach (PublishedProject pubProj in projContext.Projects)
        {
            Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                pubProj.CreatedDate.ToString());
        }
    }
   ```

2. Legen Sie den richtigen Wert für die Project Web App-URL, kompilieren Sie die Anwendung **QueueCreateProject** , und Testen Sie die Anwendung wie in der Prozedur 6. 
    
## <a name="testing-the-queuecreateproject-application"></a>Testen der QueueCreateProject-Anwendung
<a name="pj15_GettingStartedCSOM_Testing"> </a>

Wenn Sie zuerst die **QueueCreateProject** -Anwendung auf einer Testinstanz von Project Web App ausführen, insbesondere wenn Project Server auf einem virtuellen Computer installiert ist möglicherweise die Anwendung mehr Zeit als das Standardtimeout für die Warteschlange von zehn Sekunden ausführen erforderlich. 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Verfahren 6: So testen Sie die QueueCreateProject-Anwendung

1. Öffnen Sie das Fenster **QueueCreateProject Eigenschaften** , wählen Sie die Registerkarte **Debuggen** , und fügen Sie im Abschnitt **Startoptionen** die folgenden Befehlszeilenargumente:`-n "Test proj 1" -t 20`
    
   Führen Sie die Anwendung (z. B. drücken Sie **F5**). Wenn Sie der Timeoutwert lange genug ist, zeigt die Anwendung die folgende Ausgabe (wenn andere veröffentlichte Projekte in der Project Web App-Instanz vorhanden ist, sie werden auch werden angezeigt):
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Führen Sie einen weiteren Test das Standardtimeout 10 Sekunden Warteschlange verwendet die folgenden Befehlszeilenargumente aus:`-n "Test proj 1"`
    
   Da „Test Proj 1“ bereits vorhanden ist, zeigt die Anwendung folgende Ausgabe an.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Führen Sie einen weiteren Test das Standardtimeout 10 Sekunden Warteschlange verwendet die folgenden Befehlszeilenargumente aus:`-n "Test proj 2"`
    
   Die **QueueCreateProject** -Anwendung erstellt und veröffentlicht das Projekt mit dem Namen Test Proj 2. 
    
4. Führen Sie einen anderen Test mit den folgenden Befehlszeilenargumente, und legen Sie den Timeoutwert zu kurz für Warteschlangenauftrag beendet werden:`-n "Test proj 3" -t 1`
    
   Da das Warteschlangen-Zeitlimit zu kurz ist, wird das Projekt nicht erstellt. Die Anwendung zeigt die folgende Ausgabe.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Ändern Sie den Code, damit die Anwendung nicht darauf warten, dass der Warteschlangenauftrag. Beispielsweise kommentieren Sie den Code, die für die Warteschlange, außer für wartet die `projCreated = true` Zeile wie folgt. 
    
   ```cs
    //JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    //if (jobState == JobState.Success)
    //{
    projCreated = true;
    //}
    //else
    //{
    //    Console.ForegroundColor = ConsoleColor.Yellow;
    //    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.",
    //        timeoutSeconds);
    //    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
    //    Console.ResetColor();
    //}
    
   ```

6. Kompilieren Sie die Anwendung neu, und führen Sie einen weiteren Test mit den folgenden Befehlszeilenargumente:`-n "Test proj 4"`
    
   Da die Routine **WaitForQueue** auskommentiert ist, wird die Anwendung Standardtimeoutwert nicht verwendet. Obwohl die Anwendung für die Warteschlange nicht wartet kann es Test Proj 4, anzeigen, wenn die Veröffentlichungsaktion in Project Server schnell genug ist. 
    
   ```MS-DOS
    Creating project: Test proj 4 ...
    Project ID : Project name : Created date
            cdd54103-082f-425c-b075-9ff52ac7d4e6 :
            Test proj 2 : 9/25/2011 4:28:55 PM
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
            5c0c73f2-f5dd-499b-8bd8-ebb74bf8c122 :
            Test proj 4 : 9/25/2011 4:39:21 PM
    Press any key to exit...
   ```

Aktualisieren Sie die Seite Projektcenter in Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), um die veröffentlichten Projekte anzeigen. Die folgende Abbildung zeigt, dass die Testprojekte veröffentlicht werden.

**Überprüfen der veröffentlichten Projekte in Project Web App**

![Überprüfen der veröffentlichten Projekte in Project Web App] (media/pj15_GetStartedCSOMNET_pwa.gif "Überprüfen der veröffentlichten Projekte in Project Web App")
  
Die beispielanwendung **QueueCreateProject** zeigt eine typische Beispiel dafür, wie eine Project-Entität mit dem Clientobjektmodell So erstellen Sie mithilfe der **ProjectCreationInformation** -Klasse zum Hinzufügen des Projekts zu der veröffentlichten-Auflistung, wie von einem Warteschlangenauftrag gewartet verwenden die **WaitForQueue** -Methode und wie die Auflistung von veröffentlichten Projekten aufgelistet werden. 
  
## <a name="complete-code-example"></a>Vollständiges Codebeispiel
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

Es folgt der vollständige Code für die **QueueCreateProject** beispielanwendung aus. [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) Class Reference enthält auch den Code in diesem Thema. 
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Microsoft.ProjectServer.Client;
namespace QueueCreateProject
{
    class Program
    {
        private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
        private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
        private static string projName = string.Empty;
        private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
        private static ProjectContext projContext;
        static void Main(string[] args)
        {
            if (!ParseCommandLine(args))
            {
                Usage();
                ExitApp();
            }
            projContext = new ProjectContext(pwaPath);
            if (CreateTestProject())
                ListPublishedProjects();
            else
                Console.WriteLine("\nProject creation failed: {0}", projName);
            ExitApp();
        }
        // Create a project.
        private static bool CreateTestProject()
        {
            bool projCreated = false;
            try
            {
                Console.Write("\nCreating project: {0} ...", projName);
                ProjectCreationInformation newProj = new ProjectCreationInformation();
                newProj.Id = Guid.NewGuid();
                newProj.Name = projName;
                newProj.Description = "Test creating a project with CSOM";
                newProj.Start = DateTime.Today.Date;
                // Setting the EPT GUID is optional. If no EPT is specified, Project Server uses 
                // the default EPT. 
                newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
                PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
                QueueJob qJob = projContext.Projects.Update();
                // Calling Load and ExecuteQuery for the queue job is optional. If qJob is 
                // not initialized when you call WaitForQueue, Project Server initializes it.
                // projContext.Load(qJob);
                // projContext.ExecuteQuery();
                JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
                if (jobState == JobState.Success)
                {
                    projCreated = true;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
                        timeoutSeconds);
                    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
                    Console.ResetColor();
                }
                Console.WriteLine();
            }
            catch(Exception ex)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("\nError: {0}", ex.Message);
                Console.ResetColor();
            }
            return projCreated;
        }
        // Get the GUID of the specified enterprise project type.
        private static Guid GetEptUid(string eptName)
        {
            Guid eptUid = Guid.Empty;
            try
            {
                // Get the list of EPTs that have the specified name. 
                // If the EPT name exists, the list will contain only one EPT.
                var eptList = projContext.LoadQuery(
                    projContext.EnterpriseProjectTypes.Where(
                        ept => ept.Name == eptName));
                projContext.ExecuteQuery();
                eptUid = eptList.First().Id;
                // Alternate routines to find the EPT GUID. Both (a) and (b) download the entire list of EPTs.
                // (a) Using a foreach block:
                //foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
                //{
                //    if (ept.Name == eptName)
                //    {
                //        eptUid = ept.Id;
                //        break;
                //    }
                //}
                // (b) Querying for the EPT list, and then using a lambda expression to select the EPT:
                //var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
                //projContext.ExecuteQuery();
                //eptUid = eptList.First(ept => ept.Name == eptName).Id;
            }
            catch (Exception ex)
            {
                string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                    eptName, ex.GetBaseException().ToString());
                throw new ArgumentException(msg);
            }
            return eptUid;
        }
        // List the published projects.
        private static void ListPublishedProjects()
        {
            // Get the list of projects on the server.
            projContext.Load(projContext.Projects);
            projContext.ExecuteQuery();
            Console.WriteLine("\nProject ID : Project name : Created date");
            foreach (PublishedProject pubProj in projContext.Projects)
            {
                Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                    pubProj.CreatedDate.ToString());
            }
        }
        // Parse the command line. Return true if there are no errors.
        private static bool ParseCommandLine(string[] args)
        {
            bool error = false;
            int argsLen = args.Length;
            try
            {
                for (int i = 0; i < argsLen; i++)
                {
                    if (error) break;
                    if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                        args[i] = "*" + args[i].Substring(1).ToLower();
                    switch (args[i])
                    {
                        case "*projname":
                        case "*n":
                            if (++i >= argsLen) return false;
                            projName = args[i];
                            break;
                        case "*timeout":
                        case "*t":
                            if (++i >= argsLen) return false;
                            timeoutSeconds = Convert.ToInt32(args[i]);
                            break;
                        case "*?":
                        default:
                            error = true;
                            break;
                    }
                }
            }
            catch (FormatException)
            {
                error = true;
            }
            if (string.IsNullOrEmpty(projName)) error = true;
            return !error;
        }
        private static void Usage()
        {
            string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
            example += "\nExample: QueueCreateProject -n \"My new project\"";
            example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
            Console.WriteLine(example);
        }
        private static void ExitApp()
        {
            Console.Write("\nPress any key to exit... ");
            Console.ReadKey(true);
            Environment.Exit(0);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md) 
- [Client-seitigen Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
    

