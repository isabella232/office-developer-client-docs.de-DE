---
title: Grundlegendes zur Anpassungsdatei
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721885"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="aa2ff-102">Grundlegendes zur Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="aa2ff-102">Understanding the Customization File</span></span>


<span data-ttu-id="aa2ff-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa2ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa2ff-104">Jeder Abschnittsheader in der Anpassungsdatei besteht aus eckigen Klammern (**\[**), die einen Typ und einen Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="aa2ff-105">Die vier Abschnittstypen werden durch die Literalzeichenfolgen **connect**, **sql**, **userlist** oder **logs** angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="aa2ff-106">Der Parameter ist die Literalzeichenfolge, der Standardwert, ein benutzerdefinierter Bezeichner oder nichts.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="aa2ff-107">Jeder Abschnitt wird daher durch einen der folgenden Abschnittsheader gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="aa2ff-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="aa2ff-108">Die Abschnittsheader bestehen aus den folgenden Teilen.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa2ff-109">Argument</span><span class="sxs-lookup"><span data-stu-id="aa2ff-109">Part</span></span></p></th>
<th><p><span data-ttu-id="aa2ff-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa2ff-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa2ff-111"><strong>connect</strong></span><span class="sxs-lookup"><span data-stu-id="aa2ff-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="aa2ff-112">Eine Literalzeichenfolge, durch die eine Verbindungszeichenfolge geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa2ff-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="aa2ff-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="aa2ff-114">Eine Literalzeichenfolge, durch die eine Befehlszeichenfolge geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa2ff-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="aa2ff-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="aa2ff-116">Eine Literalzeichenfolge, durch die die Zugriffsrechte eines bestimmten Benutzers geändert werden.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa2ff-117"><strong>logs</strong></span><span class="sxs-lookup"><span data-stu-id="aa2ff-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="aa2ff-118">Eine Literalzeichenfolge, durch die eine Protokolldatei angegeben wird, in der Ausführungsfehler aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa2ff-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="aa2ff-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="aa2ff-120">Eine Literalzeichenfolge, die verwendet wird, wenn kein Bezeichner angegeben ist oder gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa2ff-121"><em>identifier</em></span><span class="sxs-lookup"><span data-stu-id="aa2ff-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="aa2ff-122">Eine Zeichenfolge, die mit einer Zeichenfolge in der <strong>connect</strong>- oder <strong>command</strong>-Zeichenfolge übereinstimmt.
</span><span class="sxs-lookup"><span data-stu-id="aa2ff-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="aa2ff-123">Verwenden Sie diesen Abschnitt, wenn der Abschnittsheader <strong>connect</strong> enthält und die Bezeichnerzeichenfolge in der Verbindungszeichenfolge gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="aa2ff-124">Verwenden Sie diesen Abschnitt, wenn der Abschnittsheader <strong>sql</strong> enthält und die Bezeichnerzeichenfolge in der Befehlszeichenfolge gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="aa2ff-125">Verwenden Sie diesen Abschnitt, wenn der Abschnittsheader <strong>userlist</strong> enthält und die Bezeichnerzeichenfolge mit einem <strong>connect</strong>-Abschnittsbezeichner übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa2ff-p102">Durch **DataFactory** wird der Handler aufgerufen, dabei werden Clientparameter übergeben. Die Clientparameter werden vom Handler nach gesamten Zeichenfolgen durchsucht, die mit Bezeichnern in den entsprechenden Abschnittsheadern übereinstimmen. Wenn eine Übereinstimmung gefunden wird, wird der Inhalt dieses Abschnitts auf den Clientparameter angewendet.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-p102">The **DataFactory** calls the handler, passing client parameters. The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers. If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="aa2ff-129">Unter den folgenden Bedingungen wird ein bestimmter Abschnitt verwendet:</span><span class="sxs-lookup"><span data-stu-id="aa2ff-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="aa2ff-130">Ein Abschnitt **Verbinden** wird verwendet, wenn der Wertteil des Clients-Schlüsselworts, verbinden "\**Data Source = \*\*\* Wert*", mit einem Abschnittsbezeichner **Verbinden** *.* übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="aa2ff-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="aa2ff-131">Ein **sql** -Abschnitt wird verwendet, wenn die Clientbefehlszeichenfolge eine Zeichenfolge enthält, die mit einem **sql** -Abschnittsbezeichner übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="aa2ff-132">Ein **connect** - oder **sql** -Abschnitt mit einem Standardparameter wird verwendet, wenn kein entsprechender Bezeichner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="aa2ff-p103">Ein **userlist** -Abschnitt wird verwendet, wenn der **userlist** -Abschnittsbezeichner mit einem **connect** -Abschnittsbezeichner übereinstimmt. Wenn eine Übereinstimmung vorliegt, wird der Inhalt des **userlist** -Abschnitts auf die Verbindung angewendet, die dem **connect** -Abschnitt unterliegt.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-p103">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier. If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="aa2ff-135">Wenn die Zeichenfolge in einer Verbindungs- oder Befehlszeichenfolge nicht mit dem Bezeichner in einem **connect** - oder **sql** -Abschnittsheader übereinstimmt und kein **connect** - oder **sql** -Abschnittsheader mit einem Standardparameter vorhanden ist, wird die Clientzeichenfolge ohne Änderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="aa2ff-136">Der **logs** -Abschnitt wird verwendet, wenn **DataFactory** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa2ff-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

