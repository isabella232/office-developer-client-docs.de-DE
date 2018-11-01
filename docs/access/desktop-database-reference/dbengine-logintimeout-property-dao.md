---
title: DBEngine.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8c6b7798419dc72dc28822741e2d038203ae257e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880719"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="0b470-102">DBEngine.LoginTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0b470-102">DBEngine.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="0b470-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b470-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b470-104">Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="0b470-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b470-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b470-105">Syntax</span></span>

<span data-ttu-id="0b470-106">*Ausdruck* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="0b470-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="0b470-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b470-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b470-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b470-108">Remarks</span></span>

<span data-ttu-id="0b470-p101">Die Standardeinstellung der LoginTimeout-Eigenschaft beträgt 20 Sekunden. Wenn die LoginTimeout-Eigenschaft auf 0 gesetzt ist, tritt kein Timeout ein.</span><span class="sxs-lookup"><span data-stu-id="0b470-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="0b470-p102">Wenn Sie versuchen, sich bei einer ODBC-Datenbank anzumelden, wie etwa bei Microsoft SQL Server, kann die Verbindung aufgrund eines Netzwerkfehlers fehlschlagen oder aber weil der Server nicht ausgeführt wird. Anstatt die standardmäßig festgelegten 20 Sekunden auf die Verbindung zu warten, können Sie festlegen, wie lange gewartet werden soll, bis ein Fehler erzeugt wird. Die Anmeldung beim Server wird implizit als Teil einer Reihe von verschiedenen Ereignissen ausgeführt, wie etwa beim Ausführen einer Abfrage einer externen Serverdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0b470-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

