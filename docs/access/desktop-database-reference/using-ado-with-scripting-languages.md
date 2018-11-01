---
title: Verwenden von ADO mit Skriptsprachen
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffab726a38b5cd6890bff694c52156d3f45a40be
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870380"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="89ae1-102">Verwenden von ADO mit Skriptsprachen</span><span class="sxs-lookup"><span data-stu-id="89ae1-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="89ae1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89ae1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89ae1-104">In einer Umgebung mit Skripting ermöglicht ADO Daten mithilfe von serverseitigen Skripts verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="89ae1-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="89ae1-105">In diesem Szenario ADO die zugrunde liegende OLE DB-Anbieter, der es verwendet, und andere Komponenten erforderlich, um einen bestimmten Datenspeicher verweisen auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="89ae1-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="89ae1-106">ADO ist Active Server Pages (ASP) verwenden, eine Komponente, die in einem Skript die HTML, beispielsweise generieren kann verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="89ae1-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="89ae1-107">Dieser HTML-Inhalt kann über HTTP in einem Clientwebbrowser übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="89ae1-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="89ae1-108">Mithilfe von Skripting kann die Webseite Aktionen zurück an das serverseitige Skript ermöglicht es Ihnen, aktualisieren, Traversieren oder anzeigen bestimmte Daten senden.</span><span class="sxs-lookup"><span data-stu-id="89ae1-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="89ae1-109">ODBC-Datenquellen</span><span class="sxs-lookup"><span data-stu-id="89ae1-109">ODBC Data Sources</span></span>

<span data-ttu-id="89ae1-p102">Ein wichtiger Unterschied zwischen ADO-Code mit und ohne Skripting ist die ODBC-Datenquelle, wenn sie verwendet wird. Für Anwendungen ohne Skripting können Sie einen Benutzer-DSN im ODBC-Datenquellenadministrator erstellen. Für unter IIS ausgeführte Skripts müssen Sie einen System-DSN erstellen; andernfalls wird die erstellte Datenquelle von den Skripts nicht erkannt. Dies gilt für alle ADO-Skriptinganwendungen, von denen der Microsoft OLE DB-Anbieter für ODBC über Microsoft IIS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89ae1-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="89ae1-114">Verweisen auf die ADO-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89ae1-114">Referencing the ADO Library</span></span>

<span data-ttu-id="89ae1-115">Bei Skriptsprachen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89ae1-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="89ae1-116">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="89ae1-116">Handling events</span></span>

<span data-ttu-id="89ae1-117">Bei Skriptsprachen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89ae1-117">N/A with scripting languages.</span></span>

<span data-ttu-id="89ae1-118">Die folgenden Themen enthalten konkretere Informationen zum Verwenden von ADO mit Skriptsprachen:</span><span class="sxs-lookup"><span data-stu-id="89ae1-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="89ae1-119">JScript ADO Programming</span><span class="sxs-lookup"><span data-stu-id="89ae1-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="89ae1-120">VBScript-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="89ae1-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)