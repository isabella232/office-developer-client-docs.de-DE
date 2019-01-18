---
title: Anpassungsdatei – UserList-Abschnitt
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721500"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="c7002-102">Anpassungsdatei – UserList-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c7002-102">Customization File UserList section</span></span>


<span data-ttu-id="c7002-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7002-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7002-104">Der **Userlist** -Abschnitt bezieht sich auf den Abschnitt **Verbinden** mit dem gleichen *Identifier* -Abschnittsparameter.</span><span class="sxs-lookup"><span data-stu-id="c7002-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="c7002-105">Dieser Abschnitt kann einen *Benutzerzugriffseintrag*enthalten, die durch den Zugriffsrechte für den angegebenen Benutzer und überschreibt die *standardmäßige* *Zugriffseintrag* im entsprechenden Abschnitt **Verbinden** .</span><span class="sxs-lookup"><span data-stu-id="c7002-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7002-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7002-106">Syntax</span></span>

<span data-ttu-id="c7002-107">Ein Benutzerzugriffseintrag hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="c7002-107">A user access entry is of the form:</span></span>

<span data-ttu-id="c7002-108">*UserName \*\*\* =* AccessRights \*\*\*</span><span class="sxs-lookup"><span data-stu-id="c7002-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7002-109">Teil</span><span class="sxs-lookup"><span data-stu-id="c7002-109">Part</span></span></p></th>
<th><p><span data-ttu-id="c7002-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7002-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7002-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="c7002-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="c7002-p101">Der <em>Benutzername</em> der Person, die diese Verbindung verwendet. Gültige Benutzernamen werden mit dem Dialog <strong>Dienst-Manager</strong> von Internetinformationsdienste (Internet Information Services, IIS) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c7002-p101">The <em>user name</em> of the person employing this connection. Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7002-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="c7002-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="c7002-115">Eines der folgenden Zugriffsrechte:
</span><span class="sxs-lookup"><span data-stu-id="c7002-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="c7002-116"><strong>NoAccess</strong> - Benutzer kann nicht auf die Datenquelle zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c7002-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="c7002-117"><strong>ReadOnly</strong> - Benutzer kann die Datenquelle lesen.</span><span class="sxs-lookup"><span data-stu-id="c7002-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="c7002-118"><strong>ReadWrite</strong> - Benutzer kann in der Datenquelle lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="c7002-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

