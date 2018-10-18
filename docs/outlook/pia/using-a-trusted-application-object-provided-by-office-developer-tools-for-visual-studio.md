---
title: Verwenden eines vertrauenswürdigen, von den Office Developer Tools für Visual Studio bereitgestellten Anwendungsobjekts
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7b56e59b19f1c9a0ee4c730f14200c3e501f5290
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406113"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a>Verwenden eines vertrauenswürdigen, von den Office Developer Tools für Visual Studio bereitgestellten Anwendungsobjekts

Wenn Sie ein verwaltetes Add-In mithilfe von Office Developer Tools für Visual Studio entwickeln, verwenden Sie immer das [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt, das von Visual Studio bereitgestellt wird. 

Wenn Sie nicht planen, eine neue Instanz von Outlook zu automatisieren, verwenden Sie nicht das New- oder das new-Schlüsselwort zum Erstellen einer neuen Instanz von Outlook, da diese Instanz des **Application**-Objekts sonst durch den Outlook Object Model Guard nicht als vertrauenswürdig eingestuft wird. 

Falls Ihr Add-In eine nicht vertrauenswürdige Instanz des **Application**-Objekts verwendet, kann das Add-In, abhängig von der Outlook-Version des Clients, standardmäßig den Object Model Guard von Outlook für einen Reihe von Mitgliedern des Objektmodells abrufen. 

Weitere Informationen zum Verhalten des Objektmodellwächter finden Sie unter [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)). Beachten Sie dabei, dass obwohl sich dieser Artikel auf COM-Add-Ins bezieht, die standardmäßig als vertrauenswürdig eingestuft werden, der Entwurf für Outlook-Versionen ab Outlook 2007 und gleichermaßen für verwaltete Add-Ins gilt. Unabhängig davon, ob das Add-In verwaltet wird, basiert die Vertrauenswürdigkeit auf der Annahme, dass das Add-In ein vertrauenswürdiges **Application**-Objekt verwendet.

