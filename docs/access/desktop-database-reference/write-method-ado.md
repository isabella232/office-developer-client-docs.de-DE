---
title: Write-Methode - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475403"
---
# <a name="write-method-ado"></a><span data-ttu-id="fa579-102">Write-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa579-102">Write Method (ADO)</span></span>


<span data-ttu-id="fa579-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa579-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="fa579-104">Schreibt Binärdaten in ein [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fa579-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa579-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa579-105">Syntax</span></span>

<span data-ttu-id="fa579-106">*Stream-Objekt*. Schreiben des*Puffers*</span><span class="sxs-lookup"><span data-stu-id="fa579-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="fa579-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa579-107">Parameters</span></span>

  - <span data-ttu-id="fa579-108">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="fa579-108">*Buffer*</span></span>

  - <span data-ttu-id="fa579-109">Ein Wert vom Datentyp **Variant**, der ein Bytearray enthält, das geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa579-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa579-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa579-110">Remarks</span></span>

<span data-ttu-id="fa579-111">Die angegebenen Bytes werden ohne Leerzeichen zwischen den einzelnen Bytes in das **Stream** -Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa579-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="fa579-p101">Als aktuelle [Position](position-property-ado.md) wird das Byte festgelegt, das auf die geschriebenen Daten folgt. Mit der **Write** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.</span><span class="sxs-lookup"><span data-stu-id="fa579-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="fa579-115">Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) für **Stream** um neue Bytes erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.</span><span class="sxs-lookup"><span data-stu-id="fa579-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fa579-p102">Die <STRONG>Write</STRONG>-Methode wird für binäre Datenströme verwendet (<A href="type-property-ado-stream.md">Type</A> ist <STRONG>adTypeBinary</STRONG>). Für Textdatenströme (<STRONG>Type</STRONG> ist <STRONG>adTypeText</STRONG>) verwenden Sie <A href="writetext-method-ado.md">WriteText</A>.</span><span class="sxs-lookup"><span data-stu-id="fa579-p102">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>). For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>


