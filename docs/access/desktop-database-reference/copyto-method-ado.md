---
title: CopyTo-Methode (ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bd949b92068619b76ac78d5e62cde0e247ed7b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474065"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="df891-102">CopyTo-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="df891-102">CopyTo Method (ADO)</span></span>


<span data-ttu-id="df891-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="df891-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="df891-104">Kopiert die angegebene Anzahl von Zeichen oder Bytes (in Abhängigkeit vom [Type](type-property-ado-stream.md)) von einem [Stream](stream-object-ado.md)-Objekt in ein anderes **Stream** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="df891-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="df891-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df891-105">Syntax</span></span>

<span data-ttu-id="df891-106">*Stream-Objekt*. CopyTo *DestStream*, *NumChars*</span><span class="sxs-lookup"><span data-stu-id="df891-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="df891-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="df891-107">Parameters</span></span>

  - <span data-ttu-id="df891-108">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="df891-108">*DestStream*</span></span>

  - <span data-ttu-id="df891-p101">Der Wert einer Objektvariable, der einen Verweis auf ein geöffnetes **Stream**-Objekt enthält. Das aktuelle **Stream**-Objekt wird in das durch *DestStream* angegebene **Stream**-Zielobjekt kopiert. Das **Stream**-Zielobjekt muss bereits geöffnet sein. Ist dies nicht der Fall, tritt ein Laufzeitfehler auf.

</span><span class="sxs-lookup"><span data-stu-id="df891-p101">An object variable value that contains a reference to an open **Stream** object. The current **Stream** is copied to the destination **Stream** specified by *DestStream*. The destination **Stream** must already be open. If not, a run-time error occurs.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="df891-113">Der Parameter <EM>DestStream</EM> möglicherweise nicht, da dies erfordert Zugriff auf eine private Schnittstelle am <STRONG>Stream</STRONG> -Objekt, das an den Client nicht remotefähig einen Proxy des <STRONG>Stream</STRONG> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="df891-113">The <EM>DestStream</EM> parameter may not be a proxy of <STRONG>Stream</STRONG> object because this requires access to a private interface on the <STRONG>Stream</STRONG> object that cannot be remoted to the client.</span></span></P>



  - <span data-ttu-id="df891-114">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="df891-114">*NumChars*</span></span>

  - <span data-ttu-id="df891-115">Optional.</span><span class="sxs-lookup"><span data-stu-id="df891-115">Optional.</span></span> <span data-ttu-id="df891-116">Ein **Integer** -Wert, der angibt, die Anzahl von Bytes oder Zeichen von der aktuellen Position in der Quelle **Stream-Objekt** an das Ziel **Stream**kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="df891-116">An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**.</span></span> <span data-ttu-id="df891-117">Der Standardwert ist-1, gibt an, dass alle Zeichen oder Bytes in [EOS](eos-property-ado.md)von der aktuellen Position kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="df891-117">The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df891-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df891-118">Remarks</span></span>

<span data-ttu-id="df891-p103">Diese Methode kopiert die angegebene Anzahl von Zeichen oder Bytes ab der durch die Position-Eigenschaft angegebenen aktuellen Position. Ist die angegebene Anzahl höher als die verfügbare Anzahl von Bytes bis zu EOS, werden nur die Zeichen oder Bytes ab der aktuellen Position bis zu EOS kopiert. Wenn der Wert für NumChars -1 oder nicht angegeben ist, werden alle Zeichen oder Bytes ab der aktuellen Position kopiert.</span><span class="sxs-lookup"><span data-stu-id="df891-p103">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property. If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied. If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="df891-p104">Wenn der Zieldatenstrom bereits Zeichen oder Bytes enthält, bleibt der gesamte Inhalt nach dem Punkt, an dem die Kopie endet, erhalten und wird nicht abgeschnitten. **Position** beginnt bei dem Byte, dass unmittelbar auf das letzte kopierte Byte folgt. Wenn Sie diese Bytes abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.</span><span class="sxs-lookup"><span data-stu-id="df891-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="df891-p105">**CopyTo** sollte verwendet werden, um Daten in ein **Stream**-Zielobjekt zu kopieren, das denselben Typ wie das **Stream**-Quellobjekt aufweist (ihre **Type**-Eigenschaften sind jeweils auf **adTypeText** oder auf **adTypeBinary** festgelegt). Bei **Stream**-Textobjekten können Sie die Einstellung der [Charset](charset-property-ado.md)-Eigenschaft für das **Stream**-Zielobjekt so ändern, dass ein Datensatz in einen anderen übertragen wird. **Stream**-Textobjekte können auch in binäre **Stream**-Objekte kopiert werden, aber binäre **Stream**-Objekte können nicht in **Stream**-Textobjekte kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="df891-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

