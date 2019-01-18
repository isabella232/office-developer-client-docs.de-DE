---
title: Typen von Sperren (Access PC-Datenbank-Referenz)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47b212be1922f783889f1e5be436a616909dc5c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699534"
---
# <a name="types-of-locks"></a><span data-ttu-id="27732-102">Typen von Sperren</span><span class="sxs-lookup"><span data-stu-id="27732-102">Types of locks</span></span>


<span data-ttu-id="27732-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27732-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="27732-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="27732-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="27732-p101">Gibt optimistische Batchaktualisierungen an und ist für den Batchaktualisierungsmodus erforderlich.</span><span class="sxs-lookup"><span data-stu-id="27732-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span>

<span data-ttu-id="27732-p102">Viele Anwendungen rufen eine Reihe von Zeilen gleichzeitig ab und müssen dann koordinierte Aktualisierungen vornehmen, die die gesamten Zeilen enthalten, die eingefügt, aktualisiert oder gelöscht werden sollen. Mit Batchcursorn ist nur ein Roundtrip zum Server erforderlich. Dadurch wird die Aktualisierungsleistung verbessert und der Netzwerkverkehr reduziert. Mit einer Batchcursorbibliothek können Sie einen statischen Cursor erstellen und dann die Verbindung mit der Datenquelle trennen. Nun können Sie die Zeilen ändern und anschließend erneut eine Verbindung herstellen und die Änderungen in einem Batch in der Datenquelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="27732-p102">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted. With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic. Using a batch cursor library, you can create a static cursor and then disconnect from the data source. At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="27732-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="27732-111">adLockOptimistic</span></span>

<span data-ttu-id="27732-p103">Gibt an, dass der Anbieter optimistische Sperren verwendet. Datensätze werden also nur gesperrt, wenn Sie die **Update** -Methode aufrufen. Es besteht deshalb die Möglichkeit, dass Daten zwischen Ihrer Bearbeitung des Datensatzes und dem Aufrufen von **Update** von einem anderen Benutzer geändert werden. Dadurch entstehen Konflikte. Verwenden Sie diesen Sperrtyp in Fällen, in denen die Chance von Konflikten niedrig ist oder in denen Konflikte auf einfache Weise gelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="27732-p103">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method. This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts. Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="27732-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="27732-115">adLockPessimistic</span></span>

<span data-ttu-id="27732-p104">Gibt an, dass datensatzweise pessimistische Sperren verwendet werden. Der Anbieter unternimmt alles Erforderliche, um die erfolgreiche Bearbeitung der Datensätze sicherzustellen, indem er gewöhnlich Datensätze in der Datenquelle unmittelbar vor der Bearbeitung sperrt. Dies bedeutet natürlich, dass die Datensätze, sobald Sie mit dem Bearbeiten begonnen haben, erst wieder für andere Benutzer verfügbar sind, wenn Sie die Sperre durch Aufrufen von **Update** aufheben. Verwenden Sie diesen Sperrtyp für ein System, in dem gleichzeitige Änderungen an Daten auf keinen Fall zulässig sind, wie z. B. für ein Reservierungssystem.</span><span class="sxs-lookup"><span data-stu-id="27732-p104">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing. Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.** Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="27732-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="27732-120">adLockReadOnly</span></span>

<span data-ttu-id="27732-p105">Gibt schreibgeschützte Datensätze an. Die Daten können nicht geändert werden. Eine schreibgeschützte Sperre ist der "schnellste" Sperrtyp, weil der Server keine Sperre in den Datensätzen verwalten muss.</span><span class="sxs-lookup"><span data-stu-id="27732-p105">Indicates read-only records. You cannot alter the data. A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="27732-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="27732-124">adLockUnspecified</span></span>

<span data-ttu-id="27732-125">Gibt keinen Sperrtyp an.</span><span class="sxs-lookup"><span data-stu-id="27732-125">Does not specify a type of lock.</span></span>

