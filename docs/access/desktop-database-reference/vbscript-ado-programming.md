---
title: VBScript-ADO-Programmierung
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e91eedbb790eabd49cfacc83b37a9db8cfad720
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867671"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="cef5f-102">VBScript-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="cef5f-102">VBScript ADO Programming</span></span>


<span data-ttu-id="cef5f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cef5f-103">**Applies to**: Access 2013, Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="cef5f-104">Erstellen eines ADO-Projekts</span><span class="sxs-lookup"><span data-stu-id="cef5f-104">Creating an ADO Project</span></span>

<span data-ttu-id="cef5f-p101">Da von Microsoft Visual Basic Scripting Edition keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in VBScript nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cef5f-p101">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="cef5f-108">In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit VBScript verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="cef5f-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="cef5f-109">Verwenden, Sie für serverseitiges Skripting Adovbs.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Ado\\ Ordner standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="cef5f-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="cef5f-110">Verwenden, Sie für clientseitiges Skripting Datei Adcvbs.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Msdac\\ Ordner standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="cef5f-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="cef5f-111">Sie können entweder kopieren und Konstantendefinitionen aus diesen Dateien in ASP-Seiten einfügen, oder, wenn Sie serverseitiges Skripting, kopieren Adovbs.inc Datei in einen Ordner auf Ihrer Website und verweisen auf die sie über die ASP-Seite wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cef5f-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="cef5f-112">Erstellen von ADO-Objekten in VBScript</span><span class="sxs-lookup"><span data-stu-id="cef5f-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="cef5f-p102">Sie können die **Dim** -Anweisung nicht zum Zuweisen von Objekten zu einem bestimmten Typ in VBScript verwenden. Außerdem wird in VBScript die Syntax **New**, die mit der **Dim** -Anweisung in Visual Basic für Applikationen verwendet wird, nicht unterstützt. Sie müssen stattdessen den **CreateObject** -Funktionsaufruf verwenden:</span><span class="sxs-lookup"><span data-stu-id="cef5f-p102">You cannot use the **Dim** statement to assign objects to a specific type in VBScript. Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications. You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="cef5f-116">VBScript (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="cef5f-116">VBScript Examples</span></span>

<span data-ttu-id="cef5f-117">Der folgende Code ist ein allgemeines Beispiel für die serverseitige VBScript-Programmierung in einer ASP-Datei (Active Server Pages):</span><span class="sxs-lookup"><span data-stu-id="cef5f-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

<span data-ttu-id="cef5f-118">Konkretere VBScript-Beispiele sind in der ADO-Dokumentation enthalten.</span><span class="sxs-lookup"><span data-stu-id="cef5f-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="cef5f-119">Weitere Informationen finden Sie unter [ADO-Codebeispiele in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span><span class="sxs-lookup"><span data-stu-id="cef5f-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="cef5f-120">Unterschiede zwischen VBScript und Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cef5f-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="cef5f-p104">Das Verwenden von ADO mit VBScript ist in vielerlei Hinsicht, z. B. hinsichtlich der Verwendung der Syntax, mit der Verwendung von ADO mit Visual Basic vergleichbar. Es sind jedoch einige erhebliche Unterschiede vorhanden:</span><span class="sxs-lookup"><span data-stu-id="cef5f-p104">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used. However, some significant differences exist:</span></span>

- <span data-ttu-id="cef5f-p105">In VBScript wird nur der Datentyp Variant unterstützt, der verschiedene Datentypen enthalten kann. Sie können die benötigten Daten in einem Datentyp Variant speichern, und die Daten sind aufgrund der durch VBScript ausgeführten Umwandlung ordnungsgemäß funktionsfähig. Der für ADO erforderliche Typ wird erkannt, und der Wert in der Variante wird entsprechend konvertiert.</span><span class="sxs-lookup"><span data-stu-id="cef5f-p105">VBScript supports only the Variant data type, which can hold different types of data. You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript. It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="cef5f-126">Sie können keine `on error goto <label>` in VBScript.</span><span class="sxs-lookup"><span data-stu-id="cef5f-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="cef5f-p106">In VBScript werden einige der integrierten Visual Basic-Funktionen, wie z. B. **Msgbox**, **Date** und **IsNumeric**, unterstützt. Da es sich bei VBScript jedoch um eine Teilmenge von Visual Basic handelt, werden nicht alle integrierten Funktionen unterstützt. Beispielsweise werden in VBScript die **Format** -Funktion und die Datei-E/A-Funktionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cef5f-p106">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**. However, because VBScript is a subset of Visual Basic, not all built-in functions are supported. For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>

