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
- Codebeispiele, Projektserver,Project Server, Programmierung, PSI, Kompilieren von Codebeispielen,PSI, Programmierung
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen Project Server Interface (PSI) enthalten sind.
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357083"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Voraussetzungen für ASMX-basierte Codebeispiele in Project

Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen Project Server Interface (PSI) enthalten sind.
  
Viele der Codebeispiele in der klassenbibliotheks- und webdienstreferenz von [Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) wurden ursprünglich für das Office Project 2007 SDK erstellt und verwenden ein Standardformat für ASMX-Webdienste. Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden. Ausnahmen werden im Beispiel erwähnt. 
  
Neue PSI-Beispiele im Project 2013 SDK entsprechen einem Format, das Windows Communication Foundation (WCF)-Dienste verwendet. Die ASMX-basierten Beispiele können auch für die Verwendung von WCF-Diensten angepasst werden. In diesem Artikel wird gezeigt, wie Sie die Beispiele mit ASMX-Webdiensten verwenden. Informationen zur Verwendung der Beispiele mit WCF-Diensten finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 zwar veraltet, wird aber weiterhin unterstützt. Wenn das clientseitige Objektmodell (CSOM) die von Ihrer Anwendung benötigten Methoden enthält, sollten neue Anwendungen mit dem CSOM entwickelt werden. Mit dem CSOM können Anwendungen mit Project Online oder einer lokalen Installation von Project Server 2013 arbeiten. Wenn Ihre Anwendung andernfalls die PSI verwendet, sollte sie die WCF-Schnittstelle verwenden, die Technologie, die wir für die Netzwerkkommunikation empfehlen. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 verwendet werden. Weitere Informationen zum CSOM finden Sie [unter Project Server 2013](project-server-2013-architecture.md) architecture and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Bevor Sie die Codebeispiele ausführen, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren und generische Konstantenwerte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Richten Sie einen Test Project Serversystem ein.**
    
   Verwenden Sie ein Project Serversystem, wenn Sie entwickeln oder testen. Auch wenn Ihr Code einwandfrei funktioniert, können Abhängigkeiten zwischen Projekten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Folgen haben. 
    
   > [!NOTE]
   > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die von Ihrer Anwendung verwendeten PSI-Aufrufe verfügen. Das Referenzthema für jede PSI-Methode enthält eine Project Server Permissions-Tabelle. Beispielsweise wird [Project. Die QueueCreateProject-Methode](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) erfordert die globale **NewProject-Berechtigung** und **die SaveProjectTemplate-Berechtigung.** 
  
   In einigen Fällen müssen Sie möglicherweise remote debuggen auf dem Server. Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie auf jedem Project Server-Computer in der SharePoint-Farm eine Ereignishandler assembly installieren und dann den Ereignishandler für die Project Web App-Instanz mithilfe der Seite Project Server Einstellungen in der Allgemeinen Anwendung Einstellungen der SharePoint-Zentraladministration konfigurieren.
    
2. **Richten Sie einen Entwicklungscomputer ein.**
    
   In der Regel greifen Sie über ein Netzwerk auf die PSI zu. Die Codebeispiele sind so konzipiert, dass sie auf einem Client ausgeführt werden, der vom Server getrennt ist, sofern nicht angegeben.
    
   1. **Installieren Sie die richtige Version Visual Studio.** Sofern nicht erwähnt, werden die Codebeispiele in Visual C#. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass Das neueste Service Pack installiert ist. 
        
   2. **Kopieren Project Server-DLLs auf den Entwicklungscomputer.** Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` aus Project Servercomputer auf den Entwicklungscomputer: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Informationen zum Kompilieren und Verwenden der ProjectServerServices.dll-Proxy-Assembly für die ASMX-Webdienste in der PSI finden Sie unter [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Installieren Sie die IntelliSense Dateien.**
    
    Um IntelliSense Beschreibungen für Klassen und Mitglieder in Project Serverassemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013-SDK-Download in das Verzeichnis, in dem sich die Project Server-Assemblys befinden. Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml in das Verzeichnis, in dem Ihre Anwendung einen Verweis auf die Assembly Microsoft.Office.Project.Server.Library.dll wird.
    
    IntelliSense Beschreibungen für die PSI-Webdienste erfordern, dass Sie eine PSI-Proxyassembly mithilfe des Skripts CompileASMXProxyAssembly.cmd im Unterverzeichnis im `Documentation\IntelliSense\WSDL` Project 2013 SDK-Download erstellen. Das Skript erstellt die ASMX-basierte ProjectServerServices.dll Proxy-Assembly. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im SDK-Download. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Erstellen der Anwendung und Hinzufügen einer Webdienstreferenz
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Erstellen einer Konsolenanwendung**.
    
   Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds Neue **Project** die Option **.NET Framework 4 aus.** Sie können den PSI-Beispielcode in die neue Anwendung kopieren.
    
2. **Fügen Sie den für ASMX erforderlichen Verweis hinzu.**
    
   Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.Web.Services** hinzu (siehe Abbildung 1). 
    
   **Abbildung 1. Hinzufügen eines Verweises in Visual Studio**

   ![Hinzufügen eines Verweises in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Hinzufügen eines Verweises in Visual Studio")
  
3. **Kopieren Sie den Code**.
    
   Kopieren Sie das vollständige Codebeispiel in die Datei Program.cs der Konsolenanwendung.
    
4. **Legen Sie den Namespace für die Beispielanwendung .**
    
   Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standardanwendungsnamespace so ändern, dass er mit dem Beispiel übereinstimmen kann. Sie können den Standardanwendungsnamespace ändern, indem Sie die Anwendungseigenschaften ändern.
    
   Das Codebeispiel für [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) verfügt beispielsweise über den Namespace **Microsoft.SDK.Project. Samples.RenameProject**. Wenn der Name des Visual Studio-Projekts **RenameProject** ist, kopieren Sie den Namespace aus der  Datei Program.cs, und öffnen Sie dann den Projekteigenschaftenbereich **(wählen** Sie im Menü Project **RenameProject Properties** aus). Kopieren Sie **auf** der Registerkarte Anwendung den Namespace in das Textfeld **Standardnamespace.** 
    
5. **Legen Sie die Webverweise .**
    
   Die meisten Beispiele erfordern einen Verweis auf mindestens einen der PSI-Webdienste. Diese werden im Beispiel selbst oder in Kommentaren vor dem Beispiel aufgeführt. Um den richtigen Namespace der Webverweise zu erhalten, stellen Sie sicher, dass Sie zuerst den Standardanwendungsnamespace festlegen.
    
   Es gibt drei Möglichkeiten, eine ASMX-Webdienstreferenz für die PSI hinzuzufügen:
    
   - Erstellen Sie eine PSI-Proxy assembly namens ProjectServerServices.dll, und legen Sie dann einen Verweis auf die Assembly. Um eine IntelliSense zu erhalten, wird empfohlen, einen PSI-Verweis hinzuzufügen. Weitere Informationen finden Sie unter Using [a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Fügen Sie eine Proxydatei aus der wsdl.exe der Visual Studio hinzu. Weitere [Informationen finden Sie unter Hinzufügen einer PSI-Proxydatei](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Fügen Sie einen Webdienstverweis mithilfe von Visual Studio. Weitere [Informationen finden Sie unter Hinzufügen einer Webdienstreferenz](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxy-Assembly und IntelliSense Beschreibungen

Sie können die ProjectServerServices.dll-Proxyassembly für alle ASMX-basierten Webdienste in der PSI erstellen und verwenden, indem Sie das Skript CompileASMXProxyAssembly.cmd im Ordner des `Documentation\IntelliSense\WSDL` Project 2013 SDK-Downloads verwenden. Einen Link zum Download finden Sie unter [Project 2013 Developer Documentation](project-2013-developer-documentation.md).
  
> [!NOTE]
> Wenn Sie die Proxyquellendateien aus der Source.zip-Datei extrahieren, sind die Dateien im Ordner ab dem Veröffentlichungsdatum des Project `Documentation\IntelliSense\WSDL\Source` 2013 SDK-Downloads aktuell. Führen Sie zum Generieren aktualisierter PSI-Proxyquellendateien das Skript GenASMXProxyAssembly.cmd auf dem Project Server aus. Die Skripts im  `Documentation\IntelliSense\WCF` Ordner funktionieren nicht für ASMX-basierte Anwendungen. Das GenWCFProxyAssembly.cmd-Skript ruft SvcUtil.exe auf, das Quellcodedateien für die WCF-Dienste generiert. Die WCF-Proxydateien enthalten unterschiedliche Attribute, die Kanalschnittstelle und eine Clientklasse für jeden PSI-Dienst. Der WCF-basierte Ressourcendienst umfasst beispielsweise die **ResourceChannel-Schnittstelle,** die **Resource-Schnittstelle** und die **ResourceClient-Klasse.** Das ASMX-basierte Ressourcenweb enthält die **Resource-Klasse** mit einigen verschiedenen Eigenschaften. 
  
Im Folgenden sehen Sie das GenASMXProxyAssembly.cmd-Skript, das WSDL-Ausgabedateien für die PSI-Webdienste generiert und anschließend die Assembly kompiliert.
  
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

Das Skript verwendet die ClassList_asmx.txt-Datei, die die Liste der Webdienste enthält, die für Drittanbieterentwickler verfügbar sind.
  
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

Die Skripts erstellen eine Assembly namens ProjectServerServices.dll. Vermeiden Sie es mit ProjectServerServices.dll für die WCF-basierte Assembly zu verwechseln. Die Assemblynamen sind identisch, um die Verwendung einer assembly mit der ProjectServerServices.xml IntelliSense aktivieren.
  
Der von den Skripts für die ASMX-Webdienste und die WCF-Dienste erstellte beliebige Namespace ist identisch, sodass die ProjectServerServices.xml IntelliSense-Datei mit beiden Assemblys funktioniert. Beispielsweise ist der Namespace des Ressourcendiensts in der WCF-basierten Proxy-Assembly und in der ASMX-basierten Proxy-Assembly **SvcResource**. Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass sie in der Proxy-Assembly und in der ProjectServerServices.xml IntelliSense sind.
  
Wenn in einem Codebeispiel ein anderer Name für einen PSI-Webdienstnamespace verwendet wird, z. B. **ProjectWebSvc** IntelliSense , müssen Sie das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace der Proxy assembly entspricht. 
  
Ein Vorteil bei der Verwendung der ASMX-basierten Proxy-Assembly ist, dass sie alle #A0 enthält. Sie müssen nicht mehrere Webverweise erstellen. Ein weiterer Vorteil: Wenn Sie die ProjectServerServices.xml-Datei demselben Verzeichnis hinzufügen, in dem Sie einen Verweis auf die ProjectServerServices.dll-Proxy assembly festlegen, können Sie IntelliSense Beschreibungen für die PSI-Klassen und -Member erhalten. Abbildung 2 zeigt den IntelliSense text für die **Project. QueueCreateProject-Methode.** Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im ordner IntelliSense des Project 2013 SDK-Downloads. 
  
**Abbildung 2. Verwenden IntelliSense für eine Methode im Project Webdienst**

![Verwenden von Intellisense für eine Methode in einem PSI-Dienst]Verwenden von(media/pj15_PrerequisitesASMX_Intellisense.gif "Intellisense für eine Methode in einem PSI-Dienst")
  
Nachteile bei der Verwendung der Proxy assembly sind, dass die Lösung größer ist und Sie die Proxy assembly mit der Lösung verteilen und installieren müssen. Sie müssen auch die gleichen Namespaces verwenden, die sich in der Proxy assembly und IntelliSense-Dateien befinden, es sei denn, Sie ändern das Skript und die ProjectServerServices.xml IntelliSense-Datei, um unterschiedliche Namespaces zu verwenden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxydatei
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Der Project 2013 SDK-Download enthält die Quelldateien, die durch den Befehl Wsdl.exe für die Proxy assembly generiert werden. Die Quelldateien befinden sich Source.zip im  `Documentation\IntelliSense\ASMX` Unterverzeichnis. Anstatt einen Verweis auf die Proxy assembly zu setzen, können Sie eine oder mehrere Quelldateien zu einer Visual Studio hinzufügen. Fügen Sie beispielsweise nach dem Ausführen des Skripts GenASMXProxyAssembly.cmd das wsdl hinzu. Project.cs-Datei in die Lösung. Anstatt das Skript auszuführen, können Sie die folgenden Befehle ausführen, um eine einzelne Quelldatei zu generieren, z. B.: 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Verwenden Sie den **folgenden Code, um** ein Project als Klassenvariable namens **Project** zu definieren. Die **AddContextInfo-Methode** fügt dem  Projektobjekt die Kontextinformationen für die Windows und formularbasierte Authentifizierung hinzu. 
  
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
> Unabhängig davon, ob Sie eine PSI-Proxy-Assembly verwenden oder eine Proxydatei für einen Project-Dienstverweis namens **SvcProject** hinzufügen, würden Sie denselben Code verwenden, um ein **Projektobjekt zu** erstellen. 
  
### <a name="adding-a-web-service-reference"></a>Hinzufügen einer Webdienstreferenz
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Wenn Sie die ASMX-basierte Proxy-Assembly nicht verwenden oder keine WSDL-Ausgabedatei hinzufügen, können Sie einen oder mehrere einzelne Webverweise festlegen. Die folgenden Schritte zeigen, wie Sie einen Webverweis mithilfe von Visual Studio 2012 festlegen.
  
1. Klicken **Sie im** Projektmappen-Explorer mit der rechten Maustaste auf den Ordner **Verweise,** und wählen Sie **dann Dienstreferenz hinzufügen aus.** 
    
2. Wählen Sie **im Dialogfeld Dienstreferenz** hinzufügen die Option **Erweitert aus.**
    
3. Wählen Sie **im Einstellungen** Dienstreferenz die Option **Webreferenz hinzufügen aus.**
    
4. Geben Sie **im Textfeld URL** `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` ein, und drücken Sie dann die **EINGABETASTE,** oder wählen Sie das **Symbol Los** aus. Wenn Secure Sockets Layer (SSL) installiert ist, sollten Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls verwenden. 

   Verwenden Sie beispielsweise die folgende URL für den Project auf der Website `https://MyServer/pwa` für Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Öffnen Sie auch Ihren Webbrowser, und navigieren Sie zu `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` . Speichern Sie die Datei in einem lokalen Verzeichnis, z. B. `C:\Project\WebServices\ServiceName.wsdl` . Geben Sie **im Dialogfeld Webreferenz** hinzufügen für **URL** das Dateiprotokoll und den Pfad zur Datei ein. Geben Sie z. B. `file://C:\Project\WebServices\Project.wsdl` ein. 
    
5. Nachdem der Verweis aufgelöst wurde, geben Sie den Verweisnamen in das Textfeld **Webverweisname** ein. Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden den beliebigen Standardreferenznamen **Svc _ServiceName_**. Beispielsweise heißt Project Webdienst **SvcProject** (siehe Abbildung 3). 
    
   **Abbildung 3. Hinzufügen einer ASMX-Webdienstreferenz**

   ![Hinzufügen einer ASMX-Webdienstreferenz](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Hinzufügen einer ASMX-Webdienstreferenz")
  
Verwenden Sie für Anwendungskomponenten, die auf dem computer Project Server ausgeführt werden müssen, den Identitätswechsel verwenden oder über erhöhte Berechtigungen verfügen, einen WCF-Dienstverweis anstelle eines ASMX-Webverweises. Weitere Informationen finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Serveranwendungen verwenden häufig andere Dienste, z. B. SharePoint Server 2013-Webdienste. Wenn andere Dienste erforderlich sind, werden sie im Beispiel notiert.
  
Lokale Verweise für das Codebeispiel sind in **using-Anweisungen** am Anfang des Beispiels aufgeführt: 
  
1. Klicken **Sie im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **Verweise,** und wählen Sie **dann Verweis hinzufügen aus.**
    
2. Wählen **Sie Durchsuchen** aus, und navigieren Sie dann zu dem Speicherort, an dem Sie die zuvor kopierten Project Server-DLLs gespeichert haben. Wählen Sie die benötigten DLLs aus, und wählen Sie dann **OK aus.**
    
> [!NOTE]
> Stellen Sie sicher, dass die Assemblyversionen auf Ihrem Entwicklungscomputer genau mit denen auf dem Zielcomputer Project übereinstimmen. 
  
## <a name="using-multiple-authentication"></a>Verwenden mehrerer Authentifizierungen
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Die Authentifizierung von lokalen Project Serverbenutzern, Windows Authentifizierung oder Formularauthentifizierung, erfolgt über die Anspruchsverarbeitung in SharePoint Server 2013. Die mehrfache Authentifizierung bedeutet, dass die Webanwendung, für die Project Web App bereitgestellt wird, sowohl die Windows als auch die formularbasierte Authentifizierung unterstützt. In diesem Fall tritt bei einem Aufruf eines ASMX-Webdiensts, der die Windows-Authentifizierung verwendet, ein Fehler auf, da der Anspruchsprozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:
  
`The server was unable to process the request due to an internal error. . . .`

Um das Problem für ASMX zu beheben, sollten alle Aufrufe von PSI-Methoden für eine abgeleitete Klasse verwendet werden, die für jeden PSI-Webdienst definiert ist. Die abgeleitete Klasse muss auch die **SvcLoginWindows.LoginWindows-Klasse** verwenden, um ein Cookie für die abgeleitete PSI-Dienstklasse zu erhalten. Im folgenden Beispiel wird die **ProjectDerived-Klasse** von der **SvcProject.Project-Klasse** ab. Die abgeleitete Klasse fügt die **EnforceWindowsAuth-Eigenschaft** hinzu und überschreibt den Webanforderungsheader für jeden Aufruf einer Methode in der **Project** Klasse. Wenn die **EnforceWindowsAuth-Eigenschaft** **true** ist, fügt die **GetWebRequest-Methode** einen Header hinzu, der die Formularauthentifizierung deaktiviert. Wenn **EnforceWindowsAuth** **auf false gesetzt ist,** kann die Formularauthentifizierung fortgesetzt werden.
  
Um das folgende ASMXLogon_MultiAuth **zu** verwenden, erstellen Sie eine Konsolenanwendung, führen Sie die Schritte unter [Erstellen](#pj15_PrerequisitesASMX_Configure)der Anwendung und Hinzufügen eines Webdienstverweises aus, und fügen Sie dann das wsdl hinzu. LoginWindows.cs-Proxydatei und wsdl. Project.cs-Proxydatei. Die **Main-Methode** erstellt **die Projektinstanz** der **ProjectDerived-Klasse.** Das Beispiel muss die abgeleitete **LoginWindowsDerived-Klasse** verwenden, um ein **CookieContainer-Objekt** für das Projekt **zu erhalten. CookieContainer-Eigenschaft,** die die Formularauthentifizierung von der Windows unterscheidet. Das **Projektobjekt** kann dann zum Aufrufen einer beliebigen Methode in der **SvcProject.Project** werden. 
  
> [!NOTE]
> Der **LoginWindows-Dienst** ist nur für ASMX-Anwendungen in einer Umgebung mit mehreren Authentifizierungen erforderlich. Im **ASMXLogon_MultiAuth** ruft die **GetLogonCookie-Methode** ein Cookie für das **loginWindows-Objekt** ab. Das **Projekt. Die CookieContainer-Eigenschaft** wird auf den **Wert loginWindows.CookieContainer** festgelegt. 
  
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

Die Verwendung der abgeleiteten **LoginWindows-Klasse** und das Ausführen von PSI-Aufrufen mit einem Webanforderungsheader, der die Formularauthentifizierung deaktiviert, ist für Anwendungen erforderlich, die in einer Umgebung mit mehreren Authentifizierungen ausgeführt werden. Wenn Project Server nur die Anspruchsauthentifizierung verwendet, ist es nicht erforderlich, eine Klasse zu leiten, die einen Webanforderungsheader hinzufügt. Das vorherige Beispiel wird in beiden Umgebungen ausgeführt. 
  
Die Lösung für eine WCF-basierte Anwendung ist anders. Weitere Informationen finden  Sie im Abschnitt Verwenden mehrerer Authentifizierungen unter [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Ändern der Werte generischer Konstanten
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

Die meisten Beispiele enthalten eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel in Ihrer Umgebung ordnungsgemäß funktioniert. Wenn Sie SSL installiert haben, verwenden Sie im folgenden Beispiel das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen  _Sie ServerName_ durch den Namen des servers, den Sie verwenden. Ersetzen _Sie ProjectServerName_ durch den virtuellen Verzeichnisnamen Ihrer Project Serverwebsite, z. B. PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, oder andere Voraussetzungen werden am Anfang des Codebeispiels notiert.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Das Abrufen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach. Wenn Sie beispielsweise ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Seite Project Center in Project Web App angezeigt werden kann.
  
Sie können Codebeispielergebnisse auf verschiedene Weise überprüfen, z. B.:
  
- Verwenden Sie Project Professional 2013-Client, um das Projekt auf dem Project Server-Computer zu öffnen und die elemente, die Sie möchten, anzeigen.
    
- Zeigen Sie veröffentlichte Projekte auf der Project Center-Seite von Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ) an.
    
- Anzeigen des Warteschlangenprotokolls in Project Web App. Öffnen Sie die Seite Server Einstellungen (wählen Sie **das Symbol Einstellungen** in der  oberen rechten Ecke aus), und wählen Sie dann Meine Warteschlangenaufträge unter dem Abschnitt Persönliche **Einstellungen** aus ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). In der **Dropdownliste** Ansicht können Sie nach auftragsstatus sortieren. Der Standardstatus ist **In Bearbeitung und Fehlgeschlagene Aufträge in der vergangenen Woche**. 
    
- Verwenden Sie die Seite Server Einstellungen in Project Web App ( ), um alle Warteschlangenaufträge zu verwalten und Unternehmensobjekte zu löschen oder `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` zu erzwingen. Sie müssen über Administratorberechtigungen verfügen, um auf diese Links auf der Serverserverseite Einstellungen können.
    
- Verwenden **Microsoft SQL Server Management Studio,** um eine Abfrage für eine Tabelle in der Datenbank Project ausführen. Verwenden Sie beispielsweise die folgende Abfrage, um die 200 obersten Zeilen des Pubs auszuwählen. MSP_WORKFLOW_STAGE_PDPS, um Informationen zu den Projektdetailsetailseiten (PDPs) in Workflowphasen zu zeigen. 
    
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

Nachdem Sie einige Codebeispiele testiert haben, gibt es Enterprise-Objekte und -Einstellungen, die gelöscht oder zurückgesetzt werden sollten. Sie können die Seite Server Einstellungen in Project Web App verwenden, um Unternehmensdaten zu verwalten ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Über Links auf der Seite Server Einstellungen können Sie alte Elemente löschen, Eincheckprojekte erzwingen, die Auftragswarteschlange für alle Benutzer verwalten und andere administrative Aufgaben ausführen.
  
Im Folgenden finden Sie einige der Links auf der Seite Server Einstellungen, die Sie für typische Bereinigungsaktivitäten verwenden können, nachdem Sie Codebeispiele ausgeführt haben:
  
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
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Verwenden des Identitätswechsels mit WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md)
- [SharePoint Developer Center](https://msdn.microsoft.com/sharepoint/default.aspx)
    

