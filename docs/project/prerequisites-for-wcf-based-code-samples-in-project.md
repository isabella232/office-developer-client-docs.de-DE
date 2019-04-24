---
title: VoraussetZungen für WCF-basierte Codebeispiele in Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierten Codebeispiele, die in der Project Server-Schnittstelle (PSI)-Referenzthemen enthalten sind.
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357161"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>VoraussetZungen für WCF-basierte Codebeispiele in Project

Informationen zum Erstellen von Projekten in Visual Studio mithilfe der WCF-basierten Codebeispiele, die in der Project Server-Schnittstelle (PSI)-Referenzthemen enthalten sind.
   
Viele der in der [Project Server 2013-Klassenbibliothek und dem Webdienstverweis](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) enthaltenen WCF-basierten Codebeispiele wurden ursprünglich für die Project 2010-Entwicklerdokumentation erstellt und verwenden ein Standardformat für WCF-Webdienste. Die Beispiele funktionieren weiterhin in Project Server 2013 und sind so konzipiert, dass Sie in eine Konsolenanwendung kopiert und als vollständige Einheit ausgeführt werden können. Im Beispiel werden Ausnahmen angegeben. 
  
Code Beispiele in der Project 2013-Entwicklerdokumentation, die nicht in den für Office Project Server 2007 entwickelten Beispielen verwendet werden, verwenden ASMX-Webdienste. Die ASMX-basierten Beispiele können auch zur Verwendung von WCF-Diensten angepasst werden. In diesem Artikel wird gezeigt, wie Sie die Beispiele mit WCF-Diensten verwenden. Informationen zur Verwendung der Beispiele mit ASMX-Webdiensten finden Sie unter [vorausSetzungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Wenn das clientseitige Objektmodell (CSOM) die Methoden enthält, die für Ihre Anwendung erforderlich sind, sollten neue Anwendungen mit dem CSOM entwickelt werden. Die CSOM ermöglicht es Anwendungen, mit Project Online oder einer lokalen Installation von Project Server 2013 zu arbeiten. Wenn Ihre Anwendung die PSI verwendet, sollte Sie andernfalls die WCF-Schnittstelle verwenden, bei der es sich um die Technologie handelt, die wir für die Netzwerkkommunikation empfehlen. Anwendungen, die die ASMX-Schnittstelle oder die WCF-Schnittstelle verwenden, können nur für lokale Installationen von Project Server 2013 funktionieren. 
>
> Weitere Informationen zu CSOM finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md) und [Client seitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Bevor Sie die Codebeispiele verwenden, müssen Sie die Entwicklungsumgebung einrichten, die Anwendung konfigurieren, eine Dienstkonfigurationsdatei hinzufügen (oder die WCF-Dienste programmgesteuert konfigurieren) und generische Konstante Werte entsprechend Ihrer Umgebung ändern.
  
## <a name="setting-up-the-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Richten Sie ein Test Project Server-System ein.**
    
    Verwenden Sie ein Test Project Server-System, wenn Sie entwickeln oder testen. Auch wenn Ihr Code einwandfrei funktioniert, können interprojekt-Abhängigkeiten, Berichte oder andere Umgebungsfaktoren unbeabsichtigte Konsequenzen verursachen. 
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie ein gültiger Benutzer auf dem Server sind, und überprüfen Sie, ob Sie über ausreichende Berechtigungen für die PSI-Aufrufe verfügen, die Ihre Anwendung verwendet. Das Themaentwickler Dokumentation für jede PSI-Methode enthält eine Project Server Permissions-Tabelle. Die [Project. QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) -Methode erfordert beispielsweise die globale **Neuprojekt** -Berechtigung und die **SaveProjectTemplate** -Berechtigung. 
  
    In einigen Fällen müssen Sie möglicherweise das Remote Debugging auf dem Server durchführen. Möglicherweise müssen Sie auch einen Ereignishandler einrichten, indem Sie auf jedem Project Server-Computer in der SharePoint-Farm eine Ereignishandler-Assembly installieren und dann den Ereignishandler für die Project Web App-Instanz mithilfe der Project Server-Einstellungsseite im allgemeinen konfigurieren. Anwendungseinstellungen der SharePoint-zentral Administration.
    
2. **Richten Sie einen Entwicklungscomputer ein.**
    
    Sie greifen in der Regel über ein Netzwerk auf das PSI zu. Die Codebeispiele sind so konzipiert, dass Sie auf einem Client ausgeführt werden, der vom Server getrennt ist, sofern nicht angegeben.
    
    1. **Installieren Sie die richtige Version von Visual Studio.** Sofern nicht angegeben, werden die Codebeispiele in Visual C# geschrieben. Sie können mit Visual Studio 2010 oder Visual Studio 2012 verwendet werden. Stellen Sie sicher, dass das neueste Service Pack installiert ist. 
    
    2. **Kopieren Sie Project Server-DLLs auf den Entwicklungscomputer.** Kopieren Sie die folgenden Assemblys `[Program Files]\Microsoft Office Servers\15.0\Bin` von auf dem Project Server-Computer auf den Entwicklungscomputer: 
    
       - Microsoft. Office. Project. Server. Events. Receivers. dll
    
       - Microsoft. Office. Project. Server. Library. dll
    
    3. Informationen zum Kompilieren und Verwenden der Proxy-Assembly ProjectServerServices. dll für die WCF-Dienste in der PSI finden Sie unter [using a PSI Proxy Assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Installieren Sie die IntelliSense-Dateien.**
    
    Um IntelliSense-Beschreibungen für Klassen und Member in Project Server-Assemblys zu verwenden, kopieren Sie die aktualisierten IntelliSense-XML-Dateien aus dem Project 2013 SDK-Download in das Verzeichnis, in dem sich die Project Server-Assemblys befinden. Kopieren Sie beispielsweise die Datei Microsoft. Office. Project. Server. Library. XML in das Verzeichnis, in dem Ihre Anwendung einen Verweis auf die Microsoft. Office. Project. Server. Library. dll-Assembly festlegen soll.
    
    Die IntelliSense-Beschreibungen für die PSI-Dienste erfordern das Erstellen einer PSI-Proxy-Assembly mithilfe des CompileWCFProxyAssembly. cmd `Documentation\IntelliSense\WCF` -Skripts im Unterverzeichnis des Project 2013 SDK-Downloads. Das Skript erstellt die WCF-basierte Proxy-Assembly ProjectServerServices. dll. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense]. MHT im SDK-Download. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Erstellen der Anwendung und Hinzufügen eines Dienstverweises
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Erstellen Sie eine Konsolenanwendung.**
    
    Wenn Sie eine Konsolenanwendung erstellen, wählen Sie in der Dropdownliste des Dialogfelds **Neues Projekt** **.NET Framework 4**aus. Sie können den PSI-Beispielcode in die neue Anwendung kopieren.
    
2. **Fügen Sie für WCF erforderliche Verweise hinzu.**
    
    Fügen Sie im Projektmappen-Explorer einen Verweis auf **System. ServiceModel** hinzu (siehe Abbildung 1). Eine Webanwendung würde **System. ServiceModel. Web**verwenden.
    
    Fügen Sie auch einen Verweis auf **System. Runtime. Serialization**hinzu.
    
    **Abbildung 1. Hinzufügen der Verweise in Visual Studio für eine WCF-basierte Anwendung**

    ![Hinzufügen von Verweisen für WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Hinzufügen von Verweisen für WCF")
  
3. **Kopieren Sie den Code**.
    
    Kopieren Sie das vollständige Codebeispiel in die Program.cs-Datei der Konsolenanwendung.
    
4. **Legen Sie den Namespace für die Beispielanwendung fest.**
    
    Sie können entweder den oben im Beispiel aufgeführten Namespace in den Standardnamespace der Anwendung ändern oder den Standard Anwendungs Namespace so ändern, dass er mit dem Beispiel übereinstimmt. Sie können den Standard Anwendungs Namespace ändern, indem Sie die Anwendungseigenschaften ändern. 
    
    Das Codebeispiel für [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) verfügt beispielsweise über den Namespace **Microsoft. SDK. Project. Samples. CreateResourceTest**. Wenn der Name des Visual Studio-Projekts **ResourceTest**ist, kopieren Sie den Namespace aus der Program.cs-Datei, und öffnen Sie dann den Bereich Projekt **Eigenschaften** (Klicken Sie im Menü **Projekt** auf **ResourceTest Eigenschaften**). Kopieren Sie auf der Registerkarte **Anwendung** den Namespace in das Textfeld **Standardnamespace** . 
    
5. **Legen Sie die Dienstverweise fest.**
    
    Viele Beispiele erfordern einen Verweis auf einen oder mehrere PSI-Dienste. Diese werden im Beispiel selbst oder in Kommentaren aufgeführt, die dem Beispiel vorangestellt sind. Um den richtigen Namespace der Dienstverweise abzurufen, stellen Sie sicher, dass Sie zuerst den Standard Anwendungs Namespace festlegen.
    
    Es gibt drei Möglichkeiten zum Hinzufügen eines WCF-Dienstverweises:
    
    - Erstellen Sie eine PSI-Proxy-Assembly mit dem Namen ProjectServerServices. dll, und legen Sie dann einen Verweis auf die Assembly fest. Weitere Informationen finden Sie unter [using a PSI Proxy Assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Fügen Sie der Visual Studio-Projektmappe eine Proxydatei aus der Ausgabe von Svcutil. exe hinzu. Weitere Informationen finden Sie unter [Hinzufügen einer PSI-Proxydatei](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Hinzufügen eines Dienstverweises mithilfe von Visual Studio. Weitere Informationen finden Sie unter [Hinzufügen eines Dienst](#pj15_PrerequisitesWCF_AddingServiceReference)Verweises.
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Verwenden einer PSI-Proxy-Assembly und IntelliSense-Beschreibungen
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Sie können eine Proxy Assembly für alle öffentlichen WCF-Dienste in der PSI verwenden. Kompilieren Sie die ProjectServerServices. dll-Proxy Assembly mithilfe `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` des Skripts im Project 2013 SDK-Download, und kopieren Sie dann die Proxy Assembly auf Ihren Entwicklungscomputer. Kopieren Sie die Datei ProjectServerServices. XML für IntelliSense an denselben Speicherort. Legen Sie in Visual Studio einen Verweis auf die Proxy Assembly ProjectServerServices. dll fest. 
  
Für Project Server Service Packs und Updates können Sie die Proxy Quelldateien aktualisieren und eine neue Proxy Assembly mithilfe des GenWCFProxyAssembly. cmd-Skripts im gleichen SDK-Downloadordner erstellen. Einen Link zum SDK-Download finden Sie unter [Project 2013 Developer Documentation](project-2013-developer-documentation.md). Weitere Informationen finden Sie im Abschnitt [Hinzufügen eines Dienst](#pj15_PrerequisitesWCF_AddingServiceReference) Verweises. 
  
> [!NOTE]
> Wenn Sie die Proxy Quelldateien aus der ZIP-Datei extrahieren, sind die Dateien im `Documentation\IntelliSense\WCF\Source` Ordner ab dem Veröffentlichungsdatum des Project 2013 SDK-Downloads aktuell. Um aktualisierte PSI-Proxy-Quelldateien zu generieren, führen Sie das Skript GenASMXProxyAssembly. cmd auf dem Project Server-Computer aus. Weitere Informationen finden Sie unter [Hinzufügen eines Dienst](#pj15_PrerequisitesWCF_AddingServiceReference)Verweises. 
> 
> Die Skripts im `Documentation\IntelliSense\ASMX` Ordner funktionieren nicht für WCF-basierte Anwendungen. Das Skript GenASMXProxyAssembly. cmd ruft WSDL. exe auf, das Quellcodedateien für die ASMX-Dienste generiert. Die ASMX-Proxydateien schließen unterschiedliche Klassen und Eigenschaften ein. Der ASMX-basierte Ressourcen-Webdienst enthält beispielsweise die **Ressourcen** Klasse, während der WCF-basierte Ressourcendienst die **Ressourcen** Schnittstelle, die **ResourceChannel** -Schnittstelle und die **ResourceClient** -Klasse umfasst. 
  
Die für die ASMX-Webdienste und die WCF-Dienste erstellten willkürlichen Namespaces sind identisch, sodass die Datei ProjectServerServices. XML für IntelliSense mit beiden Assemblys funktioniert. Beispielsweise ist der Namespace des Ressourcen Diensts in der WCF-basierten Proxy Assembly und in der ASMX-basierten Proxy Assembly **SvcResource**. Sie können die Namespacenamen natürlich ändern, wenn Sie sicherstellen, dass Sie in der Proxy-Assembly und in der IntelliSense-Datei ProjectServerServices. XML übereinstimmen.
  
Wenn ein Codebeispiel einen anderen Namen für einen PSI-Dienstnamespace verwendet (beispielsweise **ProjectWebSvc**), müssen Sie das Beispiel so ändern, dass **SvcProject** verwendet wird, damit der Namespace mit der Proxy Assembly übereinstimmt. 
  
Zu den Vorteilen der WCF-basierten Proxy Assembly gehört Folgendes:
  
- Sie können die meisten Lösungen mit der Proxy-Assembly auf einem anderen Computer als dem Project Server-Computer entwickeln. Das Festlegen eines einzelnen Dienstverweises erfordert die Entwicklung auf dem Project Server-Computer.
    
- Die Proxy Assembly enthält alle PSI-Dienst-Namespaces, sodass Sie nicht mehrere Proxydateien hinzufügen müssen.
    
- Wenn Sie die Datei ProjectServerServices. XML dem gleichen Verzeichnis hinzufügen, in dem Sie einen Verweis auf die ProjectServerServices. dll-Proxy Assembly festlegen, können Sie IntelliSense-Beschreibungen für die PSI-Klassen und-Member abrufen. Weitere Informationen finden Sie in der Datei [ReadMe_IntelliSense] im `Documentation\IntelliSense` Ordner des Project 2013 SDK-Downloads. 
    
**Abbildung 2. Verwenden von IntelliSense für eine Methode im Ressourcendienst**

![Verwenden von IntelliSense für die ReadResource-Methode] (media/pj15_PrerequisitesWCF_Intellisense.gif "Verwenden von IntelliSense für die ReadResource-Methode")
  
Nachteile der Verwendung der Proxy-Assembly sind, dass die Lösung größer ist und Sie die Proxy Assembly mit der Lösung verteilen und installieren müssen. Sie müssen auch die gleichen Namespaces verwenden, die sich in der Proxy Assembly und den IntelliSense-Dateien befinden, es sei denn, Sie ändern das Skript zum Erstellen einer Proxy Assembly und ändern die Datei ProjectServerServices. XML, um verschiedene Namespaces zu verwenden.
  
### <a name="adding-a-psi-proxy-file"></a>Hinzufügen einer PSI-Proxydatei
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Der Project 2013 SDK-Download enthält die Quelldateien, die vom Befehl SvcUtil. exe für die Proxy Assembly generiert werden. Die Quelldateien befinden sich in der Datei "Source. zip `Documentation\IntelliSense\WCF` " im Unterverzeichnis. Anstatt einen Verweis auf die Proxy-Assembly festzulegen, können Sie einer Visual Studio-Lösung eine oder mehrere Quelldateien hinzufügen. Um beispielsweise den Project-Dienst und den Ressourcendienst zu verwenden, fügen Sie den WCF hinzu. Project.cs und WCF. Resource.cs-Dateien für die Lösung. 
  
In WCF wird die primäre Klasse in jedem PSI-Dienst durch eine Schnittstelle definiert und in einer Clientklasse für den Zugriff auf die Member implementiert. Beispielsweise ist die **SvcProject. Resource** -Schnittstelle in der **SvcProject. ResourceClient** -Klasse implementiert. Um ein **ResourceClient** -Objekt als Klassenvariable namens **ResourceClient**zu definieren, verwenden Sie beispielsweise den folgenden Code. Im Beispiel erstellt die **SetClientEndpoints** -Methode ein **resourceClient** -Objekt, das den **basicHttp_Project** -Endpunkt verwendet, der in der Datei app. config definiert ist. Weitere Informationen zur Datei app. config finden Sie im Abschnitt [Hinzufügen einer Dienstkonfigurationsdatei](#pj15_PrerequisitesWCF_AddConfig) . 
  
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
> Unabhängig davon, ob Sie eine PSI-Proxy-Assembly verwenden oder eine Proxydatei für einen Project-Dienstverweis namens **SvcResource**hinzufügen, würden Sie denselben Code zum Erstellen und Freigeben eines **resourceClient** -Objekts verwenden. 
  
### <a name="adding-a-service-reference"></a>Hinzufügen eines Serviceverweises
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Wenn Sie die WCF-basierte Proxy-Assembly nicht verwenden oder eine Proxydatei für einen PSI-Dienst hinzufügen, können Sie einen oder mehrere einzelne Dienstverweise direkt in Visual Studio festlegen. Sie können auch Schritt 1 des folgenden Verfahrens verwenden, um aktualisierte Proxydateien zu erstellen, um das `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` Skript vorzubereiten, das im Project 2013 SDK-Download enthalten ist. 
  
> [!NOTE]
> Zum Festlegen eines Dienstverweises müssen Sie Visual Studio auf dem Project Server-Computer verwenden. Es wird empfohlen, dass Sie die Proxy Assembly ProjectServerServices. dll verwenden oder Proxy Quelldateien hinzufügen, anstatt Dienstverweise direkt in Visual Studio hinzuzufügen. 
  
In den folgenden Schritten wird gezeigt, wie Sie einen Dienstverweis mithilfe von Visual Studio 2012 auf einem Computer mit einer Testinstallation von Project Server festlegen:
  
1. Führen Sie Visual Studio auf dem Project Server-Computer aus, um Zugriff auf die Back-End-WCF-Dienste zu erhalten.
    
2. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann **Dienstverweis hinzufügen**aus. 
    
3. Geben Sie im Dialogfeld **Dienstverweis hinzufügen** im **Textfeld Adresse** den Namen https://localhost:32843/ _GUID_/PSI/ _Service_Name. svc ein, und drücken Sie dann die **Eingabe**Taste. Ersetzen Sie _GUID_ durch den Namen des virtuellen Verzeichnisses der Project Server-Dienstanwendung, beispielsweise 534c37eb00d74ccfadcecf9827e95239. Ersetzen Sie _Service_ Name durch den Namen des Diensts, beispielsweise Resource (siehe Abbildung 3). 
    
   Sie können den Namen des virtuellen Verzeichnisses des Project Server-Diensts auf eine der folgenden Arten abrufen:
    
   - Öffnen Sie die SharePoint 2013-Zentraladministrationsanwendung in Ihrem Browser. Wählen Sie **Dienstanwendungen verwalten**aus, und wählen Sie dann die gewünschte Project Server-PSI-Dienstanwendung aus. Wählen Sie beispielsweise **ProjectServerService**aus. Die URL der Seite Project Web App-Websites verwalten enthält den Namen des virtuellen Verzeichnisses. In `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`wird beispielsweise der Name des virtuellen Verzeichnisses `534c37eb00d74ccfadcecf9827e95239` (der Verzeichnisname enthält keine Striche). 
    
   - Öffnen Sie das Dialogfeld **Internet Informationsdienste-Manager (IIS)** auf dem Project Server-Computer. Erweitern Sie im Bereich **Verbindungen** den Knoten **sharePoint-** Webdienste, und erweitern Sie dann die virtuellen Dienst Verzeichnisse darunter, bis Sie das Verzeichnis mit dem PSI-Ordner gefunden haben. Wählen Sie das Verzeichnis aus, wählen Sie **Erweiterte Einstellungen** im Bereich **Aktionen** aus, und kopieren Sie dann den Verzeichnisnamen in das Feld **virtueller Pfad** . 
    
      > [!NOTE]
      > Es kann mehr als ein virtuelles Verzeichnis des Project Server-Diensts geben. Stellen Sie sicher, dass Sie das virtuelle Verzeichnis auswählen, das die gewünschte Project Web App-Instanz enthält. 
  
   - Verwenden Sie das Cmdlet **Get-SPServiceApplication** in Windows PowerShell, das mit sharepoint 2013 installiert ist. Klicken Sie im **Startmenü** der Taskleiste auf **Alle Programme**, wählen sie **Microsoft SharePoint 2013 Produkte**aus, und wählen Sie dann **SharePoint 2013 Management Shell**aus. Es folgt der Befehl und die Ergebnisse im Fenster **SharePoint-2013get-Verwaltungsshell** für die definierten Dienstanwendungen (Ihre GUIDs sind unterschiedlich). Kopieren Sie die GUID für die Project Server-Dienstanwendung. 
    
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

      Wenn Sie den vollständigen Namen der Project Server-Dienstanwendung kennen, können Sie ihn zum Abrufen des GUID-Werts verwenden, zum Beispiel:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Entfernen Sie die Striche in der GUID, um den Namen des virtuellen Verzeichnisses abzurufen. 
  
   URLs wie `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` sind Standard für Project Server-Dienste. 
    
4. Nachdem der Dienstverweis aufgelöst wurde, geben Sie den Verweisnamen in das Textfeld **Namespace** ein. Code Beispiele in der Project 2013-Entwicklerdokumentation verwenden den willkürlichen Namespacenamen **svc _Service_** Name. Der Ressourcendienst in den Codebeispielen heißt beispielsweise **SvcResource**.
    
    **Abbildung 3. Hinzufügen der WCF-basierten Ressourcendienst Referenz**

    ![Hinzufügen der WCF-basierten Ressourcendienst Referenz] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Hinzufügen der WCF-basierten Ressourcendienst Referenz")
  
5. Ersetzen Sie die temporäre Web. config-Datei im Project-Dienstverzeichnis durch die ursprüngliche (in Web. config umbenannt), und `iisreset`führen Sie dann eine erneute Ausführung aus.
    
## <a name="setting-other-references"></a>Festlegen anderer Verweise
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Project Server-Anwendungen verwenden häufig andere Dienste wie SharePoint 2013-Webdienste. Wenn andere Dienste oder Verweise erforderlich sind, werden Sie im Codebeispiel notiert.
  
Lokale Verweise für das Codebeispiel werden in **using** -Anweisungen am Anfang des Beispiels aufgeführt. 
  
1. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Ordner **Verweise** , und wählen Sie dann **Verweis hinzufügen**aus.
    
2. Klicken Sie auf **Durchsuchen**, und navigieren Sie dann zu dem Speicherort, an dem Sie die Project Server-DLLs gespeichert haben, die Sie zuvor kopiert haben. Wählen Sie die gewünschten DLLs aus, und klicken Sie dann auf **OK**.
    
> [!NOTE]
> Stellen Sie sicher, dass die Assemblyversion auf dem Entwicklungscomputer genau mit denen auf dem Ziel-Project Server-Computer übereinstimmen. 
  
## <a name="adding-a-service-configuration-file"></a>Hinzufügen einer Dienstkonfigurationsdatei
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Wenn eine Anwendung die WCF-Dienste programmgesteuert konfiguriert, wird keine Dienstkonfigurationsdatei verwendet. Andernfalls verwendet eine Windows-Anwendung oder Konsolenanwendung das **System. ServiceModel** -Element in einer Datei app. config; eine Webanwendung enthält **System. ServiceModel** in Web. config. Weitere Informationen zur Verwendung einer Datei app. config oder Programmgesteuertes Konfigurieren der WCF-Dienste finden Sie unter [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mit WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Beim Generieren einer Dienstproxy-Quelldatei erstellt der Befehl SvcUtil. exe auch eine Datei Output. config, die die Grundlage für das standardmäßige **System. ServiceModel** -Element in einer Datei app. config oder Web. config darstellt. Der Project 2013 SDK-Download enthält eine Beispieldatei Output. config `Documentation\IntelliSense\WCF\Source.zip`in. Die Standarddatei Output. config, die von SvcUtil. exe für den Ressourcendienst erstellt wird, umfasst beispielsweise zwei Bindungen mit dem Namen **BasicHttpBinding_Resource** und **BasicHttpBinding_Resource1**. Das **Client** -Element enthält zwei Standardendpunkte. Ein Endpunkt ist für den sicheren Zugriff auf die HTTP-Adresse an Anschluss 32843 und der andere für den normalen Zugriff auf Anschluss 32843 wie folgt: 
  
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

Bei der PSI-Dienstkonfiguration werden nicht die Standardbindungen und-Endpunkte verwendet. Project Server erfordert, dass Anwendungen auf PSI-Dienste über den Front-End-ProjectServer. svc zugreifen, der als Router für Aufrufe an die Back-End-Dienste fungiert. Führen Sie die folgenden Schritte aus, um die Datei "App. config" zu erstellen:
  
1. Wenn Sie einen Verweis auf die Proxy-Assembly ProjectServerServices. dll festlegen oder die Proxy Quelldatei für einen Dienst hinzufügen, enthält die Anwendung keine app. config-Datei. Fügen Sie dem Visual Studio-Projekt ein neues Element hinzu. Wählen Sie im Dialogfeld **Neues Element hinzufügen** die Vorlage **Anwendungskonfigurationsdatei** aus, nennen Sie Sie App. config, und wählen Sie dann **Hinzufügen**aus.
    
2. Löschen Sie den gesamten Text in der Datei "App. config", und kopieren Sie den folgenden Code in die Datei. Sie können die gleiche Bindung beispielsweise `basicHttpConf`für jeden Dienstendpunkt verwenden. Wenn Sie mehr als eine Bindung verwenden möchten, um beispielsweise sowohl HTTP-als auch HTTPS-Protokolle zu binden, müssen Sie für jedes Protokoll eine Bindung erstellen.
    
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

3. Ersetzen `ServerName/ProjectServerName` Sie in der Clientendpunkt Adresse durch den Namen Ihrer Server-und Project Web App-Instanz. 
    
4. Ersetzen `ServiceName` Sie durch den Namen des PSI-Diensts, beispielsweise Resource. Stellen Sie sicher, dass Sie alle drei Instanzen des Dienst namens ersetzen, zum Beispiel:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Um mehr als einen PSI-Dienst zu verwenden, erstellen Sie ein **EndPoint** -Element für jeden Dienst und für jedes **Bindungs** Element, das von Dienst verwendet wird. Die folgenden Endpunkte konfigurieren beispielsweise den Client für die Verwendung der standardmäßigen HTTP-Bindung für den Project-Dienst und den Queue System-Dienst. 
    
    > [!NOTE]
    > Wenn Sie eine Anwendung ausführen und eine Fehlermeldung erhalten, dass der Server zu beschäftigt ist oder dass die HTTP-Anforderung nicht autorisiert ist, stellen Sie sicher, dass die Endpunktadressen in der Datei "App. config" korrekt sind. 
  
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

Sie können eine Datei app. config mithilfe des **WCF-Dienst Konfigurations-Editors** in Visual Studio (im Menü **Extras** ) bearbeiten. Abbildung 4 zeigt, wie Sie das **Contract** -Element im Dialogfeld **Konfigurations-Editor für Microsoft-Dienst** festlegen. Wenn die Lösung die PSI-Proxy-Assembly verwendet, öffnen Sie ProjectServerServices. dll `bin\debug` im Verzeichnis der Visual Studio-Projektmappe. Im Dialogfeld **vertragsTyp Browser** werden alle WCF-Dienstverträge angezeigt (siehe Abbildung 5). 
  
**Abbildung 4. Verwenden des WCF-Dienst Konfigurations-Editors**

![Verwenden des WCF-Dienst Konfigurations-Editors] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Verwenden des WCF-Dienst Konfigurations-Editors")
  
Wenn die Lösung eine Dienstproxy Datei wie wcfResource.cs verwendet, kompilieren Sie die Anwendung, und öffnen Sie dann die ausführbare Datei im `bin\debug` Verzeichnis. Weitere Informationen zum Bearbeiten der Datei "App. config" finden Sie unter [Exemplarische Vorgehensweise: Entwickeln von PSI-Anwendungen mit WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Abbildung 5. Verwenden des Vertragstyp Browsers im WCF-Dienst Konfigurations-Editor**

![Verwenden des vertragsTyp Browsers] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Verwenden des vertragsTyp Browsers")
  
## <a name="using-multiple-authentication"></a>Verwenden mehrerer Authentifizierungen
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Die Authentifizierung von lokalen Project Server-Benutzern, sei es durch die Windows-Authentifizierung oder die Formularauthentifizierung, erfolgt über die Anspruchsverarbeitung in SharePoint. Mehrere Authentifizierung bedeutet, dass die Webanwendung, in der Project Web App bereitgestellt wird, sowohl die Windows-Authentifizierung als auch die formularbasierte Authentifizierung unterstützt. Wenn dies der Fall ist, schlägt jeder Aufruf eines WCF-Diensts, der die Windows-Authentifizierung verwendet, mit dem folgenden Fehler fehl, da der Forderungs Prozess nicht bestimmen kann, welcher Benutzertyp authentifiziert werden soll:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Um das Problem für WCF zu beheben, sollten alle Aufrufe an PSI-Methoden innerhalb einer **OperationContextScope** sein, die für jeden PSI-Dienst definiert ist. Schachteln Sie keine Bereiche für mehrere Dienste; Wenn Sie beispielsweise Aufrufe der Ressourcen-und Projektdienste verwenden, sollte sich jeder Satz von Anrufen innerhalb seines eigenen Bereichs befinden. 
  
Im folgenden Beispiel kann die **DisableFormsAuth** -Methode von jedem **OperationContextScope** -Abschnitt in einer Anwendung aufgerufen werden. Die-Methode entfernt alle Headerwerte, die zuvor die Formularauthentifizierung deaktiviert haben, sodass die Formularauthentifizierung fortgesetzt werden kann, wenn der _isWindowsAuth_ -Parameter auf **false festgelegt**ist. Wenn _isWindowsAuth_ ist ****, deaktiviert die **DisableFormsAuth** -Methode die Formularauthentifizierung. 
  
In der **WcfSample** -Methode ist das **projectClient** -Objekt eine Instanz der PSI- **SvcProject. projectClient** -Klasse. 
  
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
> Das tätigen von PSI-Anrufen innerhalb eines **OperationContextScope** ist nur für Anwendungen erforderlich, die in einer Umgebung mit mehreren Authentifizierung ausgeführt werden. Wenn in Project Server nur die Windows-Authentifizierung verwendet wird, ist es nicht erforderlich, einen Bereich festzulegen und einen Webanforderungs Header hinzuzufügen, der die Formularauthentifizierung deaktiviert. 
> 
> Die Fehlerbehebung für eine ASMX-basierte Anwendung ist unterschiedlich. Weitere Informationen finden Sie im Abschnitt *Using Multiple Authentication* in Prerequisites [for ASMX-based Code Samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Ändern von Werten generischer Konstanten
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

Die meisten Beispiele enthalten eine oder mehrere Variablen, die Sie aktualisieren müssen, damit das Beispiel in Ihrer Umgebung ordnungsgemäß funktioniert. Wenn Sie im folgenden Beispiel SSL installiert haben, verwenden Sie das HTTPS-Protokoll anstelle des HTTP-Protokolls. Ersetzen Sie _Server_ Name durch den Namen des Servers, den Sie verwenden. Ersetzen Sie _ProjectServerName_ durch den Namen des virtuellen Verzeichnisses Ihrer Project Server-Website, wie beispielsweise PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Alle anderen Variablen, die Sie ändern müssen, werden oben im Codebeispiel notiert.
  
## <a name="verifying-the-results"></a>Überprüfen der Ergebnisse
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Das Lesen und Interpretieren von Ergebnissen aus einem Codebeispiel ist nicht immer einfach. Wenn Sie beispielsweise ein Projekt erstellen, müssen Sie das Projekt veröffentlichen, bevor es auf der Project Center-Seite in Project Web App angezeigt werden kann.
  
Sie können Codebeispiel Ergebnisse auf verschiedene Weise überprüfen, beispielsweise:
  
- Verwenden Sie den Project Professional 2013-Client, um das Projekt vom Project Server-Computer aus zu öffnen, und zeigen Sie die gewünschten Elemente an.
    
- Zeigen Sie veröffentlichte Projekte auf der Project Center-Seite von Project Web `https://ServerName/ProjectServerName/projects.aspx`app () an.
    
- Anzeigen des Warteschlangen Protokolls in Project Web App. Öffnen Sie die Seite Server Einstellungen (Klicken Sie auf das Symbol **Einstellungen** in der oberen rechten Ecke), und wählen Sie dann **meine Warteschlangenaufträge** im Abschnitt `https://ServerName/ProjectServerName/MyJobs.aspx` **persönliche Einstellungen** () aus. In der Dropdownliste **Ansicht** können Sie nach dem Auftragsstatus sortieren. Der Standardstatus ist **in Arbeit und fehlGeschlagene Aufträge in der letzten Woche**. 
    
- Auf der Seite Server Einstellungen in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) können Sie alle Warteschlangenaufträge verwalten und das Einchecken von Enterprise-Objekten erzwingen. Sie benötigen Administratorberechtigungen für den Zugriff auf diese Links auf der Seite Server Einstellungen.
    
- Verwenden Sie **Microsoft SQL Server Management Studio** zum Ausführen einer Abfrage für eine Tabelle einer Project Server-Datenbank. Verwenden Sie beispielsweise die folgende Abfrage, um die obersten 200 Zeilen der MSP_WORKFLOW_STAGE_PDPS-Tabelle auszuwählen, um Informationen zu den Projektdetailseiten (PDPs) in Workflow Phasen anzuzeigen. 
    
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

Nachdem Sie einige Codebeispiele getestet haben, gibt es Enterprise-Objekte und Einstellungen, die gelöscht oder zurückgesetzt werden sollen. Sie können die Seite Server Einstellungen in Project Web App verwenden, um Unternehmensdaten zu `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`verwalten (). Links auf der Seite Server Einstellungen können Sie alte Elemente löschen, Eincheck Projekte erzwingen, die Auftragswarteschlange für alle Benutzer verwalten und andere Verwaltungsaufgaben ausführen.
  
NachFolgend finden Sie einige der Links auf der Seite Server Einstellungen, die für typische Bereinigungsaktivitäten nach dem Ausführen von Codebeispielen verwendet werden:
  
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

- [VoraussetZungen für ASMX-basierte Codebeispiele in Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Exemplarische vorGehensWeise: Entwickeln von PSI-Anwendungen mit WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Identitätswechsel mit WCF verwenden](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md) 
- [SharePoint Developer Center](https://msdn.microsoft.com/sharepoint/default.aspx)
    

