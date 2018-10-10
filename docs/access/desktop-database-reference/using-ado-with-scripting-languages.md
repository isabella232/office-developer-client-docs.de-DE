---
title: Verwenden von ADO mit Skriptsprachen
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475980"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="5519e-102">Verwenden von ADO mit Skriptsprachen</span><span class="sxs-lookup"><span data-stu-id="5519e-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="5519e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5519e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5519e-p101">In einer Skriptingumgebung können Sie mit ADO Daten mithilfe von serverseitigen Skripts verfügbar machen. In diesem Szenario werden ADO, der von ADO genutzte zugrunde liegende OLE DB-Anbieter und alle anderen Komponenten, die zum Verweisen auf einen bestimmten Datenspeicher verwendet werden, auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert. ADO ist eine Komponente, auf die in einem Skript, das z. B. HTML erstellen kann, mithilfe von Active Server Pages (ASP) verwiesen wird. Dieser HTML-Inhalt kann über HTTP einem Clientwebbrowser übergeben werden. Mithilfe von Skripting können von der Webseite Aktionen zurück an das serverseitige Skript gesendet werden, sodass Sie bestimmte Daten aktualisieren, traversieren oder anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="5519e-p101">Within a scripting environment, ADO allows you to expose data by way of server-side scripting. In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS). Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example. This HTML content can be passed via HTTP to a client Web browser. Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="5519e-109">ODBC-Datenquellen</span><span class="sxs-lookup"><span data-stu-id="5519e-109">ODBC Data Sources</span></span>

<span data-ttu-id="5519e-p102">Ein wichtiger Unterschied zwischen ADO-Code mit und ohne Skripting ist die ODBC-Datenquelle, wenn sie verwendet wird. Für Anwendungen ohne Skripting können Sie einen Benutzer-DSN im ODBC-Datenquellenadministrator erstellen. Für unter IIS ausgeführte Skripts müssen Sie einen System-DSN erstellen; andernfalls wird die erstellte Datenquelle von den Skripts nicht erkannt. Dies gilt für alle ADO-Skriptinganwendungen, von denen der Microsoft OLE DB-Anbieter für ODBC über Microsoft IIS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5519e-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="5519e-114">Verweisen auf die ADO-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5519e-114">Referencing the ADO Library</span></span>

<span data-ttu-id="5519e-115">Bei Skriptsprachen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5519e-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="5519e-116">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="5519e-116">Handling events</span></span>

<span data-ttu-id="5519e-117">Bei Skriptsprachen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5519e-117">N/A with scripting languages.</span></span>

<span data-ttu-id="5519e-118">Die folgenden Themen enthalten konkretere Informationen zum Verwenden von ADO mit Skriptsprachen:</span><span class="sxs-lookup"><span data-stu-id="5519e-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="5519e-119">VBScript-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="5519e-119">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="5519e-120">JScript-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="5519e-120">ADO in JScript</span></span>](jscript-ado-programming.md)

