---
title: Command-Objekt (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 153f59ebbcfae89f6358fe0d707791aab8a8cdd7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864074"
---
# <a name="command-object-ado"></a><span data-ttu-id="bfeac-102">Command-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="bfeac-102">Command Object (ADO)</span></span>


<span data-ttu-id="bfeac-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfeac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bfeac-104">Definiert einen spezifischen Befehl, den Sie in einer Datenquelle ausführen wollen.</span><span class="sxs-lookup"><span data-stu-id="bfeac-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfeac-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfeac-105">Remarks</span></span>

<span data-ttu-id="bfeac-p101">Mit einem **Command** -Objekt können Sie eine Datenbank abfragen und Datensätze in einem [Recordset](recordset-object-ado.md)-Objekt zurückgeben, einen Massenvorgang ausführen oder die Struktur einer Datenbank ändern. Abhängig von der Funktionalität des Anbieters wird von einigen **Command** -Auflistungen, -Methoden oder -Eigenschaften möglicherweise ein Fehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="bfeac-p101">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database. Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="bfeac-108">Die Auflistungen, Methoden und Eigenschaften eines **Command** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bfeac-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="bfeac-109">Festlegen des ausführbaren Texts des Befehls (z. B. eine SQL-Anweisung) mit der [CommandText](commandtext-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bfeac-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfeac-110">Festlegen von parametrisierten Abfragen oder von Argumenten für gespeicherte Prozeduren mit [Parameter](parameter-object-ado.md)-Objekten und der [Parameters](parameters-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bfeac-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="bfeac-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="bfeac-111"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="bfeac-112">Ausführen eines Befehls und Rückgabe eines **Recordset** -Objekts, falls zutreffend, mit der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))-Methode.</span><span class="sxs-lookup"><span data-stu-id="bfeac-112">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>
=======
  - <span data-ttu-id="bfeac-113">Ausführen eines Befehls und Rückgabe eines **Recordset** -Objekts, falls zutreffend, mit der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)-Methode.</span><span class="sxs-lookup"><span data-stu-id="bfeac-113">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>
>>>>>>> <span data-ttu-id="bfeac-114">master</span><span class="sxs-lookup"><span data-stu-id="bfeac-114">master</span></span>

  - <span data-ttu-id="bfeac-115">Festlegen des Befehlstyps mit der [CommandType](commandtype-property-ado.md)-Eigenschaft vor dem Ausführen des Befehls, um die Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="bfeac-115">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="bfeac-116">Steuern, ob der Anbieter vor dem Ausführen eine vorbereitete (oder kompilierte) Version des Befehls speichert, mit der [Prepared](prepared-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bfeac-116">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfeac-117">Festlegen, wie viele Sekunden ein Anbieter auf die Ausführung eines Befehls wartet, mithilfe der [CommandTimeout](commandtimeout-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bfeac-117">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfeac-118">Zuordnen einer geöffneten Verbindung zu einem **Command** -Objekt, indem dessen [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bfeac-118">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfeac-119">Festlegen der [Name](name-property-ado.md) -Eigenschaft, um das **Command** -Objekt als Methode im zugeordneten [Connection](connection-object-ado.md) -Objekt zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfeac-119">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="bfeac-120">Übergeben eines **Command** -Objekts an die [Source](source-property-ado-recordset.md)-Eigenschaft eines **Recordset** -Objekts, um Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bfeac-120">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="bfeac-121">Zugreifen auf anbieterspezifische Attribute für die [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bfeac-121">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="bfeac-p102">[!HINWEIS] Sie können eine Abfrage ausführen, ohne ein **Command** -Objekt zu verwenden, indem Sie eine Abfragezeichenfolge an die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)-Methode eines **Connection** -Objekts oder an die [Open](open-method-ado-recordset.md)-Methode eines **Recordset** -Objekts übergeben. Es ist jedoch ein **Command** -Objekt erforderlich, wenn der Befehlstext gespeichert und erneut ausgeführt werden soll. Sie können aber auch Abfrageparameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="bfeac-p102">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object. However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="bfeac-p103">Wenn Sie ein **Command** -Objekt unabhängig von einem zuvor definierten **Connection** -Objekt erstellen möchten, geben Sie für seine **ActiveConnection** -Eigenschaft eine gültige Verbindungszeichenfolge an. ADO erstellt auch in diesem Fall ein **Connection** -Objekt, weist das Objekt aber keiner Objektvariablen zu. Wenn Sie jedoch derselben Verbindung mehrere **Command** -Objekte zuordnen, müssen Sie ein **Connection** -Objekt explizit erstellen und öffnen. Auf diese Weise wird dem **Connection** -Objekt eine Objektvariable zugeordnet. Wenn Sie die **ActiveConnection** -Eigenschaft des **Command** -Objekts nicht auf diese Objektvariable festlegen, erstellt ADO für jedes **Command** -Objekt ein neues **Connection** -Objekt, selbst wenn Sie dieselbe Verbindungszeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="bfeac-p103">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string. ADO still creates a **Connection** object, but it doesn't assign that object to an object variable. However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable. If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="bfeac-p104">Sie führen ein **Command** -Objekt aus, indem Sie es einfach mit seiner [Name](name-property-ado.md)-Eigenschaft im zugeordneten **Connection** -Objekt aufrufen. Die **ActiveConnection** -Eigenschaft des **Command** -Objekts muss den Wert des **Connection** -Objekts haben. Wenn das **Command** -Objekt Parameter besitzt, übergeben Sie diese als Argumente an die Methode.</span><span class="sxs-lookup"><span data-stu-id="bfeac-p104">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object. The **Command** must have its **ActiveConnection** property set to the **Connection** object. If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="bfeac-p105">Wenn zwei oder mehrere **Command** -Objekte auf derselben Verbindung ausgeführt werden und eines der beiden **Command** - Objekte eine gespeicherte Prozedur ohne Parameter ist, tritt ein Fehler auf. Verwenden Sie unterschiedliche Verbindungen, oder trennen Sie alle anderen **Command** -Objekte von der Verbindung, um alle **Command** -Objekte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bfeac-p105">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs. To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="bfeac-p106">Die **Parameters** -Auflistung ist das Standardmitglied des **Command** -Objekts. Daher haben die beiden folgenden Codeanweisungen dieselbe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="bfeac-p106">The **Parameters** collection is the default member of the **Command** object. As a result, the following two code statements are equivalent.</span></span>

