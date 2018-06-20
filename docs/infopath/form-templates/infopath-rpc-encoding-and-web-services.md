---
title: InfoPath, RPC-Codierung und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Webdienste können eine der zwei Formaten für das Binden der Webmethoden im Web Service Description Language (WSDL) Vertrag, die sie beschreibt verfügbar gemacht: Dokument oder RPC.'
ms.openlocfilehash: 01b75df42bce97d62ebb5e273588cb522e5e2a09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790760"
---
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, RPC-Codierung und Webdienste

Webdienste können eine der zwei Formaten für das Binden der Webmethoden im Web Service Description Language (WSDL) Vertrag, die sie beschreibt verfügbar gemacht: Dokument oder RPC. Darüber hinaus jedes dieser beiden Formate der Bindung als entweder Literal angegeben oder codiert. Die am häufigsten verwendeten Implementierungen für jeden Typ sind: Dokument-Literal und RPC/encoded. Microsoft InfoPath unterstützt jedoch nur eine Verbindung mit Webdiensten, die die Dokument-Literal-Formatvorlage verwenden.
  
Die meisten Webentwicklungstools für den Dienst bereitstellen einen Schalter zum Angeben von welche Art von Webdienst, der zu erstellenden. Wenn Sie einen Webdienst, den Sie entwickeln mit aus InfoPath verbunden werden soll, sollten Sie die Dokument-Literal als Format und Codierung des Webdiensts angeben.
  
Wenn Sie allerdings den Webdienst, den Sie verwenden möchten, nicht kontrollieren und eine Verbindung mit einem Webdienst vom Typ "RPC/encoded" herstellen müssen, können Sie mithilfe eines .NET-Proxydiensts eine Verbindung mit einem Webdienst vom Typ "RPC/encoded" herstellen.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Herstellen einer Verbindung mit einem Webdienst mithilfe eines .NET-Proxydiensts

Wenn Sie den Webdienst vom Typ "RPC/encoded", den Sie verwenden möchten, nicht kontrollieren, können Sie einen Microsoft .NET-Proxywebdienst vom Typ "document/literal" erstellen, der Wrapperfunktionen für alle Webmethoden bereitstellt, die Sie im Webdienst vom Typ "RPC/encoded" aufrufen möchten. Anschließend können Sie den Proxywebdienst vom Typ "document/literal" in InfoPath verwenden.
  
.NET Framework-Code kann für jeden Webdienst ("RPC/encoded" und "document/literal") verwendet werden, und alle .NET-Webdienste verwenden den Typ und die Codierung "document/literal". Da .NET Framework mit jeder Art von Webdienst kommunizieren kann, können Sie einen .NET-Webdienst erstellen, der Methoden zum Aufrufen des Webdiensts vom Typ "RPC/encoded" aufweist. Der .NET-Webdienst dient als Übersetzungsmodul, damit InfoPath Aufrufe vom Typ "document/literal" für den .NET-Webdienst ausführen kann, der wiederum Aufrufe vom Typ "RPC/encoded" für den ursprünglichen Webdienst ausführen kann.
  
Die Voraussetzungen zum Erstellen eines solchen Microsoft .NET-Proxywebdiensts sind ein Computer unter Microsoft Windows oder Microsoft Windows Server, auf dem Internetinformationsdienste (IIS) mit installiertem ASP.NET ausgeführt werden und auf dem der Proxywebdienst bereitgestellt wird. Wenn Sie eine InfoPath-Lösung erstellen, verweisen Sie nicht auf den Webdienst vom Typ "RPC/encoded", sondern auf den Proxywebdienst. Der Proxywebdienst führt dann Aufrufe für den Webdienst vom Typ "RPC/encoded" aus.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Erstellen eines Proxywebdiensts mithilfe von Visual Studio

1. Erstellen Sie ein neues Projekt **ASP.NET-Webdienstanwendung** . 
    
2. Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste in des Ordners **Verweise** Ihres neuen Projekts, und klicken Sie dann auf **Webverweis hinzufügen**. 
    
3. Geben Sie im Dialogfeld **Webverweis hinzufügen** in der URL des RPC/encoded-Webdiensts, dem Sie arbeiten mit, und klicken Sie dann auf **wechseln**möchten.
    
4. Klicken Sie auf **Verweis hinzufügen**. 
    
5. Öffnen Sie die ASMX-Datei für Ihren Webdienst, und fügen Sie eine Webdienstmethode zum Aufrufen jeder Webdienstmethode im referenzierten Webdienst vom Typ "RPC/encoded" hinzu.
    
6. Um eine Liste der Methoden in der Referenz RPC/encoded Webserver anzuzeigen, zeigt das Fenster **Klassenansicht** . Für jede Methode Web Service sehen Sie drei Methoden. Wenn die Webdienst-Methode aufgerufen wird beispielsweise `doSearch`, wird die drei Methoden angezeigt `doSearch`, `BegindoSearch`, und `EnddoSearch`. Sie müssen nur eine Wrapper-Webdienst-Methode zum Erstellen der `doSearch` Methode. Müssen Sie unbedingt die genauen Methodensignatur übereinstimmen und den Rückgabetyp. 
    
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

Weitere Informationen finden Sie im Microsoft Knowledge Base-Artikel "Wie an: übergeben aktuellen Anmeldeinformationen an einen ASP.NET-Webdienst""auf http://support.microsoft.com/.
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Erstellen eines Proxywebdiensts ohne Visual Studio .NET

Alternativ können Sie einen Proxywebdienst mithilfe der Tools im .NET Framework Software Development Kit (SDK) erstellen, das Sie von MSDN herunterladen können.
  
Verwenden Sie Web Services Description Language-Tool (Wsdl.exe), um die Codedatei für Ihren Webdienst-Proxy zu erstellen. Mithilfe von C#-Command-Line Compiler (csc.exe) oder Visual Basic .NET Command-Line Compiler (vbc.exe), die auch in .NET Framework SDK enthalten sind, kann dieser Codedatei kompiliert werden. Nachdem das Web Services Description Language-Tool die Codedatei generiert wurde, benennen Sie die Erweiterung in asmx, und öffnen Sie die Datei in einem beliebigen Texteditor. Klicken Sie auf die erste Zeile des Dokuments fügen Sie die folgende Seitendirektive hinzu:
  
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


