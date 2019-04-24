---
title: CacheSize-Eigenschaft (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 725c2f81b3f3bce05a3007c50705e9cf35f7008f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296745"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="98487-102">CacheSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="98487-102">CacheSize property (ADO)</span></span>


<span data-ttu-id="98487-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98487-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98487-104">Gibt die Anzahl von Datensätzen aus einem [Recordset](recordset-object-ado.md)-Objekt an, die lokal im Arbeitsspeicher zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="98487-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="98487-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="98487-105">Settings and return values</span></span>

<span data-ttu-id="98487-106">Sets or returns a **Long** value that must be greater than 0.</span><span class="sxs-lookup"><span data-stu-id="98487-106">Sets or returns a **Long** value that must be greater than 0.</span></span> <span data-ttu-id="98487-107">Default is 1.</span><span class="sxs-lookup"><span data-stu-id="98487-107">Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="98487-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98487-108">Remarks</span></span>

<span data-ttu-id="98487-p102">Verwenden Sie die **CacheSize**-Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 hat, ruft der Anbieter, nachdem er zunächst das **Recordset**-Objekt geöffnet hat, die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Durchlaufen des **Recordset**-Objekts gibt der Anbieter die Daten aus dem lokalen Arbeitsspeicherpuffer zurück. Sobald Sie hinter den letzten Datensatz im Cache gelangt sind, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.</span><span class="sxs-lookup"><span data-stu-id="98487-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="98487-p103">[!HINWEIS] **CacheSize** basiert auf der anbieterspezifischen Eigenschaft **Maximale Anzahl geöffneter Zeilen** (in der **Properties** -Auflistung des **Recordset** -Objekts). **CacheSize** kann nicht auf einen höheren Wert als **Maximale Anzahl geöffneter Zeilen** festgelegt werden. Legen Sie **Maximale Anzahl geöffneter Zeilen** fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="98487-p103">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows which can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="98487-p104">Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgendem Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="98487-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="98487-118">Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="98487-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="98487-119">A **CacheSize** setting of zero is not allowed and returns an error.</span><span class="sxs-lookup"><span data-stu-id="98487-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="98487-p105">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="98487-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="98487-122">Wenn **CacheSize** auf einen Wert größer als 1 festgelegt ist, können die Navigationsmethoden ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext und MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) zu einer Navigation zu einem gelöschten Datensatz führen, wenn nach dem Abrufen der Datensätze ein Löschvorgang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="98487-122">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</span></span> <span data-ttu-id="98487-123">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span><span class="sxs-lookup"><span data-stu-id="98487-123">After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</span></span> <span data-ttu-id="98487-124">However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span><span class="sxs-lookup"><span data-stu-id="98487-124">However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

