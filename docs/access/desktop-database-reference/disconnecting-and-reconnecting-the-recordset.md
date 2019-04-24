---
title: Trennen und erneutes Verbinden des Recordsets
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c028a7d867a105f35b4848ecbe95339f5fcd4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293861"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Trennen und erneutes Verbinden des Recordsets


**Gilt für**: Access 2013, Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt

Eine der leistungsstärksten Features in ADO ist die Funktion zum Öffnen eines clientseitigen **Recordset**-Objekts in einer Datenquelle und das anschließende *Trennen* des **Recordset**-Objekts von der Datenquelle. Nachdem das **Recordset**-Objekt getrennt wurde, kann die Verbindung zur Datenquelle geschlossen werden, wodurch die auf dem Server vorhandenen Ressourcen zur Verwaltung der Verbindung freigegeben werden. Sie können die Daten im **Recordset**-Objekt weiterhin bearbeiten und anzeigen, wenn keine Verbindung besteht. Später können Sie dann erneut eine Verbindung mit der Datenquelle herstellen und Ihre Aktualisierungen im Batchmodus senden.

Zum Trennen eines **Recordset**-Objekts, öffnen Sie dieses mit der Cursorplatzierung **adUseClient**, und legen Sie dann die **ActiveConnection**-Eigenschaft auf *Nothing* fest. (C++-Benutzer sollten zum Trennen die **ActiveConnection**-Eigenschaft auf NULL festlegen.)

Weiter unten in diesem Kapitel bei der Behandlung der permanenten Verfügbarkeit des **Recordset** -Objekts werden wir ein getrenntes **Recordset** -Objekt verwenden, um die Daten in einem **Recordset** -Objekt für eine Anwendung bereitzustellen, während der Clientcomputer mit keinem Netzwerk verbunden ist.

