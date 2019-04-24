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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306902"
---
# <a name="solutions-for-remote-data-access"></a>Lösungen für Remote-Datenzugriff

**Gilt für**: Access 2013, Office 2013

## <a name="the-issue"></a>Das Problem

Mit ADO ist es möglich, über die Anwendung direkt auf Datenquellen zuzugreifen und sie zu ändern (wird manchmal als zweistufiges System bezeichnet). Wenn die Verbindung z. B. mit der Datenquelle hergestellt wird, die die Daten enthält, handelt es sich um eine direkte Verbindung in einem zweistufigen System.

Möglicherweise möchten Sie jedoch indirekt über einen Vermittler wie Microsoft Internet Information Services (IIS) auf Datenquellen zugreifen. Diese Anordnung wird manchmal als dreistufiges System bezeichnet. IIS ist ein Client-/Server-System, durch das eine effiziente Möglichkeit bereitgestellt wird, mit einer lokalen Anwendung oder Clientanwendung ein Remoteprogramm oder Serverprogramm über das Internet oder ein Intranet aufzurufen. Durch das Serverprogramm wird auf die Datenquelle zugegriffen, und optional werden die erfassten Daten verarbeitet.

Beispielsweise enthält Ihre Intranet-Webseite eine in Microsoft Visual Basic Scripting Edition (VBScript) geschriebene Anwendung, die eine Verbindung mit IIS herstellt. IIS stellt wiederum eine Verbindung mit der tatsächlichen Datenquelle her, ruft die Daten ab, verarbeitet sie in irgendeiner Weise und gibt dann die verarbeiteten Informationen an Ihre Anwendung zurück.

In diesem Beispiel wurde durch die Anwendung nie direkt eine Verbindung mit der Datenquelle hergestellt; dies erfolgte über IIS. Und durch IIS wurde mithilfe von ADO auf die Daten zugegriffen.

> [!NOTE]
> Die Client/Server-Anwendung muss nicht auf dem Internet oder einem Intranet (also webbasiert) basieren, sondern ausschließlich aus kompilierten Programmen in einem lokalen Netzwerk bestehen. Der typische Fall ist jedoch eine webbasierte Anwendung.

Da die zurückgegebenen Informationen möglicherweise von manchen visuellen Steuerelementen, z. B. von Rastern, Kontrollkästchen oder Listen, verwendet werden, müssen die zurückgegebenen Informationen leicht durch ein visuelles Steuerelement verwendet werden können.

Sie benötigen eine einfache und effiziente Anwendungsprogrammierschnittstelle, von der dreistufige Systeme unterstützt und Informationen so einfach zurückgegeben werden, als seien sie auf einem zweistufigen System abgerufen worden. Diese Schnittstelle ist Remote Data Service (RDS).

## <a name="the-solution"></a>Die Lösung

RDS definiert ein Programmiermodell – die Abfolge der erforderlichen Aktivitäten für den Zugriff auf und das Aktualisieren einer Datenquelle –, um Zugriff auf Daten über einen Vermittler wie Internet Informationsdienste (IIS) zu erhalten. Im Programmiermodell wird die gesamte Funktionalität von RDS zusammengefasst.

