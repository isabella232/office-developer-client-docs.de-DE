---
title: Was ist eine Sperre? (Access PC-Datenbank-Referenz)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f852901be41060568bdbad539906e9166d080fad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474499"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="2c731-103">Was ist eine Sperre?</span><span class="sxs-lookup"><span data-stu-id="2c731-103">What is a Lock?</span></span>


<span data-ttu-id="2c731-104">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c731-104">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2c731-p102">Unter dem Sperren versteht man den Prozess, mit dem ein DBMS den Zugriff auf eine Zeile in einer Mehrbenutzerumgebung sperrt. Wenn eine Zeile oder Spalte exklusiv gesperrt ist, können andere Benutzer erst auf die gesperrten Daten zugreifen, wenn die Sperre aufgehoben wurde. Dadurch wird verhindert, dass zwei Benutzer gleichzeitig dieselbe Spalte in einer Zeile aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2c731-p102">Locking is the process by which a DBMS restricts access to a row in a multi-user environment. When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released. This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="2c731-p103">Sperren können im Hinblick auf die Ressourcen sehr teuer sein und sollten nur verwendet werden, wenn sie zur Aufrechterhaltung der Datenintegrität erforderlich sind. In einer Datenbank, in der jede Sekunde Hunderte oder Tausende von Benutzern versuchen könnten, auf einen Datensatz zuzugreifen (z. B. eine Datenbank, die mit dem Internet verbunden ist), könnten unnötige Sperren schnell zu einer Leistungsbeeinträchtigung der Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="2c731-p103">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity. In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="2c731-110">Sie können steuern, wie die Datenquelle und die ADO-Cursorbibliothek die Parallelität verwalten, indem Sie die entsprechende Sperroption auswählen.</span><span class="sxs-lookup"><span data-stu-id="2c731-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="2c731-p104">Legen Sie die **LockType** -Eigenschaft vor dem Öffnen eines **Recordset** -Objekts fest, um anzugeben, welchen Sperrtyp der Anbieter beim Öffnen verwenden soll. Lesen Sie die Eigenschaft, um den in einem geöffneten **Recordset** -Objekt verwendeten Sperrtyp zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2c731-p104">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="2c731-p105">Anbieter unterstützen möglicherweise nicht alle Sperrtypen. Wenn ein Anbieter die angeforderte Einstellung für **LockType** nicht unterstützt, wird stattdessen ein anderer Sperrtyp verwendet. Die tatsächlich verfügbare Sperrfunktionalität in einem **Recordset** -Objekt bestimmen Sie mithilfe der [Supports](supports-method-ado.md)-Methode mit **adUpdate** und **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="2c731-p105">Providers might not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="2c731-p106">Die Einstellung **adLockPessimistic** wird nicht unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Falls ein nicht unterstützter Wert festgelegt wird, wird kein Fehler gemeldet. Stattdessen wird die ähnlichste unterstützte **LockType** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c731-p106">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="2c731-118">Die LockType-Eigenschaft hat Lese-/Schreibzugriff, wenn das Recordset-Objekt geschlossen ist. Wenn das Recordset-Objekt geöffnet ist, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2c731-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

