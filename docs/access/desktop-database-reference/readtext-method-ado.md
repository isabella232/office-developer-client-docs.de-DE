---
title: ReadText-Methode (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300798"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="ba387-102">ReadText-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ba387-102">ReadText method (ADO)</span></span>

<span data-ttu-id="ba387-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba387-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba387-104">Liest eine angegebene Anzahl von Zeichen aus einem [Stream](stream-object-ado.md)-Textobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba387-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba387-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba387-105">Syntax</span></span>

<span data-ttu-id="ba387-106">*String* = -*Stream*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="ba387-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ba387-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba387-107">Parameters</span></span>

|<span data-ttu-id="ba387-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba387-108">Parameter</span></span>|<span data-ttu-id="ba387-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba387-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ba387-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="ba387-110">*NumChars*</span></span> |<span data-ttu-id="ba387-p101">Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Zeichen oder einen [StreamReadEnum](streamreadenum.md)-Wert angibt. Der Standardwert lautet **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="ba387-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="ba387-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba387-114">Return value</span></span>

<span data-ttu-id="ba387-115">Die **ReadText**-Methode liest eine angegebene Anzahl von Zeichen, eine vollständige Zeile oder einen vollständigen Datenstrom aus einem **Stream**-Objekt und gibt die resultierende Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="ba387-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba387-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba387-116">Remarks</span></span>

<span data-ttu-id="ba387-117">Wenn *NumChar* größer als die Anzahl der Zeichen im Stream ist, werden nur die verbleibenden Zeichen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba387-117">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned.</span></span> <span data-ttu-id="ba387-118">Die Zeichenfolge Read wird nicht mit der durch *NumChar*angegebenen Länge aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ba387-118">The string read is not padded to match the length specified by *NumChar*.</span></span> <span data-ttu-id="ba387-119">If there are no characters left to read, a variant whose value is null is returned.</span><span class="sxs-lookup"><span data-stu-id="ba387-119">If there are no characters left to read, a variant whose value is null is returned.</span></span> <span data-ttu-id="ba387-120">**ReadText** cannot be used to read backwards.</span><span class="sxs-lookup"><span data-stu-id="ba387-120">**ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="ba387-p103">Die **ReadText**-Methode wird bei Textdatenströmen verwendet ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt). Verwenden Sie bei binären Datenströmen (**Type** ist auf **adTypeBinary** festgelegt) die [Read](read-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="ba387-p103">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>

