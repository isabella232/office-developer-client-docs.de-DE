---
title: Voraussetzungen für WCF-basierte Codebeispiele in Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Hier erfahren Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierte Codebeispiele, die in den Referenzthemen für Project Server Interface (PSI) enthalten sind.
ms.openlocfilehash: 43700a9db4445dacf366c7ca2efe1bfb10914372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796309"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Voraussetzungen für WCF-basierte Codebeispiele in Project

Hier erfahren Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierte Codebeispiele, die in den Referenzthemen für Project Server Interface (PSI) enthalten sind.
   
Viele der WCF-basierte Codebeispiele in der [Project Server 2013 Class Library und Web-Dienst verweisen](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) enthalten ursprünglich für die Entwicklerdokumentation für Project 2010 erstellt wurden, und verwenden ein Standardformat für WCF-Webdienste. Die Beispiele weiterhin Arbeit in Project Server 2013 und in eine Konsolenanwendung kopiert und als eine vollständige Einheit ausgeführt werden sollen. Ausnahmen sind in der Stichprobe notiert haben. 
  
Codebeispiele in der Dokumentation zu Project 2013 für Entwickler, die aus der Beispiele für Office Project Server 2007 entwickelte unverändert sind verwenden ASMX-Webdienste. Die ASMX-basierte Codebeispiele können auch mithilfe der WCF-Dienste angepasst werden. In diesem Artikel veranschaulicht, wie die Beispiele mit WCF-Diensten. Informationen zur Verwendung der Beispiele mit ASMX-Webdiensten finden Sie unter [Voraussetzungen für ASMX-basierte Codebeispiele im Projekt](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Wenn das Client-seitigen Objektmodell (CSOM) die Methoden, die die Anwendung erforderlich ist enthält, sollten neue Anwendungen mit dem Clientobjektmodell entwickelt werden. Das CSOM kann mit Project Online oder einer lokalen Installation von Project Server 2013. Andernfalls, wenn die Anwendung die PSI verwendet wird, sollte die WCF-Schnittstelle verwendet werden also die Technologie, die für die Netzwerkkommunikation empfohlen. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Interface verwenden, können nur für lokale Installationen von Project Server 2013 arbeiten. 
>
> Weitere Informationen zu den CSOM finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md) und [den clientseitigen Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Vor dem Ausführen der Codebeispiele, Sie müssen Einrichten der Entwicklungsumgebung, konfigurieren Sie die Anwendung, hinzufügen eine Konfigurationsdatei Service (oder die WCF-Dienste programmgesteuert konfigurieren), und generische Konstantenwerte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Richten Sie einen Test Project Server-System.**
    
    Verwenden Sie einen Test Project Server-System, wenn Sie entwickeln oder testen. Auch wenn Ihr Code perfekt interproject Abhängigkeiten funktioniert, können Berichte oder andere Umgebungsfaktoren unerwartete Ergebnisse verursachen. 
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server, und überprüfen Sie, dass Sie über ausreichende Berechtigungen für die PSI-Aufrufe verfügen, die die Anwendung verwendet. Das Thema des Developer-Dokumentation für jede PSI-Methode enthält eine Project Server-Berechtigungen-Tabelle. Die [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) -Methode erfordert beispielsweise die globale Berechtigung **Neues Projekt** und die Berechtigung **SaveProjectTemplate** . 
  
    In einigen Fällen müssen Sie möglicherweise das Remotedebuggen auf dem Server. Sie müssen auch einen Ereignishandler einrichten, indem ein Ereignishandlerassembly auf jeden Project Server-Computer in der SharePoint-Farm installieren und konfigurieren Sie dann den Ereignishandler für die Project Web App-Instanz mithilfe der Seite Project Server-Einstellungen in den allgemeinen Anwendungseinstellungen der SharePoint-Zentraladministration.
    
2. **Einrichten von einem Entwicklungscomputer.**
    
    Sie werden in der Regel die PSI über ein Netzwerk zugreifen. Die folgenden Codebeispiele dienen zum auf einem Client ausgeführt werden, die getrennt vom Server, sofern nicht anders angegeben ist.
    
    1. **Installieren Sie die richtige Version von Visual Studio.** Wenn nicht anders angegeben werden die folgenden Codebeispiele in Visual c# geschrieben. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass Sie das neueste Servicepack installiert haben. 
    
    2. **Kopieren Sie Project Server-DLLs auf dem Entwicklungscomputer installiert.** Kopieren Sie die folgenden Assemblys aus `[Program Files]\Microsoft Office Servers\15.0\Bin` auf dem Project Server-Computer, auf dem Entwicklungscomputer installiert: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Informationen dazu, wie Sie kompilieren und die Assembly ProjectServerServices.dll Proxy für die WCF-Dienste in die PSI verwenden finden Sie unter [Verwendung einer PSI-Proxy-Assembly und IntelliSense Beschreibungen](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Installieren Sie die IntelliSense-Dateien.**
    
    Laden IntelliSense Beschreibungen für Klassen und Member in Project Server-Assemblys Kopie zu verwenden, um die aktualisierten IntelliSense-XML-Dateien aus dem Projekt 2013 SDK in dasselbe Verzeichnis, in dem die Project Server-Assemblys gespeichert sind. Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml-Datei in das Verzeichnis, in dem die Anwendung einen Verweis auf die Assembly Microsoft.Office.Project.Server.Library.dll festgelegt wird.
    
    IntelliSense eine Beschreibung der PSI-Dienste erfordern, dass das Erstellen einer PSI-Proxy-Assembly mithilfe des CompileWCFProxyAssembly.cmd-Skripts in der `Documentation\IntelliSense\WCF` Unterverzeichnis des Project 2013 SDK-Downloads. Das Skript erstellt die WCF-basierte ProjectServerServices.dll Proxy-Assembly. Weitere Informationen finden Sie unter die [ReadMe_IntelliSense] MHT-Datei im Download SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Erstellen der Anwendung und Hinzufügen eines Dienstverweises
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Erstellen Sie eine Konsolenanwendung.**
    
    Wenn Sie eine Konsolenanwendung, in der Dropdown-Liste im Dialogfeld **Neues Projekt** erstellen, wählen Sie **.NET Framework 4**. Sie können den Beispielcode PSI in der neuen Anwendung kopieren.
    
2. **Fügen Sie Verweise für WCF erforderlich.**
    
    Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.ServiceModel** (siehe Abbildung 1). Eine Webanwendung würde **System.ServiceModel.Web**verwenden.
    
    Fügen Sie auch einen Verweis auf **System.Runtime.Serialization**.
    
    **Abbildung 1. Hinzufügen der Verweise in Visual Studio für einen WCF-basierte Anwendung**

    ![Hinzufügen von Verweisen für WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Hinzufügen von Verweisen für WCF")
  
3. **Kopieren Sie den Code**.
    
    Kopieren Sie das vollständige Codebeispiel in der Datei Program.cs der Konsole an.
    
4. **Legen Sie den Namespace für die beispielanwendung aus.**
    
    Sie können ändern Sie den Namespace am oberen Rand des Beispiels zum Standard-Namespace Anwendung aufgeführt oder Standardnamespace Anwendung im Beispiel entsprechend ändern. Sie können den Standardnamespace Anwendung durch Ändern der Anwendungseigenschaften ändern. 
    
    Das Codebeispiel für [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) verfügt beispielsweise über den **Microsoft.SDK.Project.Samples.CreateResourceTest**-Namespace. Wenn der Name des Visual Studio-Projekts **ResourceTest**ist, kopieren Sie den Namespace aus der Datei Program.cs, und öffnen Sie **Project Eigenschaftenbereich** (Wählen Sie im Menü **Projekt** **ResourceTest Eigenschaften**ein). Kopieren Sie auf der Registerkarte **Anwendung** den Namespace in das Textfeld **Standardnamespace** . 
    
5. **Legen Sie die Dienstverweise.**
    
    Viele Beispiele erfordern einen Verweis auf eine oder mehrere der PSI-Dienste. Diese werden in der Stichprobe selbst oder Kommentare, die im Beispiel vorangehen aufgelistet. Wenn den richtigen Namespace, der die Dienstverweise erhalten möchten, stellen Sie sicher, dass Sie zunächst den Standardnamespace Anwendung festlegen.
    
    Es gibt drei Möglichkeiten zum Hinzufügen eines WCF-Dienstverweises:
    
    - Erstellen einer PSI-Proxy-Assembly mit dem Namen ProjectServerServices.dll, und legen Sie einen Verweis auf die Assembly. Finden Sie unter [Verwendung einer PSI-Proxy-Assembly und IntelliSense Beschreibungen](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Fügen Sie eine Proxydatei aus der svcutil.exe Ausgabe der Visual Studio-Projektmappe. Finden Sie unter [Hinzufügen einer PSI-Proxy-Datei](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Hinzufügen eines Dienstverweises mithilfe von Visual Studio. Finden Sie unter [Hinzufügen eines Dienstverweises](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxy-Assembly und Beschreibungen von IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Sie können eine Proxyassembly für alle öffentlichen WCF-Dienste in die PSI verwenden. Kompilieren Sie die ProjectServerServices.dll-Proxy-Assembly mithilfe der `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` Skript in den Project 2013-SDK-Download, und kopieren Sie die Proxyassembly auf Ihrem Entwicklungscomputer. Kopieren Sie die Datei ProjectServerServices.xml für IntelliSense an den gleichen Speicherort. Legen Sie Sie in Visual Studio einen Verweis auf die Assembly ProjectServerServices.dll Proxy. 
  
Für Project Server Servicepacks und Updates können Sie die Quelldateien Proxy aktualisieren und erstellen eine neue Proxyassembly mithilfe des GenWCFProxyAssembly.cmd-Skripts in der gleichen SDK-Download-Ordner. Eine Verknüpfung mit den SDK-Download finden Sie unter [Project 2013-Entwicklerdokumentation](project-2013-developer-documentation.md). Weitere Informationen finden Sie im Abschnitt [Hinzufügen eines Dienstverweises](#pj15_PrerequisitesWCF_AddingServiceReference) . 
  
> [!NOTE]
> Beim Extrahieren der Quelldateien Proxy aus der Datei Source.zip herunter-Datei, die Dateien in die `Documentation\IntelliSense\WCF\Source` Ordner ab dem Datum der Veröffentlichung des Project 2013-SDK-Downloads aktuell sind. Generieren aktualisiert PSI Proxy Quelldateien, führen Sie das Skript GenASMXProxyAssembly.cmd auf dem Project Server-Computer. Weitere Informationen finden Sie unter [Hinzufügen eines Dienstverweises](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Die Skripts in der `Documentation\IntelliSense\ASMX` Ordner für WCF-basierte Applikationen nicht mehr verwendet. Das GenASMXProxyAssembly.cmd-Skript ruft Wsdl.exe, die Quellcodedateien für die ASMX-Dienste generiert. Die ASMX-Proxy-Dateien enthalten die verschiedenen Klassen und Eigenschaften. Der Ressource ASMX-basierte Webdienst umfasst beispielsweise **die Klasse,** während der Dienst WCF-basierte Ressource die **Ressource** Interface, die **ResourceChannel** -Schnittstelle und die **ResourceClient** -Klasse enthält. 
  
Die beliebigen Namespaces für die ASMX-Webdienste und die WCF-Dienste erstellt sind identisch, so, dass die Datei ProjectServerServices.xml für IntelliSense mit entweder Assembly funktioniert. Beispielsweise ist der Namespace des Diensts Ressource in der Proxyassembly für WCF-basierte und in der Proxyassembly für ASMX-basierte **SvcResource**. Sie können die Namespacenamen natürlich ändern – Wenn Sie sicherstellen, dass sie in der Proxyassembly und in der Datei ProjectServerServices.xml IntelliSense übereinstimmen.
  
Wenn ein Codebeispiel einen anderen Namen für einen Namespace der PSI-Dienst verwendet wird, muss beispielsweise **ProjectWebSvc**IntelliSense Sie zusammenarbeiten, ändern Sie das Beispiel um **SvcProject** verwenden, damit der Namespace Proxyassembly entspricht. 
  
Die folgenden: Vorteile der Verwendung der WCF-basierte Proxyassembly
  
- Sie können die meisten Lösungen entwickeln, mit der Proxyassembly auf einem anderen Computer als der Project Server-Computer. Festlegen einer einzelnen Dienstverweis erfordert die Entwicklung auf dem Project Server-Computer.
    
- Die Proxyassembly enthält alle PSI-Dienst-Namespaces, damit Sie keine Hinzufügen mehrerer Proxydateien.
    
- Wenn Sie die ProjectServerServices.xml-Datei in dasselbe Verzeichnis hinzufügen, in dem Sie einen Verweis auf die Assembly ProjectServerServices.dll Proxy festlegen, können Sie IntelliSense Beschreibungen für die PSI-Klassen und Member abrufen. Weitere Informationen finden Sie unter die Datei [ReadMe_IntelliSense] in der `Documentation\IntelliSense` Ordner des Project 2013-SDK-Downloads. 
    
**Abbildung 2. Verwenden von IntelliSense für eine Methode in der Ressource-Dienst**

![Verwenden von Intellisense für die ReadResource-Methode] (media/pj15_PrerequisitesWCF_Intellisense.gif "Verwenden von Intellisense für die ReadResource-Methode")
  
Nachteile der Verwendung der Proxyassembly sind, dass die Lösung größer ist, und Sie müssen verteilen und installieren Sie die Proxyassembly mit der Lösung. Sie müssen den gleichen Namespaces, die in der Proxyassembly und die IntelliSense-Dateien sind auch verwenden, es sei denn, Sie ändern das Skript aus, um eine Proxyassembly erstellen und ändern Sie die ProjectServerServices.xml IntelliSense-Datei, um unterschiedliche Namespaces zu verwenden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxy-Datei
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Der Project 2013-SDK-Download enthält die Quelldateien, die für die Proxyassembly mit dem Befehl SvcUtil.exe generiert werden. Die Quelldateien sind in der Datei Source.zip herunter-Datei in die `Documentation\IntelliSense\WCF` Unterverzeichnis. Anstatt einen Verweis auf die Proxyassembly, können Sie eine oder mehrere der Quelldateien für Visual Studio-Projektmappe hinzufügen. Um den Project-Dienst und den Dienst für die Ressource verwenden, fügen Sie beispielsweise die Wcf. Project.cs und Wcf. Resource.cs Dateien zu der Lösung an. 
  
In WCF ist die primäre Klasse in jedem PSI-Dienst durch eine Schnittstelle definiert und in einer Clientklasse für den Zugriff auf die Member implementiert. Beispielsweise wird in der **SvcProject.ResourceClient** -Klasse die **SvcProject.Resource** -Schnittstelle implementiert. Um ein **ResourceClient** -Objekt als einer Klassenvariablen namens **ResourceClient**definieren möchten, verwenden Sie beispielsweise den folgenden Code. Im Beispiel erstellt die **SetClientEndpoints** -Methode ein **ResourceClient** -Objekt, das den Endpunkt **BasicHttp_Project** verwendet wird, die in der App.config.Datei definiert ist. Weitere Informationen zur Datei ' App.config ' finden Sie im Abschnitt [Hinzufügen einer Konfigurationsdatei Service](#pj15_PrerequisitesWCF_AddConfig) . 
  
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
> Ob Sie mit einer PSI-Proxy-Assembly oder einer Proxydatei für eine Project Dienstverweis mit dem Namen **SvcResource hinzufügen**, verwenden Sie den gleichen Code zum Erstellen und Verwenden eines **ResourceClient** -Objekts. 
  
### <a name="adding-a-service-reference"></a>Hinzufügen eines Serviceverweises
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Wenn Sie nicht die Proxyassembly WCF-basierte verwenden oder einer Proxydatei für eine PSI-Dienst hinzufügen, können Sie eine oder mehrere einzelne Dienstverweise direkt in Visual Studio festlegen. Sie können auch Schritt 1 des folgenden Verfahrens zum Erstellen von aktualisierten Proxydateien, zur Vorbereitung der `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` Skript, d. h. im Project 2013-SDK-Download enthalten. 
  
> [!NOTE]
> Wenn Sie einen Dienstverweis festlegen, müssen Sie Visual Studio auf dem Project Server-Computer verwenden. Es wird empfohlen, dass Sie die Assembly ProjectServerServices.dll Proxy verwenden oder Proxydateien hinzufügen, anstatt direkt in Visual Studio Dienstverweise hinzufügen. 
  
Die folgenden Schritte zeigen, wie einen Dienstverweis auf einem Computer mit einer Testinstallation von Project Server mithilfe von Visual Studio 2012 festgelegt:
  
1. Führen Sie Visual Studio auf dem Project Server-Computer, um Zugriff auf die Back-End-WCF-Dienste zu erhalten.
    
2. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann auf **Dienstverweis hinzufügen**. 
    
3. Geben Sie im Dialogfeld **Dienstverweis hinzufügen** in das Textfeld **Adresse** http://localhost:32843/ _GUID_/psi/ _ServiceName_svc, und drücken Sie die **EINGABETASTE**. Ersetzen Sie mit der Name des virtuellen Verzeichnisses der Project Server-Anwendung, wie beispielsweise 534c37eb00d74ccfadcecf9827e95239 _GUID_ . Ersetzen _ServiceName_ durch den Namen des Diensts, wie Ressource (siehe Abbildung 3). 
    
   Sie können den Namen des virtuellen Verzeichnisses von Project Server-Dienst in einem der folgenden Methoden abrufen:
    
   - Öffnen Sie die SharePoint 2013-Zentraladministration-Anwendung in Ihrem Browser. Wählen Sie **dienstanwendungen verwalten**, und wählen Sie dann die PSI-Dienst für Project Server-Anwendung, die Sie möchten. Wählen Sie beispielsweise **ProjectServerService**. Die URL der Seite Project Web App-Sites verwalten enthält den Namen des virtuellen Verzeichnisses an. Beispielsweise `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, ist der Name des virtuellen Verzeichnisses `534c37eb00d74ccfadcecf9827e95239` (der Name des Verzeichnisses enthält keine Bindestriche). 
    
   - Öffnen Sie das Dialogfeld **Internetinformationsdienste (Internet Information Services, IIS)-Manager** auf dem Project Server-Computer. Erweitern Sie den Knoten **SharePoint-Webdienste** im Bereich **Verbindungen** , und erweitern Sie dann die virtuellen Verzeichnissen des Diensts darunter, bis Sie das Verzeichnis gefunden, das einen PSI-Ordner enthält. Wählen Sie das Verzeichnis, wählen Sie **Erweiterte Einstellungen** im Bereich **Aktionen** , und klicken Sie dann kopieren Sie den Name des Verzeichnisses im Feld **Virtuelle Pfade** . 
    
      > [!NOTE]
      > Mehr als ein virtuelles Verzeichnis von Project Server-Dienst kann vorhanden sein. Stellen Sie sicher, dass Sie das virtuelle Verzeichnis auswählen, das die Project Web App-Instanz enthält, die Sie möchten. 
  
   - Verwenden Sie das Cmdlet **Get-SPServiceApplication** in Windows PowerShell, die mit SharePoint 2013 installiert ist. Wählen Sie auf der Taskleiste im **Startmenü** **Alle Programme**, wählen Sie **Microsoft SharePoint 2013-Produkte**, und wählen Sie dann auf **SharePoint 2013-Verwaltungsshell**. Es folgt der Befehl und die Ergebnisse im Fenster **SharePoint 2013get-Verwaltungsshell** für die definierten dienstanwendungen (Ihre GUIDs werden). Kopieren Sie die GUID für die Project Server-Anwendung. 
    
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

      Wenn Sie den vollständigen Namen der Project Server-Anwendung kennen, können Sie es verwenden, beispielsweise den GUID-Wert abgerufen:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Entfernen der Striche in der GUID zum Abrufen des Namens des virtuellen Verzeichnisses an. 
  
   URLs wie `http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` standard für Project Server-Dienste sind. 
    
4. Nachdem Sie der Dienstverweis aufgelöst wird, geben Sie den Verweisnamen in das Textfeld **Namespace** . Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden den Namespacenamen beliebige **Svc _ServiceName_**. Beispielsweise ist der Dienst Ressource in den Codebeispielen **SvcResource**mit dem Namen.
    
    **Abbildung 3. Hinzufügen der WCF-basierten ressourcendienstverweises**

    ![Hinzufügen der WCF-basierten ressourcendienstverweises] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Hinzufügen der WCF-basierten ressourcendienstverweises")
  
5. Ersetzen Sie die temporären web.config-Datei im Verzeichnis Project Service mit dem ursprünglichen (umbenannt zu "Web.config"), und führen Sie `iisreset`.
    
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Project Server-Anwendungen verwenden häufig andere Dienste, wie SharePoint 2013-Webdienste. Wenn andere Dienste oder Verweise erforderlich sind, werden sie in das Codebeispiel aufgeführt.
  
Lokale Referenzen für das Codebeispiel sind in **using** -Anweisungen am oberen Rand des Beispiels aufgeführt. 
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann auf **Verweis hinzufügen**.
    
2. Wählen Sie **Durchsuchen aus**, und wechseln Sie zu dem Speicherort, in dem Sie die Project Server-DLLs gespeichert, die Sie zuvor kopiert. Wählen Sie die DLLs, die Sie möchten, und wählen Sie dann auf **OK**.
    
> [!NOTE]
> Stellen Sie sicher, dass die Versionen der Assembly auf Ihrem Entwicklungscomputer genau auf dem Zielcomputer für Project Server übereinstimmen. 
  
## <a name="adding-a-service-configuration-file"></a>Hinzufügen einer Service-Konfigurationsdatei
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Wenn eine Anwendung programmgesteuert die WCF-Dienste konfiguriert, wird es eine Konfigurationsdatei Service nicht verwendet. Anderenfalls verwendet eine Windows-Anwendung oder ein Konsolenanwendungsprojekt **system.serviceModel** -Element in einer app. eine Webanwendung enthält **system.serviceModel** in der Datei web.config. Weitere Informationen zur Verwendung einer App oder die WCF-Dienste Programmgesteuertes Konfigurieren, finden Sie unter [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mithilfe von WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Wenn eine Service Proxy-Quelldatei generiert wird, erstellt der Befehl SvcUtil.exe auch ein output.config-Datei, die die Grundlage für das Default **system.serviceModel** -Element in der App.config.Datei ist oder der Datei web.config. Der Download des Project 2013-SDK enthält eine Beispieldatei output.config in `Documentation\IntelliSense\WCF\Source.zip`. Output.config Standarddatei SvcUtil.exe erstellt, die für die Ressource Service umfasst beispielsweise zwei Bindungen, die mit dem Namen **BasicHttpBinding_Resource** und **BasicHttpBinding_Resource1**. Das **Client** -Element enthält zwei Standardendpunkte. Einen Endpunkt für den sicheren Zugriff auf die HTTP-Adresse auf Port 32843 ist und der andere für den normalen Zugriff auf Port 32843, wie folgt: 
  
```XML
<client>
    <endpoint address="http://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="http://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

PSI-Dienstkonfiguration verwendet nicht die standardmäßige Bindungen und Endpunkte. Projektserver erfordert, dass Anwendungen PSI-Dienste mithilfe der Front-End-ProjectServer.svc zugreifen, die fungiert als Router für Aufrufe an die Back-End-Dienste. Führen Sie die folgenden Schritte aus, um die App zu erstellen:
  
1. Wenn Sie einen Verweis auf die Assembly ProjectServerServices.dll Proxy festgelegt oder die Proxy-Quelldatei für einen Dienst hinzufügen, enthält die Anwendung keine App. Fügen Sie dem Visual Studio-Projekt ein neues Element hinzu. Klicken Sie im Dialogfeld **Neues Element hinzufügen** wählen Sie die Vorlage **Anwendungskonfigurationsdatei** , nennen Sie es app.config, und wählen Sie dann **Hinzufügen**.
    
2. Löschen Sie alle Textabschnitte in der App.config.Datei, und kopieren Sie den folgenden Code in die Datei. Verwenden Sie die gleiche Bindung, beispielsweise `basicHttpConf`, für jeden Dienstendpunkt. Wenn Sie mehr als eine Bindung verwenden möchten muss beispielsweise HTTP- und HTTPS-Protokolle für die Bindung eine Bindung für jedes Protokoll erstellen.
    
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
                                <transport clientCredentialType="Ntlm" realm="http://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="http://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Ersetzen Sie `ServerName/ProjectServerName` Endpunktadresse Client mit dem Namen des Servers und Project Web App-Instanz. 
    
4. Ersetzen Sie `ServiceName` mit dem Namen des Diensts PSI wie Ressource. Stellen Sie sicher, dass Sie alle drei Instanzen der Dienstname, beispielsweise ersetzen:
    
    ```XML
        <endpoint address="http://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Um mehr als eine PSI-Dienst verwenden, erstellen Sie ein **Endpunkt** -Element für jeden Dienst und für jede **Bindung** -Element, das-Dienst verwendet wird. Beispielsweise konfigurieren die folgenden Endpunkte des Clients, um die grundlegende HTTP-Bindung für den Project-Dienst und den QueueSystem-Dienst zu verwenden. 
    
    > [!NOTE]
    > Wenn Sie eine Anwendung ausführen und eine Fehlermeldung, dass der Server ausgelastet ist oder die HTTP-Anforderung durch nicht autorisierte ist, stellen Sie sicher, dass die Endpunktadressen in der App.config.Datei richtig sind. 
  
    ```XML
        <client>
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Sie können eine App bearbeiten, mit dem **WCF-Dienstkonfigurations-Editors** in Visual Studio (Menü **Extras** ). Abbildung 4 zeigt, wie das **Vertrag** -Element im Dialogfeld **Microsoft-Dienstkonfigurations-Editors** festgelegt. Wenn die Lösung die Assembly der PSI-Proxy verwendet wird, öffnen Sie ProjectServerServices.dll in die `bin\debug` Verzeichnis von Visual Studio-Lösung. Das Dialogfeld **Contract Type Browser** zeigt alle WCF Service-Verträge (siehe Abbildung 5). 
  
**Abbildung 4. Mithilfe der WCF-Dienstkonfigurations-Editors**

![Mithilfe der WCF-Dienstkonfigurations-Editors] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Mithilfe der WCF-Dienstkonfigurations-Editors")
  
Wenn die Lösung eine Service Proxy-Datei, z. B. wcfResource.cs verwendet, kompilieren Sie die Anwendung, und öffnen Sie die ausführbare Datei in die `bin\debug` Directory. Weitere Informationen zum Bearbeiten der Datei ' App.config ' finden Sie unter [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mithilfe von WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Abbildung 5. Verwenden des Contract Type Browsers in der WCF-Dienstkonfigurations-Editors**

![Verwenden des Contract Type Browser] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Verwenden des Contract Type Browser")
  
## <a name="using-multiple-authentication"></a>Verwenden mehrere Authentifizierungsmethoden
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Die Authentifizierung des lokalen Project Server-Benutzer, erfolgt durch Windows-Authentifizierung oder Formularauthentifizierung über Claims processing in SharePoint. Mehrere Authentifizierungsmethoden bedeutet, dass die Webanwendung, die auf der Project Web App bereitgestellt wird Windows-Authentifizierung und formularbasierte Authentifizierung unterstützt. Wenn dies der Fall ist, wird jeder Aufruf eines WCF-Diensts, das die Windows-Authentifizierung verwendet die folgende Fehler auftreten, da der Ansprüche Prozess die Bestimmung des Typs des Benutzers zum authentifizieren kann nicht:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Zur Behebung des Problems für WCF sollten alle Aufrufe von PSI-Methoden innerhalb einer **OperationContextScope** befinden, die für jeden Dienst PSI definiert ist. Schachteln Sie Bereiche für mehrere Dienste nicht; Wenn Sie Anrufe an die Ressourcen und Project-Dienste verwenden möchten, sollte jeder Gruppe von Anrufen innerhalb seines eigenen Bereichs sein. 
  
Im folgenden Beispiel kann aus jeder Abschnitt **OperationContextScope** in einer Anwendung die **DisableFormsAuth** -Methode aufgerufen werden. Die Methode entfernt alle Header-Wert, die Formularauthentifizierung zuvor deaktiviert, damit die Formularauthentifizierung fortgesetzt werden kann, wenn der Parameter _IsWindowsAuth_ **false ist**. Wenn _IsWindowsAuth_ auf **true**festgelegt ist, wird die Methode **DisableFormsAuth** formularbasierte Authentifizierung deaktiviert. 
  
In der **WcfSample** -Methode ist das **ProjectClient** -Objekt eine Instanz der PSI- **SvcProject.ProjectClient** -Klasse. 
  
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
> PSI-Aufrufe innerhalb einer **OperationContextScope** ist nur für Anwendungen, die in einer Umgebung mit mehreren Authentifizierung ausgeführt erforderlich. Wenn in Project Server nur Windows-Authentifizierung verwendet wird, ist es nicht erforderlich sind, um einen Bereich festgelegt, und fügen einen Web-Anforderungsheader, der formularbasierte Authentifizierung deaktiviert. 
> 
> Die Fehlerbehebung für eine ASMX-basierte Anwendung ist unterschiedlich. Weitere Informationen finden Sie im Abschnitt " *Using Authentifizierungen* " in [erforderliche Komponenten für ASMX-basierte Codebeispiele im Projekt](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Ändern der Werte der generische-Konstanten
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

Die meisten Beispiele haben eine oder mehrere Variablen, die Sie für das Beispiel funktioniert ordnungsgemäß in Ihrer Umgebung aktualisieren müssen. Im folgenden Beispiel wenn Sie SSL installiert haben, verwenden Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen Sie _ServerName_ mit dem Namen des Servers, den Sie verwenden. Ersetzen Sie _ProjectServerName_ durch den Namen des virtuellen Verzeichnisses Ihrer Project Server-Website, wie etwa PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, sind am Anfang des Codebeispiels aufgeführt.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Abrufen und ein Codebeispiel Ergebnisse interpretieren ist nicht immer einfach. Angenommen, wenn Sie ein Projekt erstellt haben, müssen Sie das Projekt veröffentlichen, bevor es auf der Seite Project Center in Project Web App angezeigt werden kann.
  
Sie können beispielsweise Code Beispielergebnisse auf verschiedene Weise überprüfen:
  
- Verwenden Sie den Project Professional 2013 Client, um das Projekt vom Project Server-Computer zu öffnen, und zeigen Sie die gewünschten Elemente.
    
- Veröffentlichte Projekte anzuzeigen, die auf der Seite Projektcenter von Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Anzeigen des Protokolls Warteschlange in Project Web App. Öffnen Sie die Seite servereinstellungen (Wählen Sie das Symbol **Einstellungen** in der oberen rechten Ecke), und wählen Sie dann im Abschnitt **Persönliche Einstellungen** **Eigene Warteschlangenaufträge** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). In der Dropdown-Liste **Ansicht** können Sie nach der Auftragsstatus sortiert werden. Die Standardstatus ist **In Bearbeitung und Fehler bei der Aufträge in der letzten Woche**. 
    
- Verwenden die Seite servereinstellungen in Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) alle Warteschlangenaufträge verwalten und löschen oder Erzwingen des Eincheckens von Enterprise-Objekten. Sie benötigen Administratorberechtigungen auf diese Links auf der Seite servereinstellungen zugreifen.
    
- Verwenden Sie **Microsoft SQL Server Management Studio** , um eine Abfrage in einer Tabelle mit einer Project Server-Datenbank auszuführen. Verwenden Sie beispielsweise die folgende Abfrage aus, um die obersten 200 Zeilen der Tabelle zum Anzeigen von Informationen zu den Projektdetailseiten (PDPs) in Workflowstufen MSP_WORKFLOW_STAGE_PDPS auszuwählen. 
    
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

## <a name="cleaning-up"></a>Bereinigen
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Nachdem Sie einige Codebeispiele testen, gibt es Enterprise-Objekte und Einstellungen, die gelöscht oder zurückgesetzt werden sollte. Sie können die Seite servereinstellungen in Project Web App verwenden, zum Verwalten von Enterprise-Daten ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Links auf der Seite servereinstellungen können Sie alte Elemente löschen, Projekte Einchecken erzwingen, Verwalten der Auftragswarteschlange für alle Benutzer und andere administrativen Aufgaben ausführen.
  
Es folgen einige der Links auf der Seite servereinstellungen für typische Bereinigungen verwenden Sie nach dem Ausführen der Codebeispiele:
  
- **Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**
    
- **Verwalten von Warteschlangenaufträgen**
    
- **Enterprise-Objekte löschen**
    
- **Einchecken von Enterprise-Objekten erzwingen**
    
- **Enterprise-Projekttypen**
    
- **Workflowphasen**
    
- **Workflowstufen**
    
- **Projektdetailseiten**
    
- **Zeiträume für Zeitberichte**
    
- **Einstellungen und Standardwerte in der**
    
- **Zeilenklassifizierungen**
    
Zusätzliche Einstellungen werden von SharePoint Server 2013 für jede Project Web App-Instanz und nicht von einer bestimmten Seite Project Web App-servereinstellungen verwaltet. Wählen Sie in der Anwendung der SharePoint-Zentraladministration **Allgemeine Anwendungseinstellungen**, wählen Sie **Verwalten** unter **Project Server-Einstellungen**, und wählen Sie dann die Project Web App-Instanz in der Dropdown-Liste auf der Seite servereinstellungen . Wählen Sie beispielsweise **Serverseitige Ereignishandler** hinzufügen oder Löschen von Ereignishandlern für die ausgewählte Project Web App-Instanz. 
  
## <a name="see-also"></a>Siehe auch

- [Voraussetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mithilfe von WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Verwenden des Identitätswechsels mit WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Übersicht über Project PSI-Verweis](project-psi-reference-overview.md) 
- [SharePoint Developer Center](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

