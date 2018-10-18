---
title: Verwenden einer separaten Anwendungsdomäne zur Vermeidung von Abstürzen
TOCTitle: Using a separate application domain to avoid crashing
ms:assetid: 7fc6d1e5-7032-47a9-826f-6b5d3b43fef9
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb623114(v=office.15)
ms:contentKeyID: 55119786
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b397fa2ad37102e12a3a0cf569e74323391b8e86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407254"
---
# <a name="using-a-separate-application-domain-to-avoid-crashing"></a>Verwenden einer separaten Anwendungsdomäne zur Vermeidung von Abstürzen

Verwaltete Add-Ins, durch die die **IDTExtensibility2**-Schnittstelle implementiert wird, werden in dieselbe Standardanwendungsdomäne geladen. Wenn ein Add-In in der Anwendungsdomäne abstürzt, treten unter Umständen auch in anderen Add-Ins in derselben Anwendungsdomäne Fehler auf.

Zur Umgehung des Problems können Sie einen Shim für das Add-In erstellen, sodass das Add-In in einer eigenen Anwendungsdomäne geladen werden kann. Ein Shim ist eine nicht verwaltete, in C++ geschriebene Dynamic Link Library. Wenn Sie einen Shim verwenden, registrieren Sie den Shim anstelle des Add-Ins. Outlook lädt den Shim, und der Shim lädt das Add-In, für das er erstellt wurde. Sie müssen für jedes Add-In einen gesonderten Shim erstellen und registrieren. Weitere Informationen zum Entwickeln von Shims für verwaltete Add-Ins finden Sie unter [Isolieren von Office-Erweiterungen mit dem COM Shim-Assistenten](https://go.microsoft.com/fwlink/?linkid=89109).

Eine weitere Alternative zum Laden Ihres Add-Ins in einer separaten Anwendungsdomäne besteht darin, das Add-In mithilfe von Office-Entwicklungstools in Visual Studio 2010 oder in einer höheren Version der Office Developer Tools für Visual Studio zu entwickeln. Add-Ins, die mit diesen Versionen von Office Developer Tools für Visual Studio entwickelt wurden, implementieren nicht die IDTExtensibility2-Schnittstelle nicht, aber verwenden die **IStartup**-Schnittstelle. Sie verwenden ein von Visual Studio bereitgestelltes Ladeprogramm von Visual Studio (AddinLoader.dll), das als allgemeines Shim fungiert. Outlook sucht in der Registrierung nach Add-Ins, die mit Visual Studio erstellt wurden. 

Wenn Outlook derartige Add-Ins findet, wird „AddinLoader.dll“ gestartet, wodurch wiederum die Laufzeit der Visual Studio-Tools für Office gestartet und das Anwendungsmanifest an diese übermittelt wird. Die Laufzeit von Visual Studio Tools für Office lädt dann die einzelnen Add-Ins in einer separaten Anwendungsdomäne. Weitere Informationen dazu, wie ein Add-In in Visual Studio geladen wird, finden Sie unter [Architektur von Add-Ins auf Anwendungsebene](https://msdn.microsoft.com/library/bb386298\(v=office.15\)).

