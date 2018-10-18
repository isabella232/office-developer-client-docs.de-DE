---
title: ReadText-Methode (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083dccd2c1d328e825a198008fd773bc3a592f6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605212"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="90733-102">ReadText-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="90733-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="90733-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="90733-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="90733-104">Liest eine angegebene Anzahl von Zeichen aus einem [Stream](stream-object-ado.md)-Textobjekt.</span><span class="sxs-lookup"><span data-stu-id="90733-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="90733-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90733-105">Syntax</span></span>

<span data-ttu-id="90733-106">*Zeichenfolge* = *Stream-Objekt*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="90733-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="90733-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="90733-107">Parameters</span></span>

  - <span data-ttu-id="90733-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="90733-108">*NumChars*</span></span>

  - <span data-ttu-id="90733-p101">Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Zeichen oder einen [StreamReadEnum](streamreadenum.md)-Wert angibt. Der Standardwert lautet **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="90733-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>

<span data-ttu-id="90733-112"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="90733-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="90733-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90733-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="90733-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90733-114">Return value</span></span>
>>>>>>> <span data-ttu-id="90733-115">master</span><span class="sxs-lookup"><span data-stu-id="90733-115">master</span></span>

<span data-ttu-id="90733-116">Die **ReadText** -Methode liest eine angegebene Anzahl von Zeichen, eine vollständige Zeile oder einen vollständigen Datenstrom aus einem **Stream** -Objekt und gibt die resultierende Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="90733-116">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="90733-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90733-117">Remarks</span></span>

<span data-ttu-id="90733-p102">Ist NumChar größer als die Anzahl der im Datenstrom verbliebenen Zeichen, werden nur die verbliebenen Zeichen zurückgegeben. Die gelesene Zeichenfolge wird nicht aufgefüllt, damit sie der durch NumChar angegebenen Länge entspricht. Wenn keine zu lesenden Zeichen vorhanden sind, wird ein Variant-Wert mit einem Nullwert zurückgegeben. ReadText kann nicht verwendet werden, um rückwärts zu lesen.</span><span class="sxs-lookup"><span data-stu-id="90733-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="90733-p103">Die <STRONG>ReadText</STRONG>-Methode wird bei Textdatenströmen verwendet (<A href="type-property-ado-stream.md">Type</A> ist auf <STRONG>adTypeText</STRONG> festgelegt). Verwenden Sie bei binären Datenströmen (<STRONG>Type</STRONG> ist auf <STRONG>adTypeBinary</STRONG> festgelegt) die <A href="read-method-ado.md">Read</A>-Methode.</span><span class="sxs-lookup"><span data-stu-id="90733-p103">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>


