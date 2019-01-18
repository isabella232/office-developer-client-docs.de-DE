---
title: Write-Methode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702516"
---
# <a name="write-method-ado"></a><span data-ttu-id="a2b94-102">Write-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2b94-102">Write method (ADO)</span></span>

<span data-ttu-id="a2b94-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2b94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2b94-104">Schreibt Binärdaten in ein [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a2b94-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2b94-105">Syntax</span></span>

<span data-ttu-id="a2b94-106">*Stream-Objekt*. Schreiben des*Puffers*</span><span class="sxs-lookup"><span data-stu-id="a2b94-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="a2b94-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b94-107">Parameters</span></span>

|<span data-ttu-id="a2b94-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b94-108">Parameter</span></span>|<span data-ttu-id="a2b94-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2b94-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a2b94-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="a2b94-110">*Buffer*</span></span> |<span data-ttu-id="a2b94-111">Ein Wert vom Datentyp **Variant**, der ein Bytearray enthält, das geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2b94-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a2b94-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a2b94-112">Remarks</span></span>

<span data-ttu-id="a2b94-113">Die angegebenen Bytes werden ohne Leerzeichen zwischen den einzelnen Bytes in das **Stream** -Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a2b94-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="a2b94-p101">Als aktuelle [Position](position-property-ado.md) wird das Byte festgelegt, das auf die geschriebenen Daten folgt. Mit der **Write** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.</span><span class="sxs-lookup"><span data-stu-id="a2b94-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="a2b94-117">Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) für **Stream** um neue Bytes erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.</span><span class="sxs-lookup"><span data-stu-id="a2b94-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="a2b94-p102">Die **Write**-Methode wird für binäre Datenströme verwendet ([Type](type-property-ado-stream.md) ist **adTypeBinary**). Für Textdatenströme (**Type** ist **adTypeText**) verwenden Sie [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a2b94-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

