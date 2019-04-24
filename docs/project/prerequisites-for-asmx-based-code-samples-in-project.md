---
title: VoraussetZungen für ASMX-basierte Codebeispiele in Project
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
- Codebeispiele, Project Server, Project Server, Programmierung, PSI, Kompilieren von Codebeispielen, PSI, Programmierung
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Hier finden Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen zu PSI (Project Server Interface) enthalten sind.
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357083"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>VoraussetZungen für ASMX-basierte Codebeispiele in Project

Hier finden Sie Informationen zum Erstellen von Projekten in Visual Studio mithilfe der ASMX-basierten Codebeispiele, die in den Referenzthemen zu PSI (Project Server Interface) enthalten sind.
  
Viele der in der [Project Server 2013-Klassenbibliothek und dem Webdienstverweis](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) enthaltenen Codebeispiele wurden ursprünglich für das Office Project 2007-SDK erstellt und verwenden ein Standardformat für ASMX-Webdienste. Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass Sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden können. Im Beispiel werden Ausnahmen angegeben. 
  
Neue PSI-Beispiele im Project 2013 SDK entsprechen einem Format, das Windows Communication Foundation (WCF)-Dienste verwendet. Die ASMX-basierten Beispiele können auch zur Verwendung von WCF-Diensten angepasst werden. In diesem Artikel wird gezeigt, wie Sie die Beispiele mit ASMX-Webdiensten verwenden. Informationen zur Verwendung der Beispiele mit WCF-Diensten finden Sie unter [vorausSetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> Die ASMX-Webdienst-Schnittstelle der PSI ist in Project Server 2013 veraltet, wird jedoch weiterhin unterstützt. Wenn das clientseitige Objektmodell (CSOM) die Methoden enthält, die für Ihre Anwendung erforderlich sind, sollten neue Anwendungen mit dem CSOM entwickelt werden. Die CSOM ermöglicht es Anwendungen, mit Project Online oder einer lokalen Installation von Project Server 2013 zu arbeiten. Wenn Ihre Anwendung die PSI verwendet, sollte Sie andernfalls die WCF-Schnittstelle verwenden, bei der es sich um die Technologie handelt, die wir für die Netzwerkkommunikation empfehlen. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 funktionieren. Weitere Informationen zu CSOM finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md) und [Client seitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Bevor Sie die Codebeispiele verwenden, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren und generische Konstante Werte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Richten Sie ein Test Project Server-System ein**.
    
   Verwenden Sie ein Test Project Server-System, wenn Sie entwickeln oder testen. Auch wenn Ihr Code einwandfrei funktioniert, können interprojekt-Abhängigkeiten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Konsequenzen verursachen. 
    
   > [!NOTE]
   > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die PSI-Aufrufe verfügen, die Ihre Anwendung verwendet. Das Referenzthema für jede PSI-Methode enthält eine Project Server Permissions-Tabelle. Die [Project. QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) -Methode erfordert beispielsweise die globale **Neuprojekt** -Berechtigung und die **SaveProjectTemplate** -Berechtigung. 
  
   In einigen Fällen müssen Sie möglicherweise das Remote Debugging auf dem Server durchführen. Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie auf jedem Project Server-Computer in der SharePoint-Farm eine Ereignishandler-Assembly installieren und dann den Ereignishandler für die Project Web App-Instanz mithilfe der Project Server-Einstellungsseite im allgemeinen konfigurieren. Anwendungseinstellungen der SharePoint-zentral Administration.
    
2. **Richten Sie einen Entwicklungscomputer ein.**
    
   Sie greifen in der Regel über ein Netzwerk auf das PSI zu. Die Codebeispiele sind so konzipiert, dass Sie auf einem Client ausgeführt werden, der vom Server getrennt ist, sofern nicht angegeben.
    
   1. **Installieren Sie die richtige Version von Visual Studio.** Sofern nicht angegeben, werden die Codebeispiele in Visual C# geschrieben. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass das neueste Service Pack installiert ist. 
        
   2. **Kopieren Sie Project Server-DLLs auf den Entwicklungscomputer.** Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` von auf dem Project Server-Computer auf den Entwicklungscomputer: 
        
      - Microsoft. Office. Project. Server. Events. Receivers. dll
      - Microsoft. Office. Project. Server. Library. dll
        
   3. Informationen zum Kompilieren und Verwenden der Proxy-Assembly ProjectServerServices. dll für die ASMX-Webdienste in der PSI finden Sie unter [using a PSI Proxy Assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Installieren Sie die IntelliSense-Dateien.**
    
    Um IntelliSense-Beschreibungen für Klassen und Member in Project Server-Assemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013 SDK-Download in das Verzeichnis, in dem sich die Project Server-Assemblys befinden. Kopieren Sie beispielsweise die Datei Microsoft. Office. Project. Server. Library. XML in das Verzeichnis, in dem Ihre Anwendung einen Verweis auf die Microsoft. Office. Project. Server. Library. dll-Assembly festlegen soll.
    
    Die IntelliSense-Beschreibungen für die PSI-Webdienste erfordern das Erstellen einer PSI-Proxy-Assembly mithilfe des CompileASMXProxyAssembly. `Documentation\IntelliSense\WSDL` CMD-Skripts im Unterverzeichnis des Project 2013 SDK-Downloads. Das Skript erstellt die ASMX-basierte Proxy-Assembly ProjectServerServices. dll. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im SDK-Download. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Erstellen der Anwendung und Hinzufügen eines Webdienstverweises
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Erstellen Sie eine Konsolenanwendung**.
    
   Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds **Neues Projekt** **.NET Framework 4**aus. Sie können den PSI-Beispielcode in die neue Anwendung kopieren.
    
2. **Fügen Sie den für ASMX erforderlichen Verweis hinzu.**
    
   Fügen Sie im Projektmappen-Explorer einen Verweis auf **System. Web. Services** hinzu (siehe Abbildung 1). 
    
   **Abbildung 1. Hinzufügen eines Verweises in Visual Studio**

   ![Hinzufügen eines Verweises in Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Hinzufügen eines Verweises in Visual Studio")
  
3. **Kopieren Sie den Code**.
    
   Kopieren Sie das vollständige Codebeispiel in die Program.cs-Datei der Konsolenanwendung.
    
4. **Legen Sie den Namespace für die Beispielanwendung fest**.
    
   Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standard Anwendungs Namespace so ändern, dass er mit dem Beispiel übereinstimmt. Sie können den Standard Anwendungs Namespace ändern, indem Sie die Anwendungseigenschaften ändern.
    
   Das Codebeispiel für [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) verfügt beispielsweise über den Namespace **Microsoft. SDK. Project. Samples. RenameProject**. Wenn der Name des Visual Studio-Projekts **RenameProject**ist, kopieren Sie den Namespace aus der Program.cs-Datei, und öffnen Sie dann den Bereich Projekt **Eigenschaften** (Klicken Sie im Menü **Projekt** auf **RenameProject Eigenschaften**). Kopieren Sie auf der Registerkarte **Anwendung** den Namespace in das Textfeld **Standardnamespace** . 
    
5. **Legen Sie die Webverweise fest**.
    
   Die meisten Beispiele erfordern einen Verweis auf einen oder mehrere der PSI-Webdienste. Diese werden im Beispiel selbst oder in Kommentaren aufgeführt, die dem Beispiel vorangestellt sind. Um den korrekten Namespace der Webverweise abzurufen, stellen Sie sicher, dass Sie zuerst den Standard Anwendungs Namespace festlegen.
    
   Es gibt drei Möglichkeiten, eine ASMX-Webdienst Referenz für die PSI hinzuzufügen:
    
   - Erstellen Sie eine PSI-Proxy-Assembly mit dem Namen ProjectServerServices. dll, und legen Sie dann einen Verweis auf die Assembly fest. Um IntelliSense zu erhalten, empfiehlt es sich, einen PSI-Verweis hinzuzufügen. Weitere Informationen finden Sie unter [using a PSI Proxy Assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Fügen Sie der Visual Studio-Projektmappe eine Proxydatei aus der Ausgabe von WSDL. exe hinzu. Weitere Informationen finden Sie unter [Hinzufügen einer PSI-Proxydatei](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Hinzufügen eines Webdienstverweises mithilfe von Visual Studio. Weitere Informationen finden Sie unter [Hinzufügen eines Webdienst](#pj15_PrerequisitesASMX_AddingServiceReference)Verweises.

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxy-Assembly und IntelliSense-Beschreibungen

Sie können die ProjectServerServices. dll-Proxy Assembly für alle ASMX-basierten Webdienste in der PSI erstellen, indem Sie das Skript CompileASMXProxyAssembly. cmd im `Documentation\IntelliSense\WSDL` Ordner des Project 2013 SDK-Downloads verwenden. Einen Link zum Download finden Sie unter [Project 2013 Developer Documentation](project-2013-developer-documentation.md).
  
> [!NOTE]
> Wenn Sie die Proxy Quelldateien aus der ZIP-Datei extrahieren, sind die Dateien im `Documentation\IntelliSense\WSDL\Source` Ordner ab dem Veröffentlichungsdatum des Project 2013 SDK-Downloads aktuell. Um aktualisierte PSI-Proxy-Quelldateien zu generieren, führen Sie das Skript GenASMXProxyAssembly. cmd auf dem Project Server-Computer aus. Die Skripts im `Documentation\IntelliSense\WCF` Ordner funktionieren nicht für ASMX-basierte Anwendungen. Das Skript GenWCFProxyAssembly. cmd ruft SvcUtil. exe auf, wodurch Quellcodedateien für die WCF-Dienste generiert werden. Die WCF-Proxydateien schließen unterschiedliche Attribute, die Kanalschnittstelle und eine Clientklasse für jeden PSI-Dienst ein. Der WCF-basierte Ressourcendienst umfasst beispielsweise die **ResourceChannel** -Schnittstelle, die **Ressourcen** Schnittstelle und die **ResourceClient** -Klasse. Die ASMX-basierte Ressourcen-Web enthält die **Ressourcen** Klasse mit einigen unterschiedlichen Eigenschaften. 
  
Nachfolgend sehen Sie das Skript GenASMXProxyAssembly. cmd, das WSDL-Ausgabedateien für die PSI-Webdienste generiert und dann die Assembly kompiliert.
  
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

Das Skript verwendet die Datei ClassList_asmx. txt, die die Liste der Webdienste enthält, die für Drittanbieterentwickler verfügbar sind.
  
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

Die Skripts erstellen eine Assembly mit dem Namen ProjectServerServices. dll. Vermeiden Sie eine Verwechslung mit ProjectServerServices. dll für die WCF-basierte Assembly. Die Assemblynamen sind identisch, um die Verwendung einer der Assemblys mit der IntelliSense-Datei ProjectServerServices. XML zu aktivieren.
  
Der willkürliche Namespace, der von den Skripts für die ASMX-Webdienste und die WCF-Dienste erstellt wurde, ist identisch, sodass die IntelliSense-Datei ProjectServerServices. XML mit beiden Assemblys funktioniert. Beispielsweise ist der Namespace des Ressourcen Diensts in der WCF-basierten Proxy Assembly und in der ASMX-basierten Proxy Assembly **SvcResource**. Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass Sie in der Proxy-Assembly und in der IntelliSense-Datei ProjectServerServices. XML übereinstimmen.
  
Wenn ein Codebeispiel einen anderen Namen für einen PSI-Webdienst Namespace verwendet (beispielsweise **ProjectWebSvc**), müssen Sie das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace mit der Proxy Assembly übereinstimmt. 
  
Ein Vorteil bei der Verwendung der ASMX-basierten Proxy-Assembly besteht darin, dass Sie alle PSI-Webdienst-Namespaces enthält; Sie müssen nicht mehrere Webverweise erstellen. Ein weiterer Vorteil besteht darin, dass Sie beim Hinzufügen der Datei ProjectServerServices. XML zu demselben Verzeichnis, in dem Sie einen Verweis auf die ProjectServerServices. dll-Proxy Assembly festlegen, IntelliSense-Beschreibungen für die PSI-Klassen und-Member abrufen können. Abbildung 2 zeigt den IntelliSense-Text für die **Project. QueueCreateProject** -Methode. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im IntelliSense-Ordner des Project 2013 SDK-Downloads. 
  
**Abbildung 2. Verwenden von IntelliSense für eine Methode im Project-Webdienst**

![Verwenden von IntelliSense für eine Methode in einem PSI-Dienst] (media/pj15_PrerequisitesASMX_Intellisense.gif "Verwenden von IntelliSense für eine Methode in einem PSI-Dienst")
  
Nachteile der Verwendung der Proxy-Assembly sind, dass die Lösung größer ist und Sie die Proxy Assembly mit der Lösung verteilen und installieren müssen. Sie müssen auch die gleichen Namespaces verwenden, die sich in der Proxy-Assembly und den IntelliSense-Dateien befinden, es sei denn, Sie ändern die IntelliSense-Datei Script und ProjectServerServices. XML, um verschiedene Namespaces zu verwenden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxydatei
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Der Project 2013 SDK-Download enthält die Quelldateien, die vom Befehl WSDL. exe für die Proxy Assembly generiert werden. Die Quelldateien befinden sich in Source. zip im `Documentation\IntelliSense\ASMX` Unterverzeichnis. Anstatt einen Verweis auf die Proxy-Assembly festzulegen, können Sie einer Visual Studio-Lösung eine oder mehrere Quelldateien hinzufügen. Fügen Sie beispielsweise nach dem Ausführen des Skripts GenASMXProxyAssembly. cmd die WSDL hinzu. Project.cs-Datei für die Lösung. Anstatt das Skript auszuführen, können Sie beispielsweise die folgenden Befehle zum Generieren einer einzelnen Quelldatei ausführen: 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Verwenden Sie den folgenden Code, um ein **Project** -Objekt als Klassenvariable mit dem Namen **Project**zu definieren. Die **AddContextInfo** -Methode fügt die Kontextinformationen zum **Project** -Objekt für die Windows-Authentifizierung und formularbasierte Authentifizierung hinzu. 
  
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
> Unabhängig davon, ob Sie eine PSI-Proxy-Assembly verwenden oder eine Proxydatei für einen Project-Dienstverweis namens **SvcProject**hinzufügen, würden Sie denselben Code zum Erstellen eines **Project** -Objekts verwenden. 
  
### <a name="adding-a-web-service-reference"></a>Hinzufügen eines Webdienstverweises
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Wenn Sie die ASMX-basierte Proxy-Assembly nicht verwenden oder eine WSDL-Ausgabedatei hinzufügen, können Sie einen oder mehrere einzelne Webverweise festlegen. In den folgenden Schritten wird gezeigt, wie Sie einen Webverweis mithilfe von Visual Studio 2012 festlegen.
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann **Dienstverweis hinzufügen**aus. 
    
2. Klicken Sie im Dialogfeld **Dienstverweis hinzufügen** auf **erweitert**.
    
3. Klicken Sie im Dialogfeld **Dienstverweiseinstellungen** auf **Webverweis hinzufügen**.
    
4. Geben `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`Sie in das Textfeld **URL** ein, und drücken Sie dann die **Eingabe** Taste, oder klicken Sie auf das Symbol **Gehe** zu. Wenn Sie SSL (Secure Sockets Layer) installiert haben, sollten Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls verwenden. 

   Verwenden Sie beispielsweise die folgende URL für den Project-Dienst auf `https://MyServer/pwa` der Website für Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Oder öffnen Sie den Webbrowser, und navigieren Sie zu `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`. Speichern Sie die Datei in einem lokalen Verzeichnis wie `C:\Project\WebServices\ServiceName.wsdl`. Geben Sie im Dialogfeld **Webverweis hinzufügen** unter **URL**das Dateiprotokoll und den Pfad zu der Datei ein. Geben `file://C:\Project\WebServices\Project.wsdl`Sie beispielsweise ein. 
    
5. Nachdem der Verweis aufgelöst wurde, geben Sie den Verweisnamen in das Textfeld **Webverweisname** ein. Code Beispiele in der Project 2013-Entwicklerdokumentation verwenden den beliebigen Standardverweis Namen **svc _Service_** Name. Der Project-Webdienst heißt beispielsweise **SvcProject** (siehe Abbildung 3). 
    
   **Abbildung 3. Hinzufügen eines ASMX-Webdienstverweises**

   ![Hinzufügen eines ASMX-Webdienst] Verweises (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Hinzufügen eines ASMX-Webdienst") Verweises
  
Verwenden Sie für Anwendungskomponenten, die auf dem Project Server-Computer ausgeführt werden müssen, den Identitätswechsel oder über erhöhte Berechtigungen, einen WCF-Dienstverweis anstelle eines ASMX-Webverweises. Weitere Informationen finden Sie unter [vorausSetzungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Server-Anwendungen verwenden häufig andere Dienste wie SharePoint Server 2013-Webdienste. Wenn andere Dienste erforderlich sind, werden Sie im Beispiel notiert.
  
Lokale Verweise für das Codebeispiel werden in **using** -Anweisungen am Anfang des Beispiels aufgeführt: 
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann **Verweis hinzufügen**aus.
    
2. Klicken Sie auf **Durchsuchen**, und navigieren Sie dann zu dem Speicherort, an dem Sie die Project Server-DLLs gespeichert haben, die Sie zuvor kopiert haben. Wählen Sie die DLLs, die Sie benötigen, und klicken Sie dann auf **OK**.
    
> [!NOTE]
> Stellen Sie sicher, dass die Assemblyversion auf dem Entwicklungscomputer genau mit denen auf dem Ziel-Project Server-Computer übereinstimmen. 
  
## <a name="using-multiple-authentication"></a>Verwenden mehrerer Authentifizierungen
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Die Authentifizierung von lokalen Project Server-Benutzern, sei es durch die Windows-Authentifizierung oder die Formularauthentifizierung, erfolgt über die Anspruchsverarbeitung in SharePoint Server 2013. Mehrere Authentifizierung bedeutet, dass die Webanwendung, in der Project Web App bereitgestellt wird, sowohl die Windows-Authentifizierung als auch die formularbasierte Authentifizierung unterstützt. Wenn dies der Fall ist, schlägt ein Aufruf eines ASMX-Webdiensts, der die Windows-Authentifizierung verwendet, mit dem folgenden Fehler fehl, da der Forderungs Prozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:
  
`The server was unable to process the request due to an internal error. . . .`

Um das Problem für ASMX zu beheben, sollten alle Aufrufe der PSI-Methoden für eine abgeleitete Klasse sein, die für jeden PSI-Webdienst definiert ist. Die abgeleitete Klasse muss auch die **SvcLoginWindows. LoginWindows** -Klasse verwenden, um ein Cookie für die abgeleitete PSI-Dienstklasse abzurufen. Im folgenden Beispiel wird die **ProjectDerived** -Klasse von der **SvcProject. Project** -Klasse abgeleitet. Die abgeleitete Klasse fügt die **EnforceWindowsAuth** -Eigenschaft hinzu und überschreibt den Webanforderungs Header für jeden Aufruf einer Methode in der **Project** -Klasse. Wenn die **EnforceWindowsAuth** -Eigenschaft auf **true**festgelegt ist, wird mit der GetWebRequest-Methode eine Kopfzeile hinzugeFügt, die die Formularauthentifizierung deaktiviert. **** Wenn **EnforceWindowsAuth** auf **false festgelegt**ist, kann die Formularauthentifizierung fortgesetzt werden.
  
Um das folgende **ASMXLogon_MultiAuth** -Beispiel zu verwenden, erstellen Sie eine Konsolenanwendung, führen Sie die Schritte unter [Erstellen der Anwendung und Hinzufügen eines Webdienst](#pj15_PrerequisitesASMX_Configure)Verweises aus, und fügen Sie dann die WSDL hinzu. LoginWindows.cs-Proxydatei und die WSDL. Project.cs-Proxydatei. Die **Main** -Methode erstellt die **Project** -Instanz der **ProjectDerived** -Klasse. Das Beispiel muss die abgeleitete **LoginWindowsDerived** -Klasse verwenden, um ein **CookieContainer** -Objekt für das **Projekt abzurufen. CookieContainer** -Eigenschaft, die die Formularauthentifizierung von der Windows-Authentifizierung unterscheidet. Das **Project** -Objekt kann dann verwendet werden, um Aufrufe einer beliebigen Methode in der **SvcProject. Project** -Klasse durchzuführen. 
  
> [!NOTE]
> Der **LoginWindows** -Dienst ist nur für ASMX-Anwendungen in einer Umgebung mit mehreren Authentifizierungen erforderlich. Im **ASMXLogon_MultiAuth** -Beispiel ruft die **GetLogonCookie** -Methode ein Cookie für das **loginWindows** -Objekt ab. Das **Projekt. CookieContainer** -Eigenschaft wird auf den Wert **LoginWindows. CookieContainer** festgelegt. 
  
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

Für Anwendungen, die in einer Umgebung mit mehreren Authentifizierungen ausgeführt werden, ist die Verwendung der abgeleiteten **LoginWindows** -Klasse und das Herstellen von PSI-aufrufen mit einem Webanforderungs Header erforderlich, der die Formularauthentifizierung deaktiviert. Wenn in Project Server nur die Forderungsauthentifizierung verwendet wird, ist es nicht erforderlich, eine Klasse abzuleiten, die einen Webanforderungs Header hinzufügt. Das vorherige Beispiel wird in beiden Umgebungen ausgeführt. 
  
Die Fehlerbehebung für eine WCF-basierte Anwendung ist unterschiedlich. Weitere Informationen finden Sie im Abschnitt *Using Multiple Authentication* in Prerequisites [for WCF-based Code Samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Ändern der Werte Generischer Konstanten
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

Die meisten Beispiele enthalten eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel in Ihrer Umgebung ordnungsgemäß funktioniert. Wenn Sie im folgenden Beispiel SSL installiert haben, verwenden Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen Sie _Server_ Name durch den Namen des Servers, den Sie verwenden. Ersetzen Sie _ProjectServerName_ durch den Namen des virtuellen Verzeichnisses Ihrer Project Server-Website, wie beispielsweise PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, oder andere Voraussetzungen werden oben im Codebeispiel angegeben.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Das Lesen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach. Wenn Sie beispielsweise ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Project Center-Seite in Project Web App angezeigt werden kann.
  
Sie können Codebeispiel Ergebnisse auf verschiedene Weise überprüfen, beispielsweise:
  
- Verwenden Sie den Project Professional 2013-Client, um das Projekt vom Project Server-Computer aus zu öffnen, und zeigen Sie die gewünschten Elemente an.
    
- Zeigen Sie veröffentlichte Projekte auf der Project Center-Seite von Project Web `https://ServerName/ProjectServerName/projects.aspx`app () an.
    
- Anzeigen des Warteschlangen Protokolls in Project Web App. Öffnen Sie die Seite Server Einstellungen (Klicken Sie auf das Symbol **Einstellungen** in der oberen rechten Ecke), und wählen Sie dann **meine Warteschlangenaufträge** im Abschnitt `https://ServerName/ProjectServerName/MyJobs.aspx` **persönliche Einstellungen** () aus. In der Dropdownliste **Ansicht** können Sie nach dem Auftragsstatus sortieren. Der Standardstatus ist **in Arbeit und fehlGeschlagene Aufträge in der letzten Woche**. 
    
- Auf der Seite Server Einstellungen in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) können Sie alle Warteschlangenaufträge verwalten und das Einchecken von Enterprise-Objekten erzwingen. Sie benötigen Administratorberechtigungen für den Zugriff auf diese Links auf der Seite Server Einstellungen.
    
- Verwenden Sie **Microsoft SQL Server Management Studio** zum Ausführen einer Abfrage für eine Tabelle in der Projektdatenbank. Verwenden Sie beispielsweise die folgende Abfrage, um die obersten 200 Zeilen des pub auszuwählen. MSP_WORKFLOW_STAGE_PDPS-Tabelle zum Anzeigen von Informationen zu den Projektdetailseiten (PDPs) in Workflow Stufen. 
    
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

Nachdem Sie einige Codebeispiele getestet haben, gibt es Enterprise-Objekte und Einstellungen, die gelöscht oder zurückgesetzt werden sollen. Sie können die Seite Server Einstellungen in Project Web App verwenden, um Unternehmensdaten zu `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`verwalten (). Links auf der Seite Server Einstellungen können Sie alte Elemente löschen, Eincheck Projekte erzwingen, die Auftragswarteschlange für alle Benutzer verwalten und andere Verwaltungsaufgaben ausführen.
  
NachFolgend finden Sie einige der Links auf der Seite Server Einstellungen, die Sie für typische Bereinigungsaktivitäten nach dem Ausführen von Codebeispielen verwenden können:
  
- **Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**
    
- **Warteschlangenaufträge verwalten**
    
- **Löschen von Enterprise-Objekten**
    
- **Erzwingen des einCheckens von Enterprise-Objekten**
    
- **Enterprise-Projekttypen**
    
- **Workflowphasen**
    
- **Workflowstufen**
    
- **Projektdetailseiten**
    
- **Zeiträume in Zeitberichten**
    
- **Einstellungen und Standardwerte in der Arbeitszeittabelle**
    
- **Linienklassifikationen**
    
Zusätzliche Einstellungen werden von SharePoint Server 2013 für jede Project Web App-Instanz statt von einer bestimmten Project Web App-Server Einstellungsseite verwaltet. Wählen Sie in der Anwendung für die SharePoint-zentral Administration **Allgemeine Anwendungseinstellungen**aus, wählen Sie unter **Project Server-Einstellungen** **Verwalten** aus, und wählen Sie dann die Project Web App-Instanz in der Dropdownliste auf der Seite Server Einstellungen aus. . Wählen Sie beispielsweise **Server seitige Ereignishandler** aus, um Ereignishandler für die ausgewählte Project Web App-Instanz hinzuzufügen oder zu löschen. 
  
## <a name="see-also"></a>Siehe auch
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [VoraussetZungen für WCF-basierte Codebeispiele in Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Identitätswechsel mit WCF verwenden](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md)
- [SharePoint Developer Center](https://msdn.microsoft.com/sharepoint/default.aspx)
    

