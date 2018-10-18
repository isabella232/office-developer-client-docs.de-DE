---
<span data-ttu-id="0d27c-101"><<<<<<< HEAD-Titel: LineSeparator-Eigenschaft (ADO) TOCTitle: LineSeparator-Eigenschaft (ADO) === Titel: LineSeparator-Eigenschaft (ADO) TOCTitle: LineSeparator-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d27c-101"><<<<<<< HEAD title: LineSeparator Property (ADO) TOCTitle: LineSeparator Property (ADO) ======= title: LineSeparator property (ADO) TOCTitle: LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0d27c-102">Master Ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) Ms:contentKeyID: 48546676 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="0d27c-102">master ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0d27c-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="0d27c-103"><<<<<<< HEAD</span></span>
# <a name="lineseparator-property-ado"></a><span data-ttu-id="0d27c-104">LineSeparator-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d27c-104">LineSeparator Property (ADO)</span></span>
=======
# <a name="lineseparator-property-ado"></a><span data-ttu-id="0d27c-105">LineSeparator-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d27c-105">LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0d27c-106">master</span><span class="sxs-lookup"><span data-stu-id="0d27c-106">master</span></span>


<span data-ttu-id="0d27c-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d27c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0d27c-108">Gibt das binäre Zeichen an, das als Zeilentrennzeichen in [Stream](stream-object-ado.md)-Textobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d27c-108">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

<span data-ttu-id="0d27c-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="0d27c-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="0d27c-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0d27c-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="0d27c-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0d27c-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="0d27c-112">master</span><span class="sxs-lookup"><span data-stu-id="0d27c-112">master</span></span>

<span data-ttu-id="0d27c-p101">Legt einen [LineSeparatorsEnum](lineseparatorsenum.md)-Wert fest, der das im **Stream** -Objekt verwendete Linientrennzeichen angibt, oder gibt diesen Wert zurück. Der Standardwert lautet **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="0d27c-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d27c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d27c-115">Remarks</span></span>

<span data-ttu-id="0d27c-p102">**LineSeparator** wird verwendet, um beim Lesen des Inhalts eines **Stream** -Textobjekts Zeilen zu interpretieren. Zeilen können mit der [SkipLine](skipline-method-ado.md)-Methode übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="0d27c-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="0d27c-p103">**LineSeparator** wird nur bei **Stream**-Textobjekten verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Diese Eigenschaft wird ignoriert, wenn **Type** auf **adTypeBinary** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0d27c-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

