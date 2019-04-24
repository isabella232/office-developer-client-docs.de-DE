---
title: Verwenden von CacheSize (Access-Desktop-Daten Bankreferenz)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312124"
---
# <a name="using-cachesize"></a><span data-ttu-id="1f6c3-102">Verwenden der CacheSize</span><span class="sxs-lookup"><span data-stu-id="1f6c3-102">Using CacheSize</span></span>

<span data-ttu-id="1f6c3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f6c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f6c3-p101">Verwenden Sie die **CacheSize** -Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 aufweist, wird zunächst das **Recordset** -Objekt geöffnet. Anschließend ruft der Anbieter die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Abarbeiten des **Recordset** -Objekts gibt der Anbieter die Daten vom lokalen Arbeitsspeicherpuffer zurück. Sobald Sie den letzten Datensatz im Cache verarbeitet haben, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="1f6c3-p102">[!HINWEIS] **CacheSize** basiert auf der anbieterspezifischen Eigenschaft **Maximale Anzahl geöffneter Zeilen** (in der **Properties** -Auflistung des **Recordset** -Objekts). **CacheSize** kann nicht auf einen höheren Wert als **Maximale Anzahl geöffneter Zeilen** festgelegt werden. Legen Sie **Maximale Anzahl geöffneter Zeilen** fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-p102">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="1f6c3-p103">Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgenden Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="1f6c3-113">Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="1f6c3-114">Die Einstellung 0 für **CacheSize** ist nicht zulässig. In diesem Fall würde ein Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="1f6c3-p104">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="1f6c3-117">Wenn **CacheSize** auf einen Wert größer als 1 festgelegt ist, können die Navigationsmethoden ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext und MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) zu einer Navigation zu einem gelöschten Datensatz führen, wenn nach dem Abrufen der Datensätze ein Löschvorgang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-117">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="1f6c3-118">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-118">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="1f6c3-119">However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span><span class="sxs-lookup"><span data-stu-id="1f6c3-119">However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

