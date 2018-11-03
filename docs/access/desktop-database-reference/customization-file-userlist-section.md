---
title: Datei UserList-Abschnitt der Anpassungsdatei
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62aaba79fa010de62fb1ac35939673b2056be3f7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944095"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="e115b-102">Datei UserList-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="e115b-102">Customization File UserList section</span></span>


<span data-ttu-id="e115b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e115b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e115b-104">Der **Userlist** -Abschnitt bezieht sich auf den Abschnitt **Verbinden** mit dem gleichen *Identifier* -Abschnittsparameter.</span><span class="sxs-lookup"><span data-stu-id="e115b-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="e115b-105">Dieser Abschnitt kann einen *Benutzerzugriffseintrag*enthalten, die durch den Zugriffsrechte für den angegebenen Benutzer und überschreibt die *standardmäßige* *Zugriffseintrag* im entsprechenden Abschnitt **Verbinden** .</span><span class="sxs-lookup"><span data-stu-id="e115b-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="e115b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e115b-106">Syntax</span></span>

<span data-ttu-id="e115b-107">Ein Benutzerzugriffseintrag hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="e115b-107">A user access entry is of the form:</span></span>

<span data-ttu-id="e115b-108">*UserName \*\*\* =* AccessRights \*\*\*</span><span class="sxs-lookup"><span data-stu-id="e115b-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e115b-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e115b-109">Part</span></span></p></th>
<th><p><span data-ttu-id="e115b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e115b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e115b-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="e115b-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="e115b-p101">Der <em>Benutzername</em> der Person, die diese Verbindung verwendet. Gültige Benutzernamen werden mit dem Dialog <strong>Dienst-Manager</strong> von Internetinformationsdienste (Internet Information Services, IIS) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e115b-p101">The <em>user name</em> of the person employing this connection. Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e115b-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="e115b-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="e115b-115">Eines der folgenden Zugriffsrechte:
</span><span class="sxs-lookup"><span data-stu-id="e115b-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="e115b-116"><strong>NoAccess</strong> - Benutzer kann nicht auf die Datenquelle zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e115b-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="e115b-117"><strong>ReadOnly</strong> - Benutzer kann die Datenquelle lesen.</span><span class="sxs-lookup"><span data-stu-id="e115b-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="e115b-118"><strong>ReadWrite</strong> - Benutzer kann in der Datenquelle lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="e115b-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

