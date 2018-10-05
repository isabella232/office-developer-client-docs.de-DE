---
title: InfoPath, RPC-Codierung und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Webdienste können eine der zwei Formaten für das Binden der Webmethoden im Web Service Description Language (WSDL) Vertrag, die sie beschreibt verfügbar gemacht: Dokument oder RPC.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387678"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="bb584-103">InfoPath, RPC-Codierung und Webdienste</span><span class="sxs-lookup"><span data-stu-id="bb584-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="bb584-104">Webdienste können eine der zwei Formaten für das Binden der Webmethoden im Web Service Description Language (WSDL) Vertrag, die sie beschreibt verfügbar gemacht: Dokument oder RPC.</span><span class="sxs-lookup"><span data-stu-id="bb584-104">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC.</span></span> <span data-ttu-id="bb584-105">Darüber hinaus jedes dieser beiden Formate der Bindung als entweder Literal angegeben oder codiert.</span><span class="sxs-lookup"><span data-stu-id="bb584-105">Additionally, each of these two styles of binding can be specified as either literal or encoded.</span></span> <span data-ttu-id="bb584-106">Die am häufigsten verwendeten Implementierungen für jeden Typ sind: Dokument-Literal und RPC/encoded.</span><span class="sxs-lookup"><span data-stu-id="bb584-106">The most common implementations for each type are: document/literal and RPC/encoded.</span></span> <span data-ttu-id="bb584-107">Microsoft InfoPath unterstützt jedoch nur eine Verbindung mit Webdiensten, die die Dokument-Literal-Formatvorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb584-107">However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="bb584-108">Die meisten Webentwicklungstools für den Dienst bereitstellen einen Schalter zum Angeben von welche Art von Webdienst, der zu erstellenden.</span><span class="sxs-lookup"><span data-stu-id="bb584-108">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create.</span></span> <span data-ttu-id="bb584-109">Wenn Sie einen Webdienst, den Sie entwickeln mit aus InfoPath verbunden werden soll, sollten Sie die Dokument-Literal als Format und Codierung des Webdiensts angeben.</span><span class="sxs-lookup"><span data-stu-id="bb584-109">If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="bb584-110">Wenn Sie allerdings den Webdienst, den Sie verwenden möchten, nicht kontrollieren und eine Verbindung mit einem Webdienst vom Typ "RPC/encoded" herstellen müssen, können Sie mithilfe eines .NET-Proxydiensts eine Verbindung mit einem Webdienst vom Typ "RPC/encoded" herstellen.</span><span class="sxs-lookup"><span data-stu-id="bb584-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="bb584-111">Herstellen einer Verbindung mit einem Webdienst mithilfe eines .NET-Proxydiensts</span><span class="sxs-lookup"><span data-stu-id="bb584-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="bb584-p103">Wenn Sie den Webdienst vom Typ "RPC/encoded", den Sie verwenden möchten, nicht kontrollieren, können Sie einen Microsoft .NET-Proxywebdienst vom Typ "document/literal" erstellen, der Wrapperfunktionen für alle Webmethoden bereitstellt, die Sie im Webdienst vom Typ "RPC/encoded" aufrufen möchten. Anschließend können Sie den Proxywebdienst vom Typ "document/literal" in InfoPath verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb584-p103">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service. You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="bb584-p104">.NET Framework-Code kann für jeden Webdienst ("RPC/encoded" und "document/literal") verwendet werden, und alle .NET-Webdienste verwenden den Typ und die Codierung "document/literal". Da .NET Framework mit jeder Art von Webdienst kommunizieren kann, können Sie einen .NET-Webdienst erstellen, der Methoden zum Aufrufen des Webdiensts vom Typ "RPC/encoded" aufweist. Der .NET-Webdienst dient als Übersetzungsmodul, damit InfoPath Aufrufe vom Typ "document/literal" für den .NET-Webdienst ausführen kann, der wiederum Aufrufe vom Typ "RPC/encoded" für den ursprünglichen Webdienst ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="bb584-p104">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding. Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service. The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="bb584-p105">Die Voraussetzungen zum Erstellen eines solchen Microsoft .NET-Proxywebdiensts sind ein Computer unter Microsoft Windows oder Microsoft Windows Server, auf dem Internetinformationsdienste (IIS) mit installiertem ASP.NET ausgeführt werden und auf dem der Proxywebdienst bereitgestellt wird. Wenn Sie eine InfoPath-Lösung erstellen, verweisen Sie nicht auf den Webdienst vom Typ "RPC/encoded", sondern auf den Proxywebdienst. Der Proxywebdienst führt dann Aufrufe für den Webdienst vom Typ "RPC/encoded" aus.</span><span class="sxs-lookup"><span data-stu-id="bb584-p105">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service. When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service. The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="bb584-120">Erstellen eines Proxywebdiensts mithilfe von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bb584-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="bb584-121">Erstellen Sie ein neues Projekt **ASP.NET-Webdienstanwendung**.</span><span class="sxs-lookup"><span data-stu-id="bb584-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="bb584-122">Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste in des Ordners **Verweise** Ihres neuen Projekts, und klicken Sie dann auf **Webverweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bb584-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="bb584-123">Geben Sie im Dialogfeld **Webverweis hinzufügen** die URL des Webdiensts vom Typ "RPC/encoded" ein, den Sie verwenden möchten, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bb584-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="bb584-124">Klicken Sie auf **Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bb584-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="bb584-125">Öffnen Sie die ASMX-Datei für Ihren Webdienst, und fügen Sie eine Webdienstmethode zum Aufrufen jeder Webdienstmethode im referenzierten Webdienst vom Typ "RPC/encoded" hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb584-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="bb584-126">Um eine Liste der Methoden in der Referenz RPC/encoded Webserver anzuzeigen, zeigt das Fenster **Klassenansicht** .</span><span class="sxs-lookup"><span data-stu-id="bb584-126">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window.</span></span> <span data-ttu-id="bb584-127">Für jede Methode Web Service sehen Sie drei Methoden.</span><span class="sxs-lookup"><span data-stu-id="bb584-127">For each Web Service method, you will see three methods.</span></span> <span data-ttu-id="bb584-128">Wenn die Webdienst-Methode aufgerufen wird beispielsweise `doSearch`, wird die drei Methoden angezeigt `doSearch`, `BegindoSearch`, und `EnddoSearch`.</span><span class="sxs-lookup"><span data-stu-id="bb584-128">For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`.</span></span> <span data-ttu-id="bb584-129">Sie müssen nur eine Wrapper-Webdienst-Methode zum Erstellen der `doSearch` Methode.</span><span class="sxs-lookup"><span data-stu-id="bb584-129">You only have to create a wrapper Web Service method for the  `doSearch` method.</span></span> <span data-ttu-id="bb584-130">Müssen Sie unbedingt die genauen Methodensignatur übereinstimmen und den Rückgabetyp.</span><span class="sxs-lookup"><span data-stu-id="bb584-130">Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="bb584-131">Innerhalb jeder Wrappermethode müssen Sie wie im folgenden Beispiel dargestellt Code erstellen, um den referenzierten Webdienst vom Typ "RPC/encoded" aufzurufen. </span><span class="sxs-lookup"><span data-stu-id="bb584-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="bb584-132">Falls für den Webdienst vom Typ "RPC/encoded" eine Authentifizierung erforderlich ist, können Sie die zum Herstellen einer Verbindung mit dem Webdienst vom Typ "RPC/encoded" erforderlichen Anmeldeinformationen im Quellcode für den .NET-Proxywebdienst hartcodieren, oder Sie verwenden Code wie im folgenden Beispiel. </span><span class="sxs-lookup"><span data-stu-id="bb584-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="bb584-133">Weitere Informationen finden Sie im Microsoft Knowledge Base-Artikel "Wie an: übergeben aktuellen Anmeldeinformationen an einen ASP.NET-Webdienst""auf https://support.microsoft.com/.</span><span class="sxs-lookup"><span data-stu-id="bb584-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on https://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="bb584-134">Erstellen eines Proxywebdiensts ohne Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="bb584-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="bb584-135">Alternativ können Sie einen Proxywebdienst mithilfe der Tools im .NET Framework Software Development Kit (SDK) erstellen, das Sie von MSDN herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="bb584-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="bb584-p107">Erstellen Sie die Codedatei für Ihren Proxywebdienst mithilfe des WSDL-Tools (Wsdl.exe). Diese Codedatei kann mit dem C#-Befehlszeilencompiler (csc.exe) oder dem Visual Basic .NET-Befehlszeilencompiler (vbc.exe) kompiliert werden, die auch im .NET Framework SDK enthalten sind. Nachdem die Codedatei vom WSDL-Tool generiert wurde, benennen Sie die Dateinamenerweiterung in ASMX um, und öffnen Sie die Datei in einem beliebigen Text-Editor. Fügen Sie in der ersten Zeile des Dokuments die folgende Seitendirektive hinzu:   
</span><span class="sxs-lookup"><span data-stu-id="bb584-p107">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service. This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK. After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor. On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="bb584-p108">Navigieren Sie zum Ende der Codedatei, und erstellen Sie einen Aufruf für jede Webdienstmethode im Webdienst vom Typ "RPC/encoded". Das folgende Codebeispiel veranschaulicht den Code für einen .NET-Webdienst, der eine Verbindung mit dem Webdienst Google herstellt und den Typ "RPC/encoded" verwendet. Es ist ein Platzhalter für den von wsdl.exe generierten Code vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bb584-p108">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service. The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development. There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
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


