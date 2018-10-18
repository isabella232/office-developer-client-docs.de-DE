---
<span data-ttu-id="75bfd-101"><<<<<<< HEAD-Titel: CacheSize-Eigenschaft (ADO) TOCTitle: CacheSize-Eigenschaft (ADO) === Titel: CacheSize-Eigenschaft (ADO) TOCTitle: CacheSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="75bfd-101"><<<<<<< HEAD title: CacheSize Property (ADO) TOCTitle: CacheSize Property (ADO) ======= title: CacheSize property (ADO) TOCTitle: CacheSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="75bfd-102">Master Ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15) Ms:contentKeyID: 48544491 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="75bfd-102">master ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15) ms:contentKeyID: 48544491 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="75bfd-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="75bfd-103"><<<<<<< HEAD</span></span>
# <a name="cachesize-property-ado"></a><span data-ttu-id="75bfd-104">CacheSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="75bfd-104">CacheSize Property (ADO)</span></span>
=======
# <a name="cachesize-property-ado"></a><span data-ttu-id="75bfd-105">CacheSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="75bfd-105">CacheSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="75bfd-106">master</span><span class="sxs-lookup"><span data-stu-id="75bfd-106">master</span></span>


<span data-ttu-id="75bfd-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75bfd-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75bfd-108">Gibt die Anzahl von Datensätzen aus einem [Recordset](recordset-object-ado.md)-Objekt an, die lokal im Arbeitsspeicher zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="75bfd-108">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

<span data-ttu-id="75bfd-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="75bfd-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="75bfd-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="75bfd-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="75bfd-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="75bfd-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="75bfd-112">master</span><span class="sxs-lookup"><span data-stu-id="75bfd-112">master</span></span>

<span data-ttu-id="75bfd-p101">Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der größer als 0 sein muss. Der Standard ist 1.</span><span class="sxs-lookup"><span data-stu-id="75bfd-p101">Sets or returns a **Long** value that must be greater than 0. Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="75bfd-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75bfd-115">Remarks</span></span>

<span data-ttu-id="75bfd-p102">Verwenden Sie die **CacheSize** -Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 hat, ruft der Anbieter, nachdem er zunächst das **Recordset** -Objekt geöffnet hat, die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Durchlaufen des **Recordset** -Objekts gibt der Anbieter die Daten aus dem lokalen Arbeitsspeicherpuffer zurück. Sobald Sie hinter den letzten Datensatz im Cache gelangt sind, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.</span><span class="sxs-lookup"><span data-stu-id="75bfd-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="75bfd-p103">[!HINWEIS] <STRONG>CacheSize</STRONG> basiert auf der anbieterspezifischen Eigenschaft <STRONG>Maximale Anzahl geöffneter Zeilen</STRONG> (in der <STRONG>Properties</STRONG> -Auflistung des <STRONG>Recordset</STRONG> -Objekts). <STRONG>CacheSize</STRONG> kann nicht auf einen höheren Wert als <STRONG>Maximale Anzahl geöffneter Zeilen</STRONG> festgelegt werden. Legen Sie <STRONG>Maximale Anzahl geöffneter Zeilen</STRONG> fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="75bfd-p103"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows which can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="75bfd-p104">Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgendem Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="75bfd-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="75bfd-125">Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="75bfd-125">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="75bfd-126">Die Einstellung 0 für **CacheSize** ist nicht zulässig. In diesem Fall würde ein Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="75bfd-126">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="75bfd-p105">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="75bfd-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="75bfd-p106">Wenn CacheSize auf einen Wert größer 1 festgelegt wird, können die Navigationsmethoden (Move, MoveFirst, MoveLast, MoveNext und MovePrevious) dazu führen, dass zu einem gelöschten Datensatz navigiert wird, falls der Löschvorgang nach dem Abrufen der Datensätze erfolgt. Nach dem Abrufen werden nachfolgende Löschvorgänge erst im Datencache übernommen, wenn Sie versuchen, auf einen Datenwert in einer gelöschten Zeile zuzugreifen. Wenn Sie allerdings CacheSize auf 1 festlegen, wird dieses Problem beseitigt, weil gelöschte Zeilen nicht abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="75bfd-p106">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

