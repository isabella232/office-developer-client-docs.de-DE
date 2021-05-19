---
title: Voraussetzungen für WCF-basierte Codebeispiele in Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierten Codebeispiele, die in den Referenzthemen Project Server Interface (PSI) enthalten sind.
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357161"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Voraussetzungen für WCF-basierte Codebeispiele in Project

Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierten Codebeispiele, die in den Referenzthemen Project Server Interface (PSI) enthalten sind.
   
Viele der WCF-basierten Codebeispiele in der [Project Server 2013-Klassenbibliothek](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) und Webdienstreferenz wurden ursprünglich für die Project 2010-Entwicklerdokumentation erstellt und verwenden ein Standardformat für WCF-Webdienste. Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden. Ausnahmen werden im Beispiel erwähnt. 
  
Codebeispiele in der Project 2013-Entwicklerdokumentation, die unverändert aus den beispielen für Office Project Server 2007 entwickelt wurden, verwenden ASMX-Webdienste. Die ASMX-basierten Beispiele können auch für die Verwendung von WCF-Diensten angepasst werden. In diesem Artikel wird gezeigt, wie Sie die Beispiele mit WCF-Diensten verwenden. Informationen zur Verwendung der Beispiele mit ASMX-Webdiensten finden Sie unter Voraussetzungen für [ASMX-basierte](prerequisites-for-asmx-based-code-samples-in-project.md)Codebeispiele in Project .
  
> [!NOTE]
> Wenn das clientseitige Objektmodell (CSOM) die von Ihrer Anwendung benötigten Methoden enthält, sollten neue Anwendungen mit dem CSOM entwickelt werden. Mit dem CSOM können Anwendungen mit Project Online oder einer lokalen Installation von Project Server 2013 arbeiten. Wenn Ihre Anwendung andernfalls die PSI verwendet, sollte sie die WCF-Schnittstelle verwenden, die Technologie, die wir für die Netzwerkkommunikation empfehlen. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 verwendet werden. 
>
> Weitere Informationen zum CSOM finden Sie [unter Project Server 2013](project-server-2013-architecture.md) architecture and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Bevor Sie die Codebeispiele ausführen, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren, eine Dienstkonfigurationsdatei hinzufügen (oder die WCF-Dienste programmgesteuert konfigurieren) und generische Konstantenwerte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Richten Sie eine Testumgebung Project Serversystem ein.**
    
    Verwenden Sie ein Project Serversystem, wenn Sie entwickeln oder testen. Auch wenn Ihr Code einwandfrei funktioniert, können Abhängigkeiten zwischen Projekten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Folgen haben. 
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die von Ihrer Anwendung verwendeten PSI-Aufrufe verfügen. Das Entwicklerdokumentationsthema für jede PSI-Methode enthält eine Project Server Permissions-Tabelle. Beispielsweise wird [Project. Die QueueCreateProject-Methode](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) erfordert die globale **NewProject-Berechtigung** und **die SaveProjectTemplate-Berechtigung.** 
  
    In einigen Fällen müssen Sie möglicherweise remote debuggen auf dem Server. Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie auf jedem Project Server-Computer in der SharePoint-Farm eine Ereignishandler assembly installieren und dann den Ereignishandler für die Project Web App-Instanz mithilfe der Seite Project Server Einstellungen in der Allgemeinen Anwendung Einstellungen der SharePoint-Zentraladministration konfigurieren.
    
2. **Richten Sie einen Entwicklungscomputer ein.**
    
    In der Regel greifen Sie über ein Netzwerk auf die PSI zu. Die Codebeispiele sind so konzipiert, dass sie auf einem Client ausgeführt werden, der vom Server getrennt ist, sofern nicht angegeben.
    
    1. **Installieren Sie die richtige Version Visual Studio.** Sofern nicht erwähnt, werden die Codebeispiele in Visual C#. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass Das neueste Service Pack installiert ist. 
    
    2. **Kopieren Project Server-DLLs auf den Entwicklungscomputer.** Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` aus Project Servercomputer auf den Entwicklungscomputer: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Informationen zum Kompilieren und Verwenden der ProjectServerServices.dll-Proxy-Assembly für die WCF-Dienste in der PSI finden Sie unter [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Installieren Sie die IntelliSense Dateien.**
    
    Um IntelliSense Beschreibungen für Klassen und Mitglieder in Project Serverassemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013-SDK-Download in das Verzeichnis, in dem sich die Project Server-Assemblys befinden. Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml in das Verzeichnis, in dem Ihre Anwendung einen Verweis auf die Assembly Microsoft.Office.Project.Server.Library.dll wird.
    
    IntelliSense Beschreibungen für die PSI-Dienste erfordern, dass Sie eine PSI-Proxyassembly mithilfe des Skripts CompileWCFProxyAssembly.cmd im Unterverzeichnis im Project `Documentation\IntelliSense\WCF` 2013 SDK-Download erstellen. Das Skript erstellt die WCF-basierte ProjectServerServices.dll Proxy-Assembly. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense].mht im SDK-Download. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Erstellen der Anwendung und Hinzufügen einer Dienstreferenz
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Erstellen sie eine Konsolenanwendung.**
    
    Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds Neue **Project** die Option **.NET Framework 4 aus.** Sie können den PSI-Beispielcode in die neue Anwendung kopieren.
    
2. **Fügen Sie Verweise hinzu, die für WCF erforderlich sind.**
    
    Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.ServiceModel** hinzu (siehe Abbildung 1). Eine Webanwendung würde **System.ServiceModel.Web verwenden.**
    
    Fügen Sie außerdem einen Verweis auf **System.Runtime.Serialization hinzu.**
    
    **Abbildung 1. Hinzufügen der Verweise in Visual Studio für eine WCF-basierte Anwendung**

    ![Hinzufügen von Verweisen für WCF]Hinzufügen von Verweisen für(media/pj15_PrerequisitesWCF_AddReference.gif "WCF")
  
3. **Kopieren Sie den Code**.
    
    Kopieren Sie das vollständige Codebeispiel in die Datei Program.cs der Konsolenanwendung.
    
4. **Legen Sie den Namespace für die Beispielanwendung.**
    
    Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standardanwendungsnamespace so ändern, dass er mit dem Beispiel übereinstimmen kann. Sie können den Standardanwendungsnamespace ändern, indem Sie die Anwendungseigenschaften ändern. 
    
    Das Codebeispiel für [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) verfügt beispielsweise über den Namespace **Microsoft.SDK.Project. Samples.CreateResourceTest**. Wenn der Name des Visual Studio-Projekts **ResourceTest** ist, kopieren Sie den Namespace aus der  Datei Program.cs, und öffnen Sie dann den Projekteigenschaftenbereich (wählen Sie im Menü **Project** **ResourceTest Properties** aus). Kopieren Sie **auf** der Registerkarte Anwendung den Namespace in das Textfeld **Standardnamespace.** 
    
5. **Legen Sie die Dienstverweise.**
    
    Viele Beispiele erfordern einen Verweis auf mindestens einen der PSI-Dienste. Diese werden im Beispiel selbst oder in Kommentaren vor dem Beispiel aufgeführt. Um den richtigen Namespace der Dienstverweise zu erhalten, stellen Sie sicher, dass Sie zuerst den Standardanwendungsnamespace festlegen.
    
    Es gibt drei Möglichkeiten, einen WCF-Dienstverweis hinzuzufügen:
    
    - Erstellen Sie eine PSI-Proxy assembly namens ProjectServerServices.dll, und legen Sie dann einen Verweis auf die Assembly. Weitere Informationen finden Sie unter Using [a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Fügen Sie eine Proxydatei aus der svcutil.exe der Visual Studio hinzu. Weitere [Informationen finden Sie unter Hinzufügen einer PSI-Proxydatei](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Fügen Sie eine Dienstreferenz mithilfe von Visual Studio. Weitere [Informationen finden Sie unter Hinzufügen einer Dienstreferenz](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxy-Assembly und IntelliSense Beschreibungen
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Sie können eine Proxy assembly für alle öffentlichen WCF-Dienste in der PSI verwenden. Kompilieren Sie ProjectServerServices.dll Proxy-Assembly mithilfe des Skripts `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` im Project 2013 SDK-Download, und kopieren Sie dann die Proxy assembly auf Ihren Entwicklungscomputer. Kopieren Sie ProjectServerServices.xml datei für IntelliSense an denselben Speicherort. Legen Visual Studio einen Verweis auf die ProjectServerServices.dll-Proxy-Assembly. 
  
Für Project Server Service Packs und Updates können Sie die Proxyquellendateien aktualisieren und eine neue Proxyassembly erstellen, indem Sie das Skript GenWCFProxyAssembly.cmd im gleichen SDK-Downloadordner verwenden. Einen Link zum SDK-Download finden Sie [in Project 2013-Entwicklerdokumentation](project-2013-developer-documentation.md). Weitere Informationen finden Sie im [Abschnitt Hinzufügen einer Dienstreferenz.](#pj15_PrerequisitesWCF_AddingServiceReference) 
  
> [!NOTE]
> Wenn Sie die Proxyquellendateien aus der Source.zip-Datei extrahieren, sind die Dateien im Ordner ab dem Veröffentlichungsdatum des Project `Documentation\IntelliSense\WCF\Source` 2013 SDK-Downloads aktuell. Führen Sie zum Generieren aktualisierter PSI-Proxyquellendateien das Skript GenASMXProxyAssembly.cmd auf dem Project Server aus. Weitere Informationen finden Sie unter [Hinzufügen einer Dienstreferenz](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Die Skripts im  `Documentation\IntelliSense\ASMX` Ordner funktionieren nicht für WCF-basierte Anwendungen. Das GenASMXProxyAssembly.cmd-Skript ruft Wsdl.exe auf, das Quellcodedateien für die ASMX-Dienste generiert. Die ASMX-Proxydateien enthalten unterschiedliche Klassen und Eigenschaften. Beispielsweise enthält der ASMX-basierte Ressourcenwebdienst die **Resource-Klasse,** während der WCF-basierte Ressourcendienst die **Resource-Schnittstelle,** die **ResourceChannel-Schnittstelle** und die **ResourceClient-Klasse** enthält. 
  
Die für die ASMX-Webdienste und die WCF-Dienste erstellten beliebigen Namespaces sind identisch, sodass die ProjectServerServices.xml-Datei für IntelliSense mit beiden Assemblys funktioniert. Beispielsweise ist der Namespace des Ressourcendiensts in der WCF-basierten Proxy-Assembly und in der ASMX-basierten Proxy-Assembly **SvcResource**. Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass sie in der Proxy assembly und in der ProjectServerServices.xml IntelliSense sind.
  
Wenn ein Codebeispiel einen anderen Namen für einen PSI-Dienstnamespace verwendet, z. B. **ProjectWebSvc** IntelliSense , müssen Sie das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace der Proxy assembly entspricht. 
  
Die Verwendung der WCF-basierten Proxy-Assembly bietet folgende Vorteile:
  
- Sie können die meisten Lösungen mit der Proxy assembly auf einem anderen Computer als dem Servercomputer Project entwickeln. Das Festlegen einer einzelnen Dienstreferenz erfordert die Entwicklung auf dem Project Servercomputer.
    
- Die Proxy assembly enthält alle PSI-Dienstnamespaces, sodass Sie nicht mehrere Proxydateien hinzufügen müssen.
    
- Wenn Sie die ProjectServerServices.xml-Datei demselben Verzeichnis hinzufügen, in dem Sie einen Verweis auf die ProjectServerServices.dll-Proxy-Assembly festlegen, können Sie IntelliSense Beschreibungen für die PSI-Klassen und -Member erhalten. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im Ordner des Project `Documentation\IntelliSense` 2013 SDK-Downloads. 
    
**Abbildung 2. Verwenden IntelliSense für eine Methode im Ressourcendienst**

![Verwenden von Intellisense für die ReadResource-Methode](media/pj15_PrerequisitesWCF_Intellisense.gif "Mithilfe von Intellisense für die ReadResource-Methode")
  
Nachteile bei der Verwendung der Proxy assembly sind, dass die Lösung größer ist und Sie die Proxy assembly mit der Lösung verteilen und installieren müssen. Sie müssen auch dieselben Namespaces verwenden, die sich in der Proxy-Assembly und IntelliSense-Dateien befinden, es sei denn, Sie ändern das Skript so, dass eine Proxy assembly erstellt wird, und ändern die ProjectServerServices.xml IntelliSense-Datei so, dass unterschiedliche Namespaces verwendet werden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxydatei
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Der Project 2013 SDK-Download enthält die Quelldateien, die vom Befehl SvcUtil.exe für die Proxy assembly generiert werden. Die Quelldateien befinden sich in Source.zip im  `Documentation\IntelliSense\WCF` Unterverzeichnis. Anstatt einen Verweis auf die Proxy assembly zu setzen, können Sie eine oder mehrere Quelldateien zu einer Visual Studio hinzufügen. Um z. B. den Project und den Ressourcendienst zu verwenden, fügen Sie den wcf hinzu. Project.cs und wcf. Resource.cs-Dateien in die Lösung. 
  
In WCF wird die primäre Klasse in jedem PSI-Dienst durch eine Schnittstelle definiert und in einer Clientklasse für den Zugriff auf die Member implementiert. Beispielsweise wird die **SvcProject.Resource-Schnittstelle** in der **SvcProject.ResourceClient-Klasse** implementiert. Verwenden Sie beispielsweise den folgenden Code, um ein **ResourceClient-Objekt** als Klassenvariablen **namens resourceClient** zu definieren. Im Beispiel erstellt die **SetClientEndpoints-Methode** ein **resourceClient-Objekt,** das den **basicHttp_Project-Endpunkt** verwendet, der in der Datei app.config ist. Weitere Informationen zur app.config finden Sie im Abschnitt [Hinzufügen einer Dienstkonfigurationsdatei.](#pj15_PrerequisitesWCF_AddConfig) 
  
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
> Unabhängig davon, ob Sie eine PSI-Proxy-Assembly verwenden oder eine Proxydatei für eine Project-Dienstreferenz namens **SvcResource** hinzufügen, würden Sie denselben Code verwenden, um ein **resourceClient-Objekt** zu erstellen und zu löschen. 
  
### <a name="adding-a-service-reference"></a>Hinzufügen eines Serviceverweises
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Wenn Sie die WCF-basierte Proxy-Assembly nicht verwenden oder keine Proxydatei für einen PSI-Dienst hinzufügen, können Sie einen oder mehrere einzelne Dienstverweise direkt in einem Visual Studio. Sie können auch Schritt 1 des folgenden Verfahrens verwenden, um aktualisierte Proxydateien zu erstellen, um das Skript vorzubereiten, das im Download des `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` Project 2013 SDK enthalten ist. 
  
> [!NOTE]
> Zum Festlegen eines Dienstverweises müssen Sie Visual Studio auf dem Project Servercomputer verwenden. Es wird empfohlen, die ProjectServerServices.dll proxy assembly zu verwenden oder Proxyquellendateien hinzuzufügen, anstatt direkt Dienstverweise in Visual Studio. 
  
Die folgenden Schritte zeigen, wie Sie einen Dienstverweis mithilfe von Visual Studio 2012 auf einem Computer festlegen, auf dem eine Testinstallation von Project ausgeführt wird:
  
1. Um Zugriff auf die Back-End-WCF-Dienste zu erhalten, führen Visual Studio auf dem Project Server aus.
    
2. Klicken **Sie im** Projektmappen-Explorer mit der rechten Maustaste auf den Ordner **Verweise,** und wählen Sie **dann Dienstreferenz hinzufügen aus.** 
    
3. Geben Sie im Dialogfeld **Dienstreferenz** hinzufügen im Textfeld Adresse  die https://localhost:32843/ _GUID_/psi/ _ServiceName_.svc ein, und drücken Sie dann die **EINGABETASTE**. Ersetzen Sie _guiD_ durch den virtuellen Verzeichnisnamen der Project Server-Dienstanwendung, z. B. 534c37eb00d74ccfadcecf9827e95239. Ersetzen  _Sie ServiceName_ durch den Namen des Diensts, z. B. Resource (siehe Abbildung 3). 
    
   Sie können den Namen des virtuellen Project Serverdienst auf eine der folgenden Arten erhalten:
    
   - Öffnen Sie SharePoint 2013-Zentraladministrationsanwendung in Ihrem Browser. Wählen **Sie Dienstanwendungen verwalten** aus, und wählen Sie dann die Project Server PSI Service-Anwendung aus, die Sie möchten. Wählen Sie beispielsweise **ProjectServerService aus.** Die URL der Seite Project Web-App-Websites verwalten enthält den namen des virtuellen Verzeichnisses. In ist beispielsweise  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239` der Name des virtuellen  `534c37eb00d74ccfadcecf9827e95239` Verzeichnisses (der Verzeichnisname enthält keine Bindestriche). 
    
   - Öffnen Sie **das Internetinformationsdienste (IIS)-Manager** auf dem Project Servercomputer. Erweitern Sie **SharePoint Web Services-Knoten** im Bereich Verbindungen, und erweitern Sie dann die darunter stehenden virtuellen Dienstverzeichnissen, bis Sie das Verzeichnis finden, das einen PSI-Ordner enthält.  Wählen Sie das Verzeichnis aus,  **wählen Einstellungen** im Bereich Aktionen aus, und kopieren Sie dann den Verzeichnisnamen im **Feld Virtueller** Pfad. 
    
      > [!NOTE]
      > Es kann mehrere Project serverdienst-virtuellen Verzeichnis vorhanden sein. Stellen Sie sicher, dass Sie das virtuelle Verzeichnis auswählen, das die Project Web App-Instanz enthält, die Sie möchten. 
  
   - Verwenden Sie **das Cmdlet get-SPServiceApplication** in Windows PowerShell, das mit SharePoint 2013 installiert ist. Wählen Sie im Startmenü der **Taskleiste** Alle Programme **aus,** wählen Sie **Microsoft SharePoint 2013-Produkte** und dann **SharePoint 2013-Verwaltungsshell aus.** Im Folgenden finden Sie den Befehl und die Ergebnisse im **Fenster SharePoint 2013get- Management Shell** für die definierten Dienstanwendungen (Ihre GUIDs unterscheiden sich). Kopieren Sie die GUID für die Project Server-Dienstanwendung. 
    
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

      Wenn Sie den vollständigen Namen der Project Serverdienstanwendung kennen, können Sie ihn verwenden, um den GUID-Wert zu erhalten, z. B.:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Entfernen Sie die Bindestriche in der GUID, um den Namen des virtuellen Verzeichnisses zu erhalten. 
  
   URLs wie sind `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` standard für Project Serverdienste. 
    
4. Nachdem der Dienstverweis aufgelöst wurde, geben Sie den Verweisnamen in das Textfeld **Namespace** ein. Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden den beliebigen Namespacenamen **Svc _ServiceName_**. Beispielsweise heißt der Ressourcendienst in den Codebeispielen **SvcResource**.
    
    **Abbildung 3. Hinzufügen der WCF-basierten Ressourcendienstreferenz**

    ![Hinzufügen der WCF-basierten Ressourcendienstreferenz](media/pj15_PrerequisitesWCF_AddSvcReference.gif "Hinzufügen der WCF-basierten Ressourcendienstreferenz")
  
5. Ersetzen Sie die temporäre web.config-Datei im Project-Dienstverzeichnis durch das Original (umbenannt in web.config), und führen Sie dann erneut `iisreset` aus.
    
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Project Serveranwendungen verwenden häufig andere Dienste, z. B. SharePoint 2013-Webdienste. Wenn andere Dienste oder Verweise erforderlich sind, werden sie im Codebeispiel notiert.
  
Lokale Verweise für das Codebeispiel werden in **using-Anweisungen** am Anfang des Beispiels aufgeführt. 
  
1. Klicken **Sie im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **Verweise,** und wählen Sie **dann Verweis hinzufügen aus.**
    
2. Wählen **Sie Durchsuchen** aus, und navigieren Sie dann zu dem Speicherort, an dem Sie die zuvor kopierten Project Server-DLLs gespeichert haben. Wählen Sie die dlLs aus, die Sie möchten, und wählen Sie dann **OK aus.**
    
> [!NOTE]
> Stellen Sie sicher, dass die Assemblyversionen auf Ihrem Entwicklungscomputer genau mit denen auf dem Zielcomputer Project übereinstimmen. 
  
## <a name="adding-a-service-configuration-file"></a>Hinzufügen einer Dienstkonfigurationsdatei
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Wenn eine Anwendung die WCF-Dienste programmgesteuert konfiguriert, wird keine Dienstkonfigurationsdatei verwendet. Andernfalls verwendet eine Windows oder Konsolenanwendung das **system.serviceModel-Element** in einer app.config Datei. Eine Webanwendung enthält **system.serviceModel** in web.config. Weitere Informationen zum Verwenden einer app.config oder zum programmgesteuerten Konfigurieren der WCF-Dienste finden Sie unter [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Wenn eine Dienstproxyquellendatei generiert wird, erstellt der befehl SvcUtil.exe auch eine output.config-Datei, die die Grundlage für das **Standardelement system.serviceModel** in einer app.config- oder web.config ist. Der Project 2013 SDK-Download enthält eine output.config-Datei in `Documentation\IntelliSense\WCF\Source.zip` . Die Standarddatei, die output.config für den Ressourcendienst erstellt SvcUtil.exe, enthält beispielsweise zwei Bindungen namens **BasicHttpBinding_Resource** **und BasicHttpBinding_Resource1**. Das **Clientelement** enthält zwei Standardendpunkte. Ein Endpunkt ist für den sicheren Zugriff auf die HTTP-Adresse an Port 32843 und der andere für den normalen Zugriff auf Port 32843, wie folgt: 
  
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

Die PSI-Dienstkonfiguration verwendet nicht die Standardbindungen und Endpunkte. Project Server erfordert, dass Anwendungen über das Front-End ProjectServer.svc auf PSI-Dienste zugreifen, das als Router für Anrufe an die Back-End-Dienste fungiert. Gehen Sie wie folgt app.config, um die Datei "app.config" zu erstellen:
  
1. Wenn Sie einen Verweis auf die ProjectServerServices.dll-Proxy-Assembly festlegen oder die Proxyquellendatei für einen Dienst hinzufügen, enthält die Anwendung keine app.config Datei. Fügen Sie ein neues Element zum Visual Studio hinzu. Wählen Sie im Dialogfeld Neues  **Element** hinzufügen die Vorlage Anwendungskonfigurationsdatei aus, nennen Sie app.config, und wählen Sie dann **Hinzufügen aus.**
    
2. Löschen Sie den ganzen Text in app.config Datei, und kopieren Sie dann den folgenden Code in die Datei. Sie können dieselbe Bindung verwenden, z. B.  `basicHttpConf` für jeden Dienstendpunkt. Wenn Sie mehr als eine Bindung verwenden möchten, z. B. um HTTP- und HTTPS-Protokolle zu binden, müssen Sie für jedes Protokoll eine Bindung erstellen.
    
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

3. Ersetzen Sie in der Clientendpunktadresse durch den Namen `ServerName/ProjectServerName` Ihres Servers und Project Web App-Instanz. 
    
4. Ersetzen  `ServiceName` Sie durch den Namen des PSI-Diensts, z. B. Resource. Stellen Sie sicher, dass Sie alle drei Instanzen des Dienstnamens ersetzen, z. B.:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Um mehr als einen PSI-Dienst zu verwenden, erstellen  Sie ein **Endpunktelement** für jeden Dienst und für jedes von diesem Dienst verwendete Bindungselement. Die folgenden Endpunkte konfigurieren den Client beispielsweise so, dass die grundlegende HTTP-Bindung für den Project und den QueueSystem-Dienst verwendet wird. 
    
    > [!NOTE]
    > Wenn Sie eine Anwendung ausführen und einen Fehler erhalten, dass der Server zu ausgelastet ist oder die HTTP-Anforderung nicht autorisierte ist, stellen Sie sicher, dass die Endpunktadressen in der Datei app.config sind. 
  
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

Sie können eine app.config bearbeiten, indem Sie den **WCF-Dienstkonfigurations-Editor** in Visual Studio (im Menü **Extras)** verwenden. Abbildung 4 zeigt, wie Sie das **Vertragselement** im Dialogfeld **Microsoft Service Configuration Editor** festlegen. Wenn die Lösung die PSI-Proxy-Assembly verwendet, öffnen ProjectServerServices.dll im Verzeichnis `bin\debug` der Visual Studio Lösung. Im **Dialogfeld Vertragstypbrowser** werden alle WCF-Dienstverträge angezeigt (siehe Abbildung 5). 
  
**Abbildung 4. Verwenden des WCF-Dienstkonfigurations-Editors**

![Verwenden des WCF-Dienstkonfigurations-Editors](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "mithilfe des WCF-Dienstkonfigurations-Editors")
  
Wenn die Lösung eine Dienstproxydatei wie wcfResource.cs verwendet, kompilieren Sie die Anwendung, und öffnen Sie dann die ausführbare Datei im  `bin\debug` Verzeichnis. Weitere Informationen zum Bearbeiten der app.config finden Sie unter [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Abbildung 5. Verwenden des Vertragstypbrowsers im WCF-Dienstkonfigurations-Editor**

![Verwenden des Vertragstypbrowsers](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "mithilfe des Vertragstypbrowsers")
  
## <a name="using-multiple-authentication"></a>Verwenden mehrerer Authentifizierungen
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Die Authentifizierung von lokalen Project Serverbenutzern erfolgt Windows Authentifizierung oder Formularauthentifizierung über die Anspruchsverarbeitung in SharePoint. Die mehrfache Authentifizierung bedeutet, dass die Webanwendung, für die Project Web App bereitgestellt wird, sowohl die Windows als auch die formularbasierte Authentifizierung unterstützt. In diesem Fall tritt bei jedem Aufruf eines WCF-Diensts, der die Windows-Authentifizierung verwendet, ein Fehler auf, da der Anspruchsprozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Um das Problem für WCF zu beheben, sollten alle Aufrufe von PSI-Methoden in einem **OperationContextScope** enthalten sein, das für jeden PSI-Dienst definiert ist. Schachteln Sie Bereiche nicht für mehrere Dienste. Wenn Sie z. B. Aufrufe an die Ressourcen- und Project verwenden, sollte jeder Anrufsatz in seinem eigenen Bereich sein. 
  
Im folgenden Beispiel kann die **DisableFormsAuth-Methode** aus jedem **OperationContextScope-Abschnitt** in einer Anwendung aufgerufen werden. Die Methode entfernt alle Headerwerte, die zuvor die Formularauthentifizierung deaktiviert haben, sodass die Formularauthentifizierung fortgesetzt werden kann, wenn der _IsWindowsAuth-Parameter_ **false ist.** Wenn  _isWindowsAuth_ **true ist,** deaktiviert **die DisableFormsAuth-Methode** die Formularauthentifizierung. 
  
In der **WcfSample-Methode** ist das **projectClient-Objekt** eine Instanz der PSI **SvcProject.ProjectClient-Klasse.** 
  
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
> Das Ausführen von PSI-Aufrufen in **einem OperationContextScope** ist nur für Anwendungen erforderlich, die in einer Umgebung mit mehreren Authentifizierungen ausgeführt werden. Wenn Project Server nur die Windows verwendet, müssen Sie keinen Bereich festlegen und einen Webanforderungsheader hinzufügen, der die Formularauthentifizierung deaktiviert. 
> 
> Die Lösung für eine ASMX-basierte Anwendung ist anders. Weitere Informationen finden Sie im Abschnitt *Verwenden der mehrfachen* Authentifizierung unter [Voraussetzungen für ASMX-basierte](prerequisites-for-asmx-based-code-samples-in-project.md)Codebeispiele in Project . 
  
## <a name="changing-values-of-generic-constants"></a>Ändern von Werten generischer Konstanten
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

Die meisten Beispiele enthalten eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel in Ihrer Umgebung ordnungsgemäß funktioniert. Wenn Sie SSL installiert haben, verwenden Sie im folgenden Beispiel das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen  _Sie ServerName_ durch den Namen des servers, den Sie verwenden. Ersetzen _Sie ProjectServerName_ durch den virtuellen Verzeichnisnamen Ihrer Projektserverwebsite, z. B. PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, werden am Anfang des Codebeispiels notiert.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Das Abrufen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach. Wenn Sie beispielsweise ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Seite Project Center in Project Web App angezeigt werden kann.
  
Sie können Codebeispielergebnisse auf verschiedene Weise überprüfen, z. B.:
  
- Verwenden Sie Project Professional 2013-Client, um das Projekt auf dem Project Server-Computer zu öffnen und die elemente, die Sie möchten, anzeigen.
    
- Zeigen Sie veröffentlichte Projekte auf der Project Center-Seite von Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ) an.
    
- Anzeigen des Warteschlangenprotokolls in Project Web App. Öffnen Sie die Seite Server Einstellungen (wählen Sie **das Symbol Einstellungen** in der  oberen rechten Ecke aus), und wählen Sie dann Meine Warteschlangenaufträge unter dem Abschnitt Persönliche **Einstellungen** aus ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). In der **Dropdownliste** Ansicht können Sie nach auftragsstatus sortieren. Der Standardstatus ist **In Bearbeitung und Fehlgeschlagene Aufträge in der vergangenen Woche**. 
    
- Verwenden Sie die Seite Server Einstellungen in Project Web App ( ), um alle Warteschlangenaufträge zu verwalten und Unternehmensobjekte zu löschen oder `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` zu erzwingen. Sie müssen über Administratorberechtigungen verfügen, um auf diese Links auf der Serverserverseite Einstellungen können.
    
- Verwenden **Microsoft SQL Server Management Studio,** um eine Abfrage in einer Tabelle einer Serverdatenbank Project ausführen. Verwenden Sie beispielsweise die folgende Abfrage, um die 200 obersten Zeilen der MSP_WORKFLOW_STAGE_PDPS-Tabelle auszuwählen, um Informationen zu den Projektdetailsetailseiten (PDPs) in Workflowphasen zu zeigen. 
    
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

Nachdem Sie einige Codebeispiele testiert haben, gibt es Enterprise-Objekte und -Einstellungen, die gelöscht oder zurückgesetzt werden sollten. Sie können die Seite Server Einstellungen in Project Web App verwenden, um Unternehmensdaten zu verwalten ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Über Links auf der Seite Server Einstellungen können Sie alte Elemente löschen, Eincheckprojekte erzwingen, die Auftragswarteschlange für alle Benutzer verwalten und andere administrative Aufgaben ausführen.
  
Nachfolgend finden Sie einige der Links auf der Server-Einstellungen, die für typische Bereinigungsaktivitäten nach der Ausführung von Codebeispielen verwendet werden:
  
- **Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**
    
- **Verwalten von Warteschlangenaufträgen**
    
- **Löschen Enterprise Objekten**
    
- **Erzwingen des Eincheckens Enterprise Objekten**
    
- **Enterprise-Projekttypen**
    
- **Workflowphasen**
    
- **Workflowstufen**
    
- **Projektdetailseiten**
    
- **Zeiträume in Zeitberichten**
    
- **Einstellungen und Standardwerte in der Arbeitszeittabelle**
    
- **Linienklassifikationen**
    
Zusätzliche Einstellungen werden von SharePoint Server 2013 für jede Project Web App-Instanz und nicht von einer bestimmten Project Web App Server-Einstellungen verwaltet. Wählen Sie in der SharePoint-Zentraladministrationsanwendung allgemeine Anwendung  **Einstellungen** aus, wählen Sie verwalten unter **Project Server Einstellungen** aus, und wählen Sie dann die Project Web App-Instanz in der Dropdownliste auf der Seite Server Einstellungen aus. Wählen Sie z. B. **Serverseitige Ereignishandler** aus, um Ereignishandler für die ausgewählte Project Web App-Instanz hinzuzufügen oder zu löschen. 
  
## <a name="see-also"></a>Siehe auch

- [Voraussetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mithilfe von WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Verwenden des Identitätswechsels mit WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md) 
- [SharePoint Developer Center](https://msdn.microsoft.com/sharepoint/default.aspx)
    

