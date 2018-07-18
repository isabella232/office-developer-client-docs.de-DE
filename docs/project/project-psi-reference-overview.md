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
- Web-service, Kalender, Authentifizierung, Web-Service, ResourcePlan, Web Service StatusReports,-Webdienst PSI, Namespaces, Ereignishandler, Project Server-Webdienst, Benachrichtigungen, QueueSystem, Project 2013-Dienst-Webplattform, LoginWindows, Web Dienst, Webdienst, Statusverwaltung, Webdienst, Ressource, die über WinProj, Web-Service, WssInterop,-Webdienst, Web-Service, Winproj, Ereignis-Handler, LookupTable, Web PWA-Dienst-Webdienst, Web-Service, Sicherheit, Benachrichtigungen, Webdienst, Webdienst Arbeitszeittabelle, Web-service, QueueSystem, PSI, Webdienste, Webdienst, Ereignisse und PSI, Programmieraufgaben, Webdienst, LookupTable, Version, Webdienst, CustomFields, Webdienst, Webdienst, PWA, PSI, Ressource, Webdienst, ResourcePlan, Arbeitszeittabelle, Web-Webdienst Service-Webdienst, Regeln, PSI, verwalteten code Verweis, Sicherheit, Webdienst, Web-Service, CustomFields,-URL für die PSI, Web-Service, WssInterop, Web Service, Admin,-Verweis PSI, Web Webdienst CubeAdmin, Ansicht, Web-Service, Kalender-Webdienst, Web Dienst, Ansicht, Admin, -Webdienst, LoginForms, Web-service, Webdienst, LoginForms, PSI, URLs, ObjectLinkProvider, Web-Service, Archivierung, Web Service, CubeAdmin, Web Service, Regeln,-Webdienst Web Service, Authentifizierung, Web Services, PSI, Project Server , Ereignisse, Ereignisse, Webdienst, Webdienst, Project, Zeitberichte, Web-service, Webdienst, ObjectLinkProvider, Project Server Interface, PSI,-Methoden Web Service StatusReports,-Webdienst Web Archiv, Project, Web-service, Webdienst, LoginWindows
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: Project Server Interface (PSI) ist die API verwenden, für die Entwicklung von Anwendungen, die Project Server 2013 lokal zu integrieren.
ms.openlocfilehash: 14ab540fd8a66cf18c576572fc0eff4df7c7d61c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796311"
---
# <a name="project-psi-reference-overview"></a>Project-PSI-Referenz – Übersicht

Project Server Interface (PSI) ist die API verwenden, für die Entwicklung von Anwendungen, die Project Server 2013 lokal zu integrieren.
  
Dieser Artikel bietet eine Übersicht über die dokumentierte Assemblys, Namespaces und Dienste in die PSI. Die [Project Server 2013 Class Library und Web-Dienst verweisen](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) im SDK enthält alle Dokumentation verwaltetem Code für die PSI und den [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) -Namespace im Project Server 2013. Informationen zum Entwickeln von Anwendungen für Project Online, müssen Sie den Namespace **Microsoft.ProjectServer.Client** anstelle der PSI verwenden. 

Die PSI in Project Server 2013 verfügt über eine duale Schnittstelle. Die ASMX-Interface für Webdienste durch Ermittlung definiert wird und Web Service Description Language (Disco und WSDL) Dateien in die `http://ServerName/ProjectServerName/_vti_bin/psi/` virtuelles Verzeichnis (z. B. Projectdisco.aspx und Projectwsdl.aspx). Sie können die ASMX-Schnittstelle zugreifen, nur über die URL einer lokalen Installation von Project Web App (z. B. `http://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`. Um den Webdienst in einem Browser anzuzeigen, müssen Sie enthalten die `?wsdl` URL-Option. Da die ASMX-Schnittstelle mit Windows Communication Foundation (WCF)-Infrastruktur erstellt wird, sind die ASMX-Dateien für Project Server-Webdienste nicht tatsächlich in das virtuelle Verzeichnis der PSI vorhanden. 
  
Die WCF-Dienste-Schnittstelle wird von SVC-Dateien in die Back-End definierten `http://ServerName:32843/GUID/PSI/` virtuelle Verzeichnis in der SharePoint-Webdienste-Anwendung. Die URL der PSI-Dienste in das virtuelle Verzeichnis für Project Service-Anwendung (z. B. `http://ServerName:32843/GUID/PSI/project.svc`) enthält die SVC-Dateien. Allerdings können nicht direkt verwenden Sie den Back-End-URL ein WCF-Dienstverweises festgelegt. Informationen zum Entwickeln einer Anwendung oder Komponente, die die WCF-Dienste die PSI verwendet, können Sie eine Proxyassembly oder eine Proxydatei verwenden. Der Project 2013-SDK-Download enthält die Proxydateien für die WCF-Dienste in Project Server 2013 und Skripts zum Abrufen von aktualisierter WCF-Proxy-Dateien und Kompilieren die Dateien in eine Proxyassembly für neueren Project Server erstellt.
  
Der Verzeichnisname Project Service-Anwendung ist ein GUID-Wert, der die GUID der lokalen Project Web App-Instanz identisch ist. Klicken Sie im Fenster **Internetinformationsdienste (Internet Information Services, IIS)-Manager** den Knoten **SharePoint-Webdienste** , wählen Sie den Namen der GUID-Verzeichnis und wählen Sie dann auf **Erweiterte Einstellungen** , um den Wert für **Virtuelle Pfade** kopieren. 
  
> [!IMPORTANT]
> Die ASMX Webdienstschnittstelle für die PSI wird ist in Project Server 2013 veraltet, jedoch weiterhin unterstützt. Neue Applikationen sollten die WCF-Schnittstelle von der PSI oder die CSOM verwenden. Weitere Informationen zu veralteten Features finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
> 
> Neue Applikationen und Middleware-Komponenten, die nur auf einer lokalen Installation von Project Server ausgeführt werden sollten das WCF-Interface verwenden also die Technologie, die für die Netzwerkkommunikation empfohlen. Legacyanwendungen, die die ASMX-Interface verwenden, müssen die URL über Project Web App verwenden die Project Server-Berechtigungen überprüft. 
> 
> Weitere Informationen über die ASMX-Schnittstelle und wie Sie den WCF-Interface verwenden finden Sie unter [Voraussetzungen für ASMX-basierte Codebeispiele im Projekt](prerequisites-for-asmx-based-code-samples-in-project.md) und der [Voraussetzungen für WCF-basierte Codebeispiele im Projekt](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Für die Entwicklung von Anwendungen, die das WCF-Interface verwenden, können Sie Visual Studio 2010 oder Visual Studio 2012. Für deklarative Workflows für Project Server erstellen, können Sie SharePoint Designer 2013. Project Server-Workflows, die benötigt Zugriff auf die PSI oder dem Clientobjektmodell können mit Visual Studio 2012 entwickelt werden.
  
### <a name="using-the-psi-reference"></a>Verwenden die PSI-Referenz
<a name="pj15_PSIRefOverview_Using"> </a>

Das PSI-Objektmodell groß ist und viele Klassen und Member sind nur zur internen Verwendung. Daher kann es sein, erhalten in den Themen, die Sie möchten in der [Project Server 2013 Class Library und Web-Dienstverweises](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)verwirrend. Die meisten den Referenzthemen, die Sie für die Entwicklung verwenden, sind in der folgenden Gruppen:
  
- **Primäre Klassenmethoden:** Jeder Dienst in die PSI enthält eine primäre Klasse mit dem Namen für den Namen des Diensts. Beispielsweise enthält der Dienst für die **Ressource** die [Ressource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) -Klasse, die im Namespace [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx) ist. Um eine Liste der Methoden anzuzeigen, die in der Klasse **Ressource** verfügbar sind, erweitern Sie den Klassenknoten in den Bereich Inhalte, und wählen Sie dann das **Ressourcenmethoden** Thema. 
    
- **DataRow-Eigenschaften:** Viele der primäre Klassenmethoden verwenden oder eines **Datasets**zurück. Jedes **DataTable** -Objekt in einem **DataSet** enthält Daten in einem oder mehreren **DataRow** -Objekten. In den meisten Fällen müssen Sie nur die Eigenschaften der Zeile, nicht aller anderen Member der Klassen **DataSet**, **DataTable**oder **DataRow** finden Sie unter. Beispielsweise enthält die **ResourceAssignmentDataSet** -Klasse Unterklassen für die **ResourceAssignmentDataTable** und die [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx) -Klasse. Um eine Liste der Eigenschaften anzuzeigen, die in der **ResourceAssignmentRow** -Klasse sind, erweitern Sie den Klassenknoten in den Bereich Inhalte, und wählen Sie dann das Thema **ResourceAssignmentDataSet.ResourceAssignmentRow Eigenschaften** . 
    
Zusätzlich zu den Namespaces Service lokaler [Project Server 2013 Class Library und Web-Dienst verweisen](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) Thema verweist auf die drei Project Server-Assemblys, die bei der Entwicklung von Lösungen für Drittanbieter-verwendet werden Installationen. Wir stellen nur minimale Dokumentation für diese Assemblys. Die PSI-Referenz wird die wichtigsten Klassen und Member in der 23 öffentlichen Diensten dokumentiert. Sechs PSI-Dienste sind nur zur internen Verwendung und sind nicht dokumentiert. 
  
> [!NOTE]
> Klassen im Client-seitigen Objektmodell (CSOM) können unabhängig von anderen Assemblys für Project Server und Dienste verwendet werden. Sie können den **Microsoft.ProjectServer.Client** -Namespace in einer remote-Entwicklungsumgebung aus der Project Server-Computer verwenden und Entwickeln von apps, die mit Project Online oder mit einer lokalen Installation von Project Server zu integrieren. Aber das CSOM enthält eine Teilmenge der Funktionalität von die vollständige PSI. Das CSOM ermöglicht die Entwicklung der gängigsten Szenarien für Project Server-Integration. Weitere Informationen finden Sie unter [Was das CSOM ist und nicht zu](what-the-csom-does-and-does-not-do.md) und [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Für die Entwicklung von den meisten Clientanwendungen, die die PSI verwenden, müssen Sie nicht auf einem Project Server-Computer entwickeln, oder legen Sie Verweise auf Project Server-Assemblys im globalen Assemblycache. Sie können die erforderlichen Project Server-Assemblys auf Ihrem Entwicklungscomputer kopieren. Projektserver 2013 installiert die folgenden Assemblys im _[Program Files]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Namespaces für die PSI-Dienste sind beliebige Namen erstellt bei einer PSI-Proxyassembly ProjectServerServices.dll, die für die Dokumentation generiert wird. In der Referenz PSI hat jeder Dienstnamespace ein Platzhaltername (beispielsweise _[Project-Webdienst]_) und einen Webverweis (z. B. `http://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Project Server-Assemblys und -Namespaces
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Viele Assemblys werden bei der Installation von Project Server installiert. der Project Server-Assemblys nur vier dokumentiert sind. Drittanbieter-Entwickler verwenden in der Regel nur ein paar Klassen und Member in diesen Assemblies. Nicht dokumentierte Project Server-Assemblys enthalten, Namespaces und Klassen, die Project Server wie Klassen für Project Web App, die Geschäftseinheiten, intern verwendet und die Daten der Datenzugriffsschicht (DAL). Wenn Sie einen Verweis auf eine der dokumentierten Project Server-Assemblys in Visual Studio festlegen, können Sie alle Namespaces, Klassen und Member in den Visual Studio-Objektbrowser angezeigt.
  
> [!NOTE]
> Viele Member der dokumentierten Project Server-Namespace werden nur intern verwendet und sind nur minimal dokumentiert. 
  
Bei der Entwicklung für Project Online können Sie nur das CSOM, Zugriff auf Project Server-Funktionen. Sie können nicht auf der PSI-Dienste oder andere Assemblys Project Server zugreifen.
  
Die [Project Server 2013 Class Library und Web-Dienst verweisen](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) für die PSI enthält Namespaces aus den folgenden Assemblys: 
  
- **Microsoft.Office.Project.Server.Library.dll** diese Assembly enthält einen dokumentierten Namespace und drei Namespaces nicht dokumentiert, wie folgt: 
    
  - Der [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx) -Namespace enthält viele Enumerationen und Klassenfelder und Eigenschaften, die häufig verwendet werden, in lokalen Anwendungen für Project Server. Normalerweise verwenden Entwickler beispielsweise Enumerationen wie **CustomField.Type**und die Klassen **PSClientError**, **PSErrorInfo**und **Filter** . 
    
    Der **Microsoft.Office.Project.Server.Library**-Namespace enthält auch die folgenden sieben Eigenschaftsklassen, die über 3.200 Unterklassen umfassen: 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    Die Eigenschaftenklassen intern verwendet werden und sind nicht dokumentiert. Die Eigenschaftenklassen sind für die Serialisierung zwischen Project Professional 2013 und Project Server verwendet. Beim Arbeiten mit dem **Microsoft.Office.Project.Server.Library** -Namespace in Visual Studio zeigt den Objektkatalog alle die Eigenschaftenklassen, die erschwert Klassen suchen, die für die Entwicklung von Drittanbieter-nützlich sind. Da Drittentwickler der Eigenschaft Klassen nicht verfügen, werden Sie von das SDK nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.DataServices** die Klassen und Member dieses Namespaces werden intern von der **OData** -Diensts in Project Online für den Zugriff auf die Berichten Tabellen in der Project-Datenbank verwendet. Die Klassen, die **DataServices** sind nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.Administration** der Klasse und Member dieses Namespaces sind für die diagnoseprotokollierung intern verwendet, und sind nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.Base** die Klassen und Member dieses Namespaces intern als Basisklassen verwendet werden und sind nicht dokumentiert. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema** dieser Namespace wird zum Generieren von Filter-Schemas intern verwendet und ist nicht dokumentiert. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** diese Assembly ist für legacy Project Server 2010-Workflows verwendet, die in Project Server 2013 funktionieren kann. Für das neue Workflows erstellen, sollten Sie SharePoint Designer 2013 verwenden, oder Sie können auch die Visual Studio 2012 verwenden, mit der [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) -Klasse. Die Assembly Microsoft.Office.Project.Server.Workflow.dll umfasst die folgenden drei Namespaces hinzu: 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) dieser Namespace enthält Klassen, die für Project Server-Workflow-Aktivitäten verwendet werden. Aktivitäten umfassen lesen, vergleichen und Aktualisieren der Projekteigenschaften. Andere Klassen Verwalten von Workflows und Workflow-Rückrufe enthalten, wenn Projekte geändert werden. 
    
  - **Microsoft.Office.Project.PWA** dieser Namespace enthält einen internen Proxy für die PSI, für die Verwendung mit Project Web App und benutzerdefinierte Workflowaktivitäten; Es ist nicht dokumentiert. 
    
    Eine benutzerdefinierten Workflowaktivität erfordert einen Verweis auf **Microsoft.Office.Project.PWA** auf alle Klassen in der PSI-Dienste zugreifen. Beispielsweise enthält die **Microsoft.Office.Project.PWA.PSI** -Klasse die **ProjectWebService** -Eigenschaft, die einen Proxy für den Namespace [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx) fungiert. 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** dieser Namespace enthält interne Proxyklassen für die primäre Klasse in jedem PSI-Dienst. Mithilfe der erweiterten Berechtigungen des Benutzers Workflow kann der Workflow über Proxyklassen PSI-Methoden aufrufen. Die Proxyklassen sind nicht dokumentiert. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll** [Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) ist der einzige Namespace in dieser Assembly. Sie umfasst Ereignisempfänger und -Argument Ereignisklassen für die PSI-Dienste und andere internen Klassen. 
    
  Entwickler schreiben Ereignishandler, die sich aus den Ereignisempfängerklassen ableiten. Die meisten der primären Klassen in den PSI-Diensten verfügen über eine entsprechende Ereignisempfängerklasse. Beispielsweise enthält die Klasse **ProjectEventReceiver** Pre-Event- und Post-Event-Empfängermethoden, die den Methoden in der **Project**-Klasse in der PSI entsprechen. Die Methode **OnCreating** und die Methode **OnCreated** sind Pre-Event- und Post-Event-Empfängermethoden für die **QueueCreateProject**-Methode. 
    
  Entwickler verwenden für gewöhnlich die folgenden Ereignisempfängerklassen:
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
    
  Die **RulesEventReceiver** -Klasse und die **StatusReportsEventReceiver** -Klasse werden in Project Web App intern verwendet. 
    
- **Microsoft.ProjectServer.Client.dll** diese Assembly enthält das CSOM für die Entwicklung mit .NET Framework 4. Die Assembly befindet sich im `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. Entwicklung von apps mit dem **Microsoft.ProjectServer.Client** -Namespace ist unabhängig von der lokalen Project Server-APIs und Dienste, obwohl die apps, mit einem lokalen arbeiten können oder online-Installation von Project Server. Verwandte CSOM-Assemblys, die mit Web-apps für Windows Phone 8, Microsoft Silverlight oder JavaScript verwendet werden können, finden Sie unter [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
    
- **Microsoft.Office.Project.Server.Schema.dll** The Project 2013-SDK werden den **Microsoft.Office.Project.Server.Schema** -Namespace, der in ist nicht dokumentiert die `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll` Assembly. Der Namespace enthält die Definitionen der alle **DataSet**, **DataTable**und **DataRow** Klassen in die PSI plus viele ähnlichen Klassen, die Project Server intern verwendet. Die öffentlichen Klassen in jedem PSI-Dienst sind in der Referenz zu bestimmten Dienst dokumentiert. Beispielsweise ist die **DriverDataSet.DriverRow** -Klasse im Namespace [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx) dokumentiert. 
    
  > [!NOTE]
  > Anwendungen, die das CSOM verwenden, verwenden Sie remote-Ereignishandler oder Zugriff auf Project Online verwenden Sie nicht den **Microsoft.Office.Project.Server.Schema** -Namespace. 
  
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

  - Für eine benutzerdefinierte Workflowaktivität kann ein Verweis auf **Microsoft.Office.Project.Server.Schema** für **DataSet**-Definitionen erforderlich sein. 
    
## <a name="psi-services"></a>PSI-Dienste
<a name="pj15_PSIRefOverview_PSI"> </a>

Die PSI ist ein WCF-Dienste und identische ASMX-Webdienste für Project Server 2013. Um einen Dienst in Visual Studio-Projekt verwenden möchten, legen Sie einen Verweis auf die URL der der `.svc` Datei oder die `.asmx?wsdl` Service mithilfe von einen beliebigen Namen für die Nameservice. Das Dienstprogramm wsdl.exe oder das Hilfsprogramm "svcutil.exe" generiert dann Proxy-Quellcode für diesen Namespace, und der Compiler erstellt eine Proxy Service Assembly in Ihre Anwendung integrieren. 
  
> [!NOTE]
> Die PSI-Referenz enthält Nameservice Platzhalternamen der PSI-Dienste wie _[Admin-Webdienst]_, _[Treiber-Webdienst]_ und _[Project-Webdienst]_. Jede Nameservice PSI enthält eine primäre Klasse, die die zu verwendenden Webmethoden für den betreffenden Dienst enthält. Wenn Sie einen Verweis auf die **Admin** -Webdienst festlegen und nennen Sie es **WebSvcAdmin**, umfasst beispielsweise klicken Sie dann in der Anwendung die **WebSvcAdmin** Nameservice die primäre **Admin** -Klasse, die die Webmethoden **GetServerCurrency**hat, **ListInstalledLanguages**, **ReadServerVersion**und So weiter. Eine Liste der veralteten PSI-Dienste finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md) . 
  
Sind der 30 insgesamt PSI-Dienste **Authentifizierung**, **ExchangeSync**, **OData**, **P12Upgrade**, **Psiserviceapp**, **PWA**, **Anzeigen**und **über WinProj** für die interne Verwendung von Project Web App und Project Professional und sind sind nicht dokumentiert. Obwohl Sie Proxydateien oder eine Proxy-Assembly handelt, die der internen PSI-Dienste erstellen können, sind die interne Dienste nicht für die Verwendung von Drittanbietern. der PSI-Verweis werden diese Dienste nicht dokumentiert. Die folgende Abbildung zeigt den Speicherort der Back-End-PSI-Dienste in Internetinformationsdienste-Manager. 
  
**Suchen der PSI-Dienste in IIS**

![PSI-Dienste im IIS-Manager] (media/pj15_PSIReference_IIS.gif "PSI-Dienste im IIS-Manager")
  
Im Folgenden finden Sie sämtliche Klassen, die Webmethoden in den PSI-Diensten umfassen:
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) Enthält Methoden, mit denen auf den Verwaltungsseiten von **Project Server** in Project Web App. Geschäftsjahren definiert, die Einstellungen für Zeitberichte und Währung, reporting Zeiträume, das Überwachungsprotokoll und Einstellungen für Active Directory verwaltet. 
    
2. [Archiv](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) Enthält Methoden zum Verwalten von Sicherung und Wiederherstellung der Projekte, Sicherheitskategorien, benutzerdefinierte Felder, Ressourcen, Systemeinstellungen, Ansichten und Enterprise-global-Projekt. Liest und aktualisiert den Terminplan Archiv. Alle Projekte archiviert oder löscht die angegebene Archivierte Projekte. Backup-Objekten in Datenbanktabellen Archiv und Wiederherstellung gesichert Objekte auf die veröffentlichte Datenbanktabellen gespeichert. 
    
3. **Authentifizierung** Enthält Methoden für die interne Verwendung nur von Project Professional und Project Web App. 
    
4. [Kalender](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Kalenderausnahmen Enterprise verwaltet. Checkt und checkt Ressourcenkalender. Erstellt, löscht, werden alle aufgelistet, aktualisiert oder Kalenderausnahmen zurückgegeben. 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) OLAP-Cubeeinstellungen verwaltet. Ruft Analysis-Server, Status der Datenbank und die Liste der Cubes. Legt eine Cube-Erstellungdienst Anforderung in der Warteschlange. Liest und aktualisiert Definitionen berechneter Elemente und Einstellungen für Dimensionen und Measures im Cube dar. 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Benutzerdefinierte Enterprise-Felder verwaltet. Enthält das Auschecken und Einchecken Methoden, und die erstellen, Read, Update und Delete (CRUD)-Methoden für benutzerdefinierte Enterprise-Felder. 
    
7. [Treiber](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Verwaltet den Portfolio Analysis Treiber und Faktorpriorisierung für das Projekt erstellen und Demand Management. Enthält die CRUD-Methoden für das Projekt Treiber. 
    
8. [Ereignisse](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Project Server-Ereignis-Handler Zuordnungen verwaltet. Enthält die CRUD-Methoden für Project Server-Ereignis-Handler Zuordnungen für ein bestimmtes Ereignis oder für alle Zuordnungen von Ereignis-Handler. 
    
9. **ExchangeSync** Dies ist ein interner Project Server-Dienst, der die Exchange-Server-Ereignisse behandelt. Project Web App verwendet **ExchangeSync** um Zuordnungen zwischen Project Server und Exchange-Server zu synchronisieren, anstatt direkt mit dem Outlook-Client wie in Office Project Server 2007 synchronisieren. 
    
    Der Zugriff auf den **ExchangeSync**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **ExchangeSync**-Klassen und -Member werden für die Drittanbieterentwicklung nicht unterstützt. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) Bietet die **Anmeldung** und **Abmeldung** Methoden formularbasierte Authentifizierung. Zugriff auf den **LoginForms** -Dienst ist nur auf einem Front-End-Project Web App-Website verfügbar. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Enthält die **Anmeldung** und **Abmeldung** Methoden, die mit ASMX-basierte Anwendungen für mehrere Authentifizierungsmethoden für Windows-Authentifizierung verwendet werden (Ansprüche und formularbasierte) Project Server 2013-Installationen. Zugriff auf den **LoginWindows** -Dienst ist nur auf einem Front-End-Project Web App-Website verfügbar. 
    
    > [!CAUTION]
    > Der **LoginWindows**-Dienst wird in WCF-basierten Anwendungen oder für Anwendungen, die auf Project Server-Installationen ausgeführt werden, welche nur die Forderungsauthentifizierung oder **OAuth** verwenden, nicht verwendet. In einigen Fällen gibt die Methode **Login** immer **false** zurück. Die Forderungsauthentifizierung verarbeitet die integrierte Windows-Authentifizierung. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Verwaltet den Nachschlagetabellen, mehrsprachiger Nachschlagetabellen und ihre entsprechenden Code Masken. Checkt, checkt, liest, erstellt, gelöscht und aktualisiert. 
    
13. [Benachrichtigungen](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Verwaltet Warnungen und Erinnerungen. Enthält Methoden, die abzurufen, festzulegen, registrieren und Aufheben der Registrierung alert Ergebnisse. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Verwaltet den Webobjekten und Links für Dokumente und Listenelemente auf SharePoint-Websites. Erstellt, gelöscht oder Project, Project verknüpft, Aufgabe oder Vorgang verknüpft Webobjekte liest. 
    
    > [!NOTE]
    > Der **ObjectLinkProvider** -Dienst ist in Project Server 2013 veraltet. Weitere Informationen finden Sie im Abschnitt *Deprecated Features* in [für Entwickler in Project 2013 aktualisiert](updates-for-developers-in-project-2013.md). 
  
15. **OData** Enthält die interne **OData** -Schnittstelle für die reporting Tabellen und Ansichten. Zugriff auf den **OData** -Dienst ist nur über die Back-End- **ProjectServiceApplication** URL verfügbar. Private **OData** -Diensts in die PSI enthält eine Methode, **ODataClient.ProcessOdataMessage**, die Project Server intern verwendet, um Anforderungen für Berichtsdaten zu verarbeiten. Die HTTP-Anfragen Durchlaufen der Front-End- **ProjectData** -Dienst. 
    
    Informationen zu den **ProjectData** -Dienst und dem OData-Protokoll zum Lesen von Berichtsdaten finden Sie unter [ProjectData - Projekt OData-Dienstverweises](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
    
16. **P12Upgrade** Interne Methoden für das Project Server 2013-Installationsprogramm zum Aktualisieren einer Installation von Office Project Server 2007 bietet. Zugriff auf den **P12Upgrade** -Dienst ist nur über die **ProjectServiceApplication** -URL verfügbar. Die **P12Upgrade** -Methoden sind für die Entwicklung von Drittanbietern nicht unterstützt. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Enthält die CRUD-Methoden für projektabhängigkeiten und für den Optimierer, Planer und Analyse-Lösungen. 
    
18. [Projekt](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Projekte verwaltet. Checkt, checkt, erstellt, gelöscht, liest oder Projekte in der Project-Datenbank Entwurf oder veröffentlichten Tabellen aktualisiert. Versetzt eine Nachricht in der Warteschlange für die Veröffentlichung. 
    
    Erstellt oder löscht Entitäten in Projekten (Aufgaben, Ressourcen, Aufgaben usw.). Ruft Informationen zu oder das Projektteam oder Projekt Siteadresse aktualisiert. Ruft Projektstatus, eine Liste der Projekte in den Tabellen Entwurf, alle Sammelvorgänge, Aufgaben, die für die Zuordnung auf eine bestimmte Ressource sind oder alle Projekte ab, in dem eine Ressource Zuordnungen hat.
    
    Erstellt und verwaltet Festlegungen, erstellt Projektvorschläge und Projekte von SharePoint-Aufgabenlisten und sucht Projekt-/Master-Projektbeziehungen.
    
19. **psiserviceapp** Wird intern von Project Online verwendet. Die **Psiserviceapp** Klassen und Member werden für die Entwicklung von Drittanbietern nicht unterstützt. 
    
20. **PWA** Enthält viele Methoden, die für Project Web App, einschließlich der Methods für die Aufgabe Update Genehmigungsregeln und Verwaltung von Statusberichten optimiert sind. Die **PWA** -Methoden sind häufig spezialisierte und etwas redundante im Vergleich zu entsprechenden Methoden in anderen PSI-Dienste. **PWA** -Methoden verwenden oder viele der gleichen Datasets als der PSI-Methoden zurückgeben. 
    
    Der Zugriff auf den **PWA**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **PWA**-Klassen und -Member werden für die Drittanbieterentwicklung nicht unterstützt. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Verwaltet die Project Server-Warteschlange. Ruft Anzahl von Aufträgen, Auftrag und Wartezeit für Auftrag Gruppe, Status aller Aufträge angegebenen Aufträge, Aufträge, deren Besitzer vom Anrufer oder Aufträge für die angegebenen Projekte. Auftrag Korrelation verwaltet und die Warteschlange konfiguriert. 
    
22. [Ressource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Enterprise-Ressourcen verwaltet. Checkt, checkt, aktualisiert oder erstellt Ressourcen oder Project Server-Benutzer und ihrer autorisierungseinstellungen für die; Sucht nach Name oder die GUID Ressourcen. liest Ressource oder von Benutzerdaten und der Ressourcenstrukturplan (RSP) und Weitere Sicherheitsinformationen. Ruft alle Zuordnungen für eine Ressource ab. und Zurücksetzen von Benutzerkennwörtern. **Die Klasse** enthält CRUD-Methoden für Benutzerstellvertretungen. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Ressourcenpläne verwaltet. Checkt, checkt, veröffentlicht und die CRUD-Methoden zum Ressourcenpläne enthält. 
    
24. [Sicherheit](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Enthält die CRUD-Methoden für Sicherheitsvorlagen, Sicherheitskategorien, Organisationseinheit und globale Berechtigungen und Gruppenberechtigungen. Die **Security** -Klasse enthält Methoden zum Projektkategorien. 
    
25. [Statuserfassung](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Verwaltet den Status wird aktualisiert und Zuordnungen. Wendet Statusupdates oder Genehmigungen, sendet Status aktualisiert, zusammenfassende Informationen für gesendete Updates festgelegt, löscht genehmigte Statusupdates oder Verlauf der Genehmigung für einen angegebenen Benutzer oder löscht alle Statusinformationen für eine Reihe von Projekten. Erstellt, abgerufen oder Zuordnungen delegiert; Zuordnungsfeld Arbeitsdauer festgelegt. Ruft die neue Zuordnungen für den aktuellen Benutzer ab. Ruft ab, Historie Zuordnung oder eines Vorgangs, die aktuelle Werte mit Zeitphasen oder der Sammelvorgang Hierarchie. 
    
    Zeigt eine Vorschau der Arbeitszeittabellendaten an oder importiert sie oder liest den Arbeits- bzw. Nichtarbeitsplan eines Benutzers. Sucht ausstehende Statusaktualisierungen, Informationen für gesendete Aktualisierungen oder einen Transaktionsdatensatz der Änderungen in einer gesendeten Aktualisierung. Liest Teamstatus.
    
26. [Arbeitszeittabelle](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Arbeitszeittabellen verwaltet. Enthält die CRUD-Methoden für Arbeitszeittabellen, und sendet oder zurückgerufen Arbeitszeittabellen. Sucht Arbeitszeittabellen, die verspätet oder ausstehender Genehmigung sind. Sucht nach Arbeitszeittabellen nach Datum oder Zeitraum. Ruft die Liste der Arbeitszeittabelle genehmigende Personen. Lädt die aktuelle Werte der Arbeitszeittabelle und eine Zeile der Arbeitszeittabelle überprüft. Die Klasse der **Arbeitszeittabelle** enthält die **ReadProjectTimesheetLines** -Methode und die **SubmitTimesheetLines** -Methode zum Lesen und Senden von Arbeitszeittabellen für eine andere Ressource ohne Identitätswechsel. 
    
27. **Ansicht** Der Dienst **Ansicht** dient zur Verwendung nur in Project Web App. Methoden in der **View** -Klasse Ansichten verwalten und Anzeigen von Berichten und schreibgeschützte Felder in Ansichten. 
    
    Der Zugriff auf den **View**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **View**-Methoden werden für die Drittanbieterentwicklung nicht unterstützt. 
    
28. **WinProj** Der Dienst **über WinProj** dient zur Verwendung nur von Project Professional. Drittanbieter-Entwickler sollten nicht **über WinProj** Methoden für die Programmierung mit Project Server verwenden. 
    
    Einige **WinProj**-Methoden verwenden Datasets wie **ProjectRelationsDataSet** und **ResourceDataSet**, die der **Project**- und **Resource**-Dienst ebenfalls verwendet, für sie sind in Project Professional jedoch bestimmte Eigenschaften und Funktionen erforderlich. 
    
    Der Zugriff auf den **WinProj**-Dienst steht nur über die **ProjectServiceApplication**-URL zur Verfügung. Die **WinProj**-Methoden werden für die Drittanbieterentwicklung nicht unterstützt. 
    
29. [Workflow](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Enthält die CRUD-Methoden für Enterprise-Projekttypen und zum Verwalten der Workflowphasen und-Stufen. Workflows ausgeführt und verwaltet den Phasen im Project Detail Seite (PDP) projektbedarfsmanagement Workflows Statusinformationen festgelegt. Informationen zum Entwickeln von Project Server-Workflows können Entwickler verwenden Sie SharePoint Designer 2013 für deklarative Workflows oder verwenden Sie die Office Developer Tools für Visual Studio 2012 für die Entwicklung mit .NET Framework 4 und der [ Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) -Klasse in der CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Projektwebsites verwaltet. Erstellt und löscht Projektwebsites. Ruft Informationen zu und SharePoint-Einstellungen und von verwaltungswebsites aktualisiert. Synchronisiert und aktualisiert die Project Site Mitgliedschaften und Gruppen. 
    
Jeder Dienstnamespace enthält alle **DataSet** -Schema und Ereignis-Handler Klassen, die der Dienst verwendet wird. Beispielsweise `Calendar.svc` (oder `Calendar.asmx?wsdl` für die ASMX-Webdienst) beschreibt den **Kalender** -Dienst. Wenn Sie den Verweis **WebSvcCalendar**benennen, enthält der Proxy-Namespace der primären **Kalender** -Klasse mit den Methoden **CheckInCalendars**, **CheckOutCalendars**usw.. Der **WebSvcCalendar** -Proxy-Namespace enthält auch die **CalendarDataSet** -Klasse und alle Unterklassen. 
  
Einige PSI-Dienste enthalten doppelte **DataSet**-Klassen. Beispielsweise enthalten die Dienste **Project** und **Statusing** beide die Klasse **ProjectDataSet**. Dies liegt daran, dass die Methoden in den Diensten **Project** und **Statusing** Verweise auf **ProjectDataSet** enthalten und die Proxyassemblys, die Sie beim Festlegen von Verweisen und Kompilieren einer Anwendung erstellen, die zugehörigen Datasets enthalten. Für die Dienste **Project** und **Statusing** können Werte für unterschiedliche Felder in der Klasse **ProjectDataSet.ProjectRow** erforderlich sein. 
  
Wenn Sie nach den Namespaces und Klassen des PSI-Verweises suchen, um beispielsweise die Webmethoden für den **Project**-Dienst anzuzeigen, erweitern Sie den Namespace **[Project web service]** in der Liste **Contents**, und erweitern Sie dann die **Project**-Klasse. 
  
## <a name="see-also"></a>Siehe auch

- [Project Server 2013-Architektur](project-server-2013-architecture.md)
- [Project Server-Programmierbarkeit](project-server-programmability.md)   
- [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)   
- [Voraussetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [.NET Framework Developer Center](http://msdn.microsoft.com/en-us/netframework/aa496123.aspx)
    

