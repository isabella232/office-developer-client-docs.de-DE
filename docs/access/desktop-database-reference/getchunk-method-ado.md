---
title: GetChunk-Methode (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a61130db9bd4564523688adc4e045f665e7310e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919010"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="22791-102">GetChunk-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="22791-102">GetChunk method (ADO)</span></span>


<span data-ttu-id="22791-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22791-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="22791-104">Gibt den gesamten Inhalt oder einen Teil des Inhalts eines [Field](field-object-ado.md)-Objekts mit umfangreichem Text oder Binärdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="22791-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22791-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22791-105">Syntax</span></span>

<span data-ttu-id="22791-106">*Variable* = *dar*. GetChunk (*Größe* )</span><span class="sxs-lookup"><span data-stu-id="22791-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="22791-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22791-107">Return value</span></span>

<span data-ttu-id="22791-108">Gibt einen **Variant** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="22791-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="22791-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="22791-109">Parameters</span></span>

  - <span data-ttu-id="22791-110">*Size*</span><span class="sxs-lookup"><span data-stu-id="22791-110">*Size*</span></span>

  - <span data-ttu-id="22791-111">Ein **Long** -Ausdruck, der der Anzahl von Bytes oder Zeichen entspricht, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="22791-111">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="22791-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22791-112">Remarks</span></span>

<span data-ttu-id="22791-p101">Verwenden Sie die **GetChunk** -Methode für ein **Field** -Objekt, um einen Teil der bzw. die gesamten umfangreichen Binär- oder Zeichendaten abzurufen. In Situationen, bei denen der Systemspeicher beschränkt ist, können Sie die **GetChunk** -Methode verwenden, um umfangreiche Werte in kleinere Einheiten aufzuteilen, statt deren Gesamtheit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="22791-p101">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="22791-p102">Die Daten, die von einem Aufruf von **GetChunk** zurückgegeben werden, werden einer *Variablen* zugewiesen. Falls die *Größe* die Größe der restlichen Daten überschreitet, gibt die **GetChunk**-Methode nur die restlichen Daten zurück, ohne die *Variable* mit Leerzeichen aufzufüllen. Falls das Feld leer ist, gibt die **GetChunk**-Methode einen NULL-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="22791-p102">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="22791-p103">Bei jedem weiteren Aufruf von **GetChunk** werden die Daten ab der Stelle abgerufen, an der beim vorherigen Aufruf von **GetChunk** abgebrochen wurde. Wenn Sie jedoch Daten aus einem Feld abrufen und anschließend den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, geht ADO davon aus, dass Sie das Abrufen von Daten aus dem ersten Feld beendet haben. Wenn Sie die **GetChunk** -Methode erneut für das erste Feld aufrufen, interpretiert ADO den Aufruf als einen neuen **GetChunk** -Vorgang und beginnt am Anfang der Daten mit dem Lesen. Beim Zugriff auf Felder in anderen [Recordset](recordset-object-ado.md)-Objekten, bei denen es sich nicht um Klone des ersten **Recordset** -Objekts handelt, werden die **GetChunk** -Operationen nicht unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="22791-p103">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="22791-122">Besitzt das **adFldLong** -Bit in der [Attributes](attributes-property-ado.md)-Eigenschaft eines **Field** -Objekts den Wert **True**, können Sie die **GetChunk** -Methode für dieses Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="22791-122">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="22791-123">Ist kein aktueller Datensatz vorhanden, wenn Sie die **GetChunk** -Methode für ein **Field** -Objekt verwenden, tritt Fehler 3021 (kein aktueller Datensatz) auf.</span><span class="sxs-lookup"><span data-stu-id="22791-123">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="22791-p104">[!HINWEIS] Die <STRONG>GetChunk</STRONG> -Methode kann nicht auf <STRONG>Field</STRONG> -Objekte eines <A href="record-object-ado.md">Record</A>-Objekts angewendet werden. Sie führt keine Vorgänge aus und generiert einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="22791-p104">The <STRONG>GetChunk</STRONG> method does not operate on <STRONG>Field</STRONG> objects of a <A href="record-object-ado.md">Record</A> object. It does not perform any operation and will produce a run-time error.</span></span></P>


