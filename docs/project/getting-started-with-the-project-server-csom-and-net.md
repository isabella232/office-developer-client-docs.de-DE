---
title: Erste Schritte mit dem Project Server-CSOM und .NET
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Sie können das clientseitige Objektmodell (CSOM) von Project Server 2013 verwenden, um Project Online und lokale Lösungen mit .NET Framework 4 zu entwickeln. Dieser Artikel beschreibt, wie Sie eine Konsolenanwendung erstellen, die das CSOM zum Erstellen und Veröffentlichen von Projekten verwendet. Nach dem Veröffentlichen eines Projekts wartet die Anwendung, bis der Project Server-Warteschlangendienst die Veröffentlichung abgeschlossen hat und listet dann die veröffentlichten Projekte auf.
localization_priority: Priority
ms.openlocfilehash: b53587ca1959faefdc1b40f08c4adfda4ee11d70
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710461"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Erste Schritte mit dem Project Server-CSOM und .NET

Sie können das clientseitige Objektmodell (CSOM) von Project Server 2013 verwenden, um Project Online und lokale Lösungen mit .NET Framework 4 zu entwickeln. Dieser Artikel beschreibt, wie Sie eine Konsolenanwendung erstellen, die das CSOM zum Erstellen und Veröffentlichen von Projekten verwendet. Nach dem Veröffentlichen eines Projekts wartet die Anwendung, bis der Project Server-Warteschlangendienst die Veröffentlichung abgeschlossen hat und listet dann die veröffentlichten Projekte auf.
  
Eine allgemeine Einführung in das Project Server-CSOM finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). Referenzthemen im CSOM-Namespace finden Sie unter [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Erstellen eines CSOM-Projekts in Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Sie können Visual Studio 2010 oder Visual Studio 2012 verwenden, um Lösungen zu entwickeln, die das Project Server-CSOM verwenden. Das Project Server-CSOM umfasst drei Assemblys für die Entwicklung von Clientanwendungen, Microsoft Silverlight-Anwendungen und Windows Phone 8-Anwendungen mit .NET Framework 4. Das CSOM umfasst außerdem eine JavaScript-Datei für die Entwicklung von Webanwendungen, wie in [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) beschrieben. 
  
Sie können die benötigte CSOM-Assembly vom Project Server-Computer oder aus dem Project 2013-SDK-Download auf einen Remote-Entwicklungscomputer kopieren. Die **QueueCreateProject**-Konsolenanwendung, die in diesem Thema beschrieben wird, ist keine Silverlight- oder Windows Phone 8-Anwendung. Sie werden also die Microsoft.ProjectServer.Client.dll-Assembly benötigen. Da das CSOM unabhängig von der WCF- oder ASMX-basierten Project Server Interface (PSI) ist, müssen Sie keine Dienstverweise für die PSI festlegen oder den **Microsoft.Office.Project.Server.Library**-Namespace festlegen. 
  
Die **QueueCreateProject**-Anwendung verwendet Befehlszeilenargumente für den Namen des zu erstellenden Projekts und das Warteschlangen-Zeitlimit In Verfahren 1 erstellen Sie die grundlegende Konsolenanwendung, fügen eine Routine zum Analysieren der Befehlszeile hinzu und fügen eine Nachricht die Verwendung hinzu, falls Fehler in der Befehlszeile auftreten. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Verfahren 1: So erstellen Sie ein CSOM-Projekt in Visual Studio

1. Kopieren Sie die Microsoft.ProjectServer.Client.dll-Assembly aus dem Ordner `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` auf den Entwicklungscomputer. Kopieren Sie die Assembly in einen geeigneten Ordner für andere Project Server- und SharePoint-Referenzassemblys, die Sie verwenden möchten, z. B. `C:\Project\Assemblies`.
    
2. Kopieren Sie die Microsoft.SharePoint.Client.dll-Assembly und die Microsoft.SharePoint.Client.Runtime.dll-Assembly aus demselben Quellordner auf Ihren Entwicklungscomputer. Die Microsoft.ProjectServer.Client.dll-Assembly verfügt über Abhängigkeiten für die zugehörigen SharePoint-Assemblys.
    
3. Erstellen Sie in Visual Studio eine Windows-Konsolenanwendung, und legen Sie das Zielframework auf .NET Framework 4 fest. Nennen Sie die Anwendung z. B. QueueCreateProject.
    
   > [!NOTE]
   > Wenn Sie vergessen, das richtige Ziel festzulegen, nachdem Visual Studio das Projekts erstellt hat, öffnen Sie **Eigenschaften von QueueCreateProject** im Menü **Projekt**. Wählen Sie auf der Registerkarte **Anwendung** in der Dropdown-Liste **Zielframework** die Option **.NET Framework 4**. Verwenden Sie nicht **.NET Framework 4 Client Profile**. 
  
4. Legen Sie im Projektmappen-Explorer Verweise auf die folgenden Assemblys fest:
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. Bearbeiten Sie in der Datei „Program.cs“ die `using`-Anweisungen wie folgt. 
    
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

Die CSOM-Entwicklung erfordert, dass das **ProjectContext**-Objekt mit der Project Web App-URL initialisiert wird. Der Code in Verfahren 2 verwendet die **pwaPath**-Konstante. Wenn Sie beabsichtigen, die Anwendung für mehrere Instanzen von Project Web App zu verwenden, können Sie **pwaPath** zu einer Variablen machen und ein weiteres Befehlszeilenargument hinzufügen. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Verfahren 2: So rufen Sie den Projektkontext ab

1. Fügen Sie **Program**-Klassenkonstanten und -Variablen hinzu, die von der **QueueCreateProject**-Anwendung verwendet werden. Zusätzlich zur Project Web App-URL verwendet die Anwendung den Namen des standardmäßigen Enterprise-Projekttyps (EPT), den Namen des zu erstellenden Projekts und ein maximales Warteschlangen-Zeitlimit in Sekunden. In diesem Fall ermöglicht Ihnen die **timeoutSeconds**-Variable zu testen, wie sich verschiedene Werte für das Zeitlimit auf die Anwendung auswirken. Das **ProjectContext**-Objekt ist das primäre Objekt für den Zugriff auf das CSOM. 
    
   ```cs
    private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Ersetzen Sie den Kommentar `/* Add calls to methods here to get the project context and create a project. */` durch den folgenden Code. Das **Microsoft.ProjectServer.Client.ProjectContext**-Objekt wird mit der Project Web App-URL initialisiert. Die **CreateTestProject**-Methode und die **ListPublishedProjects**-Methode werden in Verfahren 4 und Verfahren 5 gezeigt. 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>Abrufen eines Enterprise-Projekttyps
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

Die **QueueCreateProject**-Beispielanwendung wählt explizit den Enterprise-Projekt-EPT aus, um zu zeigen, wie eine Anwendung den EPT für ein Projekt auswählen kann. Wenn die Projekterstellungsinformationen die EPT-GUID nicht angeben, verwendet eine Anwendung den Standard-EPT. Die **GetEptUid**-Methode wird von der **CreateTestProject**-Methode verwendet, die in Verfahren 4 beschriebenen wird. 
  
Die **GetEptUid**-Methode fragt das **ProjectContext**-Objekt für die Auflistung von **EnterpriseProjectTypes** ab, deren EPT-Namen dem angegebenen Namen entsprechen. Nach dem Ausführen der Abfrage wird die **eptUid**-Variable auf die GUID des ersten **EnterpriseProjectType**-Objekts in der **eptList**-Auflistung festgelegt. Da EPT-Namen eindeutig sind, gibt es nur ein **EnterpriseProjectType**-Objekt mit dem angegebenen Namen. 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>Verfahren 3: So rufen Sie die GUID für den ETP eines neuen Projekts ab

- Fügen Sie die **GetEptUid**-Methode zur **Program**-Klasse hinzu. 
    
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

Es gibt mehrere Möglichkeiten, die EPT-GUID zu ermitteln. Die in der **GetEptUid**-Methode gezeigte Abfrage ist effizient, da sie nur das eine **EnterpriseProjectType**-Objekt herunterlädt, das dem EPT-Namen entspricht. Die folgende alternative Routine ist weniger effizient, da sie die vollständige Liste der EPTs in die Clientanwendung herunterlädt und die Liste mehrmals durchläuft. 

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

Die folgende Routine verwendet eine LINQ-Abfrage und einen Lambda-Ausdruck zum Auswählen des EPT-Objekts, lädt jedoch auch alle **EnterpriseProjectType**-Objekte herunter. 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Festlegen der Erstellungsinformationen und Veröffentlichen des Projekts
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

Die **CreateTestProject**-Methode erstellt ein **ProjectCreationInformation**-Objekt und gibt die Informationen an, die zum Erstellen eines Projekts erforderlich sind. Die GUID des Projekts und der Name sind erforderlich. Das Startdatum, die Projektbeschreibung und die EPT-GUID sind optional. 
  
Nach dem Festlegen der neuen Projekteigenschaften fügt die **Projects.Add**-Methode das Projekt zur **Projects**-Auflistung hinzu. Zum Speichern und Veröffentlichen des Projekts müssen Sie die **Projects.Update**-Methode aufrufen, um eine Nachricht an die Project Server-Warteschlange zu senden und das Projekt zu erstellen. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>Verfahren 4: So legen Sie die neuen Projekteigenschaften fest, erstellen das Projekt und veröffentlichen es

1. Fügen Sie die **CreateTestProject**-Methode zur **Program**-Klasse hinzu. Mit dem folgende Code wird ein Projekt erstellt und veröffentlicht, es wird jedoch nicht gewartet, bis der Warteschlangenauftrag abgeschlossen ist. 
    
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

2. Ersetzen Sie den Kommentar `/* Add code here to wait for the queue. */` durch den folgenden Code, damit auf den Abschluss des Warteschlangenauftrags gewartet wird. Die Routine wartet maximal die für **timeoutSeconds** angegebene Anzahl von Sekunden oder fährt fort, wenn der Warteschlangenauftrag vor dem Zeitlimit abgeschlossen ist. Mögliche Zustände von Aufträgen in der Warteschlange finden Sie unter [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx). 
    
   Das Aufrufen der **Load**-Methode und der **ExecuteQuery**-Methode für das **QueueJob**-Objekt ist optional. Wenn das **QueueJob**-Objekt beim Aufrufen der **WaitForQueue**-Methode nicht initialisiert ist, initialisiert Project Server die Methode. 
    
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

Die **ListPublishedProjects**-Methode ruft die Sammlung aller Projekte ab, die in Project Web App veröffentlicht wurden. Wenn der Warteschlangenauftrag, der in Verfahren 4 ein Projekt erstellt, nicht erfolgreich abgeschlossen wurde oder das Zeitlimit überschreitet, wird das neue Projekt nicht in die **Projects**-Sammlung aufgenommen. 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Verfahren 5: So listen Sie die veröffentlichten Projekte auf

1. Fügen Sie die **ListPublishedProjects**-Methode zur **Program**-Klasse hinzu. 
    
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

2. Legen Sie den richtigen Wert für die Project Web App-URL fest, kompilieren Sie die **QueueCreateProject**-Anwendung, und testen Sie dann die Anwendung wie in Verfahren 6 beschrieben. 
    
## <a name="testing-the-queuecreateproject-application"></a>Testen der QueueCreateProject-Anwendung
<a name="pj15_GettingStartedCSOM_Testing"> </a>

Beim ersten Ausführen der **QueueCreateProject**-Anwendung auf einer Testinstanz von Project Web App, insbesondere dann, wenn Sie Project Server auf einem virtuellen Computer installiert haben, benötigt die Anwendung möglicherweise mehr Zeit für die Ausführung als das Standardzeitlimit für Warteschlangen von 10 Sekunden. 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Verfahren 6: So testen Sie die QueueCreateProject-Anwendung

1. Öffnen Sie das Fenster **Eigenschaften von QueueCreateProject**, wählen Sie die Registerkarte **Debuggen** aus, und fügen Sie dann die folgenden Befehlszeilenargumente in den Abschnitt **Startoptionen** ein: `-n "Test proj 1" -t 20`
    
   Führen Sie die Anwendung aus (drücken Sie z. B. **F5**). Wenn das Zeitlimit lang genug ist, zeigt die Anwendung die folgende Ausgabe an (wenn in Ihrer Project Web App-Instanz andere veröffentlichte Projekte vorhanden sind, werden diese ebenfalls angezeigt):
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Führen Sie einen weiteren Test mit den folgenden Befehlszeilenargumenten durch, um das standardmäßige Warteschlangen-Zeitlimit von 10 Sekunden anzuwenden: `-n "Test proj 1"`
    
   Da „Test Proj 1“ bereits vorhanden ist, zeigt die Anwendung folgende Ausgabe an.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Führen Sie einen weiteren Test mit den folgenden Befehlszeilenargumenten durch, um das standardmäßige Warteschlangen-Zeitlimit von 10 Sekunden anzuwenden: `-n "Test proj 2"`
    
   Die **QueueCreateProject**-Anwendung erstellt und veröffentlicht das Projekt mit dem Namen „Test Proj 2“. 
    
4. Führen Sie einen weiteren Test mit den folgenden Befehlszeilenargumenten durch, und legen Sie das Zeitlimit so kurz fest, dass der Warteschlangenauftrag nicht abgeschlossen werden kann: `-n "Test proj 3" -t 1`
    
   Da das Warteschlangen-Zeitlimit zu kurz ist, wird das Projekt nicht erstellt. Die Anwendung zeigt die folgende Ausgabe an.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Ändern Sie den Code so, dass die Anwendung nicht auf den Warteschlangenauftrag wartet. Kommentieren Sie zum Beispiel den Code aus, der auf die Warteschlange wartet, mit Ausnahme der folgenden `projCreated = true`-Zeile. 
    
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

6. Kompilieren Sie die Anwendung neu, und führen Sie einen weiteren Test mit den folgenden Befehlszeilenargumenten durch: `-n "Test proj 4"`
    
   Da die **WaitForQueue**-Routine auskommentiert ist, verwendet die Anwendung nicht den Standardwert für das Zeitlimit. Obwohl die Anwendung nicht auf die Warteschlange wartet, zeigt sie möglicherweise „Test Proj 4“ an, wenn die Veröffentlichungsaktion in Project Server schnell genug ist. 
    
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

Aktualisieren Sie die Projektcenter-Seite in Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`), um die veröffentlichten Projekte anzuzeigen. Die folgende Abbildung zeigt, dass die Projekte veröffentlicht wurden.

**Überprüfen der veröffentlichten Projekte in Project Web App**

![Überprüfen die veröffentlichte Projekte in Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Überprüfen die veröffentlichte Projekte in Project Web App")
  
Die **QueueCreateProject**-Beispielanwendung zeigt ein typisches Beispiel für die Erstellung einer Projektentität mit dem CSOM anhand der **ProjectCreationInformation**-Klasse, wie Sie das Projekt zur veröffentlichten Auflistung hinzufügen, wie auf einen Auftrag in der Warteschlange mit der **WaitForQueue**-Methode auf einen Warteschlangenauftrag gewartet wird, und wie die Auflistung der veröffentlichten Projekte aufgelistet wird. 
  
## <a name="complete-code-example"></a>Vollständiges Codebeispiel
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

Nachfolgend ist der vollständige Code für die **QueueCreateProject**-Beispielanwendung aufgeführt. Die [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx)-Klassenreferenz enthält auch den Code in diesem Thema. 
  
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
        private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
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
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
    

