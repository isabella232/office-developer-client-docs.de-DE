---
<span data-ttu-id="baa91-101"><<<<<<< HEAD-Titel: vorbereitet-Eigenschaft (ADO) TOCTitle: vorbereitet-Eigenschaft (ADO) === Titel: Prepared-Eigenschaft (ADO) TOCTitle: Prepared-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="baa91-101"><<<<<<< HEAD title: Prepared Property (ADO) TOCTitle: Prepared Property (ADO) ======= title: Prepared property (ADO) TOCTitle: Prepared property (ADO)</span></span>
>>>>>>> <span data-ttu-id="baa91-102">Master Ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) Ms:contentKeyID: 48544116 ms.date: 09/18/2015 Mtps_version: Office. 15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="baa91-102">master ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: 48544116 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="baa91-103">ado210.chm1231161 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="baa91-103">ado210.chm1231161 f1_categories:</span></span>
- <span data-ttu-id="baa91-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="baa91-104">Office.Version=v15</span></span>
---

<span data-ttu-id="baa91-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="baa91-105"><<<<<<< HEAD</span></span>
# <a name="prepared-property-ado"></a><span data-ttu-id="baa91-106">Prepared-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="baa91-106">Prepared Property (ADO)</span></span>
=======
# <a name="prepared-property-ado"></a><span data-ttu-id="baa91-107">Prepared-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="baa91-107">Prepared property (ADO)</span></span>
>>>>>>> <span data-ttu-id="baa91-108">master</span><span class="sxs-lookup"><span data-stu-id="baa91-108">master</span></span>


<span data-ttu-id="baa91-109">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="baa91-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="baa91-110">Gibt an, ob eine kompilierte Version eines Befehls vor dem Ausführen gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="baa91-110">Indicates whether to save a compiled version of a command before execution.</span></span>

<span data-ttu-id="baa91-111"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="baa91-111"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="baa91-112">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="baa91-112">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="baa91-113">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="baa91-113">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="baa91-114">master</span><span class="sxs-lookup"><span data-stu-id="baa91-114">master</span></span>

<span data-ttu-id="baa91-115">Legt einen **Boolean** -Wert fest oder gibt den Wert zurück. Ein Wert **True** gibt an, dass der Befehl vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="baa91-115">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa91-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="baa91-116">Remarks</span></span>

<span data-ttu-id="baa91-p101">Verwenden Sie die **Prepared** -Eigenschaft, wenn der Anbieter eine vorbereitete (bzw. kompilierte) Version der in der [CommandText](commandtext-property-ado.md)-Eigenschaft angegebenen Abfrage speichern soll, bevor ein [Command](command-object-ado.md)-Objekt erstmalig ausgeführt wird. Dadurch wird möglicherweise das erste Ausführen des zugehörigen Befehls zwar verlangsamt, aber da der Anbieter nach dem Kompilieren des Befehls die kompilierte Version zum weiteren Ausführen des Befehls verwendet, ergibt sich eine verbesserte Leistung.</span><span class="sxs-lookup"><span data-stu-id="baa91-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="baa91-119">Ist die Eigenschaft auf **False** festgelegt, führt der Anbieter das **Command** -Objekt direkt aus, ohne eine kompilierte Version zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="baa91-119">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="baa91-p102">Unterstützt der Anbieter die Vorbereitung von Befehlen nicht, wird möglicherweise ein Fehler zurückgegeben, sobald diese Eigenschaft auf **True** festgelegt wird. Wenn kein Fehler zurückgegeben wird, wird die Anforderung zum Vorbereiten des Befehls einfach ignoriert und die **Prepared** -Eigenschaft auf **False** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="baa91-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

