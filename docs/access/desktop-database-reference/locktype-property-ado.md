---
<span data-ttu-id="8d26a-101"><<<<<<< HEAD-Titel: LockType-Eigenschaft (ADO) TOCTitle: LockType-Eigenschaft (ADO) === Titel: LockType-Eigenschaft (ADO) TOCTitle: LockType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d26a-101"><<<<<<< HEAD title: LockType Property (ADO) TOCTitle: LockType Property (ADO) ======= title: LockType property (ADO) TOCTitle: LockType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8d26a-102">Master Ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) Ms:contentKeyID: 48543589 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="8d26a-102">master ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID: 48543589 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8d26a-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8d26a-103"><<<<<<< HEAD</span></span>
# <a name="locktype-property-ado"></a><span data-ttu-id="8d26a-104">LockType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d26a-104">LockType Property (ADO)</span></span>
=======
# <a name="locktype-property-ado"></a><span data-ttu-id="8d26a-105">LockType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d26a-105">LockType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8d26a-106">master</span><span class="sxs-lookup"><span data-stu-id="8d26a-106">master</span></span>


<span data-ttu-id="8d26a-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d26a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d26a-108">Gibt den Typ der Sperren an, die bei der Bearbeitung auf Datensätze angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d26a-108">Indicates the type of locks placed on records during editing.</span></span>

<span data-ttu-id="8d26a-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8d26a-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8d26a-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8d26a-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8d26a-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8d26a-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8d26a-112">master</span><span class="sxs-lookup"><span data-stu-id="8d26a-112">master</span></span>

<span data-ttu-id="8d26a-p101">Legt einen [LockTypeEnum](locktypeenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="8d26a-p101">Sets or returns a [LockTypeEnum](locktypeenum.md) value. The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d26a-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d26a-115">Remarks</span></span>

<span data-ttu-id="8d26a-p102">Legen Sie die **LockType** -Eigenschaft fest, bevor Sie ein [Recordset](recordset-object-ado.md) öffnen, und geben Sie den Sperrtyp an, den der Anbieter beim Öffnen verwenden soll. Lesen Sie die Eigenschaft, um den Sperrtyp zu ermitteln, der bei einem geöffneten **Recordset** -Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d26a-p102">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="8d26a-p103">Anbieter unterstützen möglicherweise nicht alle Sperrtypen. Falls ein Anbieter die angeforderte **LockType** -Einstellung nicht unterstützt, wird der Sperrtyp ausgetauscht. Wenn Sie die Sperrfunktionalität ermitteln möchten, die tatsächlich für ein **Recordset** -Objekt verfügbar ist, verwenden Sie die [Supports](supports-method-ado.md)-Methode mit **adUpdate** und **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="8d26a-p103">Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="8d26a-p104">Die Einstellung **adLockPessimistic** wird nicht unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Wurde ein nicht unterstützter Wert festgelegt, tritt kein Fehler auf. Stattdessen wird der nächstliegende unterstützte **LockType** -Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d26a-p104">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="8d26a-123">Die **LockType** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8d26a-123">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="8d26a-124">**Remote Data Service-Verwendung** Wenn für ein clientseitiges Recordset-Objekt verwendet wird, kann die **LockType** -Eigenschaft nur auf **AdLockBatchOptimistic**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8d26a-124">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

