---
title: GetChunk-Methode (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698183"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="47e81-102">GetChunk-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="47e81-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="47e81-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47e81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47e81-104">Gibt den gesamten Inhalt oder einen Teil des Inhalts eines [Field](field-object-ado.md)-Objekts mit umfangreichem Text oder Binärdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="47e81-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47e81-105">Syntax</span></span>

<span data-ttu-id="47e81-106">*Variable* = *dar*. GetChunk (*Größe* )</span><span class="sxs-lookup"><span data-stu-id="47e81-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="47e81-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47e81-107">Return value</span></span>

<span data-ttu-id="47e81-108">Gibt einen **Variant** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="47e81-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="47e81-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e81-109">Parameters</span></span>

|<span data-ttu-id="47e81-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e81-110">Parameter</span></span>|<span data-ttu-id="47e81-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47e81-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="47e81-112">*Größe*</span><span class="sxs-lookup"><span data-stu-id="47e81-112">*Size*</span></span> |<span data-ttu-id="47e81-113">Ein **Long** -Ausdruck, der der Anzahl von Bytes oder Zeichen entspricht, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="47e81-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="47e81-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47e81-114">Remarks</span></span>

<span data-ttu-id="47e81-p101">Verwenden Sie die **GetChunk** -Methode für ein **Field** -Objekt, um einen Teil der bzw. die gesamten umfangreichen Binär- oder Zeichendaten abzurufen. In Situationen, bei denen der Systemspeicher beschränkt ist, können Sie die **GetChunk** -Methode verwenden, um umfangreiche Werte in kleinere Einheiten aufzuteilen, statt deren Gesamtheit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="47e81-p101">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="47e81-p102">Die Daten, die von einem Aufruf von **GetChunk** zurückgegeben werden, werden einer *Variablen* zugewiesen. Falls die *Größe* die Größe der restlichen Daten überschreitet, gibt die **GetChunk**-Methode nur die restlichen Daten zurück, ohne die *Variable* mit Leerzeichen aufzufüllen. Falls das Feld leer ist, gibt die **GetChunk**-Methode einen NULL-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="47e81-p102">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="47e81-p103">Bei jedem weiteren Aufruf von **GetChunk** werden die Daten ab der Stelle abgerufen, an der beim vorherigen Aufruf von **GetChunk** abgebrochen wurde. Wenn Sie jedoch Daten aus einem Feld abrufen und anschließend den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, geht ADO davon aus, dass Sie das Abrufen von Daten aus dem ersten Feld beendet haben. Wenn Sie die **GetChunk** -Methode erneut für das erste Feld aufrufen, interpretiert ADO den Aufruf als einen neuen **GetChunk** -Vorgang und beginnt am Anfang der Daten mit dem Lesen. Beim Zugriff auf Felder in anderen [Recordset](recordset-object-ado.md)-Objekten, bei denen es sich nicht um Klone des ersten **Recordset** -Objekts handelt, werden die **GetChunk** -Operationen nicht unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="47e81-p103">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="47e81-124">Besitzt das **adFldLong** -Bit in der [Attributes](attributes-property-ado.md)-Eigenschaft eines **Field** -Objekts den Wert **True**, können Sie die **GetChunk** -Methode für dieses Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="47e81-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="47e81-125">Ist kein aktueller Datensatz vorhanden, wenn Sie die **GetChunk** -Methode für ein **Field** -Objekt verwenden, tritt Fehler 3021 (kein aktueller Datensatz) auf.</span><span class="sxs-lookup"><span data-stu-id="47e81-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="47e81-p104">[!HINWEIS] Die **GetChunk** -Methode kann nicht auf **Field** -Objekte eines [Record](record-object-ado.md)-Objekts angewendet werden. Sie führt keine Vorgänge aus und generiert einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="47e81-p104">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>


