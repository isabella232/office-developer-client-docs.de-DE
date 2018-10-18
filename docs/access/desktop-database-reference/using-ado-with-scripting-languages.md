---
title: Verwenden von ADO mit Skriptsprachen
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 196366987e89f52a3c498a769fa501a3faca9dae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604435"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="5265f-102">Verwenden von ADO mit Skriptsprachen</span><span class="sxs-lookup"><span data-stu-id="5265f-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="5265f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5265f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5265f-104"><<<<<<< HEAD innerhalb einer Umgebung mit Skripting, ADO können Sie Daten mithilfe von serverseitigen Skripts verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="5265f-104"><<<<<<< HEAD Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="5265f-105">In diesem Szenario ADO die zugrunde liegende OLE DB-Anbieter, der es verwendet, und andere Komponenten erforderlich, um einen bestimmten Datenspeicher verweisen auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5265f-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="5265f-106">ADO ist Active Server Pages (ASP) verwenden, eine Komponente, die in einem Skript die HTML, beispielsweise generieren kann verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5265f-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="5265f-107">Dieser HTML-Inhalt kann über HTTP in einem Clientwebbrowser übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5265f-107">This HTML content can be passed via HTTP to a client Web browser.</span></span> <span data-ttu-id="5265f-108">Mithilfe von Skripting können die Webseite Aktionen zurück an das serverseitige Skript ermöglicht es Ihnen, aktualisieren, Traversieren oder anzeigen bestimmte Daten senden.</span><span class="sxs-lookup"><span data-stu-id="5265f-108">Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
<span data-ttu-id="5265f-109">=== Innerhalb einer Umgebung mit Skripting ermöglicht ADO Daten mithilfe von serverseitigen Skripts verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5265f-109">======= Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="5265f-110">In diesem Szenario ADO die zugrunde liegende OLE DB-Anbieter, der es verwendet, und andere Komponenten erforderlich, um einen bestimmten Datenspeicher verweisen auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5265f-110">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="5265f-111">ADO ist Active Server Pages (ASP) verwenden, eine Komponente, die in einem Skript die HTML, beispielsweise generieren kann verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5265f-111">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="5265f-112">Dieser HTML-Inhalt kann über HTTP in einem Clientwebbrowser übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5265f-112">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="5265f-113">Mithilfe von Skripting kann die Webseite Aktionen zurück an das serverseitige Skript ermöglicht es Ihnen, aktualisieren, Traversieren oder anzeigen bestimmte Daten senden.</span><span class="sxs-lookup"><span data-stu-id="5265f-113">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
>>>>>>> <span data-ttu-id="5265f-114">master</span><span class="sxs-lookup"><span data-stu-id="5265f-114">master</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="5265f-115">ODBC-Datenquellen</span><span class="sxs-lookup"><span data-stu-id="5265f-115">ODBC Data Sources</span></span>

<span data-ttu-id="5265f-p102">Ein wichtiger Unterschied zwischen ADO-Code mit und ohne Skripting ist die ODBC-Datenquelle, wenn sie verwendet wird. Für Anwendungen ohne Skripting können Sie einen Benutzer-DSN im ODBC-Datenquellenadministrator erstellen. Für unter IIS ausgeführte Skripts müssen Sie einen System-DSN erstellen; andernfalls wird die erstellte Datenquelle von den Skripts nicht erkannt. Dies gilt für alle ADO-Skriptinganwendungen, von denen der Microsoft OLE DB-Anbieter für ODBC über Microsoft IIS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5265f-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="5265f-120">Verweisen auf die ADO-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5265f-120">Referencing the ADO Library</span></span>

<span data-ttu-id="5265f-121">Bei Skriptsprachen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5265f-121">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="5265f-122">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="5265f-122">Handling events</span></span>

<span data-ttu-id="5265f-123">Bei Skriptsprachen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5265f-123">N/A with scripting languages.</span></span>

<span data-ttu-id="5265f-124">Die folgenden Themen enthalten konkretere Informationen zum Verwenden von ADO mit Skriptsprachen:</span><span class="sxs-lookup"><span data-stu-id="5265f-124">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="5265f-125">VBScript-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="5265f-125">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="5265f-126">JScript-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="5265f-126">ADO in JScript</span></span>](jscript-ado-programming.md)

