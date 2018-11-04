---
title: AppendChunk-Methode (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9103135100c5a10931ee63bfbdeabe9d97119fd2
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949264"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="ea451-102">AppendChunk-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea451-102">AppendChunk method (ADO)</span></span>

<span data-ttu-id="ea451-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea451-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea451-104">Daten werden einem großen [Field](field-object-ado.md)-Text- oder -Binärdatenobjekt oder einem [Parameter](parameter-object-ado.md)-Objekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="ea451-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea451-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea451-105">Syntax</span></span>

<span data-ttu-id="ea451-106">*-Objekt.* Methoden "AppendChunk" *Daten*</span><span class="sxs-lookup"><span data-stu-id="ea451-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="ea451-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea451-107">Parameters</span></span>

|<span data-ttu-id="ea451-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea451-108">Parameter</span></span>|<span data-ttu-id="ea451-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea451-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ea451-110">*Objekt*</span><span class="sxs-lookup"><span data-stu-id="ea451-110">*object*</span></span> |<span data-ttu-id="ea451-111">Ein **Field** - oder **Parameter** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ea451-111">A **Field** or **Parameter** object.</span></span>|
|<span data-ttu-id="ea451-112">*Daten*</span><span class="sxs-lookup"><span data-stu-id="ea451-112">*Data*</span></span> |<span data-ttu-id="ea451-113">Ein **Variant** -Objekt, das die dem Objekt anzufügenden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ea451-113">A **Variant** that contains the data to append to the object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ea451-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ea451-114">Remarks</span></span>

<span data-ttu-id="ea451-p101">Verwenden Sie die **AppendChunk** -Methode für ein **Field** - oder **Parameter** -Objekt, um es mit Long binarydaten oder Zeichendaten zu füllen. In Situationen mit beschränktem Systemspeicher können Sie mithilfe der **AppendChunk** -Methode lange Werte in Teilen anstatt als Ganzes bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ea451-p101">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data. In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="ea451-117">**Field**</span><span class="sxs-lookup"><span data-stu-id="ea451-117">**Field**</span></span>

<span data-ttu-id="ea451-118">Wenn das **AdFldLong** -Bit in der [Attributes](attributes-property-ado.md) -Eigenschaft eines **Field** -Objekts festgelegt ist, auf "true" können Sie die **AppendChunk** -Methode für dieses Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea451-118">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="ea451-p102">Beim ersten **AppendChunk** -Aufruf für ein **Field** -Objekt werden Daten in das Feld geschrieben. Dabei werden alle vorhandenen Daten überschrieben. Durch nachfolgende **AppendChunk** -Aufrufe werden Daten den vorhandenen Daten hinzugefügt. Wenn Sie Daten einem Feld anfügen und dann den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, wird von ADO angenommen, dass das Anfügen von Daten an das erste Feld beendet ist. Wenn Sie die **AppendChunk** -Methode erneut für das erste Feld aufrufen, wird der Aufruf von ADO als neue **AppendChunk** -Operation interpretiert, und die vorhandenen Daten werden überschrieben. Durch das Zugreifen auf Felder in anderen [Recordset](recordset-object-ado.md)-Objekten, die keine Klone des ersten **Recordset** -Objekts sind, werden **AppendChunk** -Operationen nicht unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="ea451-p102">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="ea451-124">Wenn beim Aufrufen von **AppendChunk** für ein **Field** -Objekt kein aktueller Datensatz vorhanden ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ea451-124">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="ea451-p103">[!HINWEIS] Die **AppendChunk** -Methode eignet sich nicht für **Field** -Objekte eines [Record](record-object-ado.md)-Objekts. Es werden keine Operationen ausgeführt, und es wird ein Laufzeitfehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="ea451-p103">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>



<span data-ttu-id="ea451-127">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="ea451-127">**Parameter**</span></span>

<span data-ttu-id="ea451-128">Wenn das adParamLong-Bit in der Attributes-Eigenschaft eines Parameter-Objekts auf True festgelegt ist, können Sie für dieses Feld die AppendChunk-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea451-128">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="ea451-p104">Durch den ersten **AppendChunk** -Aufruf für ein **Parameter** -Objekt werden Daten in den Parameter geschrieben, und alle vorhandenen Daten werden überschrieben. Durch nachfolgende **AppendChunk** -Aufrufe für ein **Parameter** -Objekt werden Daten den vorhandenen Parameterdaten hinzugefügt. Durch einen **AppendChunk** -Aufruf, bei dem ein Nullwert übergeben wird, werden alle Parameterdaten verworfen.</span><span class="sxs-lookup"><span data-stu-id="ea451-p104">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data. Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data. An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>

