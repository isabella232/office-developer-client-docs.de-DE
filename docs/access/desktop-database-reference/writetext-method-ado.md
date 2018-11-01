---
title: WriteText-Methode (ADO)
TOCTitle: WriteText Method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b457af35e0b9b5f7d61bf5a77f080a11b36232ae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884093"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="b62be-102">WriteText-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="b62be-102">WriteText Method (ADO)</span></span>


<span data-ttu-id="b62be-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b62be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b62be-104">Schreibt eine angegebene Textzeichenfolge in ein [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b62be-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b62be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b62be-105">Syntax</span></span>

<span data-ttu-id="b62be-106">*Stream-Objekt*. WriteText*Daten*, *Optionen*</span><span class="sxs-lookup"><span data-stu-id="b62be-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="b62be-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b62be-107">Parameters</span></span>

  - <span data-ttu-id="b62be-108">*Data*</span><span class="sxs-lookup"><span data-stu-id="b62be-108">*Data*</span></span>

  - <span data-ttu-id="b62be-109">Ein Wert vom Datentyp **String**, der die Textzeichenfolge enthält, die geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b62be-109">A **String** value that contains the text in characters to be written.</span></span>

  - <span data-ttu-id="b62be-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="b62be-110">*Options*</span></span>

  - <span data-ttu-id="b62be-p101">Optional. Ein [StreamWriteEnum](streamwriteenum.md)-Wert, der angibt, ob am Ende der angegebenen Zeichenfolge ein Zeilentrennzeichen geschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="b62be-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>

## <a name="remarks"></a><span data-ttu-id="b62be-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b62be-113">Remarks</span></span>

<span data-ttu-id="b62be-114">Die angegebenen Zeichenfolgen werden ohne Leerzeichen oder Buchstaben zwischen den einzelnen Zeichenfolgen in das **Stream** -Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b62be-114">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="b62be-p102">Als aktuelle [Position](position-property-ado.md) wird der Buchstabe festgelegt, der auf die geschriebenen Daten folgt. Mit der **WriteText** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Buchstaben abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.</span><span class="sxs-lookup"><span data-stu-id="b62be-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="b62be-118">Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) für **Stream** um neue Buchstaben erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.</span><span class="sxs-lookup"><span data-stu-id="b62be-118">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b62be-p103">Die <STRONG>WriteText</STRONG>-Methode wird für Textdatenströme verwendet (<A href="type-property-ado-stream.md">Type</A> ist <STRONG>adTypeText</STRONG>). Für binäre Datenströme (<STRONG>Type</STRONG> ist <STRONG>adTypeBinary</STRONG>) verwenden Sie <A href="write-method-ado.md">Write</A>.</span><span class="sxs-lookup"><span data-stu-id="b62be-p103">The <STRONG>WriteText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="write-method-ado.md">Write</A>.</span></span></P>


