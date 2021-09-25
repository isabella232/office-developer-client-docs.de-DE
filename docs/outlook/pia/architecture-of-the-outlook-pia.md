---
title: Architektur der Outlook PIA
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3bc4a03d5954e28bc423c835ee582993a9ac9bf1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590856"
---
# <a name="architecture-of-the-outlook-pia"></a>Architektur der Outlook-PIA

Die primäre Interopassembly (PIA) von Outlook unterstützt uneingeschränkt die Entwicklung für das Outlook-Objektmodell in verwaltetem Code. Wenn Sie die PIA jedoch erstmalig in einem Objektkatalog anzeigen, sind Sie möglicherweise überrascht von den vielen enthaltenen zusätzlichen Schnittstellen und davon, dass nicht alle Methoden-, Eigenschaften- und Ereignismember eines Objekts durch dieselbe Objektschnittstelle verfügbar gemacht werden. Die Themen in diesem Abschnitt enthalten Richtlinien für den Zugriff auf Objektmember in Code und für die Suche nach Hilfe zu Objekten, Methoden, Eigenschaften und Ereignissen.

## <a name="in-this-section"></a>Inhalt dieses Abschnitts

|Thema|Beschreibung|
|:----|:----------|
|[Zuordnen der Outlook-PIA zum Objektmodell](relating-the-outlook-pia-with-the-object-model.md) |Beschreibt, wie Objekte und Member im COM-basierten Outlook-Objektmodell entsprechenden verwalteten Schnittstellen und Klassen in der PIA zugeordnet werden.|
|[Objekte in der Outlook-PIA](objects-in-the-outlook-pia.md) |Beschreibt die typischen einem COM-Objekt zugeordneten .NET-Schnittstellen, Klassen und Delegate sowie den Zugriff auf ein Objekt in der PIA.|
|[Methoden und Eigenschaften in der Outlook-PIA](methods-and-properties-in-the-outlook-pia.md) |Beschreibt, wie mithilfe der PIA auf Methoden und Eigenschaften eines Objekts in verwaltetem Code zugegriffen wird.|
|[Ereignisse in der Outlook-PIA](events-in-the-outlook-pia.md) |Beschreibt ereignisabhängige Schnittstellen, Stellvertretungen und Senkenhilfsklassen in der PIA.|

## <a name="see-also"></a>Siehe auch

- [Einrichten der Outlook-PIA](setting-up-to-use-the-outlook-pia.md)
- [Entwickeln von verwalteten Outlook-Add-Ins mithilfe der Outlook-PIA](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [Gewusst wie... (Outlook 2013 PIA-Referenz)](how-do-i-outlook-2013-pia-reference.md)

