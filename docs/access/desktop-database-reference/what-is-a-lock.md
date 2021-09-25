---
title: Was ist eine Sperre? (Access-Desktopdatenbankreferenz)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b5b72e36d548d729040a3e4f5406daacc3a4fa9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593278"
---
# <a name="what-is-a-lock"></a>Was ist eine Sperre?


**Gilt für**: Access 2013, Office 2013

Unter dem Sperren versteht man den Prozess, mit dem ein DBMS den Zugriff auf eine Zeile in einer Mehrbenutzerumgebung sperrt. Wenn eine Zeile oder Spalte exklusiv gesperrt ist, können andere Benutzer erst auf die gesperrten Daten zugreifen, wenn die Sperre aufgehoben wurde. Dadurch wird verhindert, dass zwei Benutzer gleichzeitig dieselbe Spalte in einer Zeile aktualisieren.

Sperren können im Hinblick auf die Ressourcen sehr teuer sein und sollten nur verwendet werden, wenn sie zur Aufrechterhaltung der Datenintegrität erforderlich sind. In einer Datenbank, in der jede Sekunde Hunderte oder Tausende von Benutzern versuchen könnten, auf einen Datensatz zuzugreifen (z. B. eine Datenbank, die mit dem Internet verbunden ist), könnten unnötige Sperren schnell zu einer Leistungsbeeinträchtigung der Anwendung führen.

Sie können steuern, wie die Datenquelle und die ADO-Cursorbibliothek die Parallelität verwalten, indem Sie die entsprechende Sperroption auswählen.

Legen Sie die **LockType** -Eigenschaft vor dem Öffnen eines **Recordset** -Objekts fest, um anzugeben, welchen Sperrtyp der Anbieter beim Öffnen verwenden soll. Lesen Sie die Eigenschaft, um den in einem geöffneten **Recordset** -Objekt verwendeten Sperrtyp zurückzugeben.

Anbieter unterstützen möglicherweise nicht alle Sperrtypen. Wenn ein Anbieter die angeforderte Einstellung für **LockType** nicht unterstützt, wird stattdessen ein anderer Sperrtyp verwendet. Die tatsächlich verfügbare Sperrfunktionalität in einem **Recordset** -Objekt bestimmen Sie mithilfe der [Supports](supports-method-ado.md)-Methode mit **adUpdate** und **adUpdateBatch**.

Die Einstellung **adLockPessimistic** wird nicht unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Falls ein nicht unterstützter Wert festgelegt wird, wird kein Fehler gemeldet. Stattdessen wird die ähnlichste unterstützte **LockType** -Eigenschaft verwendet.

The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.

Dieser Abschnitt enthält das folgende Thema:

- [Sperrtypen](types-of-locks.md)

