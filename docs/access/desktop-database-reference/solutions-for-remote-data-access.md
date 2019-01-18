---
title: Lösungen für Remotedatenzugriff
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b64ed19c268874e0e52a87bc2e05aacb6083422
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711504"
---
# <a name="solutions-for-remote-data-access"></a>Lösungen für Remotedatenzugriff

**Betrifft**: Access 2013, Office 2013

## <a name="the-issue"></a>Das Problem

Mit ADO ist es möglich, über die Anwendung direkt auf Datenquellen zuzugreifen und sie zu ändern (wird manchmal als zweistufiges System bezeichnet). Wenn die Verbindung z. B. mit der Datenquelle hergestellt wird, die die Daten enthält, handelt es sich um eine direkte Verbindung in einem zweistufigen System.

Sie möchten jedoch indirekt Zugriff auf Datenquellen über die Vermittlung wie beispielsweise Microsoft Internet Information Services (IIS). Diese Anordnung wird manchmal als dreistufiges System bezeichnet. IIS ist ein Client-/Server-System, durch das eine effiziente Möglichkeit bereitgestellt wird, mit einer lokalen Anwendung oder Clientanwendung ein Remoteprogramm oder Serverprogramm über das Internet oder ein Intranet aufzurufen. Durch das Serverprogramm wird auf die Datenquelle zugegriffen, und optional werden die erfassten Daten verarbeitet.

Beispielsweise enthält Ihre Intranet-Webseite eine Anwendung in Microsoft Visual Basic Scripting Edition (VBScript), das mit IIS verbindet geschrieben. IIS wiederum eine Verbindung mit der tatsächlichen Datenquelle, ruft die Daten, auf irgendeine Weise verarbeitet und gibt dann die verarbeitete Informationen zu Ihrer Anwendung zurück.

In diesem Beispiel wurde durch die Anwendung nie direkt eine Verbindung mit der Datenquelle hergestellt; dies erfolgte über IIS. Und durch IIS wurde mithilfe von ADO auf die Daten zugegriffen.

> [!NOTE]
> Die Client/Server-Anwendung muss nicht auf das Internet oder Intranet basieren (d. h., webbasierte) – Es konnte bestehen kompilierte Programme auf einem lokalen Netzwerk. Jedoch ist der typische Fall eine webbasierte Anwendung.

Da die zurückgegebenen Informationen möglicherweise von manchen visuellen Steuerelementen, z. B. von Rastern, Kontrollkästchen oder Listen, verwendet werden, müssen die zurückgegebenen Informationen leicht durch ein visuelles Steuerelement verwendet werden können.

Sie benötigen eine einfache und effiziente Anwendungsprogrammierschnittstelle, von der dreistufige Systeme unterstützt und Informationen so einfach zurückgegeben werden, als seien sie auf einem zweistufigen System abgerufen worden. Diese Schnittstelle ist Remote Data Service (RDS).

## <a name="the-solution"></a>Die Lösung

RDS definiert ein Programmiermodell – die Reihenfolge der Aktivitäten, die erforderlich sind, um den Zugriff auf und Aktualisieren einer Datenquelle – den Zugriff auf Daten über die Vermittlung, wie Internetinformationsdienste (Internet Information Services, IIS). Das Programmiermodell zusammengefasst, die gesamte Funktionalität von RDS.

