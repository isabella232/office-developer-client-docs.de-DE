---
title: Voraussetzungen für WCF-basierte Codebeispiele in Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierten Codebeispiele, die in den Referenzthemen Project Serverschnittstelle (PSI) enthalten sind.
ms.openlocfilehash: e41b16f653776d57de4961f591782ef27bce5b9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619246"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Voraussetzungen für WCF-basierte Codebeispiele in Project

Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierten Codebeispiele, die in den Referenzthemen Project Serverschnittstelle (PSI) enthalten sind.
   
Viele der WCF-basierten Codebeispiele, die in der [Project Server 2013-Klassenbibliothek und webdienstreferenz](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) enthalten sind, wurden ursprünglich für die Project 2010-Entwicklerdokumentation erstellt und verwenden ein Standardformat für WCF-Webdienste. Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden. Ausnahmen sind im Beispiel aufgeführt. 
  
Codebeispiele in der Project 2013-Entwicklerdokumentation, die unverändert aus den Beispielen für Office Project Server 2007 sind, verwenden ASMX-Webdienste. Die ASMX-basierten Beispiele können auch für die Verwendung von WCF-Diensten angepasst werden. In diesem Artikel wird gezeigt, wie Sie die Beispiele mit WCF-Diensten verwenden. Informationen zur Verwendung der Beispiele mit ASMX-Webdiensten finden Sie unter [Voraussetzungen für ASMX-basierte Codebeispiele in Project.](prerequisites-for-asmx-based-code-samples-in-project.md)
  
> [!NOTE]
> Wenn das clientseitige Objektmodell (CSOM) die Methoden enthält, die Ihre Anwendung benötigt, sollten neue Anwendungen mit dem CSOM entwickelt werden. Mit dem CSOM können Anwendungen mit Project Online oder einer lokalen Installation von Project Server 2013 arbeiten. Wenn Ihre Anwendung die PSI verwendet, sollte sie andernfalls die WCF-Schnittstelle verwenden. Dies ist die Technologie, die für die Netzwerkkommunikation empfohlen wird. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 verwendet werden. 
>
> Weitere Informationen zum CSOM finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md) und [clientseitiges Objektmodell (CSOM) für Project 2013.](client-side-object-model-csom-for-project-2013.md) 
  
Bevor Sie die Codebeispiele ausführen, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren, eine Dienstkonfigurationsdatei hinzufügen (oder die WCF-Dienste programmgesteuert konfigurieren) und generische Konstantenwerte so ändern, dass sie ihrer Umgebung entsprechen.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Richten Sie ein Test-Project Serversystem ein.**
    
    Verwenden Sie beim Entwickeln oder Testen ein Test Project Serversystem. Selbst wenn Ihr Code einwandfrei funktioniert, können Abhängigkeiten zwischen Projekten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Folgen haben. 
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die PSI-Aufrufe verfügen, die Ihre Anwendung verwendet. Das Entwicklerdokumentationsthema für jede PSI-Methode enthält eine Project Serverberechtigungstabelle. Beispielsweise die [Project. Die QueueCreateProject-Methode](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) erfordert die globale **NewProject-Berechtigung** und die **SaveProjectTemplate-Berechtigung.** 
  
    In einigen Fällen müssen Sie möglicherweise Remotedebugging auf dem Server ausführen. Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie eine Ereignishandlerassembly auf jedem Project Servercomputer in der SharePoint Farm installieren und dann den Ereignishandler für die Project Web App-Instanz konfigurieren, indem Sie die Seite Project Server Einstellungen in der Einstellungen der SharePoint Zentraladministration verwenden.
    
2. **Richten Sie einen Entwicklungscomputer ein.**
    
    Normalerweise greifen Sie über ein Netzwerk auf die PSI zu. Die Codebeispiele sind so konzipiert, dass sie auf einem Vom Server getrennten Client ausgeführt werden, sofern nicht anders angegeben.
    
    1. **Installieren Sie die richtige Version von Visual Studio.** Sofern nicht anders angegeben, werden die Codebeispiele in Visual C# geschrieben. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass Sie das neueste Service Pack installiert haben. 
    
    2. **Kopieren Sie Project Server-DLLs auf den Entwicklungscomputer.** Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` vom Project Servercomputer auf den Entwicklungscomputer: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Informationen zum Kompilieren und Verwenden der ProjectServerServices.dll Proxyassembly für die WCF-Dienste in der PSI finden Sie unter [Verwenden einer PSI-Proxyassembly und IntelliSense-Beschreibungen.](#pj15_PrerequisitesWCF_BuildingProxy)
    
3. **Installieren Sie die IntelliSense-Dateien.**
    
    Um IntelliSense-Beschreibungen für Klassen und Member in Project Serverassemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013 SDK-Download in das verzeichnis, in dem sich die Project Serverassemblys befinden. Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml-Datei in das Verzeichnis, in dem ihre Anwendung einen Verweis auf die Microsoft.Office.Project.Server.Library.dll assembly festlegen wird.
    
    IntelliSense-Beschreibungen für die PSI-Dienste erfordern, dass Sie eine PSI-Proxyassembly mithilfe des Skripts CompileWCFProxyAssembly.cmd im `Documentation\IntelliSense\WCF` Unterverzeichnis im Project 2013 SDK-Download erstellen. Das Skript erstellt die WCF-basierte ProjectServerServices.dll Proxyassembly. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense].mht im SDK-Download. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Erstellen der Anwendung und Hinzufügen eines Dienstverweises
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Erstellen Sie eine Konsolenanwendung.**
    
    Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds **"Neu Project"** **.NET Framework 4** aus. Sie können den PSI-Beispielcode in die neue Anwendung kopieren.
    
2. **Fügen Sie Verweise hinzu, die für WCF erforderlich sind.**
    
    Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.ServiceModel** hinzu (siehe Abbildung 1). Eine Webanwendung würde **System.ServiceModel.Web** verwenden.
    
    Fügen Sie auch einen Verweis auf **System.Runtime.Serialization** hinzu.
    
    **Abbildung 1. Hinzufügen der Verweise in Visual Studio für eine WCF-basierte Anwendung**

    ![Hinzufügen von Verweisen für WCF](media/pj15_PrerequisitesWCF_AddReference.gif "Hinzufügen von Verweisen für WCF")
  
3. **Kopieren Sie den Code.**
    
    Kopieren Sie das vollständige Codebeispiel in die Datei "Program.cs" der Konsolenanwendung.
    
4. **Legen Sie den Namespace für die Beispielanwendung fest.**
    
    Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standardanwendungsnamespace so ändern, dass er dem Beispiel entspricht. Sie können den Standardanwendungsnamespace ändern, indem Sie die Anwendungseigenschaften ändern. 
    
    Das Codebeispiel für ["ReadResource"](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) hat beispielsweise den Namespace **"Microsoft.SDK.Project". Samples.CreateResourceTest**. If the name of the Visual Studio project is **ResourceTest**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **ResourceTest Properties**). Kopieren Sie den Namespace auf der Registerkarte **"Anwendung"** in das Textfeld **"Standardnamespace".** 
    
5. **Legen Sie die Dienstverweise fest.**
    
    Viele Beispiele erfordern einen Verweis auf einen oder mehrere psi-Dienste. Diese werden im Beispiel selbst oder in Kommentaren aufgeführt, die vor dem Beispiel stehen. Um den richtigen Namespace der Dienstverweise abzurufen, stellen Sie sicher, dass Sie zuerst den Standardanwendungsnamespace festlegen.
    
    Es gibt drei Möglichkeiten, einen WCF-Dienstverweis hinzuzufügen:
    
    - Erstellen Sie eine PSI-Proxyassembly mit dem Namen ProjectServerServices.dll, und legen Sie dann einen Verweis auf die Assembly fest. Weitere Informationen finden Sie [unter Verwenden einer PSI-Proxyassembly und IntelliSense-Beschreibungen.](#pj15_PrerequisitesWCF_BuildingProxy)
    
    - Fügen Sie der Visual Studio Lösung eine Proxydatei aus der svcutil.exe-Ausgabe hinzu. Siehe [Hinzufügen einer PSI-Proxydatei.](#pj15_PrerequisitesWCF_AddingProxyFile)
    
    - Fügen Sie einen Dienstverweis mithilfe von Visual Studio hinzu. Siehe [Hinzufügen eines Dienstverweises.](#pj15_PrerequisitesWCF_AddingServiceReference)
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxyassembly und IntelliSense-Beschreibungen
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Sie können eine Proxyassembly für alle öffentlichen WCF-Dienste in der PSI verwenden. Kompilieren Sie die ProjectServerServices.dll Proxyassembly mithilfe des `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` Skripts im Project 2013 SDK-Download, und kopieren Sie dann die Proxyassembly auf Ihren Entwicklungscomputer. Kopieren Sie die ProjectServerServices.xml-Datei für IntelliSense an denselben Speicherort. Legen Sie in Visual Studio einen Verweis auf die ProjectServerServices.dll Proxyassembly fest. 
  
Für Project Server-Service Packs und -Updates können Sie die Proxyquelldateien aktualisieren und eine neue Proxyassembly erstellen, indem Sie das Skript "GenWCFProxyAssembly.cmd" im selben SDK-Downloadordner verwenden. Einen Link zum SDK-Download finden Sie in der [Entwicklerdokumentation Project 2013.](project-2013-developer-documentation.md) Weitere Informationen finden Sie im Abschnitt [zum Hinzufügen eines Dienstverweises.](#pj15_PrerequisitesWCF_AddingServiceReference) 
  
> [!NOTE]
> Wenn Sie die Proxyquelldateien aus der datei Source.zip extrahieren, sind die Dateien im `Documentation\IntelliSense\WCF\Source` Ordner ab dem Veröffentlichungsdatum des Project 2013 SDK-Downloads aktuell. Um aktualisierte PSI-Proxyquelldateien zu generieren, führen Sie das Skript "GenASMXProxyAssembly.cmd" auf dem Project Servercomputer aus. Weitere Informationen finden Sie unter [Hinzufügen eines Dienstverweises.](#pj15_PrerequisitesWCF_AddingServiceReference) 
> 
> Die Skripts im  `Documentation\IntelliSense\ASMX` Ordner funktionieren nicht für WCF-basierte Anwendungen. Das Skript "GenASMXProxyAssembly.cmd" ruft Wsdl.exe auf, das Quellcodedateien für die ASMX-Dienste generiert. Die ASMX-Proxydateien enthalten unterschiedliche Klassen und Eigenschaften. Beispielsweise enthält der ASMX-basierte Ressourcenwebdienst die **Resource-Klasse,** während der WCF-basierte Ressourcendienst die **Resource-Schnittstelle,** die **ResourceChannel-Schnittstelle** und die **ResourceClient-Klasse** enthält. 
  
Die für die ASMX-Webdienste und die WCF-Dienste erstellten beliebigen Namespaces sind identisch, sodass die ProjectServerServices.xml-Datei für IntelliSense mit beiden Assemblys funktioniert. Beispielsweise ist der Namespace des Ressourcendiensts in der WCF-basierten Proxyassembly und in der ASMX-basierten Proxyassembly **SvcResource**. Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass sie in der Proxyassembly und in der ProjectServerServices.xml IntelliSense-Datei übereinstimmen.
  
Wenn in einem Codebeispiel ein anderer Name für einen PSI-Dienstnamespace verwendet wird, z. B. **ProjectWebSvc,** müssen Sie für IntelliSense das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace der Proxyassembly entspricht. 
  
Zu den Vorteilen der Verwendung der WCF-basierten Proxyassembly gehören folgende:
  
- Sie können die meisten Lösungen mit der Proxyassembly auf einem anderen Computer als dem Project Servercomputer entwickeln. Das Festlegen eines einzelnen Dienstverweises erfordert die Entwicklung auf dem Project Servercomputer.
    
- Die Proxyassembly enthält alle PSI-Dienstnamespaces, sodass Sie nicht mehrere Proxydateien hinzufügen müssen.
    
- Wenn Sie die ProjectServerServices.xml-Datei demselben Verzeichnis hinzufügen, in dem Sie einen Verweis auf die ProjectServerServices.dll Proxyassembly festlegen, können Sie IntelliSense-Beschreibungen für die PSI-Klassen und -Member abrufen. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im `Documentation\IntelliSense` Ordner des Project 2013 SDK-Downloads. 
    
**Abbildung 2. Verwenden von IntelliSense für eine Methode im Ressourcendienst**

![Verwenden von Intellisense für die ReadResource-Methode](media/pj15_PrerequisitesWCF_Intellisense.gif "Verwenden von Intellisense für die ReadResource-Methode")
  
Nachteile der Verwendung der Proxyassembly sind, dass die Lösung größer ist und Sie die Proxyassembly mit der Lösung verteilen und installieren müssen. Sie müssen auch dieselben Namespaces verwenden, die sich in der Proxyassembly und intelliSense-Dateien befinden, es sei denn, Sie ändern das Skript, um eine Proxyassembly zu erstellen, und ändern die ProjectServerServices.xml IntelliSense-Datei so, dass unterschiedliche Namespaces verwendet werden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxydatei
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Der Project 2013 SDK-Download enthält die Quelldateien, die vom befehl SvcUtil.exe für die Proxyassembly generiert werden. Die Quelldateien befinden sich in der Source.zip Datei im  `Documentation\IntelliSense\WCF` Unterverzeichnis. Anstatt einen Verweis auf die Proxyassembly festzulegen, können Sie einer Visual Studio Lösung eine oder mehrere Quelldateien hinzufügen. Um beispielsweise den Project dienst und den Ressourcendienst zu verwenden, fügen Sie die Wcf hinzu. Project.cs und wcf. Resource.cs-Dateien für die Lösung. 
  
In WCF wird die primäre Klasse in jedem PSI-Dienst durch eine Schnittstelle definiert und in einer Clientklasse für den Zugriff auf die Member implementiert. Beispielsweise wird die **SvcProject.Resource-Schnittstelle** in der **SvcProject.ResourceClient-Klasse** implementiert. Verwenden Sie beispielsweise den folgenden Code, um ein **ResourceClient-Objekt** als Klassenvariable mit dem Namen **"resourceClient"** zu definieren. In diesem Beispiel erstellt die **SetClientEndpoints-Methode** ein **resourceClient-Objekt,** das den **basicHttp_Project-Endpunkt** verwendet, der in der app.config-Datei definiert ist. Weitere Informationen zur app.config-Datei finden Sie im Abschnitt ["Hinzufügen einer Dienstkonfigurationsdatei".](#pj15_PrerequisitesWCF_AddConfig) 
  
```cs
private static SvcResource.ResourceClient resourceClient;
. . .
private static void SetClientEndpoints()
{
  resourceClient = new SvcResource.ResourceClient("basicHttp_Resource");
  . . .
}
public void DisposeClients()
{
  resourceClient.Close();
  . . .
}
```

> [!NOTE]
> Unabhängig davon, ob Sie eine PSI-Proxyassembly verwenden oder eine Proxydatei für einen Project Dienstverweis namens **SvcResource** hinzufügen, verwenden Sie denselben Code, um ein **resourceClient-Objekt** zu erstellen und zu verwerfen. 
  
### <a name="adding-a-service-reference"></a>Hinzufügen eines Serviceverweises
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Wenn Sie die WCF-basierte Proxyassembly nicht verwenden oder eine Proxydatei für einen PSI-Dienst hinzufügen, können Sie einen oder mehrere einzelne Dienstverweise direkt in Visual Studio festlegen. Sie können auch Schritt 1 des folgenden Verfahrens verwenden, um aktualisierte Proxydateien zu erstellen, um sich auf das `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` Skript vorzubereiten, das im Project 2013 SDK-Download enthalten ist. 
  
> [!NOTE]
> Um einen Dienstverweis festzulegen, müssen Sie Visual Studio auf dem Project Servercomputer verwenden. Es wird empfohlen, die ProjectServerServices.dll Proxyassembly zu verwenden oder Proxyquelldateien hinzuzufügen, anstatt Dienstverweise direkt in Visual Studio hinzuzufügen. 
  
Die folgenden Schritte zeigen, wie Sie einen Dienstverweis mithilfe von Visual Studio 2012 auf einem Computer mit einer Testinstallation von Project Server festlegen:
  
1. Um Zugriff auf die Back-End-WCF-Dienste zu erhalten, führen Sie Visual Studio auf dem Project Servercomputer aus.
    
2. Klicken Sie **im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **"Verweise",** und wählen Sie dann **Dienstverweis hinzufügen** aus. 
    
3. Geben Sie im Dialogfeld **Dienstverweis hinzufügen** im Textfeld **Adresse** https://localhost:32843/ _GUID_/psi/ServiceName .svc ein, und drücken Sie dann die **EINGABETASTE.**  Ersetzen Sie _die GUID_ durch den Namen des virtuellen Verzeichnisses der Project Serverdienstanwendung, z. B. 534c37eb00d74ccfadcecf9827e95239. Ersetzen Sie  _ServiceName_ durch den Namen des Diensts, z. B. Ressource (siehe Abbildung 3). 
    
   Sie können den Namen des virtuellen Serverdienst-Verzeichnisses Project auf eine der folgenden Arten abrufen:
    
   - Öffnen Sie die SharePoint 2013-Zentraladministrationsanwendung in Ihrem Browser. Wählen Sie **"Dienstanwendungen verwalten"** und dann die gewünschte Project Server PSI-Dienstanwendung aus. Wählen Sie beispielsweise **ProjectServerService** aus. Die URL der Seite "Project Web App-Websites verwalten" enthält den Namen des virtuellen Verzeichnisses. In ist beispielsweise  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239` der Name des virtuellen Verzeichnisses  `534c37eb00d74ccfadcecf9827e95239` (der Verzeichnisname enthält keine Gedankenstriche). 
    
   - Öffnen Sie das Dialogfeld **Internetinformationsdienste (IIS)-Manager** auf dem Project Servercomputer. Erweitern Sie den Knoten **SharePoint Webdienste** im **Bereich "Verbindungen",** und erweitern Sie dann die virtuellen Dienstverzeichnisse darunter, bis Sie das Verzeichnis finden, das einen PSI-Ordner enthält. Wählen Sie das Verzeichnis aus, klicken Sie im Bereich **"Aktionen"** **auf "Erweitert Einstellungen",** und kopieren Sie dann den Verzeichnisnamen in das Feld **"Virtueller Pfad".** 
    
      > [!NOTE]
      > Es können mehrere Project virtuelle Serverdienst-Verzeichnis vorhanden sein. Stellen Sie sicher, dass Sie das virtuelle Verzeichnis auswählen, das die gewünschte Project Web App-Instanz enthält. 
  
   - Verwenden Sie das Cmdlet **"get-SPServiceApplication"** in Windows PowerShell, das mit SharePoint 2013 installiert ist. Wählen Sie im **Startmenü** der Taskleiste **"Alle Programme",** **"Microsoft SharePoint 2013-Produkte"** und dann **SharePoint 2013-Verwaltungsshell** aus. Es folgt der Befehl und die Ergebnisse im Fenster **SharePoint 2013- Verwaltungsshell** für die definierten Dienstanwendungen (Ihre GUIDs unterscheiden sich). Kopieren Sie die GUID für die Project Serverdienstanwendung. 
    
        ```powershell
            PS > get-SPServiceApplication
            DisplayName          TypeName             Id
            -----------          --------             --
            State Service        State Service        04041cfa-4ab3-4473-8bc8-3967b02eff39
            ProjectServerSer...  Project Server PS... 534c37eb-00d7-4ccf-adce-cf9827e95239
            Security Token Se... Security Token Se... 7243732e-edea-405d-8cc8-1716b99faef5
            Application Disco... Application Disco... 3bfbdeb0-bc20-4a21-801c-cc6f1ce6c643
            SharePoint Server... SharePoint Server... 09912f49-3b72-462f-a44c-6533b578286a  
        ```

      Wenn Sie den vollständigen Namen der Project Serverdienstanwendung kennen, können Sie sie verwenden, um den GUID-Wert abzurufen, z. B.:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Entfernen Sie die Striche in der GUID, um den Namen des virtuellen Verzeichnisses abzurufen. 
  
   URLs, z. B. `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` Standard für Project Serverdienste. 
    
4. Nachdem der Dienstverweis aufgelöst wurde, geben Sie den Verweisnamen in das **Textfeld Namespace** ein. Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden den beliebigen Namespacenamen **Svc _ServiceName._** Der Ressourcendienst in den Codebeispielen heißt z. **B. "SvcResource".**
    
    **Abbildung 3. Hinzufügen des WCF-basierten Ressourcendienstverweises**

    ![Hinzufügen des WCF-basierten Ressourcendienstverweises](media/pj15_PrerequisitesWCF_AddSvcReference.gif "Hinzufügen des WCF-basierten Ressourcendienstverweises")
  
5. Ersetzen Sie die temporäre web.config-Datei im Project-Dienstverzeichnis durch das Ursprüngliche (umbenannt in web.config), und führen Sie dann erneut `iisreset` aus.
    
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Project Serveranwendungen verwenden häufig andere Dienste, z. B. SharePoint 2013-Webdienste. Wenn andere Dienste oder Verweise erforderlich sind, werden sie im Codebeispiel angegeben.
  
Lokale Verweise für das Codebeispiel werden in **using-Anweisungen** oben im Beispiel aufgeführt. 
  
1. Klicken Sie **im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **"Verweise",** und wählen Sie dann **Verweis hinzufügen** aus.
    
2. Wählen Sie **"Durchsuchen"** aus, und navigieren Sie dann zu dem Speicherort, an dem Sie die zuvor kopierten Project Server-DLLs gespeichert haben. Wählen Sie die gewünschten DLLs aus, und klicken Sie dann auf **OK.**
    
> [!NOTE]
> Stellen Sie sicher, dass die Assemblyversionen auf dem Entwicklungscomputer exakt mit denen auf dem Zielcomputer Project Servers übereinstimmen. 
  
## <a name="adding-a-service-configuration-file"></a>Hinzufügen einer Dienstkonfigurationsdatei
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Wenn eine Anwendung die WCF-Dienste programmgesteuert konfiguriert, wird keine Dienstkonfigurationsdatei verwendet. Andernfalls verwendet eine Windows Anwendung oder Konsolenanwendung das **System.serviceModel-Element** in einer app.config Datei. Eine Webanwendung enthält **system.serviceModel** in web.config. Weitere Informationen zur Verwendung einer app.config datei oder zum programmgesteuerten Konfigurieren der WCF-Dienste finden Sie unter [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Wenn eine Dienstproxyquelldatei generiert wird, erstellt der Befehl SvcUtil.exe auch eine output.config Datei, die die Basis für das standardmäßige **System.serviceModel-Element** in einer app.config Datei oder web.config Datei ist. Der Project 2013 SDK-Download enthält eine Beispieldatei output.config in `Documentation\IntelliSense\WCF\Source.zip` . Beispielsweise enthält die Standarddatei output.config, die SvcUtil.exe für den Ressourcendienst erstellt, zwei Bindungen mit dem Namen **BasicHttpBinding_Resource** und **BasicHttpBinding_Resource1.** Das **Clientelement** enthält zwei Standardendpunkte. Ein Endpunkt ist für den sicheren Zugriff auf die HTTP-Adresse an Port 32843 und der andere für den normalen Zugriff auf Port 32843, wie folgt: 
  
```XML
<client>
    <endpoint address="https://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="https://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

Die PSI-Dienstkonfiguration verwendet nicht die Standardbindungen und Endpunkte. Project Der Server erfordert, dass Anwendungen über den Front-End-ProjectServer.svc auf PSI-Dienste zugreifen, der als Router für Aufrufe an die Back-End-Dienste fungiert. Führen Sie die folgenden Schritte aus, um die app.config Datei zu erstellen:
  
1. Wenn Sie einen Verweis auf die ProjectServerServices.dll Proxyassembly festlegen oder die Proxyquelldatei für einen Dienst hinzufügen, enthält die Anwendung keine app.config Datei. Fügen Sie dem Visual Studio Projekt ein neues Element hinzu. Wählen Sie im Dialogfeld **"Neues Element hinzufügen"** die Vorlage **"Anwendungskonfigurationsdatei"** aus, benennen Sie sie app.config, und wählen Sie dann **"Hinzufügen"** aus.
    
2. Löschen Sie den gesamten Text in der app.config Datei, und kopieren Sie dann den folgenden Code in die Datei. Sie können die gleiche Bindung verwenden, z.  `basicHttpConf` B. für jeden Dienstendpunkt. Wenn Sie mehrere Bindungen verwenden möchten, z. B. zum Binden von HTTP- und HTTPS-Protokollen, müssen Sie eine Bindung für jedes Protokoll erstellen.
    
    ```XML
        <?xml version="1.0" encoding="utf-8" ?>
        <configuration>
            <system.serviceModel>
                <behaviors>
                    <endpointBehaviors>
                        <behavior name="basicHttpBehavior">
                            <clientCredentials>
                                <windows allowedImpersonationLevel="Impersonation" />
                            </clientCredentials>
                        </behavior>
                    </endpointBehaviors>
                </behaviors>
                <bindings>
                    <basicHttpBinding>
                        <binding name="basicHttpConf" sendTimeout="01:00:00" 
                            maxBufferSize="500000000" maxReceivedMessageSize="500000000">
                            <readerQuotas maxDepth="32" maxStringContentLength="8192" 
                                maxArrayLength="16384" maxBytesPerRead="4096" 
                                maxNameTableCharCount="500000000" />
                            <security mode="TransportCredentialOnly">
                                <transport clientCredentialType="Ntlm" realm="https://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="https://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Ersetzen Sie `ServerName/ProjectServerName` in der Clientendpunktadresse den Namen Ihres Servers und Project Web App-Instanz. 
    
4. Ersetzen Sie  `ServiceName` dies durch den Namen des PSI-Diensts, z. B. Ressource. Stellen Sie sicher, dass Sie alle drei Instanzen des Dienstnamens ersetzen, z. B.:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Um mehr als einen PSI-Dienst zu verwenden, erstellen Sie ein **Endpunktelement** für jeden Dienst und für jedes **Bindungselement,** das der Dienst verwendet. Beispielsweise konfigurieren die folgenden Endpunkte den Client so, dass er die grundlegende HTTP-Bindung für den Project dienst und den QueueSystem-Dienst verwendet. 
    
    > [!NOTE]
    > Wenn Sie eine Anwendung ausführen und einen Fehler erhalten, dass der Server zu ausgelastet ist oder die HTTP-Anforderung nicht autorisiert ist, stellen Sie sicher, dass die Endpunktadressen in der app.config Datei korrekt sind. 
  
    ```XML
        <client>
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Sie können eine app.config Datei mithilfe des **WCF-Dienstkonfigurations-Editors** in Visual Studio bearbeiten (im Menü **"Extras").** Abbildung 4 zeigt, wie das **Vertragselement** im Dialogfeld **Microsoft Service Configuration Editor** festgelegt wird. Wenn die Lösung die PSI-Proxyassembly verwendet, öffnen Sie ProjectServerServices.dll im `bin\debug` Verzeichnis der Visual Studio Lösung. Im Dialogfeld **"Vertragstypbrowser"** werden alle WCF-Dienstverträge angezeigt (siehe Abbildung 5). 
  
**Abbildung 4. Verwenden des WCF-Dienstkonfigurations-Editors**

![Verwenden des WCF-Dienstkonfigurations-Editors](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Verwenden des WCF-Dienstkonfigurations-Editors")
  
Wenn die Lösung eine Dienstproxydatei verwendet, z. B. wcfResource.cs, kompilieren Sie die Anwendung, und öffnen Sie dann die ausführbare Datei im  `bin\debug` Verzeichnis. Weitere Informationen zum Bearbeiten der app.config-Datei finden Sie unter [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Abbildung 5. Verwenden des Vertragstypbrowsers im WCF-Dienstkonfigurations-Editor**

![Verwenden des Vertragstypbrowsers](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Verwenden des Vertragstypbrowsers")
  
## <a name="using-multiple-authentication"></a>Verwenden mehrerer Authentifizierungen
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Die Authentifizierung von lokalen Project Serverbenutzern, sei es durch Windows Authentifizierung oder formularbasierte Authentifizierung, erfolgt über die Anspruchsverarbeitung in SharePoint. Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication. Wenn dies der Fall ist, schlägt jeder Aufruf eines WCF-Diensts, der Windows Authentifizierung verwendet, mit dem folgenden Fehler fehl, da der Anspruchsprozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Um das Problem für WCF zu beheben, sollten sich alle Aufrufe von PSI-Methoden in einem **OperationContextScope** befinden, der für jeden PSI-Dienst definiert ist. Bereiche für mehrere Dienste nicht verschachteln; Wenn Sie z. B. Aufrufe der Ressourcen- und Project-Dienste verwenden, sollte jeder Aufrufsatz innerhalb eines eigenen Bereichs erfolgen. 
  
Im folgenden Beispiel kann die **DisableFormsAuth-Methode** aus jedem **OperationContextScope-Abschnitt** in einer Anwendung aufgerufen werden. Die Methode entfernt alle Headerwerte, die zuvor die Formularauthentifizierung deaktiviert haben, sodass die Formularauthentifizierung fortgesetzt werden kann, wenn der Parameter  _"isWindowsAuth"_ **auf "false" festgelegt** ist. Wenn  _"isWindowsAuth"_ **auf "true"** festgelegt ist, deaktiviert die **DisableFormsAuth-Methode** die Formularauthentifizierung. 
  
In der **WcfSample-Methode** ist das **projectClient-Objekt** eine Instanz der **PSI-Klasse "SvcProject.ProjectClient".** 
  
```cs
// Class variable that determines whether to disable Forms authentication.
private bool isWindowsUser = true;
public void DisableFormsAuth(bool isWindowsAuth)
{
    WebOperationContext.Current.OutgoingRequest.Headers.Remove(
        "X-FORMS_BASED_AUTH_ACCEPTED");
    if (isWindowsAuth)
    {
        // Disable Forms authentication, to enable Windows authentication.
        WebOperationContext.Current.OutgoingRequest.Headers.Add(
            "X-FORMS_BASED_AUTH_ACCEPTED", "f");
    }
}
private void WcfSample()
{
    // Limit the scope of WCF calls to the client channel. 
    using (OperationContextScope scope = new OperationContextScope(projectClient.InnerChannel))
    {
        // Add a web request header to enable Windows authentication in 
        // multiple authentication installations.
        DisableFormsAuth(isWindowsUser);
        // Add calls to the projectClient methods here:
        // . . .
    }
}
```

> [!NOTE]
> PSI-Aufrufe in einem **OperationContextScope** sind nur für Anwendungen erforderlich, die in einer Umgebung mit mehreren Authentifizierungen ausgeführt werden. Wenn Project Server nur Windows Authentifizierung verwendet, ist es nicht erforderlich, einen Bereich festzulegen und einen Webanforderungsheader hinzuzufügen, der die Formularauthentifizierung deaktiviert. 
> 
> Die Korrektur für eine ASMX-basierte Anwendung unterscheidet sich. Weitere Informationen finden Sie im Abschnitt *"Verwenden mehrerer Authentifizierungen"* unter ["Voraussetzungen für ASMX-basierte Codebeispiele" in Project.](prerequisites-for-asmx-based-code-samples-in-project.md) 
  
## <a name="changing-values-of-generic-constants"></a>Ändern der Werte generischer Konstanten
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

Die meisten Beispiele verfügen über eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel ordnungsgemäß in Ihrer Umgebung funktioniert. Wenn Sie im folgenden Beispiel SSL installiert haben, verwenden Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen Sie  _ServerName_ durch den Namen des servers, den Sie verwenden. Ersetzen Sie _ProjectServerName_ durch den namen des virtuellen Verzeichnisses Ihrer Project Server-Website, z. B. PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, werden oben im Codebeispiel notiert.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Das Abrufen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach. Wenn Sie z. B. ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Project Center-Seite in Project Web App angezeigt werden kann.
  
Sie können Codebeispielergebnisse auf verschiedene Arten überprüfen, z. B.:
  
- Verwenden Sie den Project Professional 2013-Client, um das Projekt auf dem Project Servercomputer zu öffnen und die gewünschten Elemente anzuzeigen.
    
- Anzeigen veröffentlichter Projekte auf der Project Center-Seite von Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Zeigen Sie das Warteschlangenprotokoll Project Web App an. Öffnen Sie die Seite "Server Einstellungen" (klicken Sie in der oberen rechten Ecke auf das **Symbol Einstellungen),** und wählen Sie dann **"Meine Aufträge in der Warteschlange"** im Abschnitt **"Personal Einstellungen"** ( `https://ServerName/ProjectServerName/MyJobs.aspx` ) aus. In  der Dropdownliste Ansicht können Sie nach dem Auftragsstatus sortieren. Der Standardstatus ist **In Bearbeitung und Fehlgeschlagene Aufträge in der letzten Woche.** 
    
- Verwenden Sie die Seite "Server Einstellungen" in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ), um alle Warteschlangenaufträge zu verwalten und das Einchecken von Unternehmensobjekten zu löschen oder zu erzwingen. Sie müssen über Administratorberechtigungen verfügen, um auf diese Links auf der Seite "Server Einstellungen" zugreifen zu können.
    
- Verwenden Sie **Microsoft SQL Server Management Studio,** um eine Abfrage in einer Tabelle einer Project Serverdatenbank auszuführen. Verwenden Sie beispielsweise die folgende Abfrage, um die obersten 200 Zeilen der MSP_WORKFLOW_STAGE_PDPS Tabelle auszuwählen, um Informationen zu den Projektdetailseiten (PDPs) in Workflowphasen anzuzeigen. 
    
```sql
        SELECT TOP 200 [STAGE_UID]
                ,[PDP_UID]
                ,[PDP_NAME]
                ,[PDP_POSITION]
                ,[PDP_ID]
                ,[PDP_STAGE_DESCRIPTION]
                ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
```

## <a name="cleaning-up"></a>Löschen
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Nachdem Sie einige Codebeispiele getestet haben, gibt es Enterprise-Objekte und -Einstellungen, die gelöscht oder zurückgesetzt werden sollten. Sie können die Seite "Server Einstellungen" in Project Web App verwenden, um Unternehmensdaten ( ) zu `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` verwalten. Links auf der Seite "Server Einstellungen" ermöglichen es Ihnen, alte Elemente zu löschen, Eincheckprojekte zu erzwingen, die Auftragswarteschlange für alle Benutzer zu verwalten und andere administrative Aufgaben auszuführen.
  
Im Folgenden finden Sie einige Links auf der Seite "Server Einstellungen", die nach dem Ausführen von Codebeispielen für typische Bereinigungsaktivitäten verwendet werden können:
  
- **Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**
    
- **Verwalten von Warteschlangenaufträgen**
    
- **Löschen Enterprise-Objekte**
    
- **Erzwingen des Eincheckens Enterprise-Objekten**
    
- **Enterprise-Projekttypen**
    
- **Workflowphasen**
    
- **Workflowstufen**
    
- **Projektdetailseiten**
    
- **Zeiträume in Zeitberichten**
    
- **Einstellungen und Standardwerte in der Arbeitszeittabelle**
    
- **Zeilenklassifizierungen**
    
Zusätzliche Einstellungen werden von SharePoint Server 2013 für jede Project Web App-Instanz und nicht von einer bestimmten Project Web App Server Einstellungen Seite verwaltet. Wählen Sie in der Zentraladministrationsanwendung SharePoint allgemeine **Anwendung Einstellungen** aus, **wählen** Sie Unter Project **Server Einstellungen** verwalten und dann die Project Web App-Instanz in der Dropdownliste auf dem Server Einstellungen Seite. Wählen Sie beispielsweise **serverseitige Ereignishandler** aus, um Ereignishandler für die ausgewählte Project Web App-Instanz hinzuzufügen oder zu löschen. 
  
## <a name="see-also"></a>Siehe auch

- [Voraussetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mithilfe von WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Verwenden des Identitätswechsels mit WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md) 
- [SharePoint Developer Center](https://msdn.microsoft.com/sharepoint/default.aspx)
    

