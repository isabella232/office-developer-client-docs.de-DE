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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290891"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="06f75-102">JScript ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="06f75-102">JScript ADO programming</span></span>


<span data-ttu-id="06f75-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06f75-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="06f75-104">Erstellen eines ADO-Projekts</span><span class="sxs-lookup"><span data-stu-id="06f75-104">Creating an ADO Project</span></span>

<span data-ttu-id="06f75-p101">Da von Microsoft JScript keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in JScript nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="06f75-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="06f75-108">In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit JScript verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="06f75-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="06f75-109">Für die serverseitige Skripterstellung verwenden Sie Datei adojavas. Inc, die standardmäßig im Ordner\\c:\\Program Files\\Common\\Files\\ System ADO installiert ist.</span><span class="sxs-lookup"><span data-stu-id="06f75-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="06f75-110">Für die clientseitige Skripterstellung verwenden Sie Adcjavas. Inc, die standardmäßig im Ordner\\c:\\Program Files\\Common\\Files\\ System msdac installiert ist.</span><span class="sxs-lookup"><span data-stu-id="06f75-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="06f75-111">Sie können entweder kopieren und Einfügen von Konstanten Definitionen aus diesen Dateien in Ihre ASP-Seiten oder, wenn Sie serverseitige Skripterstellung durchführen, kopieren Sie die Datei Datei adojavas. Inc in einen Ordner auf Ihrer Website, und verweisen Sie auf Ihre ASP-Seite wie folgt:</span><span class="sxs-lookup"><span data-stu-id="06f75-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="06f75-112">Erstellen von ADO-Objekten in JScript</span><span class="sxs-lookup"><span data-stu-id="06f75-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="06f75-113">Sie müssen stattdessen den **CreateObject**-Funktionsaufruf verwenden:</span><span class="sxs-lookup"><span data-stu-id="06f75-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="06f75-114">JScript (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="06f75-114">JScript Example</span></span>

<span data-ttu-id="06f75-115">Der folgende Code ist ein allgemeines Beispiel für die serverseitige JScript-Programmierung in einer ASP-Datei (Active Server Page), durch die ein **Recordset**-Objekt geöffnet wird:</span><span class="sxs-lookup"><span data-stu-id="06f75-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

