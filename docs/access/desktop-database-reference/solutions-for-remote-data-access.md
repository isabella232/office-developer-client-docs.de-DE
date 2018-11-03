---
title: Lösungen für Remotedatenzugriff
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c03a6495b6d95723469d14dc1c3d9d2972760865
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937169"
---
# <a name="solutions-for-remote-data-access"></a>Lösungen für Remotedatenzugriff


**Betrifft**: Access 2013, Office 2013

## <a name="the-issue"></a>Das Problem

Mit ADO ist es möglich, über die Anwendung direkt auf Datenquellen zuzugreifen und sie zu ändern (wird manchmal als zweistufiges System bezeichnet). Wenn die Verbindung z. B. mit der Datenquelle hergestellt wird, die die Daten enthält, handelt es sich um eine direkte Verbindung in einem zweistufigen System.

Sie möchten jedoch indirekt Zugriff auf Datenquellen über die Vermittlung wie beispielsweise Microsoft Internet Information Services (IIS). Diese Anordnung wird manchmal als dreistufiges System bezeichnet. IIS ist ein Client-/Server-System, durch das eine effiziente Möglichkeit bereitgestellt wird, mit einer lokalen Anwendung oder Clientanwendung ein Remoteprogramm oder Serverprogramm über das Internet oder ein Intranet aufzurufen. Durch das Serverprogramm wird auf die Datenquelle zugegriffen, und optional werden die erfassten Daten verarbeitet.

Beispielsweise enthält Ihre Intranet-Webseite eine Anwendung in Microsoft Visual Basic Scripting Edition (VBScript), das mit IIS verbindet geschrieben. IIS wiederum eine Verbindung mit der tatsächlichen Datenquelle, ruft die Daten, auf irgendeine Weise verarbeitet und gibt dann die verarbeitete Informationen zu Ihrer Anwendung zurück.

In diesem Beispiel wurde durch die Anwendung nie direkt eine Verbindung mit der Datenquelle hergestellt; dies erfolgte über IIS. Und durch IIS wurde mithilfe von ADO auf die Daten zugegriffen.


> [!NOTE]
> <P>[!HINWEIS] Die Client-/Serveranwendung muss nicht auf dem Internet oder einem Intranet basieren (d. h. webbasiert sein) - sie kann ausschließlich aus kompilierten Programmen in einem lokalen Netzwerk bestehen. Der typische Fall ist jedoch eine webbasierte Anwendung.</P>



Da die zurückgegebenen Informationen möglicherweise von manchen visuellen Steuerelementen, z. B. von Rastern, Kontrollkästchen oder Listen, verwendet werden, müssen die zurückgegebenen Informationen leicht durch ein visuelles Steuerelement verwendet werden können.

Sie benötigen eine einfache und effiziente Anwendungsprogrammierschnittstelle, von der dreistufige Systeme unterstützt und Informationen so einfach zurückgegeben werden, als seien sie auf einem zweistufigen System abgerufen worden. Diese Schnittstelle ist Remote Data Service (RDS).

## <a name="the-solution"></a>Die Lösung

Durch RDS wird ein Programmiermodell definiert - die Reihenfolge der Aktivitäten, die notwendig sind, um auf eine Datenquelle zuzugreifen und sie zu aktualisieren -, um über einen Vermittler auf Daten zuzugreifen, z. B. über Internetinformationsdienste (Internet Information Services, IIS). Im Programmiermodell wird die gesamte Funktionalität von RDS zusammengefasst.

