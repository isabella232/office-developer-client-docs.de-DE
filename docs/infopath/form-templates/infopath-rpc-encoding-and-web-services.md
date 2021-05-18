---
title: InfoPath, RPC-Codierung und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Webdienste können eine von zwei Formatvorlagen für die Bindung an ihre Webmethoden im Web Service Description Language (WSDL)-Vertrag verfügbar machen, der sie beschreibt: Dokument oder RPC.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303528"
---
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, RPC-Codierung und Webdienste

Webdienste können eine von zwei Formatvorlagen für die Bindung an ihre Webmethoden im Web Service Description Language (WSDL)-Vertrag verfügbar machen, der sie beschreibt: Dokument oder RPC. Darüber hinaus können diese beiden Bindungstypen als literal oder encoded angegeben werden. Die gängigsten Implementierungen für die beiden Bindungstypen sind: "document/literal" und "RPC/encoded". Microsoft InfoPath unterstützt jedoch nur die Verbindung mit Webdiensten, die die Dokument-/Literalformatvorlage verwenden.
  
Die meisten Webdienst-Bereitstellungstools weisen eine Option auf, mit der Sie angeben können, welche Art von Webdienst Sie erstellen möchten. Wenn Sie einen Webdienst entwickeln, mit dem Sie eine Verbindung von InfoPath herstellen, sollten Sie Dokument/Literal als Stil und Codierung ihres Webdiensts angeben.
  
Wenn Sie allerdings den Webdienst, den Sie verwenden möchten, nicht kontrollieren und eine Verbindung mit einem Webdienst vom Typ "RPC/encoded" herstellen müssen, können Sie mithilfe eines .NET-Proxydiensts eine Verbindung mit einem Webdienst vom Typ "RPC/encoded" herstellen.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Herstellen einer Verbindung mit einem Webdienst mithilfe eines .NET-Proxydiensts

Wenn Sie den Webdienst vom Typ "RPC/encoded", den Sie verwenden möchten, nicht kontrollieren, können Sie einen Microsoft .NET-Proxywebdienst vom Typ "document/literal" erstellen, der Wrapperfunktionen für alle Webmethoden bereitstellt, die Sie im Webdienst vom Typ "RPC/encoded" aufrufen möchten. Anschließend können Sie den Proxywebdienst vom Typ "document/literal" in InfoPath verwenden.
  
.NET Framework-Code kann für jeden Webdienst ("RPC/encoded" und "document/literal") verwendet werden, und alle .NET-Webdienste verwenden den Typ und die Codierung "document/literal". Da .NET Framework mit jeder Art von Webdienst kommunizieren kann, können Sie einen .NET-Webdienst erstellen, der Methoden zum Aufrufen des Webdiensts vom Typ "RPC/encoded" aufweist. Der .NET-Webdienst dient als Übersetzungsmodul, damit InfoPath Aufrufe vom Typ "document/literal" für den .NET-Webdienst ausführen kann, der wiederum Aufrufe vom Typ "RPC/encoded" für den ursprünglichen Webdienst ausführen kann.
  
Die Voraussetzungen zum Erstellen eines solchen Microsoft .NET-Proxywebdiensts sind ein Computer unter Microsoft Windows oder Microsoft Windows Server, auf dem Internetinformationsdienste (IIS) mit installiertem ASP.NET ausgeführt werden und auf dem der Proxywebdienst bereitgestellt wird. Wenn Sie eine InfoPath-Lösung erstellen, verweisen Sie nicht auf den Webdienst vom Typ "RPC/encoded", sondern auf den Proxywebdienst. Der Proxywebdienst führt dann Aufrufe für den Webdienst vom Typ "RPC/encoded" aus.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Erstellen eines Proxywebdiensts mithilfe von Visual Studio

1. Erstellen Sie ein neues Projekt **ASP.NET-Webdienstanwendung**. 
    
2. Klicken Sie **im Projektmappen-Explorer** mit der rechten Maustaste auf den Ordner **Verweise** ihres neuen Projekts, und klicken Sie dann **auf Webreferenz hinzufügen.** 
    
3. Geben Sie im Dialogfeld **Webverweis hinzufügen** die URL des Webdiensts vom Typ "RPC/encoded" ein, den Sie verwenden möchten, und klicken Sie dann auf **Weiter**.
    
4. Click **Add Reference**. 
    
5. Öffnen Sie die ASMX-Datei für Ihren Webdienst, und fügen Sie eine Webdienstmethode zum Aufrufen jeder Webdienstmethode im referenzierten Webdienst vom Typ "RPC/encoded" hinzu.
    
6. Öffnen Sie das Fenster **Klassenansicht**, um eine Liste der Methoden auf dem Referenzwebserver vom Typ "RPC/encoded" anzuzeigen. Für jede Webdienstmethode werden drei Methoden angezeigt. Wenn beispielsweise die Webdienstmethode aufgerufen wird, werden drei Methoden  `doSearch` namens  `doSearch` , und  `BegindoSearch`  `EnddoSearch` angezeigt. Sie müssen nur eine Wrapperwebdienstmethode für die Methode  `doSearch` erstellen. Achten Sie darauf, dass die Methodensignatur und der Rückgabetyp genau übereinstimmen. 
    
7. Innerhalb jeder Wrappermethode müssen Sie wie im folgenden Beispiel dargestellt Code erstellen, um den referenzierten Webdienst vom Typ "RPC/encoded" aufzurufen. 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. Falls für den Webdienst vom Typ "RPC/encoded" eine Authentifizierung erforderlich ist, können Sie die zum Herstellen einer Verbindung mit dem Webdienst vom Typ "RPC/encoded" erforderlichen Anmeldeinformationen im Quellcode für den .NET-Proxywebdienst hartcodieren, oder Sie verwenden Code wie im folgenden Beispiel.  
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

Weitere Informationen finden Sie im Microsoft Knowledge Base-Artikel "HOW TO: Pass Current Credentials to an ASP.NET Web Service" unter https://support.microsoft.com/ .
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Erstellen eines Proxywebdiensts ohne Visual Studio .NET

Alternativ können Sie einen Proxywebdienst mithilfe der Tools im .NET Framework Software Development Kit (SDK) erstellen, das Sie von MSDN herunterladen können.
  
Erstellen Sie die Codedatei für Ihren Proxywebdienst mithilfe des WSDL-Tools (Wsdl.exe). Diese Codedatei kann mit dem C#-Befehlszeilencompiler (csc.exe) oder dem Visual Basic .NET-Befehlszeilencompiler (vbc.exe) kompiliert werden, die auch im .NET Framework SDK enthalten sind. Nachdem die Codedatei vom WSDL-Tool generiert wurde, benennen Sie die Dateinamenerweiterung in ASMX um, und öffnen Sie die Datei in einem beliebigen Text-Editor. Fügen Sie in der ersten Zeile des Dokuments die folgende Seitendirektive hinzu:   

  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

Navigieren Sie zum Ende der Codedatei, und erstellen Sie einen Aufruf für jede Webdienstmethode im Webdienst vom Typ "RPC/encoded". Das folgende Codebeispiel veranschaulicht den Code für einen .NET-Webdienst, der eine Verbindung mit dem Webdienst Google herstellt und den Typ "RPC/encoded" verwendet. Es ist ein Platzhalter für den von wsdl.exe generierten Code vorhanden.
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


