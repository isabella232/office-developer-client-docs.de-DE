---
title: NextRecordset-Methode (ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b824dc1b00f913e097432aae65ecac425ef19031
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475934"
---
# <a name="nextrecordset-method-ado"></a><span data-ttu-id="571e9-102">NextRecordset-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="571e9-102">NextRecordset Method (ADO)</span></span>


<span data-ttu-id="571e9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="571e9-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="571e9-104">Löscht das aktuelle [Recordset](recordset-object-ado.md)-Objekt, und gibt das nächste **Recordset** -Objekt zurück, indem sie durch eine Reihe von Befehlen wechselt.</span><span class="sxs-lookup"><span data-stu-id="571e9-104">Clears the current [Recordset](recordset-object-ado.md) object and returns the next **Recordset** by advancing through a series of commands.</span></span>

## <a name="syntax"></a><span data-ttu-id="571e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="571e9-105">Syntax</span></span>

<span data-ttu-id="571e9-106">Festlegen von *recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )</span><span class="sxs-lookup"><span data-stu-id="571e9-106">Set *recordset2* = *recordset1*.NextRecordset(*RecordsAffected* )</span></span>

## <a name="return-value"></a><span data-ttu-id="571e9-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="571e9-107">Return Value</span></span>

<span data-ttu-id="571e9-p101">Gibt ein **Recordset**-Objekt zurück. Im Syntaxmodell können Sie für *recordset1* und *recordset2* dasselbe **Recordset**-Objekt angeben oder separate Objekte verwenden. Wenn Sie separate **Recordset**-Objekte verwenden und die **ActiveConnection**-Eigenschaft auf das ursprüngliche **Recordset**-Objekt (*recordset1*) zurücksetzen, nachdem **NextRecordset** aufgerufen wurde, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="571e9-p101">Returns a **Recordset** object. In the syntax model, *recordset1* and *recordset2* can be the same **Recordset** object, or you can use separate objects. When using separate **Recordset** objects, resetting the **ActiveConnection** property on the original **Recordset** (*recordset1*) after **NextRecordset** has been called will generate an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="571e9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="571e9-111">Parameters</span></span>

- <span data-ttu-id="571e9-112">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="571e9-112">*RecordsAffected*</span></span>

- <span data-ttu-id="571e9-p102">Optional. Eine **Long** -Variable, an die der Anbieter die Anzahl der Datensätze zurückgibt, auf die sich der aktuelle Vorgang auswirkt.</span><span class="sxs-lookup"><span data-stu-id="571e9-p102">Optional. A **Long** variable to which the provider returns the number of records that the current operation affected.</span></span>


> [!NOTE]
> <P><span data-ttu-id="571e9-115">Dieser Parameter gibt nur die Anzahl der Datensätze an, auf die sich ein Vorgang auswirkt. Er gibt nicht die Anzahl der Datensätze aus einer SELECT- Anweisung zurück, die zum Generieren des Recordset-Objekts verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="571e9-115">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <STRONG>Recordset</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="571e9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="571e9-116">Remarks</span></span>

<span data-ttu-id="571e9-117">Verwenden Sie die **NextRecordset** -Methode, um die Ergebnisse des nächsten Befehls in einer zusammengesetzten befehlsanweisung oder einer gespeicherten Prozedur, die mehrere Ergebnisse zurückgibt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="571e9-117">Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</span></span> <span data-ttu-id="571e9-118">Wenn Sie ein **Recordset** -Objekt basierend auf einer befehlsanweisung zusammengesetzter öffnen (beispielsweise "Wählen Sie \* FROM Tabelle1; SELECT \* aus Tabelle2 ") mithilfe der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) -Methode auf einen [Befehl](command-object-ado.md) oder die [Open](open-method-ado-recordset.md) -Methode für ein **Recordset-Objekt**, ADO führt nur den ersten Befehl und die Ergebnisse zu *Recordset-Objekt*zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="571e9-118">If you open a **Recordset** object based on a compound command statement (for example, "SELECT \* FROM table1;SELECT \* FROM table2") using the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*.</span></span> <span data-ttu-id="571e9-119">Rufen Sie den Zugriff auf die Ergebnisse der nachfolgenden Befehle in der Anweisung die **NextRecordset** -Methode.</span><span class="sxs-lookup"><span data-stu-id="571e9-119">To access the results of subsequent commands in the statement, call the **NextRecordset** method.</span></span>

<span data-ttu-id="571e9-120">Solange es weitere Ergebnisse sind und das **Recordset-Objekt** mit der zusammengesetzten Anweisungen nicht getrennt oder über Prozess hinweg gemarshallt, wird die **NextRecordset** -Methode weiterhin **Recordset** -Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="571e9-120">As long as there are additional results and the **Recordset** containing the compound statements is not disconnected or marshaled across process boundaries, the **NextRecordset** method will continue to return **Recordset** objects.</span></span> <span data-ttu-id="571e9-121">Wenn ein Zeilen zurückgebende Befehl erfolgreich ausgeführt wird, aber keine Datensätze zurückgibt, wird das zurückgegebene **Recordset** -Objekt geöffnet, aber leer sein.</span><span class="sxs-lookup"><span data-stu-id="571e9-121">If a row-returning command executes successfully but returns no records, the returned **Recordset** object will be open but empty.</span></span> <span data-ttu-id="571e9-122">In diesem Fall testen Sie, überprüfen Sie, dass die Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) beide auf **"true"** sind.</span><span class="sxs-lookup"><span data-stu-id="571e9-122">Test for this case by verifying that the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties are both **True**.</span></span> <span data-ttu-id="571e9-123">Wenn ein Zeilen zurückgebende Befehl erfolgreich ausgeführt wird, wird das zurückgegebene **Recordset** -Objekt geschlossen werden die können Sie überprüfen, ob Sie testen die [State](state-property-ado.md) -Eigenschaft für das **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="571e9-123">If a non–row-returning command executes successfully, the returned **Recordset** object will be closed, which you can verify by testing the [State](state-property-ado.md) property on the **Recordset**.</span></span> <span data-ttu-id="571e9-124">Wenn keine weitere Ergebnisse vorhanden sind, wird die *Recordset-Objekt* auf *Nothing*festgelegt.</span><span class="sxs-lookup"><span data-stu-id="571e9-124">When there are no more results, *recordset* will be set to *Nothing*.</span></span>

<span data-ttu-id="571e9-125">Die **NextRecordset** -Methode ist in einem getrennten **Recordset** -Objekt, bei dem [ActiveConnection](activeconnection-property-ado.md) auf **Nothing** (in Microsoft Visual Basic) oder NULL (in anderen Sprachen) festgelegt wurde, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="571e9-125">The **NextRecordset** method is not available on a disconnected **Recordset** object, where [ActiveConnection](activeconnection-property-ado.md) has been set to **Nothing** (in Microsoft Visual Basic) or NULL (in other languages).</span></span>

<span data-ttu-id="571e9-126">Wenn im Modus der unmittelbaren Aktualisierung eine Bearbeitung vorgenommen wird, wird beim Aufrufen der **NextRecordset** -Methode ein Fehler generiert. Rufen Sie zunächst die [Update](update-method-ado.md)-Methode oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="571e9-126">If an edit is in progress while in immediate update mode, calling the **NextRecordset** method generates an error; call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span>

<span data-ttu-id="571e9-p105">Wenn Sie einen Parameter für mehrere Befehle in der Verbundanweisung übergeben möchten, indem Sie die [Parameters](parameters-collection-ado.md)-Auflistung auffüllen oder ein Array mit dem ursprünglichen Aufruf von **Open** oder **Execute** übergeben, muss die Reihenfolge der Parameter in der Auflistung oder im Array der Reihenfolge ihrer jeweiligen Befehle in der Befehlsreihe entsprechen. Sie müssen zunächst alle Ergebnisse lesen, bevor Sie die Werte der Ausgabeparameter lesen können.</span><span class="sxs-lookup"><span data-stu-id="571e9-p105">To pass parameters for more than one command in the compound statement by filling the [Parameters](parameters-collection-ado.md) collection, or by passing an array with the original **Open** or **Execute** call, the parameters must be in the same order in the collection or array as their respective commands in the command series. You must finish reading all the results before reading output parameter values.</span></span>

<span data-ttu-id="571e9-p106">Ihr OLE DB-Anbieter bestimmt, wann ein Befehl in einer Verbundanweisung ausgeführt wird. Der [Microsoft OLE DB Provider für SQL Server](microsoft-ole-db-provider-for-sql-server.md) führt beispielsweise alle Befehle nach dem Erhalt der Verbundanweisung nacheinander aus. Die resultierenden **Recordset** -Objekte werden beim Aufrufen von **NextRecordset** einfach zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="571e9-p106">Your OLE DB provider determines when each command command in a compound statement is executed. The [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), for example, executes all commands in a batch upon receiving the compound statement. The resulting **Recordsets** are simply returned when you call **NextRecordset**.</span></span>

<span data-ttu-id="571e9-p107">Andere Anbieter führen den nächsten Befehl in einer Anweisung jedoch möglicherweise erst aus, nachdem NextRecordset aufgerufen wurde. Wenn Sie das Recordset-Objekt bei diesen Anbietern explizit schließen, bevor die gesamte Befehlsanweisung durchlaufen wird, führt ADO die verbleibenden Befehle nicht aus.</span><span class="sxs-lookup"><span data-stu-id="571e9-p107">However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.</span></span>

