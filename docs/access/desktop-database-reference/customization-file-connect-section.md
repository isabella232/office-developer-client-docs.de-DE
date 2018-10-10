---
title: Connect-Abschnitt der Anpassungsdatei
TOCTitle: Customization File Connect Section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd4b7eed3cb5d8192866127322c00e7ecd5a15b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474502"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="cbeca-102">Connect-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="cbeca-102">Customization File Connect Section</span></span>

<span data-ttu-id="cbeca-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbeca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cbeca-p101">Das Verweigern aller Verbindungen ist das Standardverhalten des Handlers. Im **connect** -Abschnitt werden Ausnahmen für dieses Verhalten angegeben. Wenn z. B. alle **connect** -Abschnitte nicht vorhanden oder leer sind, können standardmäßig keine Verbindungen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cbeca-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="cbeca-107">Der **connect** -Abschnitt kann Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="cbeca-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="cbeca-p102">Einen Standardzugriffseintrag, in dem die für diese Verbindung zulässigen Standardlese- und -schreiboperationen angegeben werden. Wenn im Abschnitt kein Standardzugriffseintrag vorhanden ist, wird der Abschnitt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cbeca-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="cbeca-110">Eine neue Verbindungszeichenfolge, durch die die Clientverbindungszeichenfolge ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cbeca-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbeca-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbeca-111">Syntax</span></span>

<span data-ttu-id="cbeca-112">Ein Standardzugriffseintrag hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="cbeca-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="cbeca-113">Ein Eintrag für eine Ersetzungsverbindungszeichenfolge hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="cbeca-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbeca-114">Argument</span><span class="sxs-lookup"><span data-stu-id="cbeca-114">Part</span></span></p></th>
<th><p><span data-ttu-id="cbeca-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbeca-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbeca-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="cbeca-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="cbeca-117">Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Verbindungszeichenfolgeneintrag handelt.</span><span class="sxs-lookup"><span data-stu-id="cbeca-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbeca-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="cbeca-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="cbeca-119">Eine Zeichenfolge, durch die die gesamte Clientverbindungszeichenfolge ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cbeca-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbeca-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="cbeca-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="cbeca-121">Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Zugriffseintrag handelt.</span><span class="sxs-lookup"><span data-stu-id="cbeca-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbeca-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="cbeca-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="cbeca-123">Eines der folgenden Zugriffsrechte:
</span><span class="sxs-lookup"><span data-stu-id="cbeca-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="cbeca-124"><strong>NoAccess</strong> - Benutzer kann nicht auf die Datenquelle zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cbeca-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="cbeca-125"><strong>ReadOnly</strong> - Benutzer kann die Datenquelle lesen.</span><span class="sxs-lookup"><span data-stu-id="cbeca-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="cbeca-126"><strong>ReadWrite</strong> - Benutzer kann in der Datenquelle lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="cbeca-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbeca-127">Wenn Sie alle Verbindungen (in Effekt, deaktivieren das Standardverhalten des Handlers) ermöglichen, legen Sie den Zugriffseintrag im Abschnitt **Standard verbinden** , und löschen oder kommentieren Sie alle anderen **Verbinden** *Identifier* -Abschnitte möchten.</span><span class="sxs-lookup"><span data-stu-id="cbeca-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

