---
title: JScript ADO-Programmierung
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708971"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="30244-102">JScript ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="30244-102">JScript ADO programming</span></span>


<span data-ttu-id="30244-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30244-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="30244-104">Erstellen eines ADO-Projekts</span><span class="sxs-lookup"><span data-stu-id="30244-104">Creating an ADO Project</span></span>

<span data-ttu-id="30244-p101">Da von Microsoft JScript keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in JScript nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="30244-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="30244-108">In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit JScript verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="30244-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="30244-109">Verwenden, Sie für serverseitiges Skripting Datei Adojavas.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Ado\\ Ordner standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="30244-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="30244-110">Verwenden, Sie für clientseitiges Skripting Datei Adcjavas.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Msdac\\ Ordner standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="30244-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="30244-111">Sie können entweder kopieren und Konstantendefinitionen aus diesen Dateien in ASP-Seiten einfügen, oder, wenn Sie serverseitiges Skripting, kopieren Sie die Datei Adojavas.inc-Datei in einen Ordner auf Ihrer Website, und es von der ASP verweist:</span><span class="sxs-lookup"><span data-stu-id="30244-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="30244-112">Erstellen von ADO-Objekten in JScript</span><span class="sxs-lookup"><span data-stu-id="30244-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="30244-113">Sie müssen stattdessen den **CreateObject** -Funktionsaufruf verwenden:</span><span class="sxs-lookup"><span data-stu-id="30244-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="30244-114">JScript (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="30244-114">JScript Example</span></span>

<span data-ttu-id="30244-115">Der folgende Code ist ein allgemeines Beispiel für die serverseitige JScript-Programmierung in einer ASP-Datei (Active Server Page), durch die ein **Recordset** -Objekt geöffnet wird:</span><span class="sxs-lookup"><span data-stu-id="30244-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```

