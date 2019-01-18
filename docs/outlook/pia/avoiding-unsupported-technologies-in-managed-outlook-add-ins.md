---
title: Vermeiden von nicht unterstützten Technologien in verwalteten Outlook-Add-Ins
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99cdfc2447e6bf63078eb87bb9546d8b07ee83e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705421"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a><span data-ttu-id="bdf35-102">Vermeiden von nicht unterstützten Technologien in verwalteten Outlook-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="bdf35-102">Avoiding unsupported technologies in managed Outlook add-ins</span></span>

<span data-ttu-id="bdf35-103">Bestimmte Technologien, die für das .NET Framework galten, werden in der Programmierung von verwaltetem Code nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bdf35-103">Certain technologies that predate the .NET Framework are not supported in managed code programming.</span></span> <span data-ttu-id="bdf35-104">Dazu gehören Datenobjekte für die Zusammenarbeit (Collaboration Data Objects, CDO), MAPI (Messaging Application Programming Interface, auch bekannt als Extended MAPI) und Simple MAPI.</span><span class="sxs-lookup"><span data-stu-id="bdf35-104">These technologies include Collaboration Data Objects (CDO), Messaging Application Programming Interface (MAPI, often known as Extended MAPI), and Simple MAPI.</span></span> <span data-ttu-id="bdf35-105">Diese Technologien wurden mit nicht verwaltetetem Code entworfen und entwickelt, und Microsoft stellt keine offiziell verwalteten Wrapper dafür zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bdf35-105">These technologies were designed and developed with unmanaged code, and Microsoft does not provide official managed wrappers to support their use in managed applications.</span></span> 

<span data-ttu-id="bdf35-106">Weitere Informationen finden Sie im Abschnitt „APIs that are supported in managed code“ im Artikel [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).</span><span class="sxs-lookup"><span data-stu-id="bdf35-106">For more information, see the section "APIs that are supported in managed code" in the article [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).</span></span>

<span data-ttu-id="bdf35-107">Microsoft Outlook bietet dennoch viele Objektmodellfeatures, mit denen erzielt werde kann, was bisher nur mit CDO und Exchange-Clienterweiterungen (ECE) für Entwickler gelöst werden konnte.</span><span class="sxs-lookup"><span data-stu-id="bdf35-107">Nonetheless, Microsoft Outlook offers many object model features that achieve what previously only CDO and Exchange Client Extensions (ECE) solved for developers.</span></span> <span data-ttu-id="bdf35-108">Wenn Sie CDO in einer vorhandenen nicht verwalteten Outlook-Anwendung verwenden und die fehlende Unterstützung von CDO in verwalteten Lösungen Sie am Migrieren der Anwendung in verwalteten Code gehindert hat, können Sie nun überlegen, ob Sie Ihre Lösung mithilfe des Outlook-Objektmodells und der primären Interop-Assembly (PIA) auf verwalteteten Code aktualisieren, ohne dabei auf CDO zurückgreifen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="bdf35-108">If you use CDO in an existing unmanaged Outlook application and the lack of support for CDO in managed solutions has hindered you from migrating the application to managed code, you can now consider updating your solution to managed code, using only the Outlook object model and the Primary Interop Assembly (PIA), without having to resort to CDO.</span></span> 

<span data-ttu-id="bdf35-109">Weitere Informationen zur umfassenderen Outlook-Plattform und der reduzierten bedeutung von CDO und ECE in Outlook 2007 finden Sie unter [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="bdf35-109">For more information about a more comprehensive Outlook platform introduced in Outlook 2007 to reduce reliance on CDO and ECE, see [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span></span>

