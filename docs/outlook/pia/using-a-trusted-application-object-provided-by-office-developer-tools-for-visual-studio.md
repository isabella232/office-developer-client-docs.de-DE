---
title: Verwenden eines vertrauenswürdigen, von den Office Developer Tools für Visual Studio bereitgestellten Anwendungsobjekts
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f86ad294e894b4faea10d033a069638221f1bd78
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703013"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a><span data-ttu-id="a7889-102">Verwenden eines vertrauenswürdigen, von den Office Developer Tools für Visual Studio bereitgestellten Anwendungsobjekts</span><span class="sxs-lookup"><span data-stu-id="a7889-102">Using a trusted Application object provided by Office Developer Tools for Visual Studio</span></span>

<span data-ttu-id="a7889-103">Wenn Sie ein verwaltetes Add-In mithilfe von Office Developer Tools für Visual Studio entwickeln, verwenden Sie immer das [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt, das von Visual Studio bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a7889-103">If you are developing a managed add-in by using Office Developer Tools for Visual Studio, always use the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that is provided by Visual Studio.</span></span> 

<span data-ttu-id="a7889-104">Wenn Sie nicht planen, eine neue Instanz von Outlook zu automatisieren, verwenden Sie nicht das New- oder das new-Schlüsselwort zum Erstellen einer neuen Instanz von Outlook, da diese Instanz des **Application**-Objekts sonst durch den Outlook Object Model Guard nicht als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="a7889-104">Unless you intend to automate a new instance of Outlook, do not use the New or new keyword to create a new instance of Outlook, as this instance of the **Application** object is not trusted from the perspective of the Outlook Object Model Guard.</span></span> 

<span data-ttu-id="a7889-105">Falls Ihr Add-In eine nicht vertrauenswürdige Instanz des **Application**-Objekts verwendet, kann das Add-In, abhängig von der Outlook-Version des Clients, standardmäßig den Object Model Guard von Outlook für einen Reihe von Mitgliedern des Objektmodells abrufen.</span><span class="sxs-lookup"><span data-stu-id="a7889-105">If your add-in uses an untrusted instance of the **Application** object, depending on the version of Outlook that the client is running, the add-in by default will invoke Outlook's Object Model Guard on a number of members of the object model.</span></span> 

<span data-ttu-id="a7889-106">Weitere Informationen zum Verhalten des Objektmodellwächter finden Sie unter [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a7889-106">For more information about the behavior of the Object Model Guard, see [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span></span> <span data-ttu-id="a7889-107">Beachten Sie dabei, dass obwohl sich dieser Artikel auf COM-Add-Ins bezieht, die standardmäßig als vertrauenswürdig eingestuft werden, der Entwurf für Outlook-Versionen ab Outlook 2007 und gleichermaßen für verwaltete Add-Ins gilt.</span><span class="sxs-lookup"><span data-stu-id="a7889-107">Note that even though the "Code Security Changes in Outlook 2007" article refers to COM add-ins that are trusted by default, this design applies to versions of Outlook since Outlook 2007, and the trust applies to managed add-ins the same way.</span></span> <span data-ttu-id="a7889-108">Unabhängig davon, ob das Add-In verwaltet wird, basiert die Vertrauenswürdigkeit auf der Annahme, dass das Add-In ein vertrauenswürdiges **Application**-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7889-108">Regardless of whether the add-in is managed or not, the trust is based on the assumption that the add-in uses a trusted **Application** object.</span></span>

