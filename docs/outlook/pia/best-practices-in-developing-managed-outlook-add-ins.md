---
title: Bewährte Methoden beim Entwickeln von verwalteten Outlook-Add-Ins
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87573980836d63d751302b0efcec0952331b7fc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406862"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="aebac-102">Bewährte Methoden beim Entwickeln von verwalteten Outlook-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="aebac-102">Best Practices in Developing Managed Outlook Add-ins</span></span>

<span data-ttu-id="aebac-p101">Auch wenn Sie mit den Outlook-Interopassemblys verwaltete Lösungen schreiben können, die mit Outlook zusammenarbeiten, wurde Outlook bereits vor der Einführung von .NET Framework entwickelt, um die Programmierung mit nicht verwalteten Sprachen wie Visual Basic for Applications (VBA) und Visual Basic zu unterstützen. In diesem Thema sind die wichtigsten Gesichtspunkte aufgeführt, die Sie beim Entwickeln eines verwalteten Add-Ins für Outlook beachten sollten.</span><span class="sxs-lookup"><span data-stu-id="aebac-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="aebac-105">Systematisches Freigeben von Objekten</span><span class="sxs-lookup"><span data-stu-id="aebac-105">Systematically Releasing Objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="aebac-106">Verwenden einer separaten Anwendungsdomäne zur Vermeidung von Abstürzen</span><span class="sxs-lookup"><span data-stu-id="aebac-106">Using a Separate Application Domain to Avoid Crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="aebac-107">Verwenden eines vertrauenswürdigen, von den Office Developer Tools für Visual Studio bereitgestellten Anwendungsobjekts</span><span class="sxs-lookup"><span data-stu-id="aebac-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="aebac-108">Geeignetes Festlegen von Bereichen für Variablen in Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="aebac-108">Scoping Variables Appropriately in Event Handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="aebac-109">Vermeiden von nicht unterstützten Technologien in verwalteten Outlook-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="aebac-109">Avoiding Unsupported Technologies in Managed Outlook Add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="aebac-110">Verwenden von spätem Binden bei mehreren Version von Outlook</span><span class="sxs-lookup"><span data-stu-id="aebac-110">Using Late Binding If Depending on Multiple Versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

