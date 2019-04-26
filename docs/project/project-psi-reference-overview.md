---
title: Project-PSI-Referenz – Übersicht
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- Admin
- Archive
- Authentication
- Calendar
- CubeAdmin
- CustomFields
- Events
- LoginForms
- LoginWindows
- LookupTable
- Notifications
- ObjectLinkProvider
- Project
- Project Server Interface
- Project Server Web services
- PSI
- PSI reference
- PSI Web services
- PWA
- QueueSystem
- Resource
- ResourcePlan
- Rules
- Security
- Statusing
- StatusReports
- TimeSheet
- Version
- View
- Web service
- Web services
- WinProj
- WssInterop
keywords:
- Webdienst, Kalender,Authentifizierung, Web-Dienst,Ressourcenplan, Web-Dienst,Statusberichte, Web-Dienst,PSI, Namespaces,Ereignishandler, Project Server,Web-Dienst, Benachrichtigungen,Warteschlangensystem, Web-Dienst,Project 2013, Plattform,AnmeldungWindows, Web-Dienst,Web-Dienst, Statuserfassung,Web-Dienst, Ressource,WinProj, Web-Dienst,WssInterop, Web-Dienst,Web-Dienst, Winproj,Ereignishandler,Suchtabelle, Web-Dienst,PWA, Web-Dienst, Sicherheit,Benachrichtigungen, Web-Dienst,Web-Dienst, Arbeitszeittabelle,Web-Dienst, Warteschlangensystem,PSI, Web-Dienste,Web-Dienst, Ereignisse,PSI, Programmierung,Web-Dienst, Suchtabelle,Version, Web-Dienst,Benutzerdefinierte Felder, Web-Dienst,Web-Dienst, PWA,PSI,Ressource, Web-Dienst,Web-Dienst, Ressourcenplan,Arbeitszeittabelle, Web-Dienst,Web-Dienst, Regeln,PSI, verwaltete Codereferenz,Sicherheit, Web-Dienst,Web-Dienst, Benutzerdefinierte Felder,URL, für PSI,Web-Dienst, WssInterop,Web service, Admin,Web reference, PSI,Web-Dienst, Cube-Administrator,Ansicht, Web-Dienst,Kalender, Web-Dienst,Web-Dienst, Ansicht,Admin, Web-Dienst,Anmeldeformulare, Web-Dienst,Web-Dienst, Anmeldeformulare,PSI, URLs,Objektlinkprovider, Web-Dienst,Archiv, Web,Cube-Administrator, Web-Dienst,Regeln, Web-Dienst,Web-Dienst, Authentifizierung,Web-Dienst, PSI,Project Server, Ereignisse,ereignisse, Web-Dienst,Web-Dienst, Projekt,Statuserfassung, Web-Dienst,Web-Dienst, Objektlinkprovider,Project Server Interface,Webmethoden, PSI,Web-Dienst, Statusberichte,Web-Dienst, Archiv,Projekt, Web-Dienst,Web-Dienst, AnmeldungWindows
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: Die Project Server Interface (PSI) ist die API, die zum Entwickeln von Anwendungen verwendet wird, die in der lokalen Version von Project Server 2013 integriert sind.
localization_priority: Priority
ms.openlocfilehash: 178f050022916ac1d26bd3d71f0ac5210c92295d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301558"
---
# <a name="project-psi-reference-overview"></a>Übersicht über die Project PSI-Referenz

Die Project Server Interface (PSI) ist die API, die zum Entwickeln von Anwendungen verwendet wird, die in der lokalen Version von Project Server 2013 integriert sind.
  
Dieser Artikel bietet eine Übersicht über die dokumentierten Assemblys, Namespaces und Dienste in der PSI. Die [Project Server 2013-Klassenbibliotheks- und -Webdienstreferenz](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) im SDK enthält die gesamte Dokumentation mit verwaltetem Code für die PSI und den [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)-Namespace in Project Server 2013. Zum Entwickeln von Anwendungen für Project Online müssen Sie anstelle der PSI den **Microsoft.ProjectServer.Client-Namespace** verwenden. 

Die PSI in Project Server 2013 verfügt über eine duale Schnittstelle. Die ASMX-Schnittstelle für Webdienste wird durchDiscovery- und Web Service Description Language-Dateien (disco und WSDL) im virtuellen Verzeichnis `https://ServerName/ProjectServerName/_vti_bin/psi/` (beispielsweise „Projectdisco.aspx“ und „Projectwsdl.aspx“) definiert. Sie können nur über die URL einer lokalen Installation der Project Web App auf die ASMX-Schnittstelle zugreifen (z. B. `https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`). Zum Anzeigen des Webdiensts in einen Browser müssen Sie die `?wsdl`-URL-Option einbeziehen. Da die ASMX-Schnittstelle mithilfe der Windows Communication Foundation(WCF)-Infrastruktur erstellt wird, sind die ASMX-Dateien für die Project Server-Webdienste nicht wirklich im virtuellen PSI-Verzeichnis vorhanden. 
  
Die WCF-Dienstschnittstelle wird durch SVC-Dateien im virtuellen Back-End-Verzeichnis `https://ServerName:32843/GUID/PSI/` in der SharePoint-Webdiensteanwendung definiert. Die URL der PSI-Dienste im virtuellen Project-Dienstanwendungsverzeichnis (beispielsweise `https://ServerName:32843/GUID/PSI/project.svc`) enthält die SVC-Dateien. Sie können die Back-End-URL jedoch nicht direkt zum Festlegen eines WCF-Dienstverweises verwenden. Zum Entwickeln einer Anwendung oder Komponente, die die WCF-Dienste der PSI verwendet, können Sie eine Proxyassembly oder eine Proxydatei verwenden. Der Project 2013-SDK-Download umfasst Proxydateien für die WCF-Dienste in Project Server 2013 und Skripts zum Abrufen aktualisierter WCF-Proxydateien und zum Kompilieren der Dateien in eine Proxyassembly für neuere Project Server-Builds.
  
Der Verzeichnisname des Project-Anwendungsdiensts ist ein GUID-Wert, der mit der GUID der lokalen Project Web App-Instanz identisch ist. Erweitern Sie im Fenster **Internetinformationsdienste-Manager** den Knoten **SharePoint-Webdienste**. Wählen Sie den GUID-Verzeichnisnamen und dann **Erweiterte Einstellungen** zum Kopieren des Werts **Virtueller Pfad** aus. 
  
> [!IMPORTANT]
> Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 zwar veraltet, wird aber weiterhin unterstützt. Neue Anwendungen sollten die WCF-Schnittstelle der PSI oder CSOM verwenden. Weitere Informationen zu veralteten Features finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md).
> 
> Neue Anwendungen und Middleware-Komponenten, die nur auf einer lokalen Installation von Project Server ausgeführt werden, sollten die WCF-Schnittstelle verwenden, da es sich dabei um die von uns empfohlene Technologie für Netzwerkkommunikationen handelt. Legacy-Anwendungen, die die ASMX-Schnittstelle verwenden, müssen die URL über Project Web App verwenden, welche Project Server-Berechtigungen überprüft. 
> 
> Weitere Informationen über die ASMX-Schnittstelle und über die Verwendung der WCF-Schnittstelle finden Sie unter [Voraussetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md) und [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Für die Entwicklung von Anwendungen, die die WCF-Schnittstelle verwenden, können Sie Visual Studio 2010 oder Visual Studio 2012 verwenden. Zum Erstellen deklarativer Project Server-Workflows können Sie SharePoint Designer 2013 verwenden. Project Server-Workflows, die auf die PSI oder das CSOM zugreifen können müssen, können mit Visual Studio 2012 entwickelt werden.
  
### <a name="using-the-psi-reference"></a>Verwenden der PSI-Referenz
<a name="pj15_PSIRefOverview_Using"> </a>

Das PSI-Objektmodell ist groß und viele Klassen und Mitglieder sind nur zur internen Verwendung. Daher kann es verwirrend sein, die gewünschten Themen in der [Project Server 2013-Klassenbibliotheks- und -Webdienstreferenz](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) zu finden. Die meisten Referenzthemen, die Sie für die Entwicklung verwenden, sind in den folgenden Gruppen:
  
- **Primäre Klassenmethoden**: Jeder Dienst in der PSI enthält eine primäre Klasse, die nach dem Namen des Diensts benannt ist. Beispielsweise enthält der Dienst **Resource** die Klasse [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx), die sich im [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx)-Namespace befindet. Erweitern Sie zum Anzeigen einer Liste der in der Klasse **Resource** verfügbaren Methoden den Klassenknoten im Inhaltsbereich, und wählen Sie dann das Thema **Resource Methods** aus. 
    
- **DataRow-Eigenschaften:** Viele der primären Klassenmethoden verwenden ein **DataSet** oder geben eins zurück. Jedes **DataTable**-Objekt in einem **DataSet** enthält Daten in einem oder mehreren **DataRow**-Objekten. In den meisten Fällen müssen Sie nur die Zeileneigenschaften anzeigen können und nicht alle Member der **DataSet**-, **DataTable**- oder **DataRow**-Klassen. Beispielsweise enthält die **ResourceAssignmentDataSet**-Klasse Unterklassen für die Klasse **ResourceAssignmentDataTable** und die Klasse [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx). Erweitern Sie zum Anzeigen einer Liste von Eigenschaften, die sich in der Klasse **ResourceAssignmentRow** befinden, den Klassenknoten im Inhaltsbereich, und wählen Sie dann das Thema **ResourceAssignmentDataSet.ResourceAssignmentRow Properties** aus. 
    
Das Thema [Project Server 2013-Klassenbibliotheks- und -Webdienstreferenz](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) verweist neben den Dienstnamespaces auf die drei Project Server-Assembly, die in der Entwicklung von Drittanbieterlösungen für lokale Installationen verwendet werden. Für diese Assemblys stellen wir nur eine minimale Dokumentation bereit. Die PSI-Referenz dokumentiert die Hauptklassen und Member in den 23 öffentlichen Diensten. Sechs PSI-Dienste dienen nur für interne Zwecke und sind nicht dokumentiert. 
  
> [!NOTE]
> Kurse im clientseitigen Objektmodell (CSOM) können unabhängig von den anderen Project Server-Assemblys und -Diensten verwendet werden. Sie können den **Microsoft.ProjectServer.Client-Namespace** in einer Remoteentwicklungsumgebung auf einem Computer mit Project Server verwenden und Apps entwickeln, die in Project Online oder in eine lokale Installation von Project Server integriert werden können. Das CSOM enthält jedoch nur eine Teilmenge der Funktionalität der vollständigen PSI. Das CSOM ermöglicht die Entwicklung der meisten häufigen Szenarien für die Project Server-Integration. Weitere Informationen finden Sie unter [Was das CSOM durchführen kann und was nicht](what-the-csom-does-and-does-not-do.md) und [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
Für die Entwicklung der meisten Anwendungen, die die PSI verwenden, müssen Sie die Entwicklung nicht auf einem Project Server-Computer durchführen oder Verweise auf Project Server-Assemblys im globalen Assembly-Cache festlegen. Sie können die erforderlichen Project Server-Assemblys auf Ihren Entwicklungscomputer kopieren. Projekt Server 2013 installiert die folgenden Assemblys in _[Programmdateien]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Namespaces für die PSI-Dienste verfügen über willkürliche Namen, die für eine PSI-Proxyassembly ("ProjectServerServices.dll") erstellt wurden, welche für Dokumentationszwecke generiert wird. In der PSI-Referenz verfügt jeder Dienstnamespace über einen Platzhalternamen (wie _[Project-Webdienst]_) und eine Webreferenz (wie `https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Project Server-Assemblys und -Namespaces
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Beim Installieren von Project Server werden viele Assemblys installiert, es werden jedoch nur vier der Project Server-Assemblys dokumentiert. Drittanbieterentwickler verwenden im Allgemeinen nur ein paar Klassen und Member in diesen Assemblys. Die nicht dokumentierten Project Server-Assemblys umfassen Namespaces und Klassen, die Project Server intern verwendet, dazu zählen beispielsweise Klassen für Project Web App, die Geschäftsentitäten und der Datenzugriffsschicht (Data Access Layer, DAL). Wenn Sie einen Verweis in Visual Studio zu einer der dokumentierten Project Server-Assemblys festlegen, können Sie alle Namespaces, Klassen und Member im Visual Studio-Objektkatalog anzeigen.
  
> [!NOTE]
> Viele Mitglieder der dokumentierten Project Server-Namespaces werden nur intern verwendet und umfassen nur eine minimale Dokumentation. 
  
Beim Entwickeln für Project Online können Sie nur das CSOM für den Zugriff auf die Project Server-Funktionalität verwenden. Sie haben keinen Zugriff auf die PSI-Dienste oder die anderen Project Server-Assemblys.
  
Die [Project Server 2013-Klassenbibliotheks- und -Webdienstreferenz](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) für die PSI umfasst Namespaces aus den folgenden Assemblys: 
  
- **Microsoft.Office.Project.Server.Library.dll** Diese Assembly enthält einen dokumentierten Namespace und drei nicht dokumentierte Namespaces, was wie folgt aussieht: 
    
  - Der [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx)-Namespace enthält viele Enumerationen und Klassenfelder sowie Eigenschaften, die häufig in lokalen Anwendungen für Project Server verwendet werden. Entwickler verwenden zum Beispiel in der Regel Enumerationen wie **CustomField.Type** und die **PSClientError**-, **PSErrorInfo**- und **Filtern**-Klassen. 
    
    Der **Microsoft.Office.Project.Server.Library**-Namespace enthält auch die folgenden sieben Eigenschaftenklassen, die mehr als 3.200 Unterklassen enthalten: 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    Die Eigenschaftenklassen werden intern verwendet und sind nicht dokumentiert. Die Eigenschaftsklassen werden für die Serialisierung zwischen Project Professional 2013 und Project Server verwendet. Wenn Sie mit dem **Microsoft.Office.Project.Server.Library**-Namespace in Visual Studio arbeiten, zeigt der Objektkatalog alle Eigenschaftsklassen an, wodurch es schwieriger wird, Klassen zu finden, die für die Drittanbieterentwicklung nützlich sein können. Da Drittanbieterentwickler nicht die Eigenschaftenklassen verwenden müssen, werden sie im SDK nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.DataServices** Die Klassen und Mitglieder dieses Namespaces werden intern durch den Dienst **OData** in Project Online für den Zugriff auf Berichtstabellen in der Project-Datenbank verwendet. Die **DataServices**-Klassen sind nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.Administration** Die Klasse und Mitglieder dieses Namespaces werden nur für die interne Diagnoseprotokollierung verwendet und nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.Base** Die Klassen und Mitglieder dieses Namespaces werden intern als Basisklassen verwendet und sind nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema **Dieser Namespace wird intern zum Generieren vom Filterschemas verwendet und ist nicht dokumentiert. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** Diese Assembly wird für ältere Project Server 2010-Workflows verwendet, die weiterhin in Project Server 2013 funktionieren können. Zum Erstellen von neuen Workflows sollten Sie SharePoint Designer 2013 verwenden, oder Sie können Sie auch Visual Studio 2012 mit der [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx)-Klasse verwenden. Die Assembly Microsoft.Office.Project.Server.Workflow.dll-Assembly enthält die folgenden drei Namespaces: 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) Dieser Namespace enthält Klassen, die für Project Server-Workflowaktivitäten verwendet werden. Zu den Aktivitäten zählen das Lesen, Vergleichen und Aktualisieren von Projekteigenschaften. Andere Klassen verwalten Workflows und enthalten Workflowrückrufe, wenn Projekte geändert werden. 
    
  - **Microsoft.Office.Project.PWA** Dieser Namespace enthält einen internen Proxy für die PSI, für die Verwendung mit Project Web App und mit benutzerdefinierten Workflowaktivitäten, er ist nicht dokumentiert. 
    
    Eine benutzerdefinierte Workflowaktivität erfordert einen Verweis auf **Microsoft.Office.Project.PWA** für den Zugriff auf alle Klassen in den PSI-Diensten. Beispielsweise enthält die Klasse **Microsoft.Office.Project.PWA.PSI** die Eigenschaft **ProjectWebService**, die einen Proxy für den [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx)-Namespace abruft. 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** Dieser Namespace umfasst interne Proxyklassen für die primäre Klasse in jedem PSI-Dienst. Durch Verwendung der erhöhten Berechtigungen des Workflowbenutzers kann der Workflow PSI-Methoden über Proxyklassen aufrufen. Die Proxyklassen sind nicht dokumentiert. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll**[Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) ist der einzige Namespace in dieser Assembly. Er enthält Ereignisempfänger und Ereignisargumentklassen für die PSI-Dienste und andere interne Klassen. 
    
  Entwickler schreiben Ereignishandler, die sich aus den Ereignisempfängerklassen ableiten. Die meisten der primären Klassen in den PSI-Diensten verfügen über eine entsprechende Ereignisempfängerklasse. Die **ProjectEventReceiver**-Klasse enthält zum Beispiel Empfängermethoden vor dem Ereignis und nach dem Ereignis, die mit den Methoden in der **Project**-Klasse in der PSI übereinstimmen. Die **OnCreating**-Methode und die **OnCreated**-Methode sind die Empfängermethoden vor dem Ereignis und nach dem Ereignis für die **QueueCreateProject**-Methode. 
    
  Entwickler verwenden in der Regel die folgenden Ereignisempfängerklassen:
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [ProjectEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [OptimizerEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [ReportingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  Die Klassen **RulesEventReceiver** und **StatusReportsEventReceiver** werden in Project Web App intern verwendet. 
    
- **Microsoft.ProjectServer.Client.dll** Diese Assembly enthält das CSOM für die Entwicklung mit .NET Framework 4. Die Assembly befindet sich in `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. Die Entwicklung von Apps mit dem **Microsoft.ProjectServer.Client**-Namespace erfolgt unabhängig von den lokalen Project Server-APIs und -Diensten, obwohl die Apps entweder mit einer lokalen oder Onlineinstallation von Project Server funktionieren. Zugehörige CSOM-Assemblys, die für Windows Phone 8, Microsoft Silverlight oder JavaScript mit Web-Apps verwendet werden können, finden Sie unter [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
    
- **Microsoft.Office.Project.Server.Schema.dll** Das Project 2013-SDK dokumentiert nicht das **Microsoft.Office.Project.Server.Schema** -Namespace, das sich in der `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll`-Assembly befindet. Der Namespace enthält die Definitionen sämtlicher **DataSet**-, **DataTable**- und **DataRow**-Klassen, die in der PSI verwendet werden, sowie weitere ähnliche Klassen, die Project Server intern verwendet. Die öffentlichen Klassen in den jeweiligen PSI-Diensten werden in bestimmten Dienstreferenzen dokumentiert. Beispielsweise ist die Klasse **DriverDataSet.DriverRow** im [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx)-Namespace dokumentiert. 
    
  > [!NOTE]
  > Anwendungen, die das CSOM verwenden, nutzen Remoteereignishandler oder greifen auf Project Online zu und verwenden nicht den **Microsoft.Office.Project.Server.Schema-Namespace**. 
  
  In einigen Anwendungen, die Ereignishändler mit vollem Vertrauen verwenden, wo die Ereignishandler auf dem Computer mit Project Server installiert sind, muss ein Verweis auf die "Microsoft.Office.Project.Schema.dll"-Assembly festgelegt werden. Im Folgenden finden Sie zwei Beispiele:
    
  - In einem **OnCreated**-Post-Event-Handler mit vollem Vertrauen für benutzerdefinierte Felder können Sie das Ereignisargument **e.CustomFieldInformation** mit einem Verweis auf den **Microsoft.Office.Project.Server.Schema**-Namespace für die **CustomFieldDataSet**- und **CustomFieldsRow**-Definitionen verwenden. 
   
     ```cs
        using PSLibrary = Microsoft.Office.Project.Server.Library;
        using Microsoft.Office.Project.Server.Schema;
        . . .
        // Event handler for the OnCreated event of a custom field.
        public override void OnCreated(
            PSLibrary.PSContextInfo contextInfo, 
            CustomFieldsPostEventArgs e)
        {
            // Get information from the event arguments. 
            string userName = contextInfo.UserName.ToString();
            CustomFieldDataSet customFieldDs = e.CustomFieldInformation;
            CustomFieldsRow customFieldRow = customFieldDs.CustomFields.Rows[0];
            string customFieldName = customFieldRow["MD_PROP_NAME"].ToString();
            byte customFieldType = (byte)customFieldRow["MD_PROP_TYPE_ENUM"];
            Guid customFieldUid = (Guid)customFieldRow["MD_PROP_UID"];
            . . .
        }
     ```

  - Eine benutzerdefinierte Workflowaktivität kann einen Verweis auf **Microsoft.Office.Project.Server.Schema** für **DataSet**-Definitionen erfordern. 
    
## <a name="psi-services"></a>PSI-Dienste
<a name="pj15_PSIRefOverview_PSI"> </a>

Die PSI ist ein Satz an WCF-Diensten und identischen ASMX-Webdiensten für Project Server 2013. Zum Verwenden eines Diensts in einem Visual Studio-Projekt legen Sie einen Verweis auf die URL der `.svc`-Datei oder des `.asmx?wsdl`-Diensts mithilfe eines willkürlichen Namens für den Namensdienst fest. Das Hilfsprogramm "wsdl.exe" oder das Hilfsprogramm "svcutil.exe" generiert anschließend den Proxyquellcode für diesen Namespace, und der Compiler erstellt eine Proxydienstassembly, die in Ihre Anwendung einbezogen wird. 
  
> [!NOTE]
> Die PSI-Referenz enthält Platzhalter für die Namensdienstnamen für PSI-Dienste wie _[Admin-Webdienst]_, _[Driver-Webdienst]_ und _[Project-Webdienst]_. Jeder PSI-Namensdienst enthält eine primäre Klasse, die die Webmethoden für den jeweiligen Dienst enthält. Wenn Sie zum Beispiel einen Verweis auf den **Admin**-Dienst festlegen und diesen **WebSvcAdmin** nennen, enthält der Namensdienst **WebSvcAdmin** in Ihrer Anwendung die primäre **Admin**-Klasse, die über die Webmethoden **GetServerCurrency**, **ListInstalledLanguages**, **ReadServerVersion** und so weiter verfügt. Eine Liste von veralteten PSI-Diensten finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). 
  
Von den insgesamt 30 PSI-Diensten sind **authentication**, **ExchangeSync**, **OData**, **P12Upgrade**, **psiserviceapp**, **PWA**, **View** und **WinProj** für die interne Verwendung von Project Web App und Project Professional bestimmt und nicht dokumentiert. Sie können Proxydateien oder eine Proxyassembly erstellen, die die internen PSI-Dienste enthält, die internen Dienste sind aber nicht für die Verwendung von Drittanbietern bestimmt; die PSI-Referenz dokumentiert diese Dienste nicht. Die folgende Abbildung zeigt die Position des Back-End-PSI-Diensts im Internet Information Services Manager. 
  
**Finden der PSI-Dienste in IIS**

![PSI-Dienste im IIS-Manager](media/pj15_PSIReference_IIS.gif "PSI-Dienste im IIS-Manager")
  
Im Folgenden werden alle Klassen aufgeführt, die Webmethoden in den PSI-Diensten enthalten:
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) Enthält Methoden, die auf den **Project Server-Verwaltungsseiten** in Project Web App verwendet werden. Definiert Geschäftsjahre, verwaltet Statuserfassungs- und Währungseinstellungen, Reportingzeiträume, das Überwachungsprotokoll und Einstellungen für Active Directory. 
    
2. [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) Umfasst Methoden für das Verwalten der Sicherung und Wiederherstellung von Projekten, Sicherheitskategorien, benutzerdefinierte Felder, Ressourcen, Systemeinstellungen, Ansichten und das Enterprise-Global-Projekt. Liest und aktualisiert den Archivplan. Archiviert alle Projekte oder löscht angegebene archivierte Projekte. Speichert Sicherungsobjekte in den Archiv-Datenbanktabellen und stellt Objekte in den veröffentlichten Datenbanktabellen wieder her. 
    
3. **authentication** Umfasst Methoden für die ausschließlich interne Verwendung durch Project Professional und Project Web App. 
    
4. [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Verwaltet Enterprise-Kalenderausnahmen. Checkt Ressourcenkalender aus und ein. Nimmt die Erstellung, Löschung, Auflistung sämtlicher, Aktualisierung oder die Rückgabe von Kalenderausnahmen vor. 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) Verwaltet OLAP-Cubeeinstellungen. Ruft Analysis-Server, Datenbankstatus und die Liste der Cubes ab. Versetzt einen Cube-Erstellungsdienstanforderung in die Warteschlange. Liest und aktualisiert berechnete Memberdefinitionen und Feldeinstellungen für Dimensionen und Kennzahlen im Cube. 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Verwaltet benutzerdefinierte Enterprise-Felder. Umfasst das Aus- und Einchecken von Methoden und enthält die CRUD-Methoden (Create, Read, Update, Delete) für benutzerdefinierte Enterprise-Felder. 
    
7. [Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Verwaltet Portfolioanalysetreiber und die Treiberpriorisierung für die Projekterstellung und das Projektbedarfsmanagement. Enthält die CRUD-Methoden für die Project-Treiber. 
    
8. [Events](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Verwaltet Project Server-Ereignishandlerzuordnungen. Umfasst die CRUD-Methoden für Project Server-Ereignishandlerzuordnungen für ein bestimmtes Ereignis oder für alle Ereignishandlerzuordnungen. 
    
9. **ExchangeSync** Hierbei handelt es sich um einen internen Project Server-Dienst, der Exchange Server-Ereignisse verarbeitet. Project Web App verwendet **ExchangeSync** zum Synchronisieren von Aufgaben zwischen Project Server und Exchange Server, statt eine direkte Synchronisierung mit dem Outlook-Client durchzuführen wie in Office Project Server 2007. 
    
    Der Zugriff auf den **ExchangeSync**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **ExchangeSync**-Klassen und -Mitglieder werden nicht für die Entwicklung durch Drittanbieter unterstützt. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) Stellt die **Login**- und **Logoff**-Methoden mit formularbasierter Authentifizierung bereit. Der Zugriff auf den **LoginForms**-Dienst steht nur auf einer Project Web App-Front-End-Website zur Verfügung. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Stellt die **Login**- und **Logoff**-Methoden bereit, die für die Windows-Authentifizierung mit ASMX-basierten Anwendungen, die für Project Server 2013-Installation mit mehrfacher Authentifizierung (forderungs- und formularbasiert) verwendet werden. Der Zugriff auf den **LoginWindows**-Dienst steht nur auf einer Project Web App-Front-End-Website zur Verfügung. 
    
    > [!CAUTION]
    > Der **LoginWindows**-Dienst wird in WCF-basierten Anwendungen oder für Anwendungen, die auf Project Server-Installationen ausgeführt werden, welche nur die Forderungsauthentifizierung oder **OAuth** verwenden, nicht verwendet. In einigen Fällen gibt die Methode **Login** immer **false** zurück. Die Forderungsauthentifizierung verarbeitet die integrierte Windows-Authentifizierung. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Verwaltet das Durchsuchen von Tabellen, das mehrsprachige Durchsuchen von Tabellen und ihrer entsprechenden Codemasken. Checkt aus, checkt ein, liest, erstellt, löscht und aktualisiert. 
    
13. [Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Verwaltet Warnungen und Erinnerungen. Enthält Methoden, die Warnmeldungsergebnisse abrufen, festlegen, registrieren und die Registrierung der Ergebnisse aufheben. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Verwaltet Webobjekte und Links für Dokumente und Listenelemente auf SharePoint-Websites. Erstellt, löscht oder liest Projekt-, projektverknüpfte, Aufgaben- oder aufgabenverknüpfte Webobjekte. 
    
    > [!NOTE]
    > Der **ObjectLinkProvider**-Dienst ist in Project Server 2013 veraltet. Weitere Informationen finden Sie im Abschnitt *Veraltete Features[ unter ](updates-for-developers-in-project-2013.md)Updates für Entwickler in Project 2013*. 
  
15. **OData** Stellt die interne **OData**-Schnittstelle für Berichtstabellen und Ansichten bereit. Der Zugriff auf den **OData**-Dienst steht nur über die Back-End-**ProjectServiceApplication**-URL zur Verfügung. Der private **OData**-Dienst in der PSI enthält eine Methode, **ODataClient.ProcessOdataMessage**, die Project Server intern zur Verarbeitung von Anforderungen für die Berichtsdaten verwendet. Die HTTP-Anforderungen laufen durch den Front-End-**ProjectData**-Dienst. 
    
    Weitere Informationen über den **ProjectData**-Dienst und das OData-Protokoll zum Lesen von Berichtsdaten finden Sie unter [ProjectData – OData-Dienstreferenz für Project](https://msdn.microsoft.com/library/office/jj163015.aspx).
    
16. **P12Upgrade** Bietet interne Methoden für das Installationsprogramm von Project Server 2013 zum Aktualisieren einer Office Project Server 2007-Installation. Der Zugriff auf den **P12Upgrade**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **P12Upgrade**-Methoden werden nicht für die Drittanbieterentwicklung unterstützt. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Umfasst die CRUD-Methoden für Projektabhängigkeiten sowie für Optimierungs-, Planungs- und Analyselösungen. 
    
18. [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Verwaltet Projekte. Nimmt das Auschecken, Einchecken, Erstellen, Löschen, Lesen oder Aktualisieren von Projekten in den Project-Datenbank-Entwurfstabellen oder veröffentlichten Tabellen vor. Versetzt eine Nachricht in eine Warteschlange für die Veröffentlichung. 
    
    Erstellt oder löscht Entitäten innerhalb von Projekten (Aufgaben, Ressourcen, Zuweisungen usw.). Ruft Informationen über das Project-Team oder die Project-Websiteadresse ab oder aktualisiert diese. Ruft den Projektstatus, eine Liste der Projekte in den Entwurfstabellen, alle Zusammenfassungsaufgaben sowie Aufgaben, die für die Zuweisung zu einer bestimmten Ressource verfügbar sind, oder alle Projekte ab, wo eine Ressource über Zuweisungen verfügt.
    
    Erstellt und verwaltet Festlegungen, erstellt Projektvorschläge und Projekte von SharePoint-Aufgabenlisten und sucht Projekt-/Master-Projektbeziehungen.
    
19. **Psiserviceapp** Wird intern von Project Online verwendet. Die **psiserviceapp**-Klassen und -Mitglieder werden nicht für die Entwicklung durch Drittanbieter unterstützt. 
    
20. **PWA** Enthält viele für Project Web App optimierte Methoden, einschließlich der Methoden für die Aufgabenaktualisierungs-Genehmigungsregeln und für die Verwaltung von Statusberichten. Die **PWA**-Methoden sind häufig spezialisiert und redundant im Vergleich zu entsprechenden Methoden in anderen PSI-Diensten. **PWA**-Methoden verwenden viele der gleichen Datasets wie andere PSI-Methoden oder geben diese zurück. 
    
    Der Zugriff auf den **PWA**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **PWA**-Klassen und -Mitglieder werden nicht für die Entwicklung durch Drittanbieter unterstützt. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Verwaltet die Project Server-Warteschlange. Nimmt den Abruf der Auftragsanzahl, der Auftrags- und Auftragsgruppen-Wartezeit, des Status sämtlicher Aufträge, von angegebenen Aufträgen, von Aufträgen, die dem Aufrufer gehören, oder von Aufträgen für angegebene Projekte vor. Verwaltet die Auftragskorrelation und konfiguriert die Warteschlange. 
    
22. [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Verwaltet Enterprise-Ressourcen. Nimmt das Auschecken, Einchecken, Aktualisieren oder Erstellen von Ressourcen oder Project Server-Benutzern und ihrer Autorisierungseinstellungen vor, sucht Ressourcen nach Namen oder GUID, liest Ressourcen- oder Benutzerdaten und den Ressourcenstrukturplan sowie zugehörige Sicherheitsinformationen, ruft alle Zuweisungen für eine Ressource ab und setzt Benutzerkennwörter zurück. Die **Resource**-Klasse enthält CRUD-Methoden für Benutzerstellvertretungen. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Verwaltet Ressourcenpläne. Checkt die CRUD-Methoden aus, checkt sie ein, veröffentlicht sie und fügt sie für Ressourcenpläne hinzu. 
    
24. [Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Umfasst die CRUD-Methoden für Sicherheitsvorlagen, Sicherheitskategorien, Organisations- und globale Berechtigungen sowie Gruppenberechtigungen. Die **Security**-Klasse enthält Methoden für Projektkategorien. 
    
25. [Statusing](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Verwaltet Statusupdates und Zuweisungen. Übernimmt Statusaktualisierungen oder Genehmigungen, sendet Statusaktualisierungen, legt Zusammenfassungsinformationen für gesendete Updates fest, löscht genehmigte Statusaktualisierungen oder den Zustimmungsverlauf für einen bestimmten Benutzer oder löscht sämtliche Statusinformationen für einen Satz von Projekten. Nimmt das Erstellen, Abrufen oder Delegieren von Zuweisungen vor, legt die Zuweisungsarbeitsdauer fest. Ruft neue Zuweisungen für den aktuellen Benutzer ab, ruft den Zuweisungs- oder Aufgabentransaktionsverlauf, die aktuellen Werte mit Zeitphasen oder die Sammelvorgangshierarchie ab. 
    
    Zeigt eine Vorschau der Arbeitszeittabellendaten an oder importiert sie oder liest den Arbeits- bzw. Nichtarbeitsplan eines Benutzers. Sucht ausstehende Statusaktualisierungen, Informationen für gesendete Aktualisierungen oder einen Transaktionsdatensatz der Änderungen in einer gesendeten Aktualisierung. Liest Teamstatus.
    
26. [TimeSheet](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Verwaltet Arbeitszeittabellen. Umfasst die CRUD-Methoden für Arbeitszeittabellen und sendet oder ruft Arbeitszeittabellen zurück. Sucht nach Arbeitszeittabellen, die in Verzug sind oder deren Genehmigung aussteht, sucht nach Arbeitszeittabellen nach Datum oder Zeitraum. Ruft eine Liste von genehmigenden Personen für Arbeitszeittabellen ab. Lädt Arbeitszeittabellen-Ist-Werte vorab und überprüft eine Arbeitszeittabellen-Zeile. Die **TimeSheet**-Klasse enthält die **ReadProjectTimesheetLines**-Methode und die **SubmitTimesheetLines**-Methode für das Lesen und Senden von Arbeitszeittabellen für eine andere Ressource ohne erforderlichen Identitätswechsel. 
    
27. **View** Der **View**-Dienst wurde für die ausschließliche Verwendung in Project Web App entwickelt. Methoden in der **View**-Klasse verwalten Ansichten, zeigen Berichte an und lesen Felder in Ansichten. 
    
    Der Zugriff auf den **View**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **View**-Methoden werden nicht für die Drittanbieterentwicklung unterstützt. 
    
28. **WinProj** Der **WinProj**-Dienst wurde für die ausschließliche Verwendung durch Project Professional entworfen. Drittanbieterentwickler sollten keine **WinProj**-Methoden für die Programmierung mit Project Server verwenden. 
    
    Einige **WinProj**-Methoden verwenden Datasets wie **ProjectRelationsDataSet** und **ResourceDataSet**, die der **Project**- und **Resource**-Dienst ebenfalls verwendet, für sie sind in Project Professional jedoch bestimmte Eigenschaften und Funktionen erforderlich. 
    
    Der Zugriff auf den **WinProj**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **WinProj**-Methoden werden nicht für die Drittanbieterentwicklung unterstützt. 
    
29. [Workflow](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Umfasst die CRUD-Methoden für Enterprise-Projekttypen und für das Verwalten von Workflowphasen und -stufen. Führt Workflows aus, legt Statusinformationen fest und verwaltet PDP-Phasen in Bedarfsmanagementworkflows. Entwickler können zum Entwickeln von Workflows für Project Server SharePoint Designer 2013 für deklarative Workflows verwenden oder die Office Developer Tools für Visual Studio 2012 für die Entwicklung mit .NET Framework 4 und der [ Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx)-Klasse im CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Verwaltet Projektwebsites. Erstellt und löscht Projektwebsites. Ruft Informationen ab und aktualisiert SharePoint-Einstellungen und -Verwaltungswebsites. Synchronisiert und aktualisiert die Mitgliedschaften und Gruppen von Projektwebsites. 
    
Jeder Dienstnamespace umfasst alle **DataSet**-Schema- und Ereignishandlerklassen, die der Dienst verwendet. Bespielsweise beschreibt `Calendar.svc` (oder `Calendar.asmx?wsdl` für den ASMX-Webdienst) den **Calendar**-Dienst. Wenn Sie die Referenz **WebSvcCalendar** nennen, enthält der Proxy-Namespace die primäre **Calender**-Klasse mit den Methoden **CheckInCalendars**, ** CheckOutCalendars** und so weiter. Der **WebSvcCalendar**-Proxy-Namespace enthält auch die **CalendarDataSet**-Klasse und alle Unterklassen. 
  
Einige dieser PSI-Dienste enthalten doppelte **DataSet**-Klassen. Der **Project**-Dienst und der **Statusing**-Dienst enthalten beispielsweise beide die **ProjectDataSet**-Klasse. Dies liegt daran, dass die Methoden in den Diensten **Project** und **Statusing** Verweise auf **ProjectDataSet** enthalten und die Proxyassemblys, die Sie beim Festlegen von Verweisen und Kompilieren einer Anwendung erstellen, die zugehörigen Datasets enthalten. Der **Project**-Dienst und **Statusing**-Dienst erfordern eventuell Werte für verschiedene Felder in der **ProjectDataSet.ProjectRow**-Klasse. 
  
Wenn Sie nach den Namespaces und Klassen des PSI-Verweises suchen, um beispielsweise die Webmethoden für den **Project**-Dienst anzuzeigen, erweitern Sie den Namespace **[Project web service]** in der Liste **Contents**, und erweitern Sie dann die **Project**-Klasse. 
  
## <a name="see-also"></a>Siehe auch

- [Project Server 2013-Architektur](project-server-2013-architecture.md)
- [Project Server-Programmierbarkeit](project-server-programmability.md)   
- [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)   
- [Voraussetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

