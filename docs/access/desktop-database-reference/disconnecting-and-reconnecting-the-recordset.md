---
title: Trennen und erneutes Verbinden des Recordsets
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c8d9cbb5771e3f78e5917a06a27aa79cbd14ec73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553081"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Trennen und erneutes Verbinden des Recordsets


**Gilt für**: Access 2013, Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt

Eine der leistungsstärksten Features in ADO ist die Funktion zum Öffnen eines clientseitigen **Recordset**-Objekts in einer Datenquelle und das anschließende *Trennen* des **Recordset**-Objekts von der Datenquelle. Nachdem das **Recordset**-Objekt getrennt wurde, kann die Verbindung zur Datenquelle geschlossen werden, wodurch die auf dem Server vorhandenen Ressourcen zur Verwaltung der Verbindung freigegeben werden. Sie können die Daten im **Recordset**-Objekt weiterhin bearbeiten und anzeigen, wenn keine Verbindung besteht. Später können Sie dann erneut eine Verbindung mit der Datenquelle herstellen und Ihre Aktualisierungen im Batchmodus senden.

Zum Trennen eines **Recordset**-Objekts, öffnen Sie dieses mit der Cursorplatzierung **adUseClient**, und legen Sie dann die **ActiveConnection**-Eigenschaft auf *Nothing* fest. (C++-Benutzer sollten zum Trennen die **ActiveConnection**-Eigenschaft auf NULL festlegen.)

Weiter unten in diesem Kapitel bei der Behandlung der permanenten Verfügbarkeit des **Recordset** -Objekts werden wir ein getrenntes **Recordset** -Objekt verwenden, um die Daten in einem **Recordset** -Objekt für eine Anwendung bereitzustellen, während der Clientcomputer mit keinem Netzwerk verbunden ist.

