---
title: Voraussetzungen für ASMX-basierte Codebeispiele in Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- Codebeispiele, Project Server, Project Server, Programmierung,PSI, Kompilieren von Codebeispielen,PSI, Programmierung
ms.localizationpriority: medium
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Hier erhalten Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen zur Project Serverschnittstelle (PSI) enthalten sind.
ms.openlocfilehash: c3a5787933bd7dfb3826422e276421844069a770
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619232"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Voraussetzungen für ASMX-basierte Codebeispiele in Project

Hier erhalten Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen zur Project Serverschnittstelle (PSI) enthalten sind.
  
Viele der Codebeispiele, die in der [Project Server 2013-Klassenbibliothek und -Webdienstreferenz](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) enthalten sind, wurden ursprünglich für das Office Project 2007 SDK erstellt und verwenden ein Standardformat für ASMX-Webdienste. Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden. Ausnahmen sind im Beispiel aufgeführt. 
  
Neue PSI-Beispiele im Project 2013 SDK entsprechen einem Format, das Windows Communication Foundation (WCF)-Dienste verwendet. Die ASMX-basierten Beispiele können auch für die Verwendung von WCF-Diensten angepasst werden. In diesem Artikel wird gezeigt, wie Sie die Beispiele mit ASMX-Webdiensten verwenden. Informationen zur Verwendung der Beispiele mit WCF-Diensten finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 zwar veraltet, wird aber weiterhin unterstützt. Wenn das clientseitige Objektmodell (CSOM) die Methoden enthält, die Ihre Anwendung benötigt, sollten neue Anwendungen mit dem CSOM entwickelt werden. Mit dem CSOM können Anwendungen mit Project Online oder einer lokalen Installation von Project Server 2013 arbeiten. Wenn Ihre Anwendung die PSI verwendet, sollte sie andernfalls die WCF-Schnittstelle verwenden. Dies ist die Technologie, die für die Netzwerkkommunikation empfohlen wird. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 verwendet werden. Weitere Informationen zum CSOM finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md) und [clientseitiges Objektmodell (CSOM) für Project 2013.](client-side-object-model-csom-for-project-2013.md) 
  
Bevor Sie die Codebeispiele ausführen, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren und generische Konstantenwerte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Richten Sie einen Test Project Serversystem** ein.
    
   Verwenden Sie beim Entwickeln oder Testen ein Test Project Serversystem. Selbst wenn Ihr Code einwandfrei funktioniert, können Abhängigkeiten zwischen Projekten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Folgen haben. 
    
   > [!NOTE]
   > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die PSI-Aufrufe verfügen, die Ihre Anwendung verwendet. Das Referenzthema für jede PSI-Methode enthält eine Project Serverberechtigungstabelle. Beispielsweise die [Project. Die QueueCreateProject-Methode](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) erfordert die globale **NewProject-Berechtigung** und die **SaveProjectTemplate-Berechtigung.** 
  
   In einigen Fällen müssen Sie möglicherweise Remotedebugging auf dem Server ausführen. Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie eine Ereignishandlerassembly auf jedem Project Servercomputer in der SharePoint Farm installieren und dann den Ereignishandler für die Project Web App-Instanz konfigurieren, indem Sie die Seite Project Server Einstellungen in der Einstellungen der SharePoint Zentraladministration verwenden.
    
2. **Richten Sie einen Entwicklungscomputer ein.**
    
   Normalerweise greifen Sie über ein Netzwerk auf die PSI zu. Die Codebeispiele sind so konzipiert, dass sie auf einem Vom Server getrennten Client ausgeführt werden, sofern nicht anders angegeben.
    
   1. **Installieren Sie die richtige Version von Visual Studio.** Sofern nicht anders angegeben, werden die Codebeispiele in Visual C# geschrieben. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass Sie das neueste Service Pack installiert haben. 
        
   2. **Kopieren Sie Project Server-DLLs auf den Entwicklungscomputer.** Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` vom Project Servercomputer auf den Entwicklungscomputer: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Informationen zum Kompilieren und Verwenden der ProjectServerServices.dll-Proxyassembly für die ASMX-Webdienste in der PSI finden Sie unter [Verwenden einer PSI-Proxyassembly und IntelliSense-Beschreibungen.](#pj15_PrerequisitesASMX_BuildingProxy)
    
3. **Installieren Sie die IntelliSense-Dateien.**
    
    Um IntelliSense-Beschreibungen für Klassen und Member in Project Serverassemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013 SDK-Download in das verzeichnis, in dem sich die Project Serverassemblys befinden. Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml-Datei in das Verzeichnis, in dem ihre Anwendung einen Verweis auf die Microsoft.Office.Project.Server.Library.dll assembly festlegen wird.
    
    IntelliSense-Beschreibungen für die PSI-Webdienste erfordern, dass Sie eine PSI-Proxyassembly mithilfe des Skripts CompileASMXProxyAssembly.cmd im `Documentation\IntelliSense\WSDL` Unterverzeichnis im Project 2013 SDK-Download erstellen. Das Skript erstellt die ASMX-basierte ProjectServerServices.dll Proxyassembly. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im SDK-Download. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Erstellen der Anwendung und Hinzufügen eines Webdienstverweises
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Erstellen Sie eine Konsolenanwendung.**
    
   Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds **"Neu Project"** **.NET Framework 4** aus. Sie können den PSI-Beispielcode in die neue Anwendung kopieren.
    
2. **Fügen Sie den für ASMX erforderlichen Verweis hinzu.**
    
   Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.Web.Services** hinzu (siehe Abbildung 1). 
    
   **Abbildung 1. Hinzufügen eines Verweises in Visual Studio**

   ![Hinzufügen eines Verweises in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Hinzufügen eines Verweises in Visual Studio")
  
3. **Kopieren Sie den Code.**
    
   Kopieren Sie das vollständige Codebeispiel in die Datei "Program.cs" der Konsolenanwendung.
    
4. **Legen Sie den Namespace für die Beispielanwendung** fest.
    
   Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standardanwendungsnamespace so ändern, dass er dem Beispiel entspricht. Sie können den Standardanwendungsnamespace ändern, indem Sie die Anwendungseigenschaften ändern.
    
   Beispielsweise weist das Codebeispiel für [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) den Namespace **"Microsoft.SDK.Project" auf. Samples.RenameProject**. Wenn der Name des Visual Studio Projekts **RenameProject** lautet, kopieren Sie den Namespace aus der Datei Program.cs, und öffnen Sie dann den Bereich **Projekteigenschaften** (wählen Sie im Menü **Project** **Eigenschaften RenameProject**). Kopieren Sie den Namespace auf der Registerkarte **"Anwendung"** in das Textfeld **"Standardnamespace".** 
    
5. **Legen Sie die Webverweise fest.**
    
   Die meisten Beispiele erfordern einen Verweis auf einen oder mehrere psi-Webdienste. Diese werden im Beispiel selbst oder in Kommentaren aufgeführt, die vor dem Beispiel stehen. Um den richtigen Namespace der Webverweise abzurufen, stellen Sie sicher, dass Sie zuerst den Standardanwendungsnamespace festlegen.
    
   Es gibt drei Möglichkeiten, einen ASMX-Webdienstverweis für die PSI hinzuzufügen:
    
   - Erstellen Sie eine PSI-Proxyassembly mit dem Namen ProjectServerServices.dll, und legen Sie dann einen Verweis auf die Assembly fest. Zum Abrufen von IntelliSense ist dies die empfohlene Methode zum Hinzufügen eines PSI-Verweises. Weitere Informationen finden Sie [unter Verwenden einer PSI-Proxyassembly und IntelliSense-Beschreibungen.](#pj15_PrerequisitesASMX_BuildingProxy)
    
   - Fügen Sie der Visual Studio Lösung eine Proxydatei aus der wsdl.exe-Ausgabe hinzu. Siehe [Hinzufügen einer PSI-Proxydatei.](#pj15_PrerequisitesASMX_AddingProxyFile)
    
   - Fügen Sie einen Webdienstverweis mithilfe von Visual Studio hinzu. Weitere Informationen finden [Sie unter Hinzufügen eines Webdienstverweises.](#pj15_PrerequisitesASMX_AddingServiceReference)

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxyassembly und IntelliSense-Beschreibungen

Sie können die ProjectServerServices.dll Proxyassembly für alle ASMX-basierten Webdienste in der PSI erstellen und verwenden, indem Sie das Skript CompileASMXProxyAssembly.cmd im `Documentation\IntelliSense\WSDL` Ordner des Project 2013 SDK-Downloads verwenden. Einen Link zum Download finden Sie in der [Project 2013-Entwicklerdokumentation.](project-2013-developer-documentation.md)
  
> [!NOTE]
> Wenn Sie die Proxyquelldateien aus der datei Source.zip extrahieren, sind die Dateien im `Documentation\IntelliSense\WSDL\Source` Ordner ab dem Veröffentlichungsdatum des Project 2013 SDK-Downloads aktuell. Um aktualisierte PSI-Proxyquelldateien zu generieren, führen Sie das Skript "GenASMXProxyAssembly.cmd" auf dem Project Servercomputer aus. Die Skripts im  `Documentation\IntelliSense\WCF` Ordner funktionieren nicht für ASMX-basierte Anwendungen. Das Skript "GenWCFProxyAssembly.cmd" ruft SvcUtil.exe auf, das Quellcodedateien für die WCF-Dienste generiert. Die WCF-Proxydateien enthalten unterschiedliche Attribute, die Kanalschnittstelle und eine Clientklasse für jeden PSI-Dienst. Beispielsweise enthält der WCF-basierte Ressourcendienst die **ResourceChannel-Schnittstelle,** die **Resource-Schnittstelle** und die **ResourceClient-Klasse.** Das ASMX-basierte Ressourcenweb enthält die **Resource-Klasse** mit einigen unterschiedlichen Eigenschaften. 
  
Es folgt das Skript "GenASMXProxyAssembly.cmd", das WSDL-Ausgabedateien für die PSI-Webdienste generiert und dann die Assembly kompiliert.
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

Das Skript verwendet die datei ClassList_asmx.txt, die die Liste der Webdienste enthält, die für Drittanbieterentwickler verfügbar sind.
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

Die Skripts erstellen eine Assembly mit dem Namen ProjectServerServices.dll. Vermeiden Sie verwirrungen sie mit ProjectServerServices.dll für die WCF-basierte Assembly. Die Assemblynamen sind identisch, um die Verwendung einer Assembly mit der ProjectServerServices.xml IntelliSense-Datei zu ermöglichen.
  
Der von den Skripts für die ASMX-Webdienste und die WCF-Dienste erstellte beliebige Namespace ist identisch, sodass die ProjectServerServices.xml IntelliSense-Datei mit beiden Assemblys funktioniert. Beispielsweise ist der Namespace des Ressourcendiensts in der WCF-basierten Proxyassembly und in der ASMX-basierten Proxyassembly **SvcResource**. Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass sie in der Proxyassembly und in der ProjectServerServices.xml IntelliSense-Datei übereinstimmen.
  
Wenn in einem Codebeispiel ein anderer Name für einen PSI-Webdienstnamespace verwendet wird, z. B. **ProjectWebSvc,** müssen Sie für IntelliSense das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace mit der Proxyassembly übereinstimmt. 
  
Ein Vorteil bei der Verwendung der ASMX-basierten Proxyassembly besteht darin, dass sie alle PSI-Webdienstnamespaces enthält. Sie müssen nicht mehrere Webverweise erstellen. Ein weiterer Vorteil besteht darin, dass Sie intelliSense-Beschreibungen für die PSI-Klassen und -Member abrufen können, wenn Sie die ProjectServerServices.xml-Datei demselben Verzeichnis hinzufügen, in dem Sie einen Verweis auf die ProjectServerServices.dll Proxyassembly festlegen. Abbildung 2 zeigt den IntelliSense-Text für die **Project. QueueCreateProject-Methode.** Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im IntelliSense-Ordner des Project 2013 SDK-Downloads. 
  
**Abbildung 2. Verwenden von IntelliSense für eine Methode im Project Webdienst**

![Verwenden von Intellisense für eine Methode in einem PSI-Dienst](media/pj15_PrerequisitesASMX_Intellisense.gif "Verwenden von Intellisense für eine Methode in einem PSI-Dienst")
  
Nachteile der Verwendung der Proxyassembly sind, dass die Lösung größer ist und Sie die Proxyassembly mit der Lösung verteilen und installieren müssen. Sie müssen auch dieselben Namespaces verwenden, die sich in der Proxyassembly und intelliSense-Dateien befinden, es sei denn, Sie ändern das Skript und ProjectServerServices.xml IntelliSense-Datei, um unterschiedliche Namespaces zu verwenden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxydatei
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Der Project 2013 SDK-Download enthält die Quelldateien, die vom befehl Wsdl.exe für die Proxyassembly generiert wurden. Die Quelldateien befinden sich in Source.zip im  `Documentation\IntelliSense\ASMX` Unterverzeichnis. Anstatt einen Verweis auf die Proxyassembly festzulegen, können Sie einer Visual Studio Lösung eine oder mehrere Quelldateien hinzufügen. Fügen Sie beispielsweise nach dem Ausführen des Skripts "GenASMXProxyAssembly.cmd" die wsdl hinzu. Project.cs-Datei an die Lösung an. Anstatt das Skript auszuführen, können Sie die folgenden Befehle ausführen, um z. B. eine einzelne Quelldatei zu generieren: 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Verwenden Sie den folgenden Code, um ein **Project-Objekt** als Klassenvariable mit dem Namen **"Projekt"** zu definieren. Die **AddContextInfo-Methode** fügt dem **Projektobjekt** die Kontextinformationen für Windows Authentifizierung und formularbasierte Authentifizierung hinzu. 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> Unabhängig davon, ob Sie eine PSI-Proxyassembly verwenden oder eine Proxydatei für einen Project Dienstverweis namens **SvcProject** hinzufügen, verwenden Sie denselben Code, um ein **Projektobjekt** zu erstellen. 
  
### <a name="adding-a-web-service-reference"></a>Hinzufügen eines Webdienstverweises
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Wenn Sie die ASMX-basierte Proxyassembly nicht verwenden oder eine WSDL-Ausgabedatei hinzufügen, können Sie einen oder mehrere einzelne Webverweise festlegen. Die folgenden Schritte zeigen, wie Sie einen Webverweis mithilfe von Visual Studio 2012 festlegen.
  
1. Klicken Sie **im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **"Verweise",** und wählen Sie dann **Dienstverweis hinzufügen** aus. 
    
2. Wählen Sie im Dialogfeld **Dienstverweis hinzufügen** die Option **"Erweitert"** aus.
    
3. Wählen Sie im Dialogfeld **"Dienstverweis Einstellungen"** die Option **Webverweis hinzufügen** aus.
    
4. Geben Sie im **Textfeld "URL"** `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` die **EINGABETASTE** ein, oder wählen Sie das Symbol **"Los"** aus. Wenn Secure Sockets Layer (SSL) installiert ist, sollten Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls verwenden. 

   Verwenden Sie beispielsweise die folgende URL für den Project-Dienst auf der `https://MyServer/pwa` Website für Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Oder öffnen Sie Ihren Webbrowser, und navigieren Sie zu `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` . Speichern Sie die Datei in einem lokalen Verzeichnis, `C:\Project\WebServices\ServiceName.wsdl` z. B. . Geben Sie im Dialogfeld **"Webverweis hinzufügen"** für die **URL** das Dateiprotokoll und den Pfad zu der Datei ein. Geben Sie beispielsweise `file://C:\Project\WebServices\Project.wsdl` . 
    
5. Geben Sie nach der Auflösung des Verweises den Verweisnamen in das Textfeld für den **Webverweisnamen** ein. Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden den beliebigen Standardverweisnamen **Svc _ServiceName._** Der Project Webdienst heißt z. **B. "SvcProject"** (siehe Abbildung 3). 
    
   **Abbildung 3. Hinzufügen eines ASMX-Webdienstverweises**

   ![Hinzufügen eines ASMX-Webdienstverweises](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Hinzufügen eines ASMX-Webdienstverweises")
  
Verwenden Sie für Anwendungskomponenten, die auf dem Project Servercomputer ausgeführt werden müssen, den Identitätswechsel verwenden oder über erhöhte Berechtigungen verfügen, einen WCF-Dienstverweis anstelle eines ASMX-Webverweises. Weitere Informationen finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Serveranwendungen verwenden häufig andere Dienste, z. B. SharePoint Server 2013-Webdienste. Wenn andere Dienste erforderlich sind, werden sie im Beispiel angegeben.
  
Lokale Verweise für das Codebeispiel werden in **using-Anweisungen** oben im Beispiel aufgelistet: 
  
1. Klicken Sie **im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **"Verweise",** und wählen Sie dann **Verweis hinzufügen** aus.
    
2. Wählen Sie **"Durchsuchen"** aus, und navigieren Sie dann zu dem Speicherort, an dem Sie die zuvor kopierten Project Server-DLLs gespeichert haben. Wählen Sie die benötigten DLLs aus, und klicken Sie dann auf **OK.**
    
> [!NOTE]
> Stellen Sie sicher, dass die Assemblyversionen auf dem Entwicklungscomputer exakt mit denen auf dem Zielcomputer Project Servers übereinstimmen. 
  
## <a name="using-multiple-authentication"></a>Verwenden mehrerer Authentifizierungen
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Die Authentifizierung von lokalen Project Serverbenutzern, sei es durch Windows Authentifizierung oder Formularauthentifizierung, erfolgt über die Anspruchsverarbeitung in SharePoint Server 2013. Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication. Wenn dies der Fall ist, schlägt ein Aufruf eines ASMX-Webdiensts, der Windows Authentifizierung verwendet, mit dem folgenden Fehler fehl, da der Anspruchsprozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:
  
`The server was unable to process the request due to an internal error. . . .`

Um das Problem für ASMX zu beheben, sollten alle Aufrufe von PSI-Methoden an eine abgeleitete Klasse erfolgen, die für jeden PSI-Webdienst definiert ist. Die abgeleitete Klasse muss auch die **SvcLoginWindows.LoginWindows-Klasse** verwenden, um ein Cookie für die abgeleitete PSI-Dienstklasse abzurufen. Im folgenden Beispiel wird die **ProjectDerived-Klasse** von der **SvcProject.Project-Klasse** abgeleitet. Die abgeleitete Klasse fügt die **EnforceWindowsAuth-Eigenschaft** hinzu und überschreibt den Webanforderungsheader für jeden Aufruf einer Methode in der **Project** Klasse. Wenn die **EnforceWindowsAuth-Eigenschaft** **"true"** ist, fügt die **GetWebRequest-Methode** einen Header hinzu, der die Formularauthentifizierung deaktiviert. Wenn **EnforceWindowsAuth** **auf "false"** festgelegt ist, kann die Formularauthentifizierung fortgesetzt werden.
  
Um das folgende **ASMXLogon_MultiAuth** Beispiel zu verwenden, erstellen Sie eine Konsolenanwendung, führen Sie die Schritte unter [Erstellen der Anwendung und Hinzufügen eines Webdienstverweises](#pj15_PrerequisitesASMX_Configure)aus, und fügen Sie dann die wsdl hinzu. LoginWindows.cs-Proxydatei und die wsdl. Project.cs-Proxydatei. Die **Main-Methode** erstellt die **Projektinstanz** der **ProjectDerived-Klasse.** Im Beispiel muss die **abgeleitete LoginWindowsDerived-Klasse** verwendet werden, um ein **CookieContainer-Objekt** für das **Projekt abzurufen. CookieContainer-Eigenschaft,** die die Formularauthentifizierung von Windows Authentifizierung unterscheidet. Das **Projektobjekt** kann dann zum Aufrufen einer beliebigen Methode in der **Klasse "SvcProject.Project"** verwendet werden. 
  
> [!NOTE]
> Der **LoginWindows-Dienst** ist nur für ASMX-Anwendungen in einer Umgebung mit mehreren Authentifizierungen erforderlich. Im **ASMXLogon_MultiAuth** Beispiel ruft die **GetLogonCookie-Methode** ein Cookie für das **loginWindows-Objekt** ab. Das **Projekt. Die CookieContainer-Eigenschaft** ist auf den **LoginWindows.CookieContainer-Wert** festgelegt. 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

Die Verwendung der **abgeleiteten LoginWindows-Klasse** und das Ausführen von PSI-Aufrufen mit einem Webanforderungsheader, der die Formularauthentifizierung deaktiviert, ist für Anwendungen erforderlich, die in einer Umgebung mit mehreren Authentifizierungen ausgeführt werden. Wenn Project Server nur die Anspruchsauthentifizierung verwendet, ist es nicht erforderlich, eine Klasse abzuleiten, die einen Webanforderungsheader hinzufügt. Das vorherige Beispiel wird in beiden Umgebungen ausgeführt. 
  
Die Korrektur für eine WCF-basierte Anwendung unterscheidet sich. Weitere Informationen finden Sie im Abschnitt *"Verwenden mehrerer Authentifizierungen"* unter ["Voraussetzungen für WCF-basierte Codebeispiele" in Project.](prerequisites-for-wcf-based-code-samples-in-project.md)
  
## <a name="changing-the-values-of-generic-constants"></a>Ändern der Werte generischer Konstanten
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

Die meisten Beispiele verfügen über eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel ordnungsgemäß in Ihrer Umgebung funktioniert. Wenn Sie im folgenden Beispiel SSL installiert haben, verwenden Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen Sie  _ServerName_ durch den Namen des servers, den Sie verwenden. Ersetzen Sie _ProjectServerName_ durch den namen des virtuellen Verzeichnisses Ihrer Project Serverwebsite, z. B. PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, oder andere Voraussetzungen werden oben im Codebeispiel aufgeführt.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Das Abrufen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach. Wenn Sie z. B. ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Project Center-Seite in Project Web App angezeigt werden kann.
  
Sie können Codebeispielergebnisse auf verschiedene Arten überprüfen, z. B.:
  
- Verwenden Sie den Project Professional 2013-Client, um das Projekt auf dem Project Servercomputer zu öffnen und die gewünschten Elemente anzuzeigen.
    
- Anzeigen veröffentlichter Projekte auf der Project Center-Seite von Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Zeigen Sie das Warteschlangenprotokoll in Project Web App an. Öffnen Sie die Seite "Server Einstellungen" (klicken Sie in der oberen rechten Ecke auf das **Symbol Einstellungen),** und wählen Sie dann **"Meine Aufträge in der Warteschlange"** im Abschnitt **"Personal Einstellungen"** `https://ServerName/ProjectServerName/MyJobs.aspx` (). In  der Dropdownliste Ansicht können Sie nach dem Auftragsstatus sortieren. Der Standardstatus ist **In Bearbeitung und Fehlgeschlagene Aufträge in der letzten Woche.** 
    
- Verwenden Sie die Seite "Server Einstellungen" in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ), um alle Warteschlangenaufträge zu verwalten und das Einchecken von Unternehmensobjekten zu löschen oder zu erzwingen. Sie müssen über Administratorberechtigungen verfügen, um auf diese Links auf der Seite "Server Einstellungen" zugreifen zu können.
    
- Verwenden Sie **Microsoft SQL Server Management Studio,** um eine Abfrage für eine Tabelle in der Project Datenbank auszuführen. Verwenden Sie beispielsweise die folgende Abfrage, um die 200 obersten Zeilen des Pubs auszuwählen. MSP_WORKFLOW_STAGE_PDPS Tabelle, in der Informationen zu den Projektdetailseiten (Project Detail Pages, PDPs) in Workflowphasen angezeigt werden. 
    
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
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

Nachdem Sie einige Codebeispiele getestet haben, gibt es Enterprise-Objekte und -Einstellungen, die gelöscht oder zurückgesetzt werden sollten. Sie können die Seite "Server Einstellungen" in Project Web App verwenden, um Unternehmensdaten ( ) zu `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` verwalten. Links auf der Seite "Server Einstellungen" ermöglichen es Ihnen, alte Elemente zu löschen, Eincheckprojekte zu erzwingen, die Auftragswarteschlange für alle Benutzer zu verwalten und andere administrative Aufgaben auszuführen.
  
Im Folgenden finden Sie einige Links auf der Seite "Server Einstellungen", die Sie nach dem Ausführen von Codebeispielen für typische Bereinigungsaktivitäten verwenden können:
  
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
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Verwenden des Identitätswechsels mit WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md)
- [SharePoint Developer Center](https://msdn.microsoft.com/sharepoint/default.aspx)
    

