---
title: Workspace.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6427b99fd212fa358b70fb20a5ecf0c9180209fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472694"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="b90d1-102">Workspace.LoginTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b90d1-102">Workspace.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="b90d1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b90d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b90d1-104">Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="b90d1-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b90d1-105">Syntax</span></span>

<span data-ttu-id="b90d1-106">*Ausdruck* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="b90d1-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="b90d1-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b90d1-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b90d1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b90d1-108">Remarks</span></span>

<span data-ttu-id="b90d1-p101">Die Standardeinstellung der LoginTimeout-Eigenschaft beträgt 20 Sekunden. Wenn die LoginTimeout-Eigenschaft auf 0 gesetzt ist, tritt kein Timeout ein.</span><span class="sxs-lookup"><span data-stu-id="b90d1-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="b90d1-p102">Wenn Sie versuchen, sich bei einer ODBC-Datenbank anzumelden, wie etwa bei Microsoft SQL Server, kann die Verbindung aufgrund eines Netzwerkfehlers fehlschlagen oder aber weil der Server nicht ausgeführt wird. Anstatt die standardmäßig festgelegten 20 Sekunden auf die Verbindung zu warten, können Sie festlegen, wie lange gewartet werden soll, bis ein Fehler erzeugt wird. Die Anmeldung beim Server wird implizit als Teil einer Reihe von verschiedenen Ereignissen ausgeführt, wie etwa beim Ausführen einer Abfrage einer externen Serverdatenbank.</span><span class="sxs-lookup"><span data-stu-id="b90d1-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

