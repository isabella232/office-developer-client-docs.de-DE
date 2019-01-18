---
title: Type-Eigenschaft (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721955"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="11a2c-102">Type-Eigenschaft (ADO Stream)</span><span class="sxs-lookup"><span data-stu-id="11a2c-102">Type property (ADO Stream)</span></span>


<span data-ttu-id="11a2c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11a2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11a2c-104">Gibt die Art der Daten an, die im [Stream](stream-object-ado.md)-Objekt enthalten sind (binär oder Text).</span><span class="sxs-lookup"><span data-stu-id="11a2c-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="11a2c-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="11a2c-105">Settings and return values</span></span>

<span data-ttu-id="11a2c-p101">Legt einen [StreamTypeEnum](streamtypeenum.md)-Wert fest, der die Art der Daten im **Stream** -Objekt angibt, oder gibt den Wert zurück. Der Standardwert ist **adTypeText**. Wenn jedoch zuerst binäre Daten in ein neues, leeres **Stream** -Objekt geschrieben werden, wird die **Type** -Eigenschaft in **adTypeBinary** geändert.</span><span class="sxs-lookup"><span data-stu-id="11a2c-p101">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object. The default value is **adTypeText**. However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a2c-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11a2c-109">Remarks</span></span>

<span data-ttu-id="11a2c-110">Die Type-Eigenschaft ist nur dann nicht schreibgeschützt, wenn sich die aktuelle Position am Anfang des Stream-Objekts befindet (Position ist 0). Bei jeder anderen Position ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="11a2c-110">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="11a2c-p102">Die **Type** -Eigenschaft bestimmt, welche Methoden zum Lesen und Schreiben des **Stream** -Objekts verwendet werden. Verwenden Sie bei **Stream** -Textobjekten [ReadText](readtext-method-ado.md) und [WriteText](writetext-method-ado.md). Verwenden Sie bei binären **Stream** -Objekten [Read](read-method-ado.md) und [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="11a2c-p102">The **Type** property determines which methods should be used for reading and writing the **Stream**. For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md). For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

