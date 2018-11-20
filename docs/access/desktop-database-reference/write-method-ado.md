---
title: Write-Methode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 227c7a3746d0c743c33f76362023d6d374269a81
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026281"
---
# <a name="write-method-ado"></a><span data-ttu-id="b37a0-102">Write-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="b37a0-102">Write method (ADO)</span></span>

<span data-ttu-id="b37a0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b37a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b37a0-104">Schreibt Binärdaten in ein [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b37a0-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b37a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b37a0-105">Syntax</span></span>

<span data-ttu-id="b37a0-106">*Stream-Objekt*. Schreiben des*Puffers*</span><span class="sxs-lookup"><span data-stu-id="b37a0-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="b37a0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b37a0-107">Parameters</span></span>

|<span data-ttu-id="b37a0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b37a0-108">Parameter</span></span>|<span data-ttu-id="b37a0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b37a0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b37a0-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="b37a0-110">*Buffer*</span></span> |<span data-ttu-id="b37a0-111">Ein Wert vom Datentyp **Variant**, der ein Bytearray enthält, das geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b37a0-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b37a0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b37a0-112">Remarks</span></span>

<span data-ttu-id="b37a0-113">Die angegebenen Bytes werden ohne Leerzeichen zwischen den einzelnen Bytes in das **Stream** -Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b37a0-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="b37a0-p101">Als aktuelle [Position](position-property-ado.md) wird das Byte festgelegt, das auf die geschriebenen Daten folgt. Mit der **Write** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.</span><span class="sxs-lookup"><span data-stu-id="b37a0-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="b37a0-117">Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) für **Stream** um neue Bytes erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.</span><span class="sxs-lookup"><span data-stu-id="b37a0-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="b37a0-p102">Die **Write**-Methode wird für binäre Datenströme verwendet ([Type](type-property-ado-stream.md) ist **adTypeBinary**). Für Textdatenströme (**Type** ist **adTypeText**) verwenden Sie [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b37a0-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

