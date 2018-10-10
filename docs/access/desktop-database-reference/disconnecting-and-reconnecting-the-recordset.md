---
title: Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90435606bb0b3059f5769c12fe7cf3cac0c8f9f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475957"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt


**Betrifft**: Access 2013 | Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt

Eine der leistungsstärksten Features in ADO ist die Funktion zum Öffnen eines clientseitigen **Recordset**-Objekts in einer Datenquelle und das anschließende *Trennen* des **Recordset**-Objekts von der Datenquelle. Nachdem das **Recordset**-Objekt getrennt wurde, kann die Verbindung zur Datenquelle geschlossen werden, wodurch die auf dem Server vorhandenen Ressourcen zur Verwaltung der Verbindung freigegeben werden. Sie können die Daten im **Recordset**-Objekt weiterhin bearbeiten und anzeigen, wenn keine Verbindung besteht. Später können Sie dann erneut eine Verbindung mit der Datenquelle herstellen und Ihre Aktualisierungen im Batchmodus senden.

Zum Trennen eines **Recordset**-Objekts, öffnen Sie dieses mit der Cursorplatzierung **adUseClient**, und legen Sie dann die **ActiveConnection**-Eigenschaft auf *Nothing* fest. (C++-Benutzer sollten zum Trennen die **ActiveConnection**-Eigenschaft auf NULL festlegen.)

Weiter unten in diesem Kapitel bei der Behandlung der permanenten Verfügbarkeit des **Recordset** -Objekts werden wir ein getrenntes **Recordset** -Objekt verwenden, um die Daten in einem **Recordset** -Objekt für eine Anwendung bereitzustellen, während der Clientcomputer mit keinem Netzwerk verbunden ist.

