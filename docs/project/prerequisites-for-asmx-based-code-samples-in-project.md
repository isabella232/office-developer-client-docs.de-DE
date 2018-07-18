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
- Codebeispiele, Projektserver, Project Server programming PSI, Codebeispiele, PSI, kompilieren programming
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Hier erfahren Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe von die ASMX-basierte Codebeispiele, die in den Referenzthemen für Project Server Interface (PSI) enthalten sind.
ms.openlocfilehash: 73d097211dc3c68e1066c2ea1ad8d51a616184d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796312"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Voraussetzungen für ASMX-basierte Codebeispiele in Project

Hier erfahren Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe von die ASMX-basierte Codebeispiele, die in den Referenzthemen für Project Server Interface (PSI) enthalten sind.
  
Die folgenden Codebeispiele in der [Project Server 2013 Class Library und Web-Dienst verweisen](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) enthalten viele ursprünglich für Office Project 2007 SDK erstellt wurden, und verwenden ein Standardformat für ASMX-Webdienste. Die Beispiele weiterhin Arbeit in Project Server 2013 und in eine Konsolenanwendung kopiert und als eine vollständige Einheit ausgeführt werden sollen. Ausnahmen sind in der Stichprobe notiert haben. 
  
Neue PSI-Beispiele in Project 2013 SDK entsprechen in ein Format, die die Windows Communication Foundation (WCF)-Dienste verwendet. Die ASMX-basierte Codebeispiele können auch mithilfe der WCF-Dienste angepasst werden. In diesem Artikel veranschaulicht, wie die Beispiele mit ASMX-Webdiensten. Informationen zur Verwendung der Beispiele mit WCF-Diensten finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele im Projekt](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> Die ASMX Webdienstschnittstelle für die PSI wird ist in Project Server 2013 veraltet, jedoch weiterhin unterstützt. Wenn das Client-seitigen Objektmodell (CSOM) die Methoden, die die Anwendung erforderlich ist enthält, sollten neue Anwendungen mit dem Clientobjektmodell entwickelt werden. Das CSOM kann mit Project Online oder einer lokalen Installation von Project Server 2013. Andernfalls, wenn die Anwendung die PSI verwendet wird, sollte die WCF-Schnittstelle verwendet werden also die Technologie, die für die Netzwerkkommunikation empfohlen. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Interface verwenden, können nur für lokale Installationen von Project Server 2013 arbeiten. Weitere Informationen zu den CSOM finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md) und [den clientseitigen Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Vor dem Ausführen der Codebeispiele, müssen Sie Einrichten der Entwicklungsumgebung, konfigurieren Sie die Anwendung und generische Konstantenwerte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Richten Sie einen Test Project Server-System**.
    
   Verwenden Sie einen Test Project Server-System, wenn Sie entwickeln oder testen. Auch wenn Ihr Code perfekt interproject Abhängigkeiten funktioniert, können Berichte oder andere Umgebungsfaktoren unerwartete Ergebnisse verursachen. 
    
   > [!NOTE]
   > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server, und überprüfen Sie, dass Sie über ausreichende Berechtigungen für die PSI-Aufrufe verfügen, die die Anwendung verwendet. Im Referenzthema für jede PSI-Methode enthält eine Project Server-Berechtigungen-Tabelle. Die [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) -Methode erfordert beispielsweise die globale Berechtigung **Neues Projekt** und die Berechtigung **SaveProjectTemplate** . 
  
   In einigen Fällen müssen Sie möglicherweise das Remotedebuggen auf dem Server. Sie müssen auch einen Ereignishandler einrichten, indem ein Ereignishandlerassembly auf jeden Project Server-Computer in der SharePoint-Farm installieren und konfigurieren Sie dann den Ereignishandler für die Project Web App-Instanz mithilfe der Seite Project Server-Einstellungen in den allgemeinen Anwendungseinstellungen der SharePoint-Zentraladministration.
    
2. **Einrichten von einem Entwicklungscomputer.**
    
   Sie werden in der Regel die PSI über ein Netzwerk zugreifen. Die folgenden Codebeispiele dienen zum auf einem Client ausgeführt werden, die getrennt vom Server, sofern nicht anders angegeben ist.
    
   1. **Installieren Sie die richtige Version von Visual Studio.** Wenn nicht anders angegeben werden die folgenden Codebeispiele in Visual c# geschrieben. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass Sie das neueste Servicepack installiert haben. 
        
   2. **Kopieren Sie Project Server-DLLs auf dem Entwicklungscomputer installiert.** Kopieren Sie die folgenden Assemblys aus `[Program Files]\Microsoft Office Servers\15.0\Bin` auf dem Project Server-Computer, auf dem Entwicklungscomputer installiert: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Informationen dazu, wie Sie kompilieren und die Assembly ProjectServerServices.dll Proxy für die ASMX-Webdienste im PSI verwenden finden Sie unter [Verwendung einer PSI-Proxy-Assembly und IntelliSense Beschreibungen](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Installieren Sie die IntelliSense-Dateien.**
    
    Laden IntelliSense Beschreibungen für Klassen und Member in Project Server-Assemblys Kopie zu verwenden, um die aktualisierten IntelliSense-XML-Dateien aus dem Projekt 2013 SDK in dasselbe Verzeichnis, in dem die Project Server-Assemblys gespeichert sind. Kopieren Sie beispielsweise die Microsoft.Office.Project.Server.Library.xml-Datei in das Verzeichnis, in dem die Anwendung einen Verweis auf die Assembly Microsoft.Office.Project.Server.Library.dll festgelegt wird.
    
    Beschreibungen von IntelliSense für die PSI-Webdienste erfordern, dass das Erstellen einer PSI-Proxy-Assembly mithilfe des CompileASMXProxyAssembly.cmd-Skripts in der `Documentation\IntelliSense\WSDL` Unterverzeichnis des Project 2013 SDK-Downloads. Das Skript erstellt die ASMX-basierte ProjectServerServices.dll Proxy-Assembly. Weitere Informationen finden Sie unter die Datei [ReadMe_IntelliSense] im Download SDK. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Erstellen der Anwendung und einen Webverweis-Dienst
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Erstellen einer Konsolenanwendung**.
    
   Wenn Sie eine Konsolenanwendung, in der Dropdown-Liste im Dialogfeld **Neues Projekt** erstellen, wählen Sie **.NET Framework 4**. Sie können den Beispielcode PSI in der neuen Anwendung kopieren.
    
2. **Fügen Sie den Verweis für ASMX erforderlich.**
    
   Fügen Sie im Projektmappen-Explorer einen Verweis auf **System.Web.Services** (siehe Abbildung 1). 
    
   **Abbildung 1. Hinzufügen eines Verweises in Visual Studio**

   ![Hinzufügen eines Verweises in Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Hinzufügen eines Verweises in Visual Studio")
  
3. **Kopieren Sie den Code**.
    
   Kopieren Sie das vollständige Codebeispiel in der Datei Program.cs der Konsole an.
    
4. **Legen Sie den Namespace für die beispielanwendung aus**.
    
   Sie können ändern Sie den Namespace am oberen Rand des Beispiels zum Standard-Namespace Anwendung aufgeführt oder Standardnamespace Anwendung im Beispiel entsprechend ändern. Sie können den Standardnamespace Anwendung durch Ändern der Anwendungseigenschaften ändern.
    
   Das Codebeispiel für [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) verfügt beispielsweise über den **Microsoft.SDK.Project.Samples.RenameProject**-Namespace. Wenn der Name des Visual Studio-Projekts **RenameProject**ist, kopieren Sie den Namespace aus der Datei Program.cs, und öffnen Sie **Project Eigenschaftenbereich** (Wählen Sie im Menü **Projekt** **RenameProject Eigenschaften**ein). Kopieren Sie auf der Registerkarte **Anwendung** den Namespace in das Textfeld **Standardnamespace** . 
    
5. **Webverweise festgelegt**.
    
   Die meisten Beispiele erfordern einen Verweis auf eine oder mehrere der PSI-Webdienste. Diese werden in der Stichprobe selbst oder Kommentare, die im Beispiel vorangehen aufgelistet. Wenn den richtigen Namespace der Webverweise erhalten möchten, stellen Sie sicher, dass Sie zunächst den Standardnamespace Anwendung festlegen.
    
   Es gibt drei Möglichkeiten zum Hinzufügen eines ASMX-Webdienstverweises für die PSI:
    
   - Erstellen einer PSI-Proxy-Assembly mit dem Namen ProjectServerServices.dll, und legen Sie einen Verweis auf die Assembly. Wenn IntelliSense erhalten möchten, ist dies die empfohlene Option zum einen PSI-Verweis hinzufügen. Finden Sie unter [Verwendung einer PSI-Proxy-Assembly und IntelliSense Beschreibungen](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Fügen Sie eine Proxydatei aus der wsdl.exe Ausgabe der Visual Studio-Projektmappe. Finden Sie unter [Hinzufügen einer PSI-Proxy-Datei](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Hinzufügen eines Webverweises Service mithilfe von Visual Studio. Finden Sie unter [Hinzufügen einer Webs-service Verweis](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxy-Assembly und Beschreibungen von IntelliSense

Sie erstellen und verwenden können, die ProjectServerServices.dll Proxy-Assembly für alle ASMX-basierte Webdienste im PSI, mit dem Skript CompileASMXProxyAssembly.cmd in die `Documentation\IntelliSense\WSDL` Ordner des Project 2013-SDK-Downloads. Ein Link zum Download finden Sie unter [Project 2013-Entwicklerdokumentation](project-2013-developer-documentation.md).
  
> [!NOTE]
> Beim Extrahieren der Quelldateien Proxy aus der Datei Source.zip herunter-Datei, die Dateien in die `Documentation\IntelliSense\WSDL\Source` Ordner ab dem Datum der Veröffentlichung des Project 2013-SDK-Downloads aktuell sind. Generieren aktualisiert PSI Proxy Quelldateien, führen Sie das Skript GenASMXProxyAssembly.cmd auf dem Project Server-Computer. Die Skripts in der `Documentation\IntelliSense\WCF` Ordner für ASMX-basierte Anwendungen nicht mehr verwendet. Das GenWCFProxyAssembly.cmd-Skript ruft SvcUtil.exe, die Quellcodedateien für die WCF-Dienste generiert. Die WCF-Proxy-Dateien können verschiedene Attribute, die Channel-Schnittstelle und eine Client-Klasse für jeden PSI-Dienst. Der Dienst WCF-basierte Ressource umfasst beispielsweise die **ResourceChannel** -Schnittstelle, die **Ressource** Interface und der **ResourceClient** -Klasse. Das Ressource ASMX-basierte Web enthält **die Klasse mit einigen anderen Eigenschaften** . 
  
Es folgt das GenASMXProxyAssembly.cmd-Skript, das Ausgabedateien für die PSI-Webdienste WSDL-Datei generiert und anschließend die Assembly kompiliert wird.
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=http://ServerName/pwa/_vti_bin/psi)
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

Das Skript verwendet die ClassList_asmx.txt-Datei, die die Liste der Webdienste enthält, die für Entwickler von Drittanbietern verfügbar sind.
  
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

Die Skripts erstellen Sie eine Assembly mit dem Namen ProjectServerServices.dll. Vermeiden Sie es mit ProjectServerServices.dll für die Assembly des WCF-basierte verwirrend. Die Assemblynamen sind die gleichen, die ProjectServerServices.xml IntelliSense-Datei mit einer Assembly aktivieren.
  
Der durch die Skripts für die ASMX-Webdienste und die WCF-Dienste erstellten beliebige Namespace entspricht, damit die ProjectServerServices.xml IntelliSense-Datei mit einer Assembly arbeitet. Beispielsweise ist der Namespace des Diensts Ressource in der Proxyassembly für WCF-basierte und in der Proxyassembly für ASMX-basierte **SvcResource**. Sie können die Namespacenamen natürlich ändern – Wenn Sie sicherstellen, dass sie in der Proxyassembly und in der Datei ProjectServerServices.xml IntelliSense übereinstimmen.
  
Wenn ein Codebeispiel einen anderen Namen für einen PSI Web Service-Namespace verwendet wird, muss beispielsweise **ProjectWebSvc**IntelliSense Sie zusammenarbeiten, ändern Sie das Beispiel um **SvcProject** verwenden, damit der Namespace Proxyassembly entspricht. 
  
Ein Vorteil der Verwendung der ASMX-basierte Proxy-Assembly ist, dass sie alle PSI Web Service Namespaces enthält. Sie müssen keinen mehrere Webverweise erstellen. Ein weiterer Vorteil besteht darin, wenn Sie die ProjectServerServices.xml-Datei in dasselbe Verzeichnis hinzufügen, in dem Sie einen Verweis auf die Assembly ProjectServerServices.dll Proxy festlegen, können Sie IntelliSense Beschreibungen für die PSI-Klassen und Member erhalten. Abbildung 2 zeigt den Text IntelliSense für die **Project.QueueCreateProject** -Methode. Weitere Informationen finden Sie unter die Datei [ReadMe_IntelliSense] im Ordner IntelliSense des Project 2013-SDK-Downloads. 
  
**Abbildung 2. Verwenden von IntelliSense für eine Methode in den Project-Webdienst**

![Verwenden von Intellisense für eine Methode in einem PSI-Dienst] (media/pj15_PrerequisitesASMX_Intellisense.gif "Verwenden von Intellisense für eine Methode in einem PSI-Dienst")
  
Nachteile der Verwendung der Proxyassembly sind, dass die Lösung größer ist, und Sie müssen verteilen und installieren Sie die Proxyassembly mit der Lösung. Sie müssen außerdem den gleichen Namespaces, die in der Proxyassembly und die IntelliSense-Dateien sind verwenden, es sei denn, Sie ändern das Skript und die ProjectServerServices.xml IntelliSense-Datei, unterschiedliche Namespaces zu verwenden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxy-Datei
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Der Project 2013-SDK-Download enthält die Quelldateien für die Proxyassembly mit dem Befehl Wsdl.exe generiert. Die Quelldateien befinden sich in der Datei Source.zip herunter, in der `Documentation\IntelliSense\ASMX` Unterverzeichnis. Anstatt einen Verweis auf die Proxyassembly, können Sie eine oder mehrere der Quelldateien für Visual Studio-Projektmappe hinzufügen. Fügen Sie beispielsweise die WSDL-Datei nach der Ausführung des Skripts GenASMXProxyAssembly.cmd hinzu. Project.cs-Datei, die die Lösung. Anstelle des Skripts ausführen, können Sie eine einzelne Quelldatei, zum Beispiel generiert die folgenden Befehle ausführen: 
  
```MS-DOS
set VDIR=http://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Um ein **Project** -Objekt als einer Klassenvariablen namens **Projekt**definieren möchten, verwenden Sie den folgenden Code ein. Die **AddContextInfo** -Methode wird das **Project** -Objekt für die Windows-Authentifizierung und formularbasierte Authentifizierung die Kontextinformationen hinzugefügt. 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "http://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> Ob Sie mit einer PSI-Proxy-Assembly oder einer Proxydatei für eine Project Dienstverweis mit dem Namen **SvcProject hinzufügen**, verwenden Sie den gleichen Code, um ein **Project** -Objekt zu erstellen. 
  
### <a name="adding-a-web-service-reference"></a>Hinzufügen eines Webverweises service
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Wenn Sie nicht die ASMX-basierte Proxyassembly verwenden und eine Ausgabe WSDL-Datei hinzufügen, können Sie eine oder mehrere einzelne Webverweise festlegen. Die folgenden Schritte zeigen, wie Sie einen Webverweis mithilfe von Visual Studio 2012 festgelegt.
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann auf **Dienstverweis hinzufügen**. 
    
2. Wählen Sie **Erweitert**, klicken Sie im Dialogfeld **Dienstverweis hinzufügen** .
    
3. Wählen Sie im Dialogfeld **Dienstverweiseinstellungen** **Webverweis hinzufügen**.
    
4. Geben Sie in das Textfeld **URL** `http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, und drücken Sie die **EINGABETASTE** , oder wählen Sie das Symbol **wechseln** . Wenn Sie Secure Sockets Layer (SSL) installiert haben, sollten Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls verwenden. 

   Verwenden Sie beispielsweise die folgende URL für den Project-Dienst auf die `http://MyServer/pwa` Website für die Project Web App:`http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Oder, öffnen Sie Ihren Webbrowser, und navigieren Sie zu `http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`. Speichern Sie die Datei in ein lokales Verzeichnis, z. B. `C:\Project\WebServices\ServiceName.wsdl`. Geben Sie im Dialogfeld **Webverweis hinzufügen** für die **URL**, das Dateiprotokoll und den Pfad zu der Datei ein. Geben Sie zum Beispiel `file://C:\Project\WebServices\Project.wsdl`. 
    
5. Nachdem Sie der Verweis aufgelöst wird, geben Sie den Verweisnamen in das Textfeld **Webverweisname** . Codebeispiele in der Project 2013-Entwicklerdokumentation verwenden Sie den Namen beliebige Standardverweis **Svc _ServiceName_**. Beispielsweise heißt der Project-Webdienst **SvcProject** (siehe Abbildung 3). 
    
   **Abbildung 3. Hinzufügen eines ASMX-Webdienstverweises**

   ![Hinzufügen eines ASMX-Webdienstverweises] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Hinzufügen eines ASMX-Webdienstverweises")
  
Für Anwendungskomponenten, die auf dem Project Server-Computer ausführen müssen, Identitätswechsel verwenden oder haben verwenden mit erhöhten Berechtigungen ein WCF-Dienstverweises anstelle eines ASMX-Webverweis. Weitere Informationen finden Sie unter [Voraussetzungen für WCF-basierte Codebeispiele im Projekt](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Server-Anwendungen verwenden häufig andere Dienste, wie SharePoint Server 2013-Webdienste. Wenn andere Dienste erforderlich sind, werden sie in das Beispiel aufgeführt.
  
Lokale Referenzen für das Codebeispiel sind in **using** -Anweisungen am oberen Rand des Beispiels aufgeführt: 
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann auf **Verweis hinzufügen**.
    
2. Wählen Sie **Durchsuchen aus**, und wechseln Sie zu dem Speicherort, in dem Sie die Project Server-DLLs gespeichert, die Sie zuvor kopiert. Wählen Sie die DLLs, die Sie benötigen, und wählen Sie dann auf **OK**.
    
> [!NOTE]
> Stellen Sie sicher, dass die Versionen der Assembly auf Ihrem Entwicklungscomputer genau auf dem Zielcomputer für Project Server übereinstimmen. 
  
## <a name="using-multiple-authentication"></a>Verwenden mehrere Authentifizierungsmethoden
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Die Authentifizierung des lokalen Project Server-Benutzer, erfolgt durch Windows-Authentifizierung oder Formularauthentifizierung über Claims processing in SharePoint Server 2013. Mehrere Authentifizierungsmethoden bedeutet, dass die Webanwendung, die auf der Project Web App bereitgestellt wird Windows-Authentifizierung und formularbasierte Authentifizierung unterstützt. Wenn dies der Fall ist, wird ein Anrufs an eine ASMX-Webdienst, der Windows-Authentifizierung verwendet die folgende Fehler auftreten, da der Ansprüche Prozess die Bestimmung des Typs des Benutzers zum authentifizieren kann nicht:
  
`The server was unable to process the request due to an internal error. . . .`

Zur Behebung des Problems für ASMX sollten alle Aufrufe von PSI-Methoden an, in einer abgeleiteten Klasse werden, die für jeden Webdienst PSI definiert ist. Die abgeleitete Klasse muss auch die **SvcLoginWindows.LoginWindows** -Klasse verwenden, um ein Cookie für die abgeleitete Klasse der PSI-Dienst abzurufen. Im folgenden Beispiel wird die **ProjectDerived** -Klasse von der **SvcProject.Project** -Klasse abgeleitet. Die abgeleitete Klasse fügt die **EnforceWindowsAuth** -Eigenschaft und überschreibt den Web-Anforderungsheader für jeden Aufruf einer Methode in der **Project** -Klasse. Wenn die **EnforceWindowsAuth** -Eigenschaft auf **true**festgelegt ist, fügt die **GetWebRequest** -Methode eine Kopfzeile, die formularbasierte Authentifizierung deaktiviert. Wenn **EnforceWindowsAuth** auf **false**festgelegt ist, kann die Formularauthentifizierung fortgesetzt werden.
  
Um die folgenden **ASMXLogon_MultiAuth** Beispiel zu verwenden, erstellen Sie eine, führen Sie die Schritte in [der Anwendung erstellen und Hinzufügen eines Webverweises Dienst](#pj15_PrerequisitesASMX_Configure), und fügen Sie die WSDL-Datei. LoginWindows.cs Proxy-Datei und die WSDL-Datei. Project.cs Proxy-Datei. Die **Main** -Methode erstellt die **Project** -Instanz der **ProjectDerived** -Klasse. Im Beispiel muss die abgeleitete Klasse **LoginWindowsDerived** verwenden, um ein **CookieContainer** -Objekt für das Projekt **abzurufen. CookieContainer** -Eigenschaft, die formularbasierte Authentifizierung von Windows-Authentifizierung unterscheidet. **Project** -Objekts kann dann tätigen von Anrufen an eine beliebige-Methode in der **SvcProject.Project** -Klasse verwendet werden. 
  
> [!NOTE]
> Der **LoginWindows** -Dienst ist nur für ASMX-Applikationen in einer Umgebung mit mehreren Authentifizierung erforderlich. Im Beispiel **ASMXLogon_MultiAuth** Ruft die **GetLogonCookie** -Methode ein Cookie für das **LoginWindows** -Objekt ab. Das Projekt **. CookieContainer** -Eigenschaft auf den Wert **loginWindows.CookieContainer** festgelegt ist. 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "http://ServerName/ProjectServerName/_vti_bin/psi/";
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

Mit der abgeleiteten Klasse **LoginWindows** und das PSI-Aufrufe mit einem Web-Anforderungsheader, der Formularauthentifizierung deaktiviert ist erforderlich für Anwendungen, die in einer Umgebung mit mehreren Authentifizierung ausgeführt. Wenn Project Server nur die anspruchsbasierte Authentifizierung verwendet wird, ist es nicht erforderlich, eine Klasse abgeleitet, die einen Web Anforderungsheader hinzufügt. Im vorherige Beispiel wird im beider Umgebungen ausgeführt. 
  
Die Fehlerbehebung für einen WCF-basierte Anwendung ist unterschiedlich. Weitere Informationen finden Sie im Abschnitt *mit mehreren Authentifizierung* bei den [erforderlichen Komponenten für WCF-basierte Codebeispiele im Projekt](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Ändern der Werte von generischen-Konstanten
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

Die meisten Beispiele haben eine oder mehrere Variablen, die Sie für das Beispiel funktioniert ordnungsgemäß in Ihrer Umgebung aktualisieren müssen. Im folgenden Beispiel wenn Sie SSL installiert haben, verwenden Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen Sie _ServerName_ mit dem Namen des Servers, den Sie verwenden. Ersetzen Sie _ProjectServerName_ durch den Namen des virtuellen Verzeichnisses Ihrer Project Server-Website, wie etwa PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen oder andere erforderliche Komponenten werden am Anfang des Codebeispiels aufgeführt.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Abrufen und ein Codebeispiel Ergebnisse interpretieren ist nicht immer einfach. Angenommen, wenn Sie ein Projekt erstellt haben, müssen Sie das Projekt veröffentlichen, bevor es auf der Seite Project Center in Project Web App angezeigt werden kann.
  
Sie können beispielsweise Code Beispielergebnisse auf verschiedene Weise überprüfen:
  
- Verwenden Sie den Project Professional 2013 Client, um das Projekt vom Project Server-Computer zu öffnen, und zeigen Sie die gewünschten Elemente.
    
- Veröffentlichte Projekte anzuzeigen, die auf der Seite Projektcenter von Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Anzeigen des Protokolls Warteschlange in Project Web App. Öffnen Sie die Seite servereinstellungen (Wählen Sie das Symbol **Einstellungen** in der oberen rechten Ecke), und wählen Sie dann im Abschnitt **Persönliche Einstellungen** **Eigene Warteschlangenaufträge** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). In der Dropdown-Liste **Ansicht** können Sie nach der Auftragsstatus sortiert werden. Die Standardstatus ist **In Bearbeitung und Fehler bei der Aufträge in der letzten Woche**. 
    
- Verwenden die Seite servereinstellungen in Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) alle Warteschlangenaufträge verwalten und löschen oder Erzwingen des Eincheckens von Enterprise-Objekten. Sie benötigen Administratorberechtigungen auf diese Links auf der Seite servereinstellungen zugreifen.
    
- Verwenden Sie zum Ausführen einer Abfrage für eine Tabelle in der Project-Datenbank **Microsoft SQL Server Management Studio** . Verwenden Sie beispielsweise die folgende Abfrage aus, um die obersten 200 Zeilen von der Pub auszuwählen. MSP_WORKFLOW_STAGE_PDPS Tabelle Informationen über das Projekt in Workflowstufen Projektdetailseiten (PDPs) angezeigt. 
    
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
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

Nachdem Sie einige Codebeispiele testen, gibt es Enterprise-Objekte und Einstellungen, die gelöscht oder zurückgesetzt werden sollte. Sie können die Seite servereinstellungen in Project Web App verwenden, zum Verwalten von Enterprise-Daten ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Links auf der Seite servereinstellungen können Sie alte Elemente löschen, Projekte Einchecken erzwingen, Verwalten der Auftragswarteschlange für alle Benutzer und andere administrativen Aufgaben ausführen.
  
Es folgen einige der Links auf der Seite servereinstellungen, die Sie nach dem Ausführen der Codebeispiele für typische Bereinigungen verwenden können:
  
- **Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**
    
- **Verwalten von Warteschlangenaufträgen**
    
- **Enterprise-Objekte löschen**
    
- **Einchecken von Enterprise-Objekten erzwingen**
    
- **Enterprise-Projekttypen**
    
- **Workflowphasen**
    
- **Workflowphasen**
    
- **Projektdetailseiten**
    
- **Zeiträume für Zeitberichte**
    
- **Einstellungen und Standardwerte in der**
    
- **Zeilenklassifizierungen**
    
Zusätzliche Einstellungen werden von SharePoint Server 2013 für jede Project Web App-Instanz und nicht von einer bestimmten Seite Project Web App-servereinstellungen verwaltet. Wählen Sie in der Anwendung der SharePoint-Zentraladministration **Allgemeine Anwendungseinstellungen**, wählen Sie **Verwalten** unter **Project Server-Einstellungen**, und wählen Sie dann die Project Web App-Instanz in der Dropdown-Liste auf der Seite servereinstellungen . Wählen Sie beispielsweise **Serverseitige Ereignishandler** hinzufügen oder Löschen von Ereignishandlern für die ausgewählte Project Web App-Instanz. 
  
## <a name="see-also"></a>Siehe auch
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Voraussetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Verwenden des Identitätswechsels mit WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Project-PSI-Referenz – Übersicht](project-psi-reference-overview.md)
- [SharePoint Developer Center](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

