---
title: Parametrisierte Befehle mit dazwischenliegenden COMPUTE-Befehlen
TOCTitle: Parameterized commands with intervening COMPUTE commands
ms:assetid: ff3724cd-040b-4b5f-bb9b-e6a38fd938c9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250311(v=office.15)
ms:contentKeyID: 48548959
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4172fba2d9fc08d3cf9f588fe9ace65da7997b19
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701935"
---
# <a name="parameterized-commands-with-intervening-compute-commands"></a>Parametrisierte Befehle mit dazwischenliegenden COMPUTE-Befehlen


**Betrifft**: Access 2013, Office 2013

Ein typischer parametrisierter Shape-Befehl APPEND besitzt eine Klausel, die ein übergeordnetes **Recordset** -Objekt mit einen Abfragebefehl erstellt, sowie eine weitere Klausel, die ein untergeordnetes **Recordset** -Objekt mit einem parametrisierten Abfragebefehl erstellt, d. h. einem Befehl, der einen Parameterplatzhalter (ein Fragezeichen "?") enthält. Das resultierende strukturierte **Recordset** -Objekt besteht aus zwei Ebenen. Dabei bildet das übergeordnete Recordset die höhere und das untergeordnete Recordset die niedrigere Ebene.

Die Klausel, die ein untergeordnetes **Recordset**-Objekt erstellt, kann nun aus einer Reihe geschachtelter Shape-Befehle COMPUTE bestehen, wobei der am tiefsten geschachtelte Befehl die parametrisierte Abfrage enthält. Das resultierende strukturierte **Recordset**-Objekt besteht aus mehreren Ebenen. Dabei bildet das übergeordnete Recordset die höchste und das untergeordnete Recordset die niedrigste Ebene, und die dazwischen liegenden Ebenen enthalten eine beliebige Anzahl von **Recordset**-Objekten, die von den Shape-Befehlen COMPUTE erstellt werden.

In der Regel wird dieses Feature zum Aufrufen der Aggregatfunktion und der Gruppierungsfunktionen von Shape-Befehlen COMPUTE verwendet, um dazwischen liegende **Recordset** -Objekte mit analytischen Informationen zum untergeordneten **Recordset** -Objekt zu erstellen. Da es sich um einen parametrisierten Shape-Befehl handelt, wird darüber hinaus möglicherweise bei jedem Zugriff auf die Kapitelspalte des übergeordneten Recordsets ein neues untergeordnetes **Recordset** -Objekt abgerufen. Da die dazwischen liegenden Ebenen vom untergeordneten Recordset stammen, werden sie ebenfalls neu berechnet.

