---
<span data-ttu-id="b55a3-101"><<<<<<< HEAD-Titel: IsolationLevel-Eigenschaft (ADO) TOCTitle: IsolationLevel-Eigenschaft (ADO) === Titel: IsolationLevel-Eigenschaft (ADO) TOCTitle: IsolationLevel-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="b55a3-101"><<<<<<< HEAD title: IsolationLevel Property (ADO) TOCTitle: IsolationLevel Property (ADO) ======= title: IsolationLevel property (ADO) TOCTitle: IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b55a3-102">Master Ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) Ms:contentKeyID: 48543493 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="b55a3-102">master ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: 48543493 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b55a3-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b55a3-103"><<<<<<< HEAD</span></span>
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="b55a3-104">IsolationLevel-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="b55a3-104">IsolationLevel Property (ADO)</span></span>
=======
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="b55a3-105">IsolationLevel-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="b55a3-105">IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b55a3-106">master</span><span class="sxs-lookup"><span data-stu-id="b55a3-106">master</span></span>


<span data-ttu-id="b55a3-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b55a3-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b55a3-108">Gibt die Isolationsstufe für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b55a3-108">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="b55a3-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b55a3-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b55a3-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b55a3-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b55a3-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b55a3-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b55a3-112">master</span><span class="sxs-lookup"><span data-stu-id="b55a3-112">master</span></span>

<span data-ttu-id="b55a3-p101">Legt einen [IsolationLevelEnum](isolationlevelenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **AdXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="b55a3-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b55a3-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b55a3-115">Remarks</span></span>

<span data-ttu-id="b55a3-p102">Legen Sie mit der **IsolationLevel** -Eigenschaft die Isolationsstufe eines **Connection** -Objekts fest. Die Einstellung wird erst beim nächsten Aufrufen der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wirksam. Wenn die von Ihnen angeforderte Isolationsstufe nicht verfügbar ist, gibt der Anbieter möglicherweise die nächsthöhere Isolationsstufe zurück.</span><span class="sxs-lookup"><span data-stu-id="b55a3-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="b55a3-119">Die **IsolationLevel** -Eigenschaft ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b55a3-119">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="b55a3-120">**Remote Data Service-Verwendung** Wenn für ein clientseitiges Connection-Objekt verwendet wird, kann die **IsolationLevel** -Eigenschaft nur auf **AdXactUnspecified**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b55a3-120">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="b55a3-p103">Da Benutzer mit nicht verbundenen **Recordset** -Objekten in einem clientbasierten Cache arbeiten, können Probleme mit mehreren Benutzern auftreten. Wenn beispielsweise zwei unterschiedliche Benutzer versuchen, denselben Datensatz zu aktualisieren, hat der Benutzer Erfolg, der den Datensatz zuerst aktualisiert. Die Aktualisierungsanforderung des zweiten Benutzers verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="b55a3-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

