---
title: DriverPromptEnum Enumeration (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c20542c89537f16f20c9d3e30cbc14ce115bf4d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476036"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="2de11-102">DriverPromptEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="2de11-102">DriverPromptEnum Enumeration (DAO)</span></span>


<span data-ttu-id="2de11-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2de11-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2de11-104">Gibt an, ob und zu welchem Zeitpunkt der Benutzer aufgefordert wird, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2de11-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2de11-105">Name</span><span class="sxs-lookup"><span data-stu-id="2de11-105">Name</span></span></p></th>
<th><p><span data-ttu-id="2de11-106">Wert</span><span class="sxs-lookup"><span data-stu-id="2de11-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2de11-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2de11-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2de11-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="2de11-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="2de11-109">0</span><span class="sxs-lookup"><span data-stu-id="2de11-109">0</span></span></p></td>
<td><p><span data-ttu-id="2de11-110">Wenn die eingegebene Verbindungszeichenfolge das Schlüsselwort DSN enthält, verwendet der Treibermanager die in "connect" angegebene Zeichenfolge. Andernfalls verhält er sich so, als ob <strong>dbDriverPrompt</strong> angegeben worden wäre.</span><span class="sxs-lookup"><span data-stu-id="2de11-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="2de11-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="2de11-112">3</span><span class="sxs-lookup"><span data-stu-id="2de11-112">3</span></span></p></td>
<td><p><span data-ttu-id="2de11-113">(Standard) Das Verhalten entspricht dem von <strong>dbDriverComplete</strong>, mit der Ausnahme, dass der Treiber die Steuerelemente für alle Informationen deaktiviert, die nicht für die Verbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2de11-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="2de11-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="2de11-115">1</span><span class="sxs-lookup"><span data-stu-id="2de11-115">1</span></span></p></td>
<td><p><span data-ttu-id="2de11-p101">Der Treibermanager verwendet die in "connect" angegebene Verbindungszeichenfolge. Wenn nicht ausreichend Informationen angegeben werden, wird ein auffangbarer Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2de11-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="2de11-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="2de11-119">2</span><span class="sxs-lookup"><span data-stu-id="2de11-119">2</span></span></p></td>
<td><p><span data-ttu-id="2de11-p102">Der Treibermanager zeigt das Dialogfeld <strong>ODBC-Datenquellen</strong> an. Die zum Herstellen der Verbindung verwendete Verbindungszeichenfolge wird anhand des ausgewählten Datenquellennamens (Data Source Name, DSN) erstellt und vom Benutzer mithilfe der Dialogfelder fertig gestellt.</span><span class="sxs-lookup"><span data-stu-id="2de11-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>

