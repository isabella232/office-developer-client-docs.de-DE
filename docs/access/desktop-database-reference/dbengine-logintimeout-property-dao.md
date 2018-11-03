---
title: DBEngine.LoginTimeout-Eigenschaft (DAO)
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
ms.openlocfilehash: 91669b054cf9075375c4a5457086adc45ba43c70
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925905"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="0c722-102">DBEngine.LoginTimeout-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="0c722-102">DBEngine.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="0c722-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c722-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c722-104">Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="0c722-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c722-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c722-105">Syntax</span></span>

<span data-ttu-id="0c722-106">*Ausdruck* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="0c722-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="0c722-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c722-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c722-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c722-108">Remarks</span></span>

<span data-ttu-id="0c722-p101">Die Standardeinstellung der LoginTimeout-Eigenschaft beträgt 20 Sekunden. Wenn die LoginTimeout-Eigenschaft auf 0 gesetzt ist, tritt kein Timeout ein.</span><span class="sxs-lookup"><span data-stu-id="0c722-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="0c722-p102">Wenn Sie versuchen, sich bei einer ODBC-Datenbank anzumelden, wie etwa bei Microsoft SQL Server, kann die Verbindung aufgrund eines Netzwerkfehlers fehlschlagen oder aber weil der Server nicht ausgeführt wird. Anstatt die standardmäßig festgelegten 20 Sekunden auf die Verbindung zu warten, können Sie festlegen, wie lange gewartet werden soll, bis ein Fehler erzeugt wird. Die Anmeldung beim Server wird implizit als Teil einer Reihe von verschiedenen Ereignissen ausgeführt, wie etwa beim Ausführen einer Abfrage einer externen Serverdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0c722-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

